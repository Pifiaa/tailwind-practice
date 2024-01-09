# Tailwind

<img src="https://getlogovector.com/wp-content/uploads/2021/01/tailwind-css-logo-vector.png" alt="Tailwind css" margin="auto" display="block" >

**Referencias:**
- Documentación oficial de Tailwind CSS: [https://tailwindcss.com](https://tailwindcss.com)

## 1. ¿Qué es Tailwind?

Tailwind CSS es un framework de utilidades de primera clase para la construcción de interfaces web. A diferencia de otros frameworks que proporcionan componentes prediseñados, Tailwind se centra en clases de utilidad predefinidas que se aplican directamente a los elementos HTML.

## 2. ¿Para qué se usa Tailwind y sus ventajas?

Tailwind se utiliza para agilizar el proceso de desarrollo frontend al proporcionar clases de utilidad que permiten estilizar elementos de manera rápida y eficiente. Algunas ventajas clave incluyen la flexibilidad para personalizar estilos sin CSS adicional, un tamaño de archivo final optimizado y una curva de aprendizaje más rápida para los desarrolladores.

### 2.1 Clases de Utilidad en Tailwind

Las clases de utilidad son reglas de estilo de bajo nivel que se aplican directamente en el HTML. Estas clases abarcan desde márgenes y rellenos hasta tipografía y colores. Por ejemplo:

```html
<div class="bg-blue-500 text-white p-4">Este es un cuadro con fondo azul, texto blanco y relleno de 4 píxeles.</div>
```

## 3. Pasos para instalar Tailwind con Tailwind CLI

1. Instalar Node.js y npm si aún no están instalados.
2. Instalar Tailwind CSS como dependencia de desarrollo:

   ```bash
   npm install -D tailwindcss
   ```

3. Crear un archivo de configuración de Tailwind usando el comando:

   ```bash
   npx tailwindcss init
   ```

4. Configurar las rutas de tus plantillas en el archivo `tailwind.config.js`:

   ```javascript
   /** @type {import('tailwindcss').Config} */
   module.exports = {
     content: ["./src/**/*.{html,js}"],
     theme: {
       extend: {},
     },
     plugins: [],
   };
   ```

5. Añadir las directivas de Tailwind a tu archivo CSS principal:

   ```css
   @tailwind base;
   @tailwind components;
   @tailwind utilities;
   ```

6. Agregar un script para compilar los estilos en el archivo `package.json`:

   ```json
   "scripts": {
     "build:css": "tailwindcss build ./src/input.css -o ./src/output.css"
   }
   ```

7. Ejecutar el script para compilar los estilos:

   ```bash
   npm run build:css
   ```

   Asegúrate de reemplazar `./src/input.css` con la ruta de tu archivo de entrada y `./src/output.css` con la ruta deseada para el archivo de salida.

## 4. Empezar a usar Tailwind en HTML

Añade tu archivo CSS compilado al `<head>` y empieza a usar las clases de utilidad de Tailwind para dar estilo a tu contenido.

```html
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="/output.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```