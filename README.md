# 🔮 Museo Virtual del Péndulo en Cascada

Página web estática lista para GitHub Pages. Incluye física, matemática, fenomenología y la animación Blender de 17 péndulos.

## Estructura del repositorio

```
pendulo-museo/
├── index.html       ← la página (sube este archivo)
├── 00-0359.mp4      ← tu animación
├── anim22.blend     ← archivo Blender para descarga
└── README.md
```

## Subir a GitHub Pages — paso a paso

### 1. Crear el repositorio

1. Ve a [github.com/new](https://github.com/new)
2. Nombre del repositorio: `pendulo-museo` (o el que quieras)
3. Visibilidad: **Public** (GitHub Pages gratuito requiere repositorio público)
4. Haz clic en **Create repository**

### 2. Subir los archivos

Opción A — Interfaz web (más fácil):
1. En tu repositorio, haz clic en **Add file → Upload files**
2. Arrastra los 4 archivos: `index.html`, `00-0359.mp4`, `anim22.blend`, `README.md`
3. Haz clic en **Commit changes**

> ⚠️ GitHub tiene un límite de 100 MB por archivo vía interfaz web.  
> Si tu `.mp4` pesa más, usa Git LFS (ver abajo).

Opción B — Terminal:
```bash
git clone https://github.com/TUUSUARIO/pendulo-museo
cd pendulo-museo
# copia tus archivos aquí
git add .
git commit -m "Museo virtual del péndulo"
git push
```

### 3. Activar GitHub Pages

1. Ve a **Settings** del repositorio
2. Sección **Pages** (menú izquierdo)
3. Source: **Deploy from a branch**
4. Branch: `main` / carpeta: `/ (root)`
5. Guarda — en ~1 minuto tu sitio estará en:

```
https://TUUSUARIO.github.io/pendulo-museo
```

### 4. Generar el QR

Una vez activo el sitio, ve a cualquier generador de QR gratuito:
- [qr-code-generator.com](https://www.qr-code-generator.com)
- [goqr.me](https://goqr.me)

Pega la URL `https://TUUSUARIO.github.io/pendulo-museo` y descarga el QR en SVG o PNG para imprimir.

---

## Git LFS (si el mp4 pesa más de 50 MB)

```bash
git lfs install
git lfs track "*.mp4"
git lfs track "*.blend"
git add .gitattributes
git add .
git commit -m "Archivos grandes via LFS"
git push
```

GitHub LFS gratuito incluye 1 GB de almacenamiento y 1 GB de ancho de banda/mes.

---

## Tecnologías usadas

- HTML / CSS / JavaScript — sin frameworks, sin dependencias
- [MathJax 3](https://www.mathjax.org/) — renderizado de ecuaciones LaTeX
- [Blender](https://www.blender.org/) — animación 3D
- GitHub Pages — hosting gratuito

---

*Física · Matemática · Fenomenología · Arte computacional*
