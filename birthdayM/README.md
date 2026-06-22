# 🦊 Página de Cumpleaños — Guía de uso

## 📁 Estructura del proyecto
```
cumpleanos/
└── index.html    ← todo el sitio en un solo archivo
```

---

## ✏️ Cómo personalizar

### 1. Agregar tus fotos

Tienes **dos opciones**:

**Opción A — Fotos como archivos locales**
1. Crea una carpeta `img/` junto al `index.html`
2. Coloca tus fotos ahí (ej: `foto1.jpg`, `foto2.jpg`, …)
3. En el HTML busca cada `<img src="" …>` y agrega la ruta:
```html
<img src="img/foto1.jpg" alt="Foto 1" onerror="this.style.display='none'"/>
```

**Opción B — Fotos en línea (URL)**
```html
<img src="https://dominio.com/mi-foto.jpg" alt="Foto 1" .../>
```

---

### 2. Editar la carta

Busca el comentario `<!-- ✏️ EDITA AQUÍ TU CARTA PERSONAL -->` y reemplaza los párrafos con tu mensaje.

---

### 3. Cambiar nombres y fecha

- **Hero:** busca `Para ti, <em>mi amor</em>` y pon el nombre de tu pareja.
- **Fecha de la carta:** busca `Junio 2025` y actualiza.
- **Footer:** busca `<!-- Tu nombre aquí -->` al final.

---

## 🚀 Desplegar en GitHub Pages (gratis)

1. Crea un repositorio en [github.com](https://github.com) (puede ser privado o público).
2. Sube el archivo `index.html` (y la carpeta `img/` si usas fotos locales).
3. Ve a **Settings → Pages**.
4. En *Source* selecciona **Deploy from a branch → main → / (root)**.
5. Clic en **Save**.
6. En 1-2 minutos tu sitio estará en:
   ```
   https://TU_USUARIO.github.io/NOMBRE_DEL_REPO/
   ```

---

## 📱 Generar el QR

Con la URL de GitHub Pages, usa cualquier generador de QR:
- [qr-code-generator.com](https://www.qr-code-generator.com)
- [qrcode.com](https://www.qrcode.com)

Pega la URL → descarga el QR → imprímelo o compártelo 🎉

---

## 🎨 Cambiar colores (opcional)

Al inicio del `<style>` encontrarás las variables de color:
```css
--midnight:  #0d0f1a;   /* fondo principal */
--gold:      #d4a843;   /* acentos dorados */
--amber:     #e8c06a;   /* textos destacados */
--blush:     #e8a87c;   /* subtítulos */
--fox-orange:#e07430;   /* zorros */
```
