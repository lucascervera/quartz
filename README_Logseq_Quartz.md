# 📘 Publica tus Notas de Logseq con Quartz y GitHub Pages

Este proyecto convierte tus notas escritas en Logseq (archivos Markdown) en una página web moderna y navegable usando [Quartz](https://github.com/jackyzha0/quartz) y las aloja automáticamente con GitHub Pages.

---

## ✅ Requisitos previos

Antes de comenzar asegúrate de tener instalado:

- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/) (versión 16+ recomendada)
- Una cuenta en [GitHub](https://github.com/)

---

## 🚀 Pasos para configurar tu sitio

### 1. Clona el repositorio base de Quartz

```bash
git clone https://github.com/jackyzha0/quartz.git
cd quartz
```

### 2. Copia tus notas de Logseq

Copia los archivos Markdown desde tu carpeta de Logseq:

- Copia todo el contenido de `logseq/pages/` y `logseq/journals/`
- Pégalos dentro de la carpeta `content/` de este proyecto

Puedes hacerlo manualmente o con este comando (ajusta la ruta si es necesario):

```bash
cp -r ~/logseq/pages/* ./content/
cp -r ~/logseq/journals/* ./content/
```

### 3. Visualiza el sitio localmente (opcional)

Instala las dependencias y lanza un servidor local:

```bash
npm install
npx quartz dev
```

Abre en tu navegador: [http://localhost:8080](http://localhost:8080)

---

## 📝 ¿Cómo editar tu contenido?

1. Abre Logseq como siempre.
2. Escribe y organiza tus notas normalmente (en `pages/` o `journals/`).
3. Cuando quieras publicarlas:

   - **Copia nuevamente los archivos `.md` a la carpeta `content/` del repositorio.**

---

## 🌍 ¿Cómo publicar el sitio en GitHub Pages?

### 1. Sube tu repositorio a GitHub

```bash
git init
git remote add origin https://github.com/tu_usuario/tu_repositorio.git
git add .
git commit -m "Configuración inicial con mis notas"
git push -u origin main
```

### 2. Activa GitHub Pages

1. Ve a tu repositorio en GitHub.
2. Entra en `Settings` → `Pages`.
3. En “Source”, elige `main` como rama y `/` como carpeta.
4. Guarda los cambios.

Tu sitio se desplegará en `https://tu_usuario.github.io/tu_repositorio/`

---

## 🔄 ¿Cómo actualizar el sitio con nuevas notas?

Cada vez que quieras actualizar tu web:

```bash
# 1. Copia tus notas desde Logseq a la carpeta content/
cp -r ~/logseq/pages/* ./content/
cp -r ~/logseq/journals/* ./content/

# 2. (Opcional) Verifica en local
npx quartz dev

# 3. Haz commit y push
git add .
git commit -m "Actualizo contenido"
git push
```

---

## 🎨 Personaliza tu sitio

- Edita el archivo `quartz.config.ts` para cambiar:
  - El título del sitio
  - Descripción
  - Menú de navegación
  - Apariencia general

---

## ❓ Preguntas frecuentes

**¿Se necesita regenerar HTML manualmente?**  
No, Quartz genera el sitio cada vez que haces `npx quartz build` o `npx quartz dev`. GitHub Pages sirve archivos estáticos directamente del repositorio.

**¿Puedo usar etiquetas, backlinks y propiedades de Logseq?**  
Sí, Quartz es compatible con muchas funciones de Logseq, aunque algunas como `{{embed}}` pueden requerir ajustes.

---

## ✨ Recursos útiles

- [Quartz Docs](https://quartz.jzhao.xyz/)
- [Logseq](https://logseq.com/)
- [GitHub Pages](https://pages.github.com/)

---

¡Ahora ya puedes compartir tu conocimiento en la web de forma profesional y elegante! 🌐
