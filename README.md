# ❄️ Magic Snow Effect

**¡Agrega un toque de magia invernal a tu sitio web!**

Magic Snow Effect es una librería ligera de JavaScript que permite incorporar un efecto de nieve animada e interactiva en cualquier página web.

Crea ambientes invernales con copos de nieve en movimiento, interacción con el cursor, explosiones mágicas al hacer clic y fondos animados personalizables.

No necesita frameworks ni dependencias externas. ¡Solo importa los archivos CSS y JavaScript y disfruta de la magia!

---

## ✨ Características

- ❄️ Caída de nieve animada con densidad personalizable.
- 🖱️ Copos de nieve interactivos que reaccionan al movimiento del cursor.
- ✨ Explosión de partículas mágicas al hacer clic.
- 🌨️ Fondo animado con textura de nieve.
- 💨 Movimiento lateral natural mediante efecto de viento.
- 🎨 Personalización del color de los copos.
- ⚡ Ligera y fácil de integrar.
- 🌐 Compatible con cualquier sitio web.
- 📦 Disponible mediante CDN.
- 🚀 No requiere dependencias externas.

---

## 📦 Instalación

### Opción 1: Mediante CDN (recomendado)

La forma más sencilla de utilizar Magic Snow Effect es mediante [jsDelivr](https://www.jsdelivr.com/).

Agrega los siguientes archivos CSS y JavaScript a tu documento HTML:

```html
<!-- Estilos de Magic Snow Effect -->
<link
    rel="stylesheet"
    href="https://cdn.jsdelivr.net/gh/evandash6/magic-snow@v1.0.0/dist/magic-snow.min.css"
/>

<!-- Librería Magic Snow Effect -->
<script src="https://cdn.jsdelivr.net/gh/evandash6/magic-snow@v1.0.0/dist/magic-snow.min.js"></script>
```

Puedes reemplazar `v1.0.0` por la versión que desees utilizar.

### Opción 2: Descarga desde GitHub

También puedes descargar la librería directamente desde el repositorio.

1. Visita el repositorio de [Magic Snow Effect](https://github.com/evandash6/magic-snow).
2. Descarga el proyecto o clónalo.
3. Copia los archivos de la carpeta `dist` en tu proyecto.
4. Incluye los archivos CSS y JavaScript en tu HTML.

```html
<link rel="stylesheet" href="dist/magic-snow.css">

<script src="dist/magic-snow.js"></script>
```

---

## 🚀 Inicio rápido

Una vez incluidos los archivos de la librería, inicializa el efecto con unas pocas líneas de JavaScript.

```javascript
const snow = new MagicSnow();

snow.start();
```

¡Eso es todo! Tu página web ahora tendrá un efecto de nieve interactivo.

---

## ⚙️ Configuración

Magic Snow Effect permite personalizar diferentes opciones para adaptar la animación a tu sitio web.

```javascript
const snow = new MagicSnow({
    density: 100,
    speed: 1,
    interaction: true,
    clickEffect: true,
    background: true,
    wind: true,
    color: "#ffffff",
    zIndex: 9999
});

snow.start();
```

### Opciones disponibles

| Opción | Tipo | Valor predeterminado | Descripción |
|---|---|---|---|
| `density` | Number | `65` | Cantidad de copos de nieve. |
| `speed` | Number | `1` | Multiplicador de velocidad de caída. |
| `interaction` | Boolean | `true` | Activa la interacción con el cursor. |
| `clickEffect` | Boolean | `true` | Activa las partículas mágicas al hacer clic. |
| `background` | Boolean | `true` | Activa el fondo animado de nieve. |
| `wind` | Boolean | `true` | Activa el movimiento horizontal de los copos. |
| `color` | String | `#ffffff` | Color de los copos y partículas. |
| `zIndex` | Number | `9999` | Nivel de profundidad del contenedor. |

---

## 🎨 Ejemplos de personalización

### Nieve ligera

Ideal para páginas que necesitan un efecto sutil.

```javascript
const snow = new MagicSnow({
    density: 30,
    speed: 0.5,
    interaction: false,
    clickEffect: false,
    background: true,
    wind: true
});

snow.start();
```

### Nevada intensa

Para crear un ambiente de invierno más marcado.

```javascript
const snow = new MagicSnow({
    density: 150,
    speed: 1.5,
    interaction: true,
    clickEffect: true,
    background: true,
    wind: true
});

snow.start();
```

### Nieve azul

Personaliza el color de los copos y las partículas.

```javascript
const snow = new MagicSnow({
    density: 100,
    color: "#8bd3ff",
    speed: 1.2,
    interaction: true,
    clickEffect: true
});

snow.start();
```

### Nieve minimalista

Una animación sencilla sin interacciones adicionales.

```javascript
const snow = new MagicSnow({
    density: 40,
    speed: 0.7,
    interaction: false,
    clickEffect: false,
    background: false,
    wind: false
});

snow.start();
```

---

## 🎮 Métodos disponibles

Magic Snow Effect proporciona métodos para controlar la animación.

### Iniciar efecto

Inicia la animación de nieve.

```javascript
snow.start();
```

### Detener efecto

Detiene la animación, elimina sus elementos y limpia los eventos asociados.

```javascript
snow.stop();
```

### Destruir instancia

Detiene el efecto y limpia las referencias de la instancia.

```javascript
snow.destroy();
```

---

## 💻 Ejemplo HTML completo

A continuación, puedes ver cómo integrar Magic Snow Effect en una página web desde cero.

```html
<!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Magic Snow Effect - Demo</title>

    <!-- Estilos -->
    <link
        rel="stylesheet"
        href="https://cdn.jsdelivr.net/gh/evandash6/magic-snow@v1.0.0/dist/magic-snow.min.css"
    />
</head>

<body>

    <h1>¡Bienvenido al invierno! ❄️</h1>

    <!-- Librería -->
    <script src="https://cdn.jsdelivr.net/gh/evandash6/magic-snow@v1.0.0/dist/magic-snow.min.js"></script>

    <!-- Inicialización -->
    <script>
        const snow = new MagicSnow({
            density: 100,
            speed: 1,
            interaction: true,
            clickEffect: true,
            background: true,
            wind: true
        });

        snow.start();
    </script>

</body>
</html>
```

---

## 🌐 Compatibilidad

Magic Snow Effect utiliza tecnologías estándar de los navegadores:

- DOM API.
- requestAnimationFrame.
- Web Animations API.
- CSS3 Animations.

Se recomienda utilizar navegadores modernos y actualizados.

---

## 📁 Estructura del proyecto

```text
magic-snow/
│
├── dist/
│   ├── magic-snow.js
│   ├── magic-snow.min.js
│   ├── magic-snow.css
│   └── magic-snow.min.css
│
├── README.md
├── LICENSE
└── package.json
```

---

## 📄 Licencia

Magic Snow Effect está distribuida bajo la licencia **MIT**.

Puedes utilizar, modificar y distribuir esta librería, incluso en proyectos personales y comerciales, respetando las condiciones establecidas en la licencia.

Consulta el archivo [LICENSE](LICENSE) para obtener más información.

---

## 👨‍💻 Autor

Desarrollado por **evandash6**.

- GitHub: [evandash6](https://github.com/evandash6)
- Repositorio: [Magic Snow Effect](https://github.com/evandash6/magic-snow)

---

**¡Disfruta de la magia del invierno en tu sitio web! ❄️✨**

Si te gusta este proyecto, considera darle una ⭐ en GitHub.
