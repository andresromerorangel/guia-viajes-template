# 🗺️ Guía de Viajes - Plantilla Interactiva V5.2

Una plantilla HTML interactiva y profesional para crear guías de viaje personalizadas, exportables a PDF.

![Version](https://img.shields.io/badge/version-5.2-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## ✨ Características Principales

### 📝 Edición en Vivo
- **Click para editar** cualquier texto directamente en la página
- Límites de caracteres automáticos por campo
- Sistema de deshacer (Ctrl+Z)
- Guardado automático de sesión

### 🎨 Personalización Visual
- **Editor de colores** integrado en el panel lateral
- 4 colores personalizables: Primario, Secundario, Acento y Fondo
- Cambios en tiempo real con código hexadecimal visible
- Colores preservados en exportación PDF

### 📸 Gestión de Fotos
- Subir múltiples imágenes a la vez (botón dedicado)
- Drag & drop soportado
- **Toggle de ratio** clickeando el badge (1:1 ↔ 2.5:1)
- Hasta 20 fotos por guía
- Los badges de dimensión se ocultan en PDF

### 💰 Nivel de Coste Interactivo
- **5 círculos clickeables** para seleccionar nivel de coste
- Feedback visual al hacer hover
- Se actualiza automáticamente el texto descriptivo
- Valores: Muy barato → Barato → Moderado → Caro → Muy caro

### 🗺️ Mapa Interactivo
- Subir imagen de mapa personalizada
- Pins arrastrables para marcar ciudades
- Auto-ubicación de pins
- Hasta 30 ciudades

### 📍 40+ Categorías de Lugares
Sistema de categorías con emojis (click para ver todas):

| Categoría | Emoji | Categoría | Emoji |
|-----------|-------|-----------|-------|
| MUST | ⭐ | SKIP | ⛔ |
| MUSEO | 🏛️ | COMIDA | 🍽️ |
| TEMPLO | ⛩️ | HIKE | 🥾 |
| PLAYA | 🏖️ | BAR | 🍺 |
| CAFÉ | ☕ | MIRADOR | 🌄 |
| FESTIVAL | 🎉 | MERCADO | 🛒 |
| PARQUE | 🌳 | SAGRADO | 🙏 |

### 📊 Información de Presupuesto
- Presupuesto por día y total gastado
- Costos desglosados: hospedaje, comida, bebida
- Moneda e idioma
- Religiones principales

### 📄 Exportación
- **PDF A4** limpio sin controles de edición
- **Exportar JSON** con imágenes incluidas (base64)
- **Importar JSON** para restaurar completamente
- Colores, categorías y ratios de fotos preservados

### 🎯 Layout Flexible
- 2 columnas principales (38% / 62%)
- **Top Lugares**: Se expande a 2 columnas
- **Consejos Rápidos**: Se expande a ancho completo
- Responsive con escalado automático

## 🚀 Uso Rápido

### Opción 1: Editar Variables (Para nuevos países)
```javascript
const TEMPLATE_CONFIG = {
    pais: "Tu País",
    nombre_pais: "Tu País - Descripción",
    fechas: "Mes - Mes Año",
    duracion: "X días",
    coste_nivel: 3, // 1-5 (clickeable en la página)
    moneda: "USD",
    idioma: "Español",
    // ... más variables
};
```

### Opción 2: Edición Visual
1. Abre `index.html` en el navegador
2. Click en cualquier texto para editarlo
3. Click en círculos de coste para cambiar nivel
4. Usa el panel lateral para colores y exportación

## ⌨️ Atajos de Teclado

| Atajo | Acción |
|-------|--------|
| `Ctrl + S` | Guardar sesión localmente |
| `Ctrl + Z` | Deshacer última acción |
| `Escape` | Salir de vista previa |

## 📋 Variables Disponibles

### Información Básica
| Variable | Descripción | Límite |
|----------|-------------|--------|
| `pais` | Nombre del país | 30 chars |
| `nombre_pais` | Título descriptivo | 25 chars |
| `fechas` | Período del viaje | 20 chars |
| `duracion` | Duración total | 15 chars |
| `coste_nivel` | 1-5 (clickeable) | Número |

### Presupuesto
| Variable | Descripción |
|----------|-------------|
| `presupuesto_dia` | Gasto promedio diario |
| `total_gastado` | Total del viaje |
| `costo_hospedaje` | Precio de alojamiento |
| `costo_comida` | Precio de comidas |
| `costo_bebida` | Precio de bebidas |

### Colores Personalizables
```javascript
color_primario: "#0F7A78",    // Teal oscuro
color_secundario: "#5FB4B2",  // Teal claro
color_acento: "#FF6B61",      // Coral
color_fondo: "#F6EFE6",       // Arena/beige
```

## 🔧 Funcionalidades Técnicas

### Sistema de Guardado
- **Sesión local**: localStorage automático
- **Exportar JSON**: Archivo descargable con todo incluido
- **Importar JSON**: Restauración completa

### Datos que se guardan/exportan
- ✅ Contenido de todos los textos editables
- ✅ Imágenes (como base64)
- ✅ Ratios de fotos (1:1 o 2.5:1)
- ✅ Nivel de coste
- ✅ Colores personalizados
- ✅ Categorías de lugares
- ✅ Posiciones de pins del mapa
- ✅ Logo y bandera

### Impresión/PDF
- Colores preservados con `-webkit-print-color-adjust`
- Controles ocultos automáticamente
- Badges de dimensión ocultos
- Dimensiones A4 (210mm × 297mm)

## 📝 Changelog

### V5.2 (Actual)
- ✅ Layout flexible con Top Lugares y Consejos a ancho completo
- ✅ Corrección de exportación PDF (texto visible)
- ✅ Círculos de coste clickeables con feedback visual
- ✅ Exportar/Importar guarda colores, categorías y ratios
- ✅ Documentación actualizada

### V5.1
- Sistema de variables centralizadas (TEMPLATE_CONFIG)
- Editor de colores en panel lateral
- Exportar/Importar JSON con imágenes
- Toggle de ratio de fotos (1:1 ↔ 2.5:1)
- 40+ categorías de lugares con modal de selección

### V5.0
- Rediseño completo de interfaz
- Sistema de mapas con pins arrastrables
- Categorías de lugares expandidas

## 🎯 Tips de Uso

1. **Nivel de coste**: Click directamente en los círculos para cambiar
2. **Ratio de fotos**: Click en el badge "1:1" o "2.5:1" para alternar
3. **Categorías**: Click en cualquier etiqueta de lugar para ver las 40+ opciones
4. **Colores**: Usa el editor del panel para personalizar sin tocar código
5. **Mapas**: Busca imágenes en [Natural Earth](https://naturalearthdata.com) o [Wikimedia](https://commons.wikimedia.org)

## 📁 Estructura

```
guia-viajes-template/
├── index.html      # Plantilla principal (todo en uno)
├── README.md       # Esta documentación
└── exports/        # Carpeta sugerida para JSONs exportados
```

## 📄 Licencia

MIT License - Libre para uso personal y comercial.

---

Creado con ❤️ para viajeros
