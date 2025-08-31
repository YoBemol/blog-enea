# Guía de Implementación en WordPress con Elementor

## Requisitos Previos

### Plugins Necesarios
- **Elementor Pro** (recomendado para funcionalidades avanzadas)
- **Elementor** (versión gratuita mínima)
- **Custom CSS and JS** (para estilos personalizados)
- **Yoast SEO** (para optimización SEO)

### Tema Recomendado
- **Hello Elementor** (tema oficial de Elementor)
- **Astra** (compatible y ligero)
- **GeneratePress** (alternativa rápida)

## Paso 1: Configuración Inicial

### 1.1 Instalación de WordPress
```bash
# Descargar WordPress
wget https://wordpress.org/latest.zip
unzip latest.zip
# Configurar base de datos y wp-config.php
```

### 1.2 Configuración de Elementor
1. Instalar y activar Elementor
2. Ir a **Elementor > Settings**
3. Configurar:
   - Disable Default Colors: Activar
   - Disable Default Fonts: Activar
   - CSS Print Method: Internal Embedding

## Paso 2: Importación de Contenido

### 2.1 Biblioteca de Medios
Subir las siguientes imágenes a **Medios > Añadir nuevo**:
- `hero-image.jpg` → Renombrar como "Paisaje Latinoamericano Hero"
- `patrimonio-natural.jpg` → "Biodiversidad América Latina"
- `cambio-climatico.jpg` → "Tecnologías Limpias"
- `calidad-ambiental.jpg` → "Restauración Ecosistemas"
- `agua-oceano.jpg` → "Acceso Agua Latinoamérica"

### 2.2 Configuración de Menús
**Apariencia > Menús > Crear nuevo menú**

Estructura del menú principal:
```
- Inicio (enlace a página principal)
- Categorías
  - Patrimonio Natural
  - Cambio Climático
  - Calidad Ambiental
  - Agua/Océano
- Sobre Nosotros
- Contacto
```

## Paso 3: Creación de Páginas con Elementor

### 3.1 Página Principal (index.html → Página de Inicio)

#### Sección Hero
**Widget: Container**
- Layout: Flexbox
- Direction: Row
- Align Items: Center
- Min Height: 100vh

**Columna Izquierda (Contenido):**
- Widget: Heading
  - Título: "Estrategia Nacional de Educación Ambiental"
  - HTML Tag: H1
  - Color: #2d5a27
  - Typography: Inter, 700, 3.5rem

- Widget: Text Editor
  - Contenido: Subtítulo y descripción
  - Color: #4a7c59

- Widget: Button
  - Texto: "Explorar Categorías"
  - Link: #categorias
  - Background: #2d5a27
  - Border Radius: 12px

**Columna Derecha (Imagen):**
- Widget: Image
  - Imagen: hero-image.jpg
  - Border Radius: 12px
  - Box Shadow: 0 8px 25px rgba(0,0,0,0.15)

#### Sección Introducción
**Widget: Container**
- Background: #f8f9fa
- Padding: 80px 0

**Widgets incluidos:**
- Heading (H2): "Nuestra Misión"
- Text Editor: Descripción de la misión
- Counter widgets para estadísticas (4, 100+, 20+)

#### Sección Categorías
**Widget: Container**
- Padding: 80px 0

**Para cada categoría:**
- Widget: Image Box
  - Imagen: Imagen correspondiente
  - Título: Nombre de la categoría
  - Descripción: Texto descriptivo
  - Button: "Explorar Artículos"
  - Hover Effects: Activar

### 3.2 Páginas de Categorías

#### Estructura Base para Cada Categoría
1. **Hero Section**
   - Widget: Container con background image
   - Overlay: Linear gradient rgba(45,90,39,0.8)
   - Heading: Nombre de la categoría
   - Breadcrumb: Widget de navegación

2. **Sección de Artículos**
   - Widget: Posts (Elementor Pro)
   - Layout: Grid 2/3 - 1/3
   - Filtros por categoría

3. **Temas Relacionados**
   - Widget: Icon Box (3 columnas)
   - Iconos de Font Awesome

## Paso 4: Estilos CSS Personalizados

### 4.1 Variables CSS Globales
Ir a **Apariencia > Personalizar > CSS Adicional**:

```css
:root {
    --primary-color: #2d5a27;
    --secondary-color: #4a7c59;
    --accent-color: #7fb069;
    --text-dark: #2c3e50;
    --text-light: #6c757d;
    --background-light: #f8f9fa;
    --white: #ffffff;
    --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    --shadow-hover: 0 8px 25px rgba(0, 0, 0, 0.15);
    --border-radius: 12px;
    --transition: all 0.3s ease;
}

/* Estilos para elementos de Elementor */
.elementor-widget-heading .elementor-heading-title {
    color: var(--primary-color);
}

.elementor-widget-button .elementor-button {
    background-color: var(--primary-color);
    border-radius: var(--border-radius);
    transition: var(--transition);
}

.elementor-widget-button .elementor-button:hover {
    background-color: var(--secondary-color);
    transform: translateY(-2px);
    box-shadow: var(--shadow-hover);
}

.elementor-widget-image-box:hover {
    transform: translateY(-10px);
    box-shadow: var(--shadow-hover);
}

/* Responsive */
@media (max-width: 768px) {
    .elementor-widget-heading .elementor-heading-title {
        font-size: 2.5rem !important;
    }
}
```

### 4.2 Configuración de Tipografía Global
**Elementor > Settings > Style**

**Primary Heading (H1):**
- Font Family: Inter
- Weight: 700
- Size: 3.5rem (desktop), 2.5rem (mobile)
- Color: #2d5a27

**Secondary Heading (H2):**
- Font Family: Inter
- Weight: 600
- Size: 2.5rem (desktop), 2rem (mobile)
- Color: #2d5a27

**Body Text:**
- Font Family: Inter
- Weight: 400
- Size: 1.1rem
- Color: #6c757d
- Line Height: 1.7

## Paso 5: Configuración de Posts y Categorías

### 5.1 Crear Categorías
**Posts > Categorías > Añadir nueva**

1. **Patrimonio Natural**
   - Slug: patrimonio-natural
   - Descripción: Artículos sobre manejo y conservación, gestión forestal y biodiversidad

2. **Cambio Climático**
   - Slug: cambio-climatico
   - Descripción: Eficiencia energética, tecnologías limpias, energías renovables

3. **Calidad Ambiental**
   - Slug: calidad-ambiental
   - Descripción: Prevención de contaminación, recuperación de espacios degradados

4. **Agua/Océano**
   - Slug: agua-oceano
   - Descripción: Acceso al agua, contaminación, hábitos de consumo

### 5.2 Crear Posts de Ejemplo
Usar el contenido de `contenido-categorias.md` para crear posts:

**Ejemplo de Post:**
- Título: "Conservación de la Biodiversidad en los Bosques Tropicales"
- Categoría: Patrimonio Natural
- Imagen destacada: patrimonio-natural.jpg
- Contenido: Usar el texto del archivo de contenido
- Excerpt: Primer párrafo como resumen

## Paso 6: Optimización y SEO

### 6.1 Configuración de Yoast SEO
- **Título del sitio**: "Blog ENEA - Estrategia Nacional de Educación Ambiental"
- **Descripción**: "Blog especializado en los ejes temáticos de la ENEA: Patrimonio Natural, Cambio Climático, Calidad Ambiental y Agua/Océano"
- **Palabras clave**: educación ambiental, ENEA, sostenibilidad, América Latina

### 6.2 Optimización de Imágenes
- Instalar plugin de optimización (Smush, ShortPixel)
- Configurar lazy loading
- Añadir alt text descriptivo a todas las imágenes

### 6.3 Performance
- Instalar plugin de caché (WP Rocket, W3 Total Cache)
- Minificar CSS y JavaScript
- Optimizar base de datos

## Paso 7: Configuración de Hosting

### 7.1 Requisitos del Servidor
- PHP 7.4 o superior
- MySQL 5.6 o superior
- Memoria: mínimo 256MB (recomendado 512MB)
- Espacio: mínimo 1GB

### 7.2 Configuración de .htaccess
```apache
# Compresión GZIP
<IfModule mod_deflate.c>
    AddOutputFilterByType DEFLATE text/plain
    AddOutputFilterByType DEFLATE text/html
    AddOutputFilterByType DEFLATE text/xml
    AddOutputFilterByType DEFLATE text/css
    AddOutputFilterByType DEFLATE application/xml
    AddOutputFilterByType DEFLATE application/xhtml+xml
    AddOutputFilterByType DEFLATE application/rss+xml
    AddOutputFilterByType DEFLATE application/javascript
    AddOutputFilterByType DEFLATE application/x-javascript
</IfModule>

# Cache del navegador
<IfModule mod_expires.c>
    ExpiresActive on
    ExpiresByType text/css "access plus 1 year"
    ExpiresByType application/javascript "access plus 1 year"
    ExpiresByType image/png "access plus 1 year"
    ExpiresByType image/jpg "access plus 1 year"
    ExpiresByType image/jpeg "access plus 1 year"
</IfModule>
```

## Paso 8: Mantenimiento y Actualizaciones

### 8.1 Backup Regular
- Configurar backups automáticos (UpdraftPlus)
- Backup antes de actualizaciones importantes
- Probar restauración periódicamente

### 8.2 Actualizaciones
- Mantener WordPress actualizado
- Actualizar plugins regularmente
- Probar en staging antes de producción

### 8.3 Monitoreo
- Configurar Google Analytics
- Monitorear velocidad de carga
- Revisar errores 404 regularmente

## Recursos Adicionales

### Documentación
- [Elementor Documentation](https://elementor.com/help/)
- [WordPress Codex](https://codex.wordpress.org/)
- [Web Accessibility Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)

### Herramientas de Desarrollo
- [Google PageSpeed Insights](https://pagespeed.web.dev/)
- [GTmetrix](https://gtmetrix.com/)
- [Elementor Inspector](https://elementor.com/help/elementor-inspector/)

---

**Nota**: Esta guía asume conocimientos básicos de WordPress y Elementor. Para implementación completa, se recomienda contar con experiencia en desarrollo web o contratar un desarrollador especializado.

