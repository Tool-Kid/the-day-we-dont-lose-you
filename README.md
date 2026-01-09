# El día que no te perdimos - Página Web del Estreno

Página web elegante y compacta para el estreno del documental "El día que no te perdimos", con información del evento y cuenta regresiva. Diseño optimizado para verse de un vistazo.

## Características

- **Diseño Moderno y Compacto**: Inspirado en el ticket del estreno con paleta de colores rojo y dorado, optimizado para visualización completa sin scroll
- **Cuenta Regresiva**: Timer dinámico que muestra el tiempo restante hasta el estreno
- **Responsive**: Diseño adaptable a todos los dispositivos (móvil, tablet, desktop)
- **Animaciones**: Transiciones suaves y efectos visuales elegantes

## Información del Evento

- **Título**: El día que no te perdimos
- **Lugar**: CINES PEÑA DEL CUERVO
- **Fecha**: 13 de enero de 2026, 18:00 HRS
- **Producción**: Pablo Jiménez Beneitez
- **Marca**: PabLIX

## Estructura del Proyecto

```
.
├── index.html          # Estructura HTML principal
├── styles.css          # Estilos CSS
├── script.js           # Lógica JavaScript (countdown)
├── netlify.toml        # Configuración de Netlify
├── package.json        # Configuración npm y scripts de desarrollo
├── .gitignore          # Archivos ignorados por Git
├── README.md           # Este archivo
└── ticket.jpg          # Imagen optimizada del ticket (para preview de enlaces)
```

## Desarrollo Local

### Requisitos Previos

- [Node.js](https://nodejs.org/) (versión 14 o superior)
- npm (incluido con Node.js)

### Instalación

1. **Instala las dependencias**
   ```bash
   npm install
   ```

2. **Inicia el servidor de desarrollo**
   ```bash
   npm run dev
   ```
   
   O alternativamente:
   ```bash
   npm start
   ```

3. **Abre tu navegador**
   - El servidor se abrirá automáticamente en `http://localhost:3000`
   - Si no se abre automáticamente, ve manualmente a esa dirección

### Scripts Disponibles

- `npm run dev` o `npm start`: Inicia el servidor de desarrollo con recarga automática
- `npm run serve`: Inicia el servidor sin abrir el navegador automáticamente

### Características del Servidor de Desarrollo

- **Hot Reload**: Los cambios en HTML, CSS o JS se reflejan automáticamente en el navegador
- **Puerto**: El servidor corre en el puerto 3000 por defecto
- **Sin configuración adicional**: Funciona inmediatamente después de `npm install`

## Despliegue en Netlify

### Opción 1: Despliegue desde GitHub (Recomendado)

1. **Crea un repositorio en GitHub**
   - Ve a [GitHub](https://github.com) y crea un nuevo repositorio
   - Sube todos los archivos del proyecto al repositorio

2. **Conecta con Netlify**
   - Ve a [Netlify](https://www.netlify.com) y crea una cuenta o inicia sesión
   - Haz clic en "Add new site" > "Import an existing project"
   - Selecciona "GitHub" y autoriza la conexión
   - Elige tu repositorio

3. **Configuración de Build**
   - **Build command**: Dejar vacío (no se requiere build)
   - **Publish directory**: `.` (punto)
   - Haz clic en "Deploy site"


### Opción 2: Despliegue Manual (Drag & Drop)

1. **Prepara los archivos**
   - Asegúrate de tener todos los archivos en una carpeta

2. **Despliega en Netlify**
   - Ve a [Netlify](https://www.netlify.com) e inicia sesión
   - Arrastra la carpeta del proyecto a la zona de "Deploy" en el dashboard
   - Netlify desplegará automáticamente tu sitio

3. **Configurar dominio personalizado (Opcional)**
   - Ve a "Site settings" > "Domain management"
   - Puedes agregar un dominio personalizado o usar el subdominio de Netlify

## Personalización

### Cambiar la Fecha del Estreno

Edita el archivo `script.js` y modifica la línea:

```javascript
const premiereDate = new Date('2026-01-13T18:00:00').getTime();
```

Cambia la fecha y hora según necesites.

### Modificar Colores

Edita las variables CSS en `styles.css`:

```css
:root {
    --color-red-dark: #8B0000;
    --color-gold: #D4AF37;
    /* ... más colores ... */
}
```

### Configurar Preview de Enlaces (Open Graph)

Para que la imagen del ticket aparezca cuando compartas el enlace en redes sociales o mensajería:

1. **Despliega tu sitio en Netlify** (ver sección de Despliegue)
2. **Obtén la URL de tu sitio** (ejemplo: `https://tu-sitio.netlify.app`)
3. **Edita `index.html`** y reemplaza `https://your-site-url.netlify.app` con tu URL real en los meta tags:
   - Busca todas las instancias de `https://your-site-url.netlify.app`
   - Reemplázalas con tu URL completa (incluyendo `https://`)
4. **Vuelve a desplegar** el sitio

Los meta tags Open Graph y Twitter Card ya están configurados y usarán `ticket.jpg` como imagen de preview.

## Tecnologías Utilizadas

- **HTML5**: Estructura semántica
- **CSS3**: Estilos modernos con variables CSS y animaciones
- **JavaScript (Vanilla)**: Sin dependencias externas
- **Google Fonts**: Tipografías elegantes (Dancing Script, Playfair Display, Roboto)

## Compatibilidad

- ✅ Chrome/Edge (últimas versiones)
- ✅ Firefox (últimas versiones)
- ✅ Safari (últimas versiones)
- ✅ Dispositivos móviles (iOS y Android)

## Soporte

Para problemas o preguntas sobre el despliegue, consulta la [documentación de Netlify](https://docs.netlify.com/).

---

**Producción**: Pablo Jiménez Beneitez  
**Marca**: PabLIX
