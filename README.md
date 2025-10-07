# Blog ENEA - Estrategia Nacional de Educación Ambiental

## Descripción del Proyecto

Este proyecto consiste en una página web de blog especializada en los cuatro ejes temáticos de la Estrategia Nacional de Educación Ambiental (ENEA), diseñada específicamente para ser compatible con WordPress y Elementor. El sitio web está optimizado para hosting estándar y incluye imágenes apropiadas del contexto latinoamericano.

## Estructura del Proyecto

```
blog-enea/
├── index.html                 # Página principal
├── patrimonio-natural.html    # Página de categoría 
│    └── patrimonio-natural-ejes.html    #pagina sub-categoría
├── cambio-climatico.html    # Página de categoría 
│    └── cambio-climatico-ejes.html    #pagina sub-categoría
├── calidad-ambiental.html    # Página de categoría 
│    └── calidad-ambiental-ejes.html    #pagina sub-categoría
├── agua-oceano.html    # Página de categoría 
│    └── agua-oceano-ejes.html    #pagina sub-categoría
├── educacion-formal.html   # Página de categoría
├── consejos-locales.html   # Página de categoría
├── README.md                  # Este archivo
├── assets/
│   ├── css/
│   │   └── style.css         # Estilos principales
│   ├── js/
│   │   └── script.js         # JavaScript para interactividad
│   └── images/
│       ├── hero-image.jpg    # Imagen principal
│        ├── Logo.jpg
│       ├── patrimonio-natural.jpg
│       ├── cambio-climatico.jpg
│       ├── calidad-ambiental.jpg
│       └── agua-oceano.jpg
└── wordpress-elementor/       # Archivos para WordPress (se crearán)
```

## Categorías Temáticas

### 1. Patrimonio Natural
- **Temas**: Cambio Climático, Calidad Ambiental, Agua y Océano
- **Imagen**: Recuperación de espacios naturales degradados
- **Contenido**: Introducción, Ejes temáticos 

### 2. Cambio Climático, Producción y Consumo Sostenible
- **Temas**: Patrimonio Natural, Calidad Ambiental, Agua y Océano
- **Imagen**: Tecnologías limpias vs paisaje desértico
- **Contenido**: Introducción, Ejes temáticos

### 3. Calidad Ambiental
- **Temas**: Patrimonio Natural, Cambio Climático, Agua y Océano
- **Imagen**: Paisaje natural con bosques, ríos y montañas
- **Contenido**: Introducción, Ejes temáticos

### 4. Agua/Océano
- **Temas**: Patrimonio Natural, Cambio Climático, Calidad Ambiental
- **Imagen**: Ballena saltando en el océano al atardecer
- **Contenido**: Introducción, Ejes temáticos

## Características Técnicas

### Diseño Responsive
- Compatible con dispositivos móviles, tablets y desktop
- Breakpoints optimizados para diferentes tamaños de pantalla
- Navegación móvil con menú hamburguesa

### Tecnologías Utilizadas
- **HTML5**: Estructura semántica y accesible
- **CSS3**: Diseño moderno con variables CSS, flexbox y grid
- **JavaScript**: Interactividad y efectos de scroll
- **Font Awesome**: Iconografía profesional
- **Google Fonts**: Tipografía Inter para legibilidad óptima

### Características de Diseño
- Paleta de colores verde inspirada en la naturaleza
- Efectos hover y transiciones suaves
- Animaciones de aparición al hacer scroll
- Botón de scroll hacia arriba
- Efectos parallax sutiles

## Compatibilidad con WordPress/Elementor

### Preparación para WordPress
1. **Estructura de Tema**: El HTML está estructurado para ser fácilmente convertido a un tema de WordPress
2. **Clases CSS**: Utilizan nomenclatura compatible con Elementor
3. **Imágenes**: Optimizadas y organizadas para fácil importación
4. **Contenido**: Preparado para ser importado como posts y páginas

### Instrucciones para Elementor
1. **Importar Imágenes**: Subir todas las imágenes de la carpeta `assets/images/` a la biblioteca de medios
2. **Crear Páginas**: Usar el contenido de `contenido-categorias.md` para crear páginas y posts
3. **Aplicar Estilos**: Los estilos CSS pueden ser añadidos en el personalizador de WordPress
4. **Configurar Menús**: Crear menús de navegación basados en la estructura HTML

## Instalación y Configuración

### Para Desarrollo Local
1. Descargar todos los archivos del proyecto
2. Abrir `index.html` en un navegador web
3. Para desarrollo, usar un servidor local (Live Server, XAMPP, etc.)

### Para Hosting
1. Subir todos los archivos a la carpeta raíz del hosting
2. Asegurar que las rutas de imágenes sean correctas
3. Configurar redirects si es necesario

### Para WordPress
1. Instalar WordPress en el hosting
2. Instalar el plugin Elementor
3. Importar las imágenes a la biblioteca de medios
4. Crear páginas usando Elementor basadas en el diseño HTML
5. Aplicar los estilos CSS personalizados

## Optimización SEO

### Meta Tags Incluidos
- Títulos descriptivos para cada página
- Meta descriptions optimizadas
- Estructura de headings jerárquica (H1, H2, H3)
- Alt text para todas las imágenes

### Rendimiento
- Imágenes optimizadas para web
- CSS y JavaScript minificables
- Estructura HTML semántica
- Carga asíncrona de fuentes

## Mantenimiento y Actualizaciones

### Agregar Nuevos Artículos
1. Seguir la estructura HTML de los artículos existentes
2. Usar las clases CSS definidas para mantener consistencia
3. Optimizar imágenes antes de subirlas
4. Actualizar menús de navegación si es necesario

### Modificar Estilos
- Los colores principales están definidos como variables CSS en `:root`
- Modificar `style.css` para cambios de diseño
- Probar en diferentes dispositivos después de cambios

## Soporte y Contacto

Para soporte técnico o consultas sobre el proyecto:
- Email: info@eneablog.org
- Documentación adicional disponible en los comentarios del código

## Licencia

Este proyecto está diseñado específicamente para la Estrategia Nacional de Educación Ambiental (ENEA) y su uso está destinado a fines educativos y de promoción.

---

  
**Fecha**: Enero 2025  
**Versión**: 1.0

