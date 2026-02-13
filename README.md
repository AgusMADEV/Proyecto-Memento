# Proyecto-Memento

## 🎯 Mejoras a Implementar

⚙️ FUNCIONALES (Alto Calado)
❌ IndexedDB - Persistencia real entre sesiones
❌ CRUD Completo - Crear, leer, eliminar recuerdos
❌ Búsqueda semántica - Filtrado en tiempo real
✅ Import/Export JSON - Backups y migraciones
✅ Export CSV - Exportación a Excel/Sheets
❌ Formulario dinámico - 7 campos validados
✅ Notificaciones toast - Feedback visual
❌ Estadísticas live - 4 métricas actualizadas
❌ Física optimizada - Con detección de estabilidad

🎨 ESTÉTICAS
✅ Glassmorphism - Paneles con efecto cristal
✅ Animaciones CSS - fadeIn, scaleIn, slideIn, spin
❌ Variables CSS - Sistema de colores coherente
✅ Botones gradiente - Con efectos hover
❌ Modal mejorado - Diseño tipo tarjeta
✅ Iluminación 3D - 5 luces con colores temáticos
❌ Scrollbar custom - Estilo del tema
❌ Tags visuales - Chips de propiedades

## 📦 Nuevas Funcionalidades Implementadas

### Sistema de Import/Export de Datos

#### 📥 Exportar JSON
- Descarga todos los datos actuales en formato JSON
- Nombre del archivo incluye la fecha: `memento-export-YYYY-MM-DD.json`
- Mantiene la estructura completa con todas las propiedades
- Notificación de éxito/error

#### 📊 Exportar CSV
- Exporta los datos en formato CSV compatible con Excel y Google Sheets
- Incluye BOM UTF-8 para correcta visualización de caracteres especiales
- Detecta automáticamente todas las propiedades presentes
- Escapa correctamente comillas dobles y valores especiales
- Nombre del archivo: `memento-export-YYYY-MM-DD.csv`

#### 📤 Importar JSON
- Carga datos desde archivo JSON externo
- **Validaciones implementadas:**
  - Verifica que el archivo sea un array válido
  - Valida que no esté vacío
  - Comprueba la estructura de cada elemento
  - Requiere objeto `categories` en cada elemento
  - Filtra elementos inválidos automáticamente
- Recarga la escena 3D con los nuevos datos
- Actualiza propiedades y controles dinámicamente
- Notificaciones detalladas del proceso

### 🔔 Sistema de Notificaciones Toast

Sistema visual de feedback con 4 tipos:
- ✅ **Success** (verde): Operaciones exitosas
- ❌ **Error** (rojo): Errores y fallos
- ℹ️ **Info** (azul): Información general
- ⚠️ **Warning** (amarillo): Advertencias

**Características:**
- Aparecen en la esquina superior derecha
- Auto-desaparecen después de 3-5 segundos
- Click para cerrar manualmente
- Animaciones suaves de entrada/salida
- Efecto glassmorphism integrado
- Múltiples toasts apilables

### 💡 Sistema de Iluminación 3D Dinámica

Sistema de 5 luces **animadas** con colores temáticos que pulsan al ritmo del sistema:

- **🌟 Luz Ambiental Base** (#88c8ff) - Pulsación lenta (4s) para respiración ambiente
- **✅ Luz Success** (#34D399) - Pulsación rápida (2.5s) energizante arriba-derecha
- **⚠️ Luz Warning** (#FBBF24) - Pulsación media (3.2s) cálida izquierda-frontal
- **ℹ️ Luz Info** (#60A5FA) - Respiración lenta (3.8s) focal principal centro-atrás
- **🔥 Luz Accent** (#F87171) - Latido rápido (2s) sutil derecha-atrás

**Características técnicas:**
- Animaciones A-Frame nativas (`property: light.intensity`)
- Cada luz tiene ritmo único (2s a 4s) para efecto orgánico
- Rangos de intensidad calibrados sin molestar visualmente
- Funciones easing variadas: `easeInOutSine`, `easeInOutQuad`, `easeInOutCubic`
- Colores extraídos del sistema de toasts para coherencia temática
- Posicionamiento 3D estratégico para iluminación envolvente
- **Efecto "respiración" continuo** que da vida a la escena

## 🗂️ Archivos de Ejemplo Incluidos

El proyecto incluye varios datasets de ejemplo para demostrar la versatilidad del sistema:

1. **📁 personas2.json** - Dataset principal (145 personas)
2. **📁 ejemplo-importacion.json** - 40 personas variadas para pruebas
3. **⚽ ejemplo-futbolistas-laliga.json** - 40 futbolistas de LaLiga (SÚPER COMPLETO)
4. **📁 ejemplo-peliculas.json** - 20 películas internacionales
5. **📁 ejemplo-libros.json** - 15 libros clásicos y contemporáneos  
6. **📁 ejemplo-productos.json** - 15 productos tecnológicos

**📖 Guías específicas:**
- [README_FUTBOLISTAS.md](README_FUTBOLISTAS.md) - Análisis completo del dataset de futbolistas

**Cada archivo demuestra cómo el sistema se adapta automáticamente a diferentes tipos de datos y categorías.**

---

## 🎮 Cómo Usar

### Exportar Datos

1. **Exportar JSON:**
   - Click en "📥 Exportar JSON"
   - El archivo se descargará automáticamente
   - Úsalo para backups o transferir entre dispositivos

2. **Exportar CSV:**
   - Click en "📊 Exportar CSV"
   - Abre el archivo en Excel, LibreOffice Calc o Google Sheets
   - Perfecto para análisis de datos o compartir

### Importar Datos

1. Click en "📤 Importar JSON"
2. Selecciona un archivo JSON válido
3. El sistema validará automáticamente:
   - Formato JSON correcto
   - Estructura de datos
   - Elementos válidos
4. La escena se recargará con los nuevos datos
5. Verás una notificación con el resultado

### Formato de Datos Válido

```json
[
  {
    "categories": {
      "nombre": "Juan",
      "hobbie": "Ajedrez",
      "edad": 20,
      "ciudad": "Valencia",
      "profesion": "Estudiante"
    },
    "content": "<h2>Juan (20)</h2><p><strong>Ciudad:</strong> Valencia</p>"
  }
]
```

**Requisitos:**
- Debe ser un array de objetos
- Cada objeto debe tener un campo `categories` (objeto)
- `content` es opcional pero recomendado para el modal
- Las propiedades dentro de `categories` serán detectadas automáticamente

## 🛠️ Tecnologías Utilizadas

- **A-Frame 1.5.0**: Visualización 3D
- **Web Workers**: Física en segundo plano
- **FileReader API**: Lectura de archivos
- **Blob API**: Generación de archivos para descarga
- **CSS Animations**: Efectos visuales suaves
- **Glassmorphism**: Diseño moderno con efecto cristal

## 📝 Notas Técnicas

### Validación de Importación
El sistema es robusto ante errores:
- Elementos sin `categories` son ignorados (con warning)
- Continúa la importación aunque algunos elementos sean inválidos
- Muestra el número total de elementos válidos importados

### Export CSV
- Usa delimitador de coma estándar
- Comillas dobles para valores con caracteres especiales
- BOM UTF-8 para compatibilidad con Excel en Windows
- Columnas ordenadas alfabéticamente

### Seguridad
- No se ejecuta código del archivo importado
- Solo se leen estructuras de datos
- Validación estricta antes de procesar

## 🎨 Personalización Total

**¡El sistema es 100% dinámico!** Puedes usar cualquier tipo de datos con cualquier categoría.

### Archivos de Ejemplo Incluidos:

- **🎬 Películas**: Géneros, directores, países
- **📚 Libros**: Autores, idiomas, géneros literarios  
- **💻 Productos**: Marcas, categorías, precios
- **👥 Personas**: Hobbies, ciudades, profesiones

### ¿Cómo Probarlo?

1. Click en "📤 Importar JSON"
2. Selecciona cualquier archivo `ejemplo-*.json`
3. La aplicación detectará automáticamente las categorías
4. Verás las nuevas conexiones basadas en valores compartidos

### Crear Tu Propio Dataset

Consulta [GUIA_PERSONALIZACION.md](GUIA_PERSONALIZACION.md) para:
- Plantillas listas para usar
- Ejemplos de diferentes dominios
- Reglas de formato
- Casos de uso creativos

**Ejemplos de datos que puedes visualizar:**
- Restaurantes (tipo, precio, ubicación)
- Universidades (ranking, país, tipo)
- Videojuegos (plataforma, género, desarrollador)
- Recetas (cocina, dificultad, tiempo)
- Proyectos (estado, tecnología, responsable)
- ¡Y cualquier cosa que se te ocurra!