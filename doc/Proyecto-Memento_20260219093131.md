# Reporte de proyecto

## Estructura del proyecto

```
C:\xampp\htdocs\GitHub\Proyecto-Memento
├── .gitignore
├── README.md
├── ejemplo-futbolistas-laliga.json
├── ejemplo-importacion.json
├── ejemplo-libros.json
├── ejemplo-peliculas.json
├── ejemplo-productos.json
├── index.html
├── logo_azul.png
├── personas2.json
└── worker.js
```

## Código (intercalado)

# Proyecto-Memento
**README.md**
```markdown
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
✅ Estadísticas live - 4 métricas actualizadas
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

### 📊 Panel de Estadísticas Live

Panel en tiempo real con 4 métricas clave del sistema:

- **🔵 Nodos Activos** - Total de elementos/partículas en la escena
- **🟢 Conexiones Dibujadas** - Líneas activas entre nodos relacionados
- **🟣 Propiedades Habilitadas** - Categorías usadas para crear relaciones
- **🟡 FPS (Rendimiento)** - Frames por segundo de la escena 3D

**Características del panel:**
- Posicionado en esquina superior derecha para no obstruir
- Estilo glassmorphism integrado con el tema
- Actualización automática en tiempo real
- Animaciones suaves al cambiar valores
- Iconos y colores distintivos para cada métrica
- FPS actualizado cada 500ms para medición precisa
- Efecto visual de pulso al actualizar valores

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
```
**ejemplo-futbolistas-laliga.json**
```json
[
  {
    "categories": {
      "nombre": "Robert Lewandowski",
      "posicion": "Delantero",
      "equipo": "FC Barcelona",
      "goles": 23,
      "asistencias": 8,
      "edad": 35,
      "nacionalidad": "Polonia",
      "dorsal": 9,
      "pierna": "Derecha",
      "valoracion": 91
    },
    "content": "<h2>Robert Lewandowski #9</h2><p><strong>Equipo:</strong> FC Barcelona<br><strong>Posición:</strong> Delantero<br><strong>Edad:</strong> 35 años<br><strong>Nacionalidad:</strong> Polonia<br><strong>Stats:</strong> 23 goles, 8 asistencias<br><strong>Valoración:</strong> 91</p>"
  },
  {
    "categories": {
      "nombre": "Jude Bellingham",
      "posicion": "Centrocampista",
      "equipo": "Real Madrid",
      "goles": 19,
      "asistencias": 12,
      "edad": 20,
      "nacionalidad": "Inglaterra",
      "dorsal": 5,
      "pierna": "Derecha",
      "valoracion": 90
    },
    "content": "<h2>Jude Bellingham #5</h2><p><strong>Equipo:</strong> Real Madrid<br><strong>Posición:</strong> Centrocampista<br><strong>Edad:</strong> 20 años<br><strong>Nacionalidad:</strong> Inglaterra<br><strong>Stats:</strong> 19 goles, 12 asistencias<br><strong>Valoración:</strong> 90</p>"
  },
  {
    "categories": {
      "nombre": "Marc-André ter Stegen",
      "posicion": "Portero",
      "equipo": "FC Barcelona",
      "goles": 0,
      "asistencias": 0,
      "edad": 31,
      "nacionalidad": "Alemania",
      "dorsal": 1,
      "pierna": "Derecha",
      "valoracion": 89
    },
    "content": "<h2>Marc-André ter Stegen #1</h2><p><strong>Equipo:</strong> FC Barcelona<br><strong>Posición:</strong> Portero<br><strong>Edad:</strong> 31 años<br><strong>Nacionalidad:</strong> Alemania<br><strong>Valoración:</strong> 89</p>"
  },
  {
    "categories": {
      "nombre": "Vinícius Jr",
      "posicion": "Delantero",
      "equipo": "Real Madrid",
      "goles": 18,
      "asistencias": 10,
      "edad": 23,
      "nacionalidad": "Brasil",
      "dorsal": 7,
      "pierna": "Derecha",
      "valoracion": 89
    },
    "content": "<h2>Vinícius Jr #7</h2><p><strong>Equipo:</strong> Real Madrid<br><strong>Posición:</strong> Delantero<br><strong>Edad:</strong> 23 años<br><strong>Nacionalidad:</strong> Brasil<br><strong>Stats:</strong> 18 goles, 10 asistencias<br><strong>Valoración:</strong> 89</p>"
  },
  {
    "categories": {
      "nombre": "Jan Oblak",
      "posicion": "Portero",
      "equipo": "Atlético Madrid",
      "goles": 0,
      "asistencias": 0,
      "edad": 31,
      "nacionalidad": "Eslovenia",
      "dorsal": 13,
      "pierna": "Derecha",
      "valoracion": 89
    },
    "content": "<h2>Jan Oblak #13</h2><p><strong>Equipo:</strong> Atlético Madrid<br><strong>Posición:</strong> Portero<br><strong>Edad:</strong> 31 años<br><strong>Nacionalidad:</strong> Eslovenia<br><strong>Valoración:</strong> 89</p>"
  },
  {
    "categories": {
      "nombre": "Antoine Griezmann",
      "posicion": "Delantero",
      "equipo": "Atlético Madrid",
      "goles": 16,
      "asistencias": 14,
      "edad": 32,
      "nacionalidad": "Francia",
      "dorsal": 8,
      "pierna": "Izquierda",
      "valoracion": 87
    },
    "content": "<h2>Antoine Griezmann #8</h2><p><strong>Equipo:</strong> Atlético Madrid<br><strong>Posición:</strong> Delantero<br><strong>Edad:</strong> 32 años<br><strong>Nacionalidad:</strong> Francia<br><strong>Stats:</strong> 16 goles, 14 asistencias<br><strong>Valoración:</strong> 87</p>"
  },
  {
    "categories": {
      "nombre": "Pedri",
      "posicion": "Centrocampista",
      "equipo": "FC Barcelona",
      "goles": 4,
      "asistencias": 6,
      "edad": 21,
      "nacionalidad": "España",
      "dorsal": 8,
      "pierna": "Derecha",
      "valoracion": 85
    },
    "content": "<h2>Pedri #8</h2><p><strong>Equipo:</strong> FC Barcelona<br><strong>Posición:</strong> Centrocampista<br><strong>Edad:</strong> 21 años<br><strong>Nacionalidad:</strong> España<br><strong>Stats:</strong> 4 goles, 6 asistencias<br><strong>Valoración:</strong> 85</p>"
  },
  {
    "categories": {
      "nombre": "Federico Valverde",
      "posicion": "Centrocampista",
      "equipo": "Real Madrid",
      "goles": 8,
      "asistencias": 7,
      "edad": 25,
      "nacionalidad": "Uruguay",
      "dorsal": 15,
      "pierna": "Derecha",
      "valoracion": 87
    },
    "content": "<h2>Federico Valverde #15</h2><p><strong>Equipo:</strong> Real Madrid<br><strong>Posición:</strong> Centrocampista<br><strong>Edad:</strong> 25 años<br><strong>Nacionalidad:</strong> Uruguay<br><strong>Stats:</strong> 8 goles, 7 asistencias<br><strong>Valoración:</strong> 87</p>"
  },
  {
    "categories": {
      "nombre": "Gavi",
      "posicion": "Centrocampista",
      "equipo": "FC Barcelona",
      "goles": 3,
      "asistencias": 5,
      "edad": 19,
      "nacionalidad": "España",
      "dorsal": 6,
      "pierna": "Derecha",
      "valoracion": 83
    },
    "content": "<h2>Gavi #6</h2><p><strong>Equipo:</strong> FC Barcelona<br><strong>Posición:</strong> Centrocampista<br><strong>Edad:</strong> 19 años<br><strong>Nacionalidad:</strong> España<br><strong>Stats:</strong> 3 goles, 5 asistencias<br><strong>Valoración:</strong> 83</p>"
  },
  {
    "categories": {
      "nombre": "Thibaut Courtois",
      "posicion": "Portero",
      "equipo": "Real Madrid",
      "goles": 0,
      "asistencias": 0,
      "edad": 31,
      "nacionalidad": "Bélgica",
      "dorsal": 1,
      "pierna": "Izquierda",
      "valoracion": 90
    },
    "content": "<h2>Thibaut Courtois #1</h2><p><strong>Equipo:</strong> Real Madrid<br><strong>Posición:</strong> Portero<br><strong>Edad:</strong> 31 años<br><strong>Nacionalidad:</strong> Bélgica<br><strong>Valoración:</strong> 90</p>"
  },
  {
    "categories": {
      "nombre": "Ronald Araújo",
      "posicion": "Defensa",
      "equipo": "FC Barcelona",
      "goles": 2,
      "asistencias": 1,
      "edad": 24,
      "nacionalidad": "Uruguay",
      "dorsal": 4,
      "pierna": "Derecha",
      "valoracion": 85
    },
    "content": "<h2>Ronald Araújo #4</h2><p><strong>Equipo:</strong> FC Barcelona<br><strong>Posición:</strong> Defensa<br><strong>Edad:</strong> 24 años<br><strong>Nacionalidad:</strong> Uruguay<br><strong>Stats:</strong> 2 goles, 1 asistencia<br><strong>Valoración:</strong> 85</p>"
  },
  {
    "categories": {
      "nombre": "Joselu",
      "posicion": "Delantero",
      "equipo": "Real Madrid",
      "goles": 12,
      "asistencias": 4,
      "edad": 33,
      "nacionalidad": "España",
      "dorsal": 14,
      "pierna": "Derecha",
      "valoracion": 79
    },
    "content": "<h2>Joselu #14</h2><p><strong>Equipo:</strong> Real Madrid<br><strong>Posición:</strong> Delantero<br><strong>Edad:</strong> 33 años<br><strong>Nacionalidad:</strong> España<br><strong>Stats:</strong> 12 goles, 4 asistencias<br><strong>Valoración:</strong> 79</p>"
  },
  {
    "categories": {
      "nombre": "Álvaro Morata",
      "posicion": "Delantero",
      "equipo": "Atlético Madrid",
      "goles": 21,
      "asistencias": 5,
      "edad": 31,
      "nacionalidad": "España",
      "dorsal": 19,
      "pierna": "Derecha",
      "valoracion": 82
    },
    "content": "<h2>Álvaro Morata #19</h2><p><strong>Equipo:</strong> Atlético Madrid<br><strong>Posición:</strong> Delantero<br><strong>Edad:</strong> 31 años<br><strong>Nacionalidad:</strong> España<br><strong>Stats:</strong> 21 goles, 5 asistencias<br><strong>Valoración:</strong> 82</p>"
  },
  {
    "categories": {
      "nombre": "Frenkie de Jong",
      "posicion": "Centrocampista",
      "equipo": "FC Barcelona",
      "goles": 2,
      "asistencias": 4,
      "edad": 26,
      "nacionalidad": "Países Bajos",
      "dorsal": 21,
      "pierna": "Derecha",
      "valoracion": 87
    },
    "content": "<h2>Frenkie de Jong #21</h2><p><strong>Equipo:</strong> FC Barcelona<br><strong>Posición:</strong> Centrocampista<br><strong>Edad:</strong> 26 años<br><strong>Nacionalidad:</strong> Países Bajos<br><strong>Stats:</strong> 2 goles, 4 asistencias<br><strong>Valoración:</strong> 87</p>"
  },
  {
    "categories": {
      "nombre": "Luka Modrić",
      "posicion": "Centrocampista",
      "equipo": "Real Madrid",
      "goles": 3,
      "asistencias": 9,
      "edad": 38,
      "nacionalidad": "Croacia",
      "dorsal": 10,
      "pierna": "Derecha",
      "valoracion": 84
    },
    "content": "<h2>Luka Modrić #10</h2><p><strong>Equipo:</strong> Real Madrid<br><strong>Posición:</strong> Centrocampista<br><strong>Edad:</strong> 38 años<br><strong>Nacionalidad:</strong> Croacia<br><strong>Stats:</strong> 3 goles, 9 asistencias<br><strong>Valoración:</strong> 84</p>"
  },
  {
    "categories": {
      "nombre": "Koke",
      "posicion": "Centrocampista",
      "equipo": "Atlético Madrid",
      "goles": 2,
      "asistencias": 8,
      "edad": 31,
      "nacionalidad": "España",
      "dorsal": 6,
      "pierna": "Derecha",
      "valoracion": 82
    },
    "content": "<h2>Koke #6</h2><p><strong>Equipo:</strong> Atlético Madrid<br><strong>Posición:</strong> Centrocampista<br><strong>Edad:</strong> 31 años<br><strong>Nacionalidad:</strong> España<br><strong>Stats:</strong> 2 goles, 8 asistencias<br><strong>Valoración:</strong> 82</p>"
  },
  {
    "categories": {
      "nombre": "Mikel Oyarzabal",
      "posicion": "Delantero",
      "equipo": "Real Sociedad",
      "goles": 14,
      "asistencias": 7,
      "edad": 26,
      "nacionalidad": "España",
      "dorsal": 10,
      "pierna": "Izquierda",
      "valoracion": 83
    },
    "content": "<h2>Mikel Oyarzabal #10</h2><p><strong>Equipo:</strong> Real Sociedad<br><strong>Posición:</strong> Delantero<br><strong>Edad:</strong> 26 años<br><strong>Nacionalidad:</strong> España<br><strong>Stats:</strong> 14 goles, 7 asistencias<br><strong>Valoración:</strong> 83</p>"
  },
  {
    "categories": {
      "nombre": "Iago Aspas",
      "posicion": "Delantero",
      "equipo": "Celta de Vigo",
      "goles": 15,
      "asistencias": 9,
      "edad": 36,
      "nacionalidad": "España",
      "dorsal": 10,
      "pierna": "Izquierda",
      "valoracion": 81
    },
    "content": "<h2>Iago Aspas #10</h2><p><strong>Equipo:</strong> Celta de Vigo<br><strong>Posición:</strong> Delantero<br><strong>Edad:</strong> 36 años<br><strong>Nacionalidad:</strong> España<br><strong>Stats:</strong> 15 goles, 9 asistencias<br><strong>Valoración:</strong> 81</p>"
  },
  {
    "categories": {
      "nombre": "Jules Koundé",
      "posicion": "Defensa",
      "equipo": "FC Barcelona",
      "goles": 1,
      "asistencias": 2,
      "edad": 25,
      "nacionalidad": "Francia",
      "dorsal": 23,
      "pierna": "Derecha",
      "valoracion": 84
    },
    "content": "<h2>Jules Koundé #23</h2><p><strong>Equipo:</strong> FC Barcelona<br><strong>Posición:</strong> Defensa<br><strong>Edad:</strong> 25 años<br><strong>Nacionalidad:</strong> Francia<br><strong>Stats:</strong> 1 gol, 2 asistencias<br><strong>Valoración:</strong> 84</p>"
  },
  {
    "categories": {
      "nombre": "David Alaba",
      "posicion": "Defensa",
      "equipo": "Real Madrid",
      "goles": 1,
      "asistencias": 1,
      "edad": 31,
      "nacionalidad": "Austria",
      "dorsal": 4,
      "pierna": "Izquierda",
      "valoracion": 85
    },
    "content": "<h2>David Alaba #4</h2><p><strong>Equipo:</strong> Real Madrid<br><strong>Posición:</strong> Defensa<br><strong>Edad:</strong> 31 años<br><strong>Nacionalidad:</strong> Austria<br><strong>Stats:</strong> 1 gol, 1 asistencia<br><strong>Valoración:</strong> 85</p>"
  },
  {
    "categories": {
      "nombre": "Rodri De Paul",
      "posicion": "Centrocampista",
      "equipo": "Atlético Madrid",
      "goles": 5,
      "asistencias": 6,
      "edad": 29,
      "nacionalidad": "Argentina",
      "dorsal": 5,
      "pierna": "Derecha",
      "valoracion": 82
    },
    "content": "<h2>Rodri De Paul #5</h2><p><strong>Equipo:</strong> Atlético Madrid<br><strong>Posición:</strong> Centrocampista<br><strong>Edad:</strong> 29 años<br><strong>Nacionalidad:</strong> Argentina<br><strong>Stats:</strong> 5 goles, 6 asistencias<br><strong>Valoración:</strong> 82</p>"
  },
  {
    "categories": {
      "nombre": "Borja Iglesias",
      "posicion": "Delantero",
      "equipo": "Real Betis",
      "goles": 11,
      "asistencias": 3,
      "edad": 30,
      "nacionalidad": "España",
      "dorsal": 9,
      "pierna": "Derecha",
      "valoracion": 79
    },
    "content": "<h2>Borja Iglesias #9</h2><p><strong>Equipo:</strong> Real Betis<br><strong>Posición:</strong> Delantero<br><strong>Edad:</strong> 30 años<br><strong>Nacionalidad:</strong> España<br><strong>Stats:</strong> 11 goles, 3 asistencias<br><strong>Valoración:</strong> 79</p>"
  },
  {
    "categories": {
      "nombre": "Iñaki Williams",
      "posicion": "Delantero",
      "equipo": "Athletic Bilbao",
      "goles": 10,
      "asistencias": 6,
      "edad": 29,
      "nacionalidad": "Ghana",
      "dorsal": 9,
      "pierna": "Derecha",
      "valoracion": 81
    },
    "content": "<h2>Iñaki Williams #9</h2><p><strong>Equipo:</strong> Athletic Bilbao<br><strong>Posición:</strong> Delantero<br><strong>Edad:</strong> 29 años<br><strong>Nacionalidad:</strong> Ghana<br><strong>Stats:</strong> 10 goles, 6 asistencias<br><strong>Valoración:</strong> 81</p>"
  },
  {
    "categories": {
      "nombre": "Hugo Duro",
      "posicion": "Delantero",
      "equipo": "Valencia CF",
      "goles": 13,
      "asistencias": 4,
      "edad": 24,
      "nacionalidad": "España",
      "dorsal": 19,
      "pierna": "Izquierda",
      "valoracion": 78
    },
    "content": "<h2>Hugo Duro #19</h2><p><strong>Equipo:</strong> Valencia CF<br><strong>Posición:</strong> Delantero<br><strong>Edad:</strong> 24 años<br><strong>Nacionalidad:</strong> España<br><strong>Stats:</strong> 13 goles, 4 asistencias<br><strong>Valoración:</strong> 78</p>"
  },
  {
    "categories": {
      "nombre": "Nico Williams",
      "posicion": "Delantero",
      "equipo": "Athletic Bilbao",
      "goles": 8,
      "asistencias": 11,
      "edad": 21,
      "nacionalidad": "España",
      "dorsal": 10,
      "pierna": "Derecha",
      "valoracion": 82
    },
    "content": "<h2>Nico Williams #10</h2><p><strong>Equipo:</strong> Athletic Bilbao<br><strong>Posición:</strong> Delantero<br><strong>Edad:</strong> 21 años<br><strong>Nacionalidad:</strong> España<br><strong>Stats:</strong> 8 goles, 11 asistencias<br><strong>Valoración:</strong> 82</p>"
  },
  {
    "categories": {
      "nombre": "Raphinha",
      "posicion": "Delantero",
      "equipo": "FC Barcelona",
      "goles": 9,
      "asistencias": 10,
      "edad": 27,
      "nacionalidad": "Brasil",
      "dorsal": 11,
      "pierna": "Izquierda",
      "valoracion": 84
    },
    "content": "<h2>Raphinha #11</h2><p><strong>Equipo:</strong> FC Barcelona<br><strong>Posición:</strong> Delantero<br><strong>Edad:</strong> 27 años<br><strong>Nacionalidad:</strong> Brasil<br><strong>Stats:</strong> 9 goles, 10 asistencias<br><strong>Valoración:</strong> 84</p>"
  },
  {
    "categories": {
      "nombre": "Rodrygo",
      "posicion": "Delantero",
      "equipo": "Real Madrid",
      "goles": 11,
      "asistencias": 8,
      "edad": 23,
      "nacionalidad": "Brasil",
      "dorsal": 11,
      "pierna": "Derecha",
      "valoracion": 85
    },
    "content": "<h2>Rodrygo #11</h2><p><strong>Equipo:</strong> Real Madrid<br><strong>Posición:</strong> Delantero<br><strong>Edad:</strong> 23 años<br><strong>Nacionalidad:</strong> Brasil<br><strong>Stats:</strong> 11 goles, 8 asistencias<br><strong>Valoración:</strong> 85</p>"
  },
  {
    "categories": {
      "nombre": "Unai Simón",
      "posicion": "Portero",
      "equipo": "Athletic Bilbao",
      "goles": 0,
      "asistencias": 0,
      "edad": 26,
      "nacionalidad": "España",
      "dorsal": 1,
      "pierna": "Derecha",
      "valoracion": 84
    },
    "content": "<h2>Unai Simón #1</h2><p><strong>Equipo:</strong> Athletic Bilbao<br><strong>Posición:</strong> Portero<br><strong>Edad:</strong> 26 años<br><strong>Nacionalidad:</strong> España<br><strong>Valoración:</strong> 84</p>"
  },
  {
    "categories": {
      "nombre": "Rui Silva",
      "posicion": "Portero",
      "equipo": "Real Betis",
      "goles": 0,
      "asistencias": 0,
      "edad": 29,
      "nacionalidad": "Portugal",
      "dorsal": 13,
      "pierna": "Derecha",
      "valoracion": 81
    },
    "content": "<h2>Rui Silva #13</h2><p><strong>Equipo:</strong> Real Betis<br><strong>Posición:</strong> Portero<br><strong>Edad:</strong> 29 años<br><strong>Nacionalidad:</strong> Portugal<br><strong>Valoración:</strong> 81</p>"
  },
  {
    "categories": {
      "nombre": "Sergio Canales",
      "posicion": "Centrocampista",
      "equipo": "Monterrey",
      "goles": 7,
      "asistencias": 10,
      "edad": 32,
      "nacionalidad": "España",
      "dorsal": 10,
      "pierna": "Izquierda",
      "valoracion": 82
    },
    "content": "<h2>Sergio Canales #10</h2><p><strong>Equipo:</strong> Monterrey<br><strong>Posición:</strong> Centrocampista<br><strong>Edad:</strong> 32 años<br><strong>Nacionalidad:</strong> España<br><strong>Stats:</strong> 7 goles, 10 asistencias<br><strong>Valoración:</strong> 82</p>"
  },
  {
    "categories": {
      "nombre": "Álex Remiro",
      "posicion": "Portero",
      "equipo": "Real Sociedad",
      "goles": 0,
      "asistencias": 0,
      "edad": 28,
      "nacionalidad": "España",
      "dorsal": 1,
      "pierna": "Derecha",
      "valoracion": 82
    },
    "content": "<h2>Álex Remiro #1</h2><p><strong>Equipo:</strong> Real Sociedad<br><strong>Posición:</strong> Portero<br><strong>Edad:</strong> 28 años<br><strong>Nacionalidad:</strong> España<br><strong>Valoración:</strong> 82</p>"
  },
  {
    "categories": {
      "nombre": "Memphis Depay",
      "posicion": "Delantero",
      "equipo": "Atlético Madrid",
      "goles": 9,
      "asistencias": 4,
      "edad": 29,
      "nacionalidad": "Países Bajos",
      "dorsal": 9,
      "pierna": "Derecha",
      "valoracion": 81
    },
    "content": "<h2>Memphis Depay #9</h2><p><strong>Equipo:</strong> Atlético Madrid<br><strong>Posición:</strong> Delantero<br><strong>Edad:</strong> 29 años<br><strong>Nacionalidad:</strong> Países Bajos<br><strong>Stats:</strong> 9 goles, 4 asistencias<br><strong>Valoración:</strong> 81</p>"
  },
  {
    "categories": {
      "nombre": "Ilkay Gündogan",
      "posicion": "Centrocampista",
      "equipo": "FC Barcelona",
      "goles": 5,
      "asistencias": 8,
      "edad": 33,
      "nacionalidad": "Alemania",
      "dorsal": 22,
      "pierna": "Derecha",
      "valoracion": 86
    },
    "content": "<h2>Ilkay Gündogan #22</h2><p><strong>Equipo:</strong> FC Barcelona<br><strong>Posición:</strong> Centrocampista<br><strong>Edad:</strong> 33 años<br><strong>Nacionalidad:</strong> Alemania<br><strong>Stats:</strong> 5 goles, 8 asistencias<br><strong>Valoración:</strong> 86</p>"
  },
  {
    "categories": {
      "nombre": "Eduardo Camavinga",
      "posicion": "Centrocampista",
      "equipo": "Real Madrid",
      "goles": 2,
      "asistencias": 3,
      "edad": 21,
      "nacionalidad": "Francia",
      "dorsal": 12,
      "pierna": "Izquierda",
      "valoracion": 83
    },
    "content": "<h2>Eduardo Camavinga #12</h2><p><strong>Equipo:</strong> Real Madrid<br><strong>Posición:</strong> Centrocampista<br><strong>Edad:</strong> 21 años<br><strong>Nacionalidad:</strong> Francia<br><strong>Stats:</strong> 2 goles, 3 asistencias<br><strong>Valoración:</strong> 83</p>"
  },
  {
    "categories": {
      "nombre": "Axel Witsel",
      "posicion": "Defensa",
      "equipo": "Atlético Madrid",
      "goles": 0,
      "asistencias": 0,
      "edad": 35,
      "nacionalidad": "Bélgica",
      "dorsal": 20,
      "pierna": "Derecha",
      "valoracion": 78
    },
    "content": "<h2>Axel Witsel #20</h2><p><strong>Equipo:</strong> Atlético Madrid<br><strong>Posición:</strong> Defensa<br><strong>Edad:</strong> 35 años<br><strong>Nacionalidad:</strong> Bélgica<br><strong>Valoración:</strong> 78</p>"
  },
  {
    "categories": {
      "nombre": "Dani Carvajal",
      "posicion": "Defensa",
      "equipo": "Real Madrid",
      "goles": 1,
      "asistencias": 5,
      "edad": 32,
      "nacionalidad": "España",
      "dorsal": 2,
      "pierna": "Derecha",
      "valoracion": 83
    },
    "content": "<h2>Dani Carvajal #2</h2><p><strong>Equipo:</strong> Real Madrid<br><strong>Posición:</strong> Defensa<br><strong>Edad:</strong> 32 años<br><strong>Nacionalidad:</strong> España<br><strong>Stats:</strong> 1 gol, 5 asistencias<br><strong>Valoración:</strong> 83</p>"
  },
  {
    "categories": {
      "nombre": "Marcos Llorente",
      "posicion": "Centrocampista",
      "equipo": "Atlético Madrid",
      "goles": 6,
      "asistencias": 7,
      "edad": 29,
      "nacionalidad": "España",
      "dorsal": 14,
      "pierna": "Derecha",
      "valoracion": 84
    },
    "content": "<h2>Marcos Llorente #14</h2><p><strong>Equipo:</strong> Atlético Madrid<br><strong>Posición:</strong> Centrocampista<br><strong>Edad:</strong> 29 años<br><strong>Nacionalidad:</strong> España<br><strong>Stats:</strong> 6 goles, 7 asistencias<br><strong>Valoración:</strong> 84</p>"
  },
  {
    "categories": {
      "nombre": "Iago Aspas",
      "posicion": "Delantero",
      "equipo": "Celta de Vigo",
      "goles": 12,
      "asistencias": 8,
      "edad": 36,
      "nacionalidad": "España",
      "dorsal": 10,
      "pierna": "Izquierda",
      "valoracion": 81
    },
    "content": "<h2>Iago Aspas #10</h2><p><strong>Equipo:</strong> Celta de Vigo<br><strong>Posición:</strong> Delantero<br><strong>Edad:</strong> 36 años<br><strong>Nacionalidad:</strong> España<br><strong>Stats:</strong> 12 goles, 8 asistencias<br><strong>Valoración:</strong> 81</p>"
  },
  {
    "categories": {
      "nombre": "Álex Baena",
      "posicion": "Centrocampista",
      "equipo": "Villarreal CF",
      "goles": 8,
      "asistencias": 12,
      "edad": 22,
      "nacionalidad": "España",
      "dorsal": 16,
      "pierna": "Derecha",
      "valoracion": 82
    },
    "content": "<h2>Álex Baena #16</h2><p><strong>Equipo:</strong> Villarreal CF<br><strong>Posición:</strong> Centrocampista<br><strong>Edad:</strong> 22 años<br><strong>Nacionalidad:</strong> España<br><strong>Stats:</strong> 8 goles, 12 asistencias<br><strong>Valoración:</strong> 82</p>"
  },
  {
    "categories": {
      "nombre": "Alexander Sørloth",
      "posicion": "Delantero",
      "equipo": "Villarreal CF",
      "goles": 17,
      "asistencias": 3,
      "edad": 28,
      "nacionalidad": "Noruega",
      "dorsal": 11,
      "pierna": "Izquierda",
      "valoracion": 80
    },
    "content": "<h2>Alexander Sørloth #11</h2><p><strong>Equipo:</strong> Villarreal CF<br><strong>Posición:</strong> Delantero<br><strong>Edad:</strong> 28 años<br><strong>Nacionalidad:</strong> Noruega<br><strong>Stats:</strong> 17 goles, 3 asistencias<br><strong>Valoración:</strong> 80</p>"
  }
]

```
**ejemplo-importacion.json**
```json
[
  {
    "categories": {
      "nombre": "María",
      "hobbie": "Fotografía",
      "edad": 28,
      "ciudad": "Barcelona",
      "profesion": "Diseñadora"
    },
    "content": "<h2>María (28)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Diseñadora<br><strong>Hobbie:</strong> Fotografía</p>"
  },
  {
    "categories": {
      "nombre": "Carlos",
      "hobbie": "Ciclismo",
      "edad": 35,
      "ciudad": "Madrid",
      "profesion": "Ingeniero"
    },
    "content": "<h2>Carlos (35)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Ingeniero<br><strong>Hobbie:</strong> Ciclismo</p>"
  },
  {
    "categories": {
      "nombre": "Ana",
      "hobbie": "Yoga",
      "edad": 24,
      "ciudad": "Sevilla",
      "profesion": "Profesora"
    },
    "content": "<h2>Ana (24)</h2><p><strong>Ciudad:</strong> Sevilla<br><strong>Profesión:</strong> Profesora<br><strong>Hobbie:</strong> Yoga</p>"
  },
  {
    "categories": {
      "nombre": "David",
      "hobbie": "Gaming",
      "edad": 22,
      "ciudad": "Valencia",
      "profesion": "Estudiante"
    },
    "content": "<h2>David (22)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Estudiante<br><strong>Hobbie:</strong> Gaming</p>"
  },
  {
    "categories": {
      "nombre": "Laura",
      "hobbie": "Lectura",
      "edad": 30,
      "ciudad": "Bilbao",
      "profesion": "Escritora"
    },
    "content": "<h2>Laura (30)</h2><p><strong>Ciudad:</strong> Bilbao<br><strong>Profesión:</strong> Escritora<br><strong>Hobbie:</strong> Lectura</p>"
  },
  {
    "categories": {
      "nombre": "Roberto",
      "hobbie": "Cocina",
      "edad": 42,
      "ciudad": "Madrid",
      "profesion": "Chef"
    },
    "content": "<h2>Roberto (42)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Chef<br><strong>Hobbie:</strong> Cocina</p>"
  },
  {
    "categories": {
      "nombre": "Elena",
      "hobbie": "Natación",
      "edad": 26,
      "ciudad": "Valencia",
      "profesion": "Médica"
    },
    "content": "<h2>Elena (26)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Médica<br><strong>Hobbie:</strong> Natación</p>"
  },
  {
    "categories": {
      "nombre": "Javier",
      "hobbie": "Fotografía",
      "edad": 31,
      "ciudad": "Barcelona",
      "profesion": "Arquitecto"
    },
    "content": "<h2>Javier (31)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Arquitecto<br><strong>Hobbie:</strong> Fotografía</p>"
  },
  {
    "categories": {
      "nombre": "Sofia",
      "hobbie": "Baile",
      "edad": 23,
      "ciudad": "Sevilla",
      "profesion": "Bailarina"
    },
    "content": "<h2>Sofia (23)</h2><p><strong>Ciudad:</strong> Sevilla<br><strong>Profesión:</strong> Bailarina<br><strong>Hobbie:</strong> Baile</p>"
  },
  {
    "categories": {
      "nombre": "Miguel",
      "hobbie": "Ajedrez",
      "edad": 29,
      "ciudad": "Málaga",
      "profesion": "Programador"
    },
    "content": "<h2>Miguel (29)</h2><p><strong>Ciudad:</strong> Málaga<br><strong>Profesión:</strong> Programador<br><strong>Hobbie:</strong> Ajedrez</p>"
  },
  {
    "categories": {
      "nombre": "Carmen",
      "hobbie": "Jardinería",
      "edad": 38,
      "ciudad": "Granada",
      "profesion": "Bióloga"
    },
    "content": "<h2>Carmen (38)</h2><p><strong>Ciudad:</strong> Granada<br><strong>Profesión:</strong> Bióloga<br><strong>Hobbie:</strong> Jardinería</p>"
  },
  {
    "categories": {
      "nombre": "Pablo",
      "hobbie": "Escalada",
      "edad": 27,
      "ciudad": "Zaragoza",
      "profesion": "Fisioterapeuta"
    },
    "content": "<h2>Pablo (27)</h2><p><strong>Ciudad:</strong> Zaragoza<br><strong>Profesión:</strong> Fisioterapeuta<br><strong>Hobbie:</strong> Escalada</p>"
  },
  {
    "categories": {
      "nombre": "Isabel",
      "hobbie": "Pintura",
      "edad": 33,
      "ciudad": "Barcelona",
      "profesion": "Artista"
    },
    "content": "<h2>Isabel (33)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Artista<br><strong>Hobbie:</strong> Pintura</p>"
  },
  {
    "categories": {
      "nombre": "Alejandro",
      "hobbie": "Música",
      "edad": 25,
      "ciudad": "Madrid",
      "profesion": "Músico"
    },
    "content": "<h2>Alejandro (25)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Músico<br><strong>Hobbie:</strong> Música</p>"
  },
  {
    "categories": {
      "nombre": "Lucía",
      "hobbie": "Running",
      "edad": 28,
      "ciudad": "Valencia",
      "profesion": "Entrenadora"
    },
    "content": "<h2>Lucía (28)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Entrenadora<br><strong>Hobbie:</strong> Running</p>"
  },
  {
    "categories": {
      "nombre": "Fernando",
      "hobbie": "Videojuegos",
      "edad": 21,
      "ciudad": "Murcia",
      "profesion": "Estudiante"
    },
    "content": "<h2>Fernando (21)</h2><p><strong>Ciudad:</strong> Murcia<br><strong>Profesión:</strong> Estudiante<br><strong>Hobbie:</strong> Videojuegos</p>"
  },
  {
    "categories": {
      "nombre": "Beatriz",
      "hobbie": "Teatro",
      "edad": 36,
      "ciudad": "Bilbao",
      "profesion": "Actriz"
    },
    "content": "<h2>Beatriz (36)</h2><p><strong>Ciudad:</strong> Bilbao<br><strong>Profesión:</strong> Actriz<br><strong>Hobbie:</strong> Teatro</p>"
  },
  {
    "categories": {
      "nombre": "Alberto",
      "hobbie": "Surf",
      "edad": 30,
      "ciudad": "San Sebastián",
      "profesion": "Socorrista"
    },
    "content": "<h2>Alberto (30)</h2><p><strong>Ciudad:</strong> San Sebastián<br><strong>Profesión:</strong> Socorrista<br><strong>Hobbie:</strong> Surf</p>"
  },
  {
    "categories": {
      "nombre": "Patricia",
      "hobbie": "Cine",
      "edad": 32,
      "ciudad": "Sevilla",
      "profesion": "Directora"
    },
    "content": "<h2>Patricia (32)</h2><p><strong>Ciudad:</strong> Sevilla<br><strong>Profesión:</strong> Directora<br><strong>Hobbie:</strong> Cine</p>"
  },
  {
    "categories": {
      "nombre": "Raúl",
      "hobbie": "Montañismo",
      "edad": 40,
      "ciudad": "Granada",
      "profesion": "Guía"
    },
    "content": "<h2>Raúl (40)</h2><p><strong>Ciudad:</strong> Granada<br><strong>Profesión:</strong> Guía<br><strong>Hobbie:</strong> Montañismo</p>"
  },
  {
    "categories": {
      "nombre": "Cristina",
      "hobbie": "Yoga",
      "edad": 29,
      "ciudad": "Madrid",
      "profesion": "Instructora"
    },
    "content": "<h2>Cristina (29)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Instructora<br><strong>Hobbie:</strong> Yoga</p>"
  },
  {
    "categories": {
      "nombre": "Diego",
      "hobbie": "Fotografía",
      "edad": 34,
      "ciudad": "Valencia",
      "profesion": "Fotógrafo"
    },
    "content": "<h2>Diego (34)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Fotógrafo<br><strong>Hobbie:</strong> Fotografía</p>"
  },
  {
    "categories": {
      "nombre": "Marta",
      "hobbie": "Repostería",
      "edad": 27,
      "ciudad": "Barcelona",
      "profesion": "Pastelera"
    },
    "content": "<h2>Marta (27)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Pastelera<br><strong>Hobbie:</strong> Repostería</p>"
  },
  {
    "categories": {
      "nombre": "Sergio",
      "hobbie": "Tenis",
      "edad": 26,
      "ciudad": "Málaga",
      "profesion": "Deportista"
    },
    "content": "<h2>Sergio (26)</h2><p><strong>Ciudad:</strong> Málaga<br><strong>Profesión:</strong> Deportista<br><strong>Hobbie:</strong> Tenis</p>"
  },
  {
    "categories": {
      "nombre": "Natalia",
      "hobbie": "Escritura",
      "edad": 31,
      "ciudad": "Bilbao",
      "profesion": "Periodista"
    },
    "content": "<h2>Natalia (31)</h2><p><strong>Ciudad:</strong> Bilbao<br><strong>Profesión:</strong> Periodista<br><strong>Hobbie:</strong> Escritura</p>"
  },
  {
    "categories": {
      "nombre": "Ángel",
      "hobbie": "Ciclismo",
      "edad": 39,
      "ciudad": "Zaragoza",
      "profesion": "Mecánico"
    },
    "content": "<h2>Ángel (39)</h2><p><strong>Ciudad:</strong> Zaragoza<br><strong>Profesión:</strong> Mecánico<br><strong>Hobbie:</strong> Ciclismo</p>"
  },
  {
    "categories": {
      "nombre": "Verónica",
      "hobbie": "Diseño",
      "edad": 28,
      "ciudad": "Granada",
      "profesion": "Diseñadora"
    },
    "content": "<h2>Verónica (28)</h2><p><strong>Ciudad:</strong> Granada<br><strong>Profesión:</strong> Diseñadora<br><strong>Hobbie:</strong> Diseño</p>"
  },
  {
    "categories": {
      "nombre": "Adrián",
      "hobbie": "Gaming",
      "edad": 23,
      "ciudad": "Valencia",
      "profesion": "Streamer"
    },
    "content": "<h2>Adrián (23)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Streamer<br><strong>Hobbie:</strong> Gaming</p>"
  },
  {
    "categories": {
      "nombre": "Silvia",
      "hobbie": "Viajar",
      "edad": 35,
      "ciudad": "Madrid",
      "profesion": "Azafata"
    },
    "content": "<h2>Silvia (35)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Azafata<br><strong>Hobbie:</strong> Viajar</p>"
  },
  {
    "categories": {
      "nombre": "Rubén",
      "hobbie": "Ajedrez",
      "edad": 37,
      "ciudad": "Barcelona",
      "profesion": "Profesor"
    },
    "content": "<h2>Rubén (37)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Profesor<br><strong>Hobbie:</strong> Ajedrez</p>"
  },
  {
    "categories": {
      "nombre": "Andrea",
      "hobbie": "Danza",
      "edad": 24,
      "ciudad": "Sevilla",
      "profesion": "Coreógrafa"
    },
    "content": "<h2>Andrea (24)</h2><p><strong>Ciudad:</strong> Sevilla<br><strong>Profesión:</strong> Coreógrafa<br><strong>Hobbie:</strong> Danza</p>"
  },
  {
    "categories": {
      "nombre": "Iván",
      "hobbie": "Pesca",
      "edad": 44,
      "ciudad": "Santander",
      "profesion": "Pescador"
    },
    "content": "<h2>Iván (44)</h2><p><strong>Ciudad:</strong> Santander<br><strong>Profesión:</strong> Pescador<br><strong>Hobbie:</strong> Pesca</p>"
  },
  {
    "categories": {
      "nombre": "Mónica",
      "hobbie": "Lectura",
      "edad": 33,
      "ciudad": "Madrid",
      "profesion": "Bibliotecaria"
    },
    "content": "<h2>Mónica (33)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Bibliotecaria<br><strong>Hobbie:</strong> Lectura</p>"
  },
  {
    "categories": {
      "nombre": "Óscar",
      "hobbie": "Boxeo",
      "edad": 28,
      "ciudad": "Málaga",
      "profesion": "Boxeador"
    },
    "content": "<h2>Óscar (28)</h2><p><strong>Ciudad:</strong> Málaga<br><strong>Profesión:</strong> Boxeador<br><strong>Hobbie:</strong> Boxeo</p>"
  },
  {
    "categories": {
      "nombre": "Rocío",
      "hobbie": "Costura",
      "edad": 41,
      "ciudad": "Granada",
      "profesion": "Modista"
    },
    "content": "<h2>Rocío (41)</h2><p><strong>Ciudad:</strong> Granada<br><strong>Profesión:</strong> Modista<br><strong>Hobbie:</strong> Costura</p>"
  },
  {
    "categories": {
      "nombre": "Guillermo",
      "hobbie": "Música",
      "edad": 26,
      "ciudad": "Valencia",
      "profesion": "DJ"
    },
    "content": "<h2>Guillermo (26)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> DJ<br><strong>Hobbie:</strong> Música</p>"
  },
  {
    "categories": {
      "nombre": "Alicia",
      "hobbie": "Equitación",
      "edad": 30,
      "ciudad": "Barcelona",
      "profesion": "Veterinaria"
    },
    "content": "<h2>Alicia (30)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Veterinaria<br><strong>Hobbie:</strong> Equitación</p>"
  },
  {
    "categories": {
      "nombre": "Héctor",
      "hobbie": "Astronomía",
      "edad": 32,
      "ciudad": "Madrid",
      "profesion": "Astrofísico"
    },
    "content": "<h2>Héctor (32)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Astrofísico<br><strong>Hobbie:</strong> Astronomía</p>"
  },
  {
    "categories": {
      "nombre": "Teresa",
      "hobbie": "Pilates",
      "edad": 29,
      "ciudad": "Sevilla",
      "profesion": "Instructora"
    },
    "content": "<h2>Teresa (29)</h2><p><strong>Ciudad:</strong> Sevilla<br><strong>Profesión:</strong> Instructora<br><strong>Hobbie:</strong> Pilates</p>"
  },
  {
    "categories": {
      "nombre": "Marcos",
      "hobbie": "Buceo",
      "edad": 34,
      "ciudad": "Alicante",
      "profesion": "Instructor"
    },
    "content": "<h2>Marcos (34)</h2><p><strong>Ciudad:</strong> Alicante<br><strong>Profesión:</strong> Instructor<br><strong>Hobbie:</strong> Buceo</p>"
  }
]

```
**ejemplo-libros.json**
```json
[
  {
    "categories": {
      "titulo": "Cien Años de Soledad",
      "idioma": "Español",
      "año": 1967,
      "autor": "Gabriel García Márquez",
      "genero": "Realismo Mágico",
      "editorial": "Sudamericana"
    },
    "content": "<h2>Cien Años de Soledad</h2><p><strong>Autor:</strong> Gabriel García Márquez<br><strong>Año:</strong> 1967<br><strong>Género:</strong> Realismo Mágico<br><strong>Idioma:</strong> Español</p>"
  },
  {
    "categories": {
      "titulo": "1984",
      "idioma": "Inglés",
      "año": 1949,
      "autor": "George Orwell",
      "genero": "Distopía",
      "editorial": "Secker & Warburg"
    },
    "content": "<h2>1984</h2><p><strong>Autor:</strong> George Orwell<br><strong>Año:</strong> 1949<br><strong>Género:</strong> Distopía<br><strong>Idioma:</strong> Inglés</p>"
  },
  {
    "categories": {
      "titulo": "El Principito",
      "idioma": "Francés",
      "año": 1943,
      "autor": "Antoine de Saint-Exupéry",
      "genero": "Fábula",
      "editorial": "Reynal & Hitchcock"
    },
    "content": "<h2>El Principito</h2><p><strong>Autor:</strong> Antoine de Saint-Exupéry<br><strong>Año:</strong> 1943<br><strong>Género:</strong> Fábula<br><strong>Idioma:</strong> Francés</p>"
  },
  {
    "categories": {
      "titulo": "Don Quijote de la Mancha",
      "idioma": "Español",
      "año": 1605,
      "autor": "Miguel de Cervantes",
      "genero": "Novela",
      "editorial": "Francisco de Robles"
    },
    "content": "<h2>Don Quijote de la Mancha</h2><p><strong>Autor:</strong> Miguel de Cervantes<br><strong>Año:</strong> 1605<br><strong>Género:</strong> Novela<br><strong>Idioma:</strong> Español</p>"
  },
  {
    "categories": {
      "titulo": "La Sombra del Viento",
      "idioma": "Español",
      "año": 2001,
      "autor": "Carlos Ruiz Zafón",
      "genero": "Misterio",
      "editorial": "Planeta"
    },
    "content": "<h2>La Sombra del Viento</h2><p><strong>Autor:</strong> Carlos Ruiz Zafón<br><strong>Año:</strong> 2001<br><strong>Género:</strong> Misterio<br><strong>Idioma:</strong> Español</p>"
  },
  {
    "categories": {
      "titulo": "Harry Potter y la Piedra Filosofal",
      "idioma": "Inglés",
      "año": 1997,
      "autor": "J.K. Rowling",
      "genero": "Fantasía",
      "editorial": "Bloomsbury"
    },
    "content": "<h2>Harry Potter y la Piedra Filosofal</h2><p><strong>Autor:</strong> J.K. Rowling<br><strong>Año:</strong> 1997<br><strong>Género:</strong> Fantasía<br><strong>Idioma:</strong> Inglés</p>"
  },
  {
    "categories": {
      "titulo": "Rayuela",
      "idioma": "Español",
      "año": 1963,
      "autor": "Julio Cortázar",
      "genero": "Experimental",
      "editorial": "Sudamericana"
    },
    "content": "<h2>Rayuela</h2><p><strong>Autor:</strong> Julio Cortázar<br><strong>Año:</strong> 1963<br><strong>Género:</strong> Experimental<br><strong>Idioma:</strong> Español</p>"
  },
  {
    "categories": {
      "titulo": "El Señor de los Anillos",
      "idioma": "Inglés",
      "año": 1954,
      "autor": "J.R.R. Tolkien",
      "genero": "Fantasía",
      "editorial": "Allen & Unwin"
    },
    "content": "<h2>El Señor de los Anillos</h2><p><strong>Autor:</strong> J.R.R. Tolkien<br><strong>Año:</strong> 1954<br><strong>Género:</strong> Fantasía<br><strong>Idioma:</strong> Inglés</p>"
  },
  {
    "categories": {
      "titulo": "Crimen y Castigo",
      "idioma": "Ruso",
      "año": 1866,
      "autor": "Fiódor Dostoyevski",
      "genero": "Novela Psicológica",
      "editorial": "The Russian Messenger"
    },
    "content": "<h2>Crimen y Castigo</h2><p><strong>Autor:</strong> Fiódor Dostoyevski<br><strong>Año:</strong> 1866<br><strong>Género:</strong> Novela Psicológica<br><strong>Idioma:</strong> Ruso</p>"
  },
  {
    "categories": {
      "titulo": "Los Miserables",
      "idioma": "Francés",
      "año": 1862,
      "autor": "Victor Hugo",
      "genero": "Drama",
      "editorial": "A. Lacroix"
    },
    "content": "<h2>Los Miserables</h2><p><strong>Autor:</strong> Victor Hugo<br><strong>Año:</strong> 1862<br><strong>Género:</strong> Drama<br><strong>Idioma:</strong> Francés</p>"
  },
  {
    "categories": {
      "titulo": "La Casa de los Espíritus",
      "idioma": "Español",
      "año": 1982,
      "autor": "Isabel Allende",
      "genero": "Realismo Mágico",
      "editorial": "Plaza & Janés"
    },
    "content": "<h2>La Casa de los Espíritus</h2><p><strong>Autor:</strong> Isabel Allende<br><strong>Año:</strong> 1982<br><strong>Género:</strong> Realismo Mágico<br><strong>Idioma:</strong> Español</p>"
  },
  {
    "categories": {
      "titulo": "El Alquimista",
      "idioma": "Portugués",
      "año": 1988,
      "autor": "Paulo Coelho",
      "genero": "Fábula",
      "editorial": "Rocco"
    },
    "content": "<h2>El Alquimista</h2><p><strong>Autor:</strong> Paulo Coelho<br><strong>Año:</strong> 1988<br><strong>Género:</strong> Fábula<br><strong>Idioma:</strong> Portugués</p>"
  },
  {
    "categories": {
      "titulo": "Brave New World",
      "idioma": "Inglés",
      "año": 1932,
      "autor": "Aldous Huxley",
      "genero": "Distopía",
      "editorial": "Chatto & Windus"
    },
    "content": "<h2>Brave New World</h2><p><strong>Autor:</strong> Aldous Huxley<br><strong>Año:</strong> 1932<br><strong>Género:</strong> Distopía<br><strong>Idioma:</strong> Inglés</p>"
  },
  {
    "categories": {
      "titulo": "El Nombre de la Rosa",
      "idioma": "Italiano",
      "año": 1980,
      "autor": "Umberto Eco",
      "genero": "Misterio",
      "editorial": "Bompiani"
    },
    "content": "<h2>El Nombre de la Rosa</h2><p><strong>Autor:</strong> Umberto Eco<br><strong>Año:</strong> 1980<br><strong>Género:</strong> Misterio<br><strong>Idioma:</strong> Italiano</p>"
  },
  {
    "categories": {
      "titulo": "Ficciones",
      "idioma": "Español",
      "año": 1944,
      "autor": "Jorge Luis Borges",
      "genero": "Cuentos",
      "editorial": "Sur"
    },
    "content": "<h2>Ficciones</h2><p><strong>Autor:</strong> Jorge Luis Borges<br><strong>Año:</strong> 1944<br><strong>Género:</strong> Cuentos<br><strong>Idioma:</strong> Español</p>"
  }
]

```
**ejemplo-peliculas.json**
```json
[
  {
    "categories": {
      "titulo": "El Padrino",
      "genero": "Drama",
      "año": 1972,
      "director": "Francis Ford Coppola",
      "pais": "Estados Unidos",
      "duracion": "175 min"
    },
    "content": "<h2>El Padrino (1972)</h2><p><strong>Director:</strong> Francis Ford Coppola<br><strong>Género:</strong> Drama<br><strong>País:</strong> Estados Unidos<br><strong>Duración:</strong> 175 min</p>"
  },
  {
    "categories": {
      "titulo": "Pulp Fiction",
      "genero": "Crime",
      "año": 1994,
      "director": "Quentin Tarantino",
      "pais": "Estados Unidos",
      "duracion": "154 min"
    },
    "content": "<h2>Pulp Fiction (1994)</h2><p><strong>Director:</strong> Quentin Tarantino<br><strong>Género:</strong> Crime<br><strong>País:</strong> Estados Unidos<br><strong>Duración:</strong> 154 min</p>"
  },
  {
    "categories": {
      "titulo": "El Laberinto del Fauno",
      "genero": "Fantasía",
      "año": 2006,
      "director": "Guillermo del Toro",
      "pais": "España",
      "duracion": "118 min"
    },
    "content": "<h2>El Laberinto del Fauno (2006)</h2><p><strong>Director:</strong> Guillermo del Toro<br><strong>Género:</strong> Fantasía<br><strong>País:</strong> España<br><strong>Duración:</strong> 118 min</p>"
  },
  {
    "categories": {
      "titulo": "Inception",
      "genero": "Ciencia Ficción",
      "año": 2010,
      "director": "Christopher Nolan",
      "pais": "Estados Unidos",
      "duracion": "148 min"
    },
    "content": "<h2>Inception (2010)</h2><p><strong>Director:</strong> Christopher Nolan<br><strong>Género:</strong> Ciencia Ficción<br><strong>País:</strong> Estados Unidos<br><strong>Duración:</strong> 148 min</p>"
  },
  {
    "categories": {
      "titulo": "Amélie",
      "genero": "Romance",
      "año": 2001,
      "director": "Jean-Pierre Jeunet",
      "pais": "Francia",
      "duracion": "122 min"
    },
    "content": "<h2>Amélie (2001)</h2><p><strong>Director:</strong> Jean-Pierre Jeunet<br><strong>Género:</strong> Romance<br><strong>País:</strong> Francia<br><strong>Duración:</strong> 122 min</p>"
  },
  {
    "categories": {
      "titulo": "Interstellar",
      "genero": "Ciencia Ficción",
      "año": 2014,
      "director": "Christopher Nolan",
      "pais": "Estados Unidos",
      "duracion": "169 min"
    },
    "content": "<h2>Interstellar (2014)</h2><p><strong>Director:</strong> Christopher Nolan<br><strong>Género:</strong> Ciencia Ficción<br><strong>País:</strong> Estados Unidos<br><strong>Duración:</strong> 169 min</p>"
  },
  {
    "categories": {
      "titulo": "Todo sobre mi madre",
      "genero": "Drama",
      "año": 1999,
      "director": "Pedro Almodóvar",
      "pais": "España",
      "duracion": "101 min"
    },
    "content": "<h2>Todo sobre mi madre (1999)</h2><p><strong>Director:</strong> Pedro Almodóvar<br><strong>Género:</strong> Drama<br><strong>País:</strong> España<br><strong>Duración:</strong> 101 min</p>"
  },
  {
    "categories": {
      "titulo": "Kill Bill Vol. 1",
      "genero": "Acción",
      "año": 2003,
      "director": "Quentin Tarantino",
      "pais": "Estados Unidos",
      "duracion": "111 min"
    },
    "content": "<h2>Kill Bill Vol. 1 (2003)</h2><p><strong>Director:</strong> Quentin Tarantino<br><strong>Género:</strong> Acción<br><strong>País:</strong> Estados Unidos<br><strong>Duración:</strong> 111 min</p>"
  },
  {
    "categories": {
      "titulo": "El Secreto de sus Ojos",
      "genero": "Thriller",
      "año": 2009,
      "director": "Juan José Campanella",
      "pais": "Argentina",
      "duracion": "129 min"
    },
    "content": "<h2>El Secreto de sus Ojos (2009)</h2><p><strong>Director:</strong> Juan José Campanella<br><strong>Género:</strong> Thriller<br><strong>País:</strong> Argentina<br><strong>Duración:</strong> 129 min</p>"
  },
  {
    "categories": {
      "titulo": "Volver",
      "genero": "Drama",
      "año": 2006,
      "director": "Pedro Almodóvar",
      "pais": "España",
      "duracion": "121 min"
    },
    "content": "<h2>Volver (2006)</h2><p><strong>Director:</strong> Pedro Almodóvar<br><strong>Género:</strong> Drama<br><strong>País:</strong> España<br><strong>Duración:</strong> 121 min</p>"
  },
  {
    "categories": {
      "titulo": "The Shawshank Redemption",
      "genero": "Drama",
      "año": 1994,
      "director": "Frank Darabont",
      "pais": "Estados Unidos",
      "duracion": "142 min"
    },
    "content": "<h2>The Shawshank Redemption (1994)</h2><p><strong>Director:</strong> Frank Darabont<br><strong>Género:</strong> Drama<br><strong>País:</strong> Estados Unidos<br><strong>Duración:</strong> 142 min</p>"
  },
  {
    "categories": {
      "titulo": "Cinema Paradiso",
      "genero": "Romance",
      "año": 1988,
      "director": "Giuseppe Tornatore",
      "pais": "Italia",
      "duracion": "155 min"
    },
    "content": "<h2>Cinema Paradiso (1988)</h2><p><strong>Director:</strong> Giuseppe Tornatore<br><strong>Género:</strong> Romance<br><strong>País:</strong> Italia<br><strong>Duración:</strong> 155 min</p>"
  },
  {
    "categories": {
      "titulo": "El Hijo de la Novia",
      "genero": "Comedia",
      "año": 2001,
      "director": "Juan José Campanella",
      "pais": "Argentina",
      "duracion": "123 min"
    },
    "content": "<h2>El Hijo de la Novia (2001)</h2><p><strong>Director:</strong> Juan José Campanella<br><strong>Género:</strong> Comedia<br><strong>País:</strong> Argentina<br><strong>Duración:</strong> 123 min</p>"
  },
  {
    "categories": {
      "titulo": "La Vida es Bella",
      "genero": "Drama",
      "año": 1997,
      "director": "Roberto Benigni",
      "pais": "Italia",
      "duracion": "116 min"
    },
    "content": "<h2>La Vida es Bella (1997)</h2><p><strong>Director:</strong> Roberto Benigni<br><strong>Género:</strong> Drama<br><strong>País:</strong> Italia<br><strong>Duración:</strong> 116 min</p>"
  },
  {
    "categories": {
      "titulo": "The Dark Knight",
      "genero": "Acción",
      "año": 2008,
      "director": "Christopher Nolan",
      "pais": "Estados Unidos",
      "duracion": "152 min"
    },
    "content": "<h2>The Dark Knight (2008)</h2><p><strong>Director:</strong> Christopher Nolan<br><strong>Género:</strong> Acción<br><strong>País:</strong> Estados Unidos<br><strong>Duración:</strong> 152 min</p>"
  },
  {
    "categories": {
      "titulo": "Hable con Ella",
      "genero": "Drama",
      "año": 2002,
      "director": "Pedro Almodóvar",
      "pais": "España",
      "duracion": "112 min"
    },
    "content": "<h2>Hable con Ella (2002)</h2><p><strong>Director:</strong> Pedro Almodóvar<br><strong>Género:</strong> Drama<br><strong>País:</strong> España<br><strong>Duración:</strong> 112 min</p>"
  },
  {
    "categories": {
      "titulo": "Coco",
      "genero": "Animación",
      "año": 2017,
      "director": "Lee Unkrich",
      "pais": "Estados Unidos",
      "duracion": "105 min"
    },
    "content": "<h2>Coco (2017)</h2><p><strong>Director:</strong> Lee Unkrich<br><strong>Género:</strong> Animación<br><strong>País:</strong> Estados Unidos<br><strong>Duración:</strong> 105 min</p>"
  },
  {
    "categories": {
      "titulo": "Oldboy",
      "genero": "Thriller",
      "año": 2003,
      "director": "Park Chan-wook",
      "pais": "Corea del Sur",
      "duracion": "120 min"
    },
    "content": "<h2>Oldboy (2003)</h2><p><strong>Director:</strong> Park Chan-wook<br><strong>Género:</strong> Thriller<br><strong>País:</strong> Corea del Sur<br><strong>Duración:</strong> 120 min</p>"
  },
  {
    "categories": {
      "titulo": "El Orfanato",
      "genero": "Terror",
      "año": 2007,
      "director": "Juan Antonio Bayona",
      "pais": "España",
      "duracion": "105 min"
    },
    "content": "<h2>El Orfanato (2007)</h2><p><strong>Director:</strong> Juan Antonio Bayona<br><strong>Género:</strong> Terror<br><strong>País:</strong> España<br><strong>Duración:</strong> 105 min</p>"
  },
  {
    "categories": {
      "titulo": "Spirited Away",
      "genero": "Animación",
      "año": 2001,
      "director": "Hayao Miyazaki",
      "pais": "Japón",
      "duracion": "125 min"
    },
    "content": "<h2>Spirited Away (2001)</h2><p><strong>Director:</strong> Hayao Miyazaki<br><strong>Género:</strong> Animación<br><strong>País:</strong> Japón<br><strong>Duración:</strong> 125 min</p>"
  }
]

```
**ejemplo-productos.json**
```json
[
  {
    "categories": {
      "nombre": "iPhone 15 Pro",
      "categoria": "Smartphone",
      "precio": 1199,
      "marca": "Apple",
      "origen": "Estados Unidos",
      "stock": "Disponible"
    },
    "content": "<h2>iPhone 15 Pro</h2><p><strong>Marca:</strong> Apple<br><strong>Categoría:</strong> Smartphone<br><strong>Precio:</strong> €1199<br><strong>Stock:</strong> Disponible</p>"
  },
  {
    "categories": {
      "nombre": "MacBook Pro M3",
      "categoria": "Laptop",
      "precio": 2499,
      "marca": "Apple",
      "origen": "Estados Unidos",
      "stock": "Disponible"
    },
    "content": "<h2>MacBook Pro M3</h2><p><strong>Marca:</strong> Apple<br><strong>Categoría:</strong> Laptop<br><strong>Precio:</strong> €2499<br><strong>Stock:</strong> Disponible</p>"
  },
  {
    "categories": {
      "nombre": "Samsung Galaxy S24",
      "categoria": "Smartphone",
      "precio": 899,
      "marca": "Samsung",
      "origen": "Corea del Sur",
      "stock": "Disponible"
    },
    "content": "<h2>Samsung Galaxy S24</h2><p><strong>Marca:</strong> Samsung<br><strong>Categoría:</strong> Smartphone<br><strong>Precio:</strong> €899<br><strong>Stock:</strong> Disponible</p>"
  },
  {
    "categories": {
      "nombre": "Sony WH-1000XM5",
      "categoria": "Auriculares",
      "precio": 399,
      "marca": "Sony",
      "origen": "Japón",
      "stock": "Disponible"
    },
    "content": "<h2>Sony WH-1000XM5</h2><p><strong>Marca:</strong> Sony<br><strong>Categoría:</strong> Auriculares<br><strong>Precio:</strong> €399<br><strong>Stock:</strong> Disponible</p>"
  },
  {
    "categories": {
      "nombre": "Dell XPS 15",
      "categoria": "Laptop",
      "precio": 1799,
      "marca": "Dell",
      "origen": "Estados Unidos",
      "stock": "Disponible"
    },
    "content": "<h2>Dell XPS 15</h2><p><strong>Marca:</strong> Dell<br><strong>Categoría:</strong> Laptop<br><strong>Precio:</strong> €1799<br><strong>Stock:</strong> Disponible</p>"
  },
  {
    "categories": {
      "nombre": "Logitech MX Master 3S",
      "categoria": "Mouse",
      "precio": 109,
      "marca": "Logitech",
      "origen": "Suiza",
      "stock": "Disponible"
    },
    "content": "<h2>Logitech MX Master 3S</h2><p><strong>Marca:</strong> Logitech<br><strong>Categoría:</strong> Mouse<br><strong>Precio:</strong> €109<br><strong>Stock:</strong> Disponible</p>"
  },
  {
    "categories": {
      "nombre": "iPad Pro 12.9",
      "categoria": "Tablet",
      "precio": 1299,
      "marca": "Apple",
      "origen": "Estados Unidos",
      "stock": "Agotado"
    },
    "content": "<h2>iPad Pro 12.9</h2><p><strong>Marca:</strong> Apple<br><strong>Categoría:</strong> Tablet<br><strong>Precio:</strong> €1299<br><strong>Stock:</strong> Agotado</p>"
  },
  {
    "categories": {
      "nombre": "Bose QuietComfort 45",
      "categoria": "Auriculares",
      "precio": 349,
      "marca": "Bose",
      "origen": "Estados Unidos",
      "stock": "Disponible"
    },
    "content": "<h2>Bose QuietComfort 45</h2><p><strong>Marca:</strong> Bose<br><strong>Categoría:</strong> Auriculares<br><strong>Precio:</strong> €349<br><strong>Stock:</strong> Disponible</p>"
  },
  {
    "categories": {
      "nombre": "Lenovo ThinkPad X1",
      "categoria": "Laptop",
      "precio": 1699,
      "marca": "Lenovo",
      "origen": "China",
      "stock": "Disponible"
    },
    "content": "<h2>Lenovo ThinkPad X1</h2><p><strong>Marca:</strong> Lenovo<br><strong>Categoría:</strong> Laptop<br><strong>Precio:</strong> €1699<br><strong>Stock:</strong> Disponible</p>"
  },
  {
    "categories": {
      "nombre": "Google Pixel 8 Pro",
      "categoria": "Smartphone",
      "precio": 999,
      "marca": "Google",
      "origen": "Estados Unidos",
      "stock": "Disponible"
    },
    "content": "<h2>Google Pixel 8 Pro</h2><p><strong>Marca:</strong> Google<br><strong>Categoría:</strong> Smartphone<br><strong>Precio:</strong> €999<br><strong>Stock:</strong> Disponible</p>"
  },
  {
    "categories": {
      "nombre": "Samsung Galaxy Tab S9",
      "categoria": "Tablet",
      "precio": 799,
      "marca": "Samsung",
      "origen": "Corea del Sur",
      "stock": "Disponible"
    },
    "content": "<h2>Samsung Galaxy Tab S9</h2><p><strong>Marca:</strong> Samsung<br><strong>Categoría:</strong> Tablet<br><strong>Precio:</strong> €799<br><strong>Stock:</strong> Disponible</p>"
  },
  {
    "categories": {
      "nombre": "Razer DeathAdder V3",
      "categoria": "Mouse",
      "precio": 89,
      "marca": "Razer",
      "origen": "Estados Unidos",
      "stock": "Disponible"
    },
    "content": "<h2>Razer DeathAdder V3</h2><p><strong>Marca:</strong> Razer<br><strong>Categoría:</strong> Mouse<br><strong>Precio:</strong> €89<br><strong>Stock:</strong> Disponible</p>"
  },
  {
    "categories": {
      "nombre": "JBL Flip 6",
      "categoria": "Altavoz",
      "precio": 129,
      "marca": "JBL",
      "origen": "Estados Unidos",
      "stock": "Disponible"
    },
    "content": "<h2>JBL Flip 6</h2><p><strong>Marca:</strong> JBL<br><strong>Categoría:</strong> Altavoz<br><strong>Precio:</strong> €129<br><strong>Stock:</strong> Disponible</p>"
  },
  {
    "categories": {
      "nombre": "Microsoft Surface Pro 9",
      "categoria": "Tablet",
      "precio": 1199,
      "marca": "Microsoft",
      "origen": "Estados Unidos",
      "stock": "Disponible"
    },
    "content": "<h2>Microsoft Surface Pro 9</h2><p><strong>Marca:</strong> Microsoft<br><strong>Categoría:</strong> Tablet<br><strong>Precio:</strong> €1199<br><strong>Stock:</strong> Disponible</p>"
  },
  {
    "categories": {
      "nombre": "Sony A7 IV",
      "categoria": "Cámara",
      "precio": 2499,
      "marca": "Sony",
      "origen": "Japón",
      "stock": "Agotado"
    },
    "content": "<h2>Sony A7 IV</h2><p><strong>Marca:</strong> Sony<br><strong>Categoría:</strong> Cámara<br><strong>Precio:</strong> €2499<br><strong>Stock:</strong> Agotado</p>"
  }
]

```
**index.html**
```html
<!doctype html>
<html lang="es">
  <head>
    <meta charset="utf-8">
    <title>Memento — Red 3D Interactiva</title>
    <link rel="icon" type="image/png" href="logo_azul.png">
    <link rel="apple-touch-icon" href="logo_azul.png">
    <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
    <style>
      body,html{
        margin:0;
        padding:0;
        font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
        overflow:hidden;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
      }

      /* ===== ANIMACIONES CSS ===== */
      @keyframes fadeIn {
        from {
          opacity: 0;
        }
        to {
          opacity: 1;
        }
      }

      @keyframes scaleIn {
        from {
          transform: scale(0.8);
          opacity: 0;
        }
        to {
          transform: scale(1);
          opacity: 1;
        }
      }

      @keyframes slideIn {
        from {
          transform: translateX(-20px);
          opacity: 0;
        }
        to {
          transform: translateX(0);
          opacity: 1;
        }
      }

      @keyframes slideInDown {
        from {
          transform: translateY(-30px);
          opacity: 0;
        }
        to {
          transform: translateY(0);
          opacity: 1;
        }
      }

      @keyframes spin {
        from {
          transform: rotate(0deg);
        }
        to {
          transform: rotate(360deg);
        }
      }

      @keyframes pulse {
        0%, 100% {
          transform: scale(1);
        }
        50% {
          transform: scale(1.05);
        }
      }

      /* ===== FROSTED GLASS - Panel de Control macOS Style ===== */
      #controles{
        position:fixed;
        top:20px;
        left:20px;
        width: 340px;
        padding:0;
        
        /* Efecto frosted glass macOS */
        background: rgba(255, 255, 255, 0.08);
        backdrop-filter: blur(40px) saturate(180%);
        -webkit-backdrop-filter: blur(40px) saturate(180%);
        
        border: 0.5px solid rgba(255, 255, 255, 0.18);
        border-radius: 16px;
        box-shadow: 
          0 8px 32px rgba(0, 0, 0, 0.12),
          0 2px 8px rgba(0, 0, 0, 0.08),
          inset 0 0 0 1px rgba(255, 255, 255, 0.05);
        
        font-size:13px;
        z-index:10;
        max-height:90vh;
        overflow:hidden;
        color:#ffffff;
        display: flex;
        flex-direction: column;
        
        /* Animación de entrada */
        animation: slideIn 0.5s cubic-bezier(0.16, 1, 0.3, 1);
      }

      /* Header del Dashboard - Frosted Style */
      .dashboard-header {
        padding: 24px;
        background: rgba(255, 255, 255, 0.03);
        border-bottom: 0.5px solid rgba(255, 255, 255, 0.12);
        border-radius: 16px 16px 0 0;
        position: relative;
      }

      .dashboard-title {
        font-size: 17px;
        font-weight: 600;
        color: rgba(255, 255, 255, 0.95);
        margin: 0;
        display: flex;
        align-items: center;
        gap: 10px;
        letter-spacing: -0.3px;
      }

      .dashboard-title span:first-child {
        font-size: 20px;
        opacity: 0.9;
      }

      .dashboard-subtitle {
        font-size: 12px;
        color: rgba(255, 255, 255, 0.45);
        margin: 4px 0 0 0;
        font-weight: 400;
        letter-spacing: 0;
      }

      /* Contenido con scroll */
      .dashboard-content {
        overflow-y: auto;
        overflow-x: hidden;
        max-height: calc(90vh - 88px);
        padding: 20px;
        flex: 1;
      }

      .dashboard-content::-webkit-scrollbar {
        width: 8px;
      }

      .dashboard-content::-webkit-scrollbar-track {
        background: transparent;
        margin: 4px;
      }

      .dashboard-content::-webkit-scrollbar-thumb {
        background: rgba(255, 255, 255, 0.2);
        border-radius: 10px;
        border: 2px solid transparent;
        background-clip: padding-box;
      }

      .dashboard-content::-webkit-scrollbar-thumb:hover {
        background: rgba(255, 255, 255, 0.3);
        background-clip: padding-box;
      }

      /* Secciones colapsables - Frosted Style */
      .control-section {
        margin-bottom: 8px;
        border-radius: 10px;
        background: rgba(255, 255, 255, 0.04);
        border: 0.5px solid rgba(255, 255, 255, 0.08);
        overflow: hidden;
        transition: all 0.25s cubic-bezier(0.16, 1, 0.3, 1);
      }

      .control-section:hover {
        background: rgba(255, 255, 255, 0.06);
        border-color: rgba(255, 255, 255, 0.15);
      }

      .section-header {
        padding: 12px 16px;
        cursor: pointer;
        display: flex;
        align-items: center;
        justify-content: space-between;
        user-select: none;
        transition: all 0.2s ease;
        position: relative;
      }

      .section-header:active {
        opacity: 0.7;
      }

      .section-title {
        font-size: 13px;
        font-weight: 500;
        color: rgba(255, 255, 255, 0.9);
        display: flex;
        align-items: center;
        gap: 8px;
        letter-spacing: -0.1px;
      }

      .section-title .prop-counter {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        min-width: 20px;
        height: 18px;
        padding: 0 6px;
        margin-left: 4px;
        background: rgba(255, 255, 255, 0.12);
        border-radius: 9px;
        font-size: 10px;
        font-weight: 600;
        color: rgba(255, 255, 255, 0.8);
        border: 0.5px solid rgba(255, 255, 255, 0.15);
        letter-spacing: 0;
      }

      .section-icon {
        font-size: 15px;
        opacity: 0.8;
        transition: transform 0.25s ease;
      }

      .section-header:hover .section-icon {
        transform: scale(1.08);
        opacity: 1;
      }

      .section-toggle {
        font-size: 11px;
        color: rgba(255, 255, 255, 0.4);
        transition: transform 0.25s cubic-bezier(0.16, 1, 0.3, 1), color 0.2s ease;
      }

      .section-header:hover .section-toggle {
        color: rgba(255, 255, 255, 0.6);
      }

      .control-section.collapsed .section-toggle {
        transform: rotate(-90deg);
      }

      .section-content {
        padding: 0 16px 12px 16px;
        display: block;
        animation: expandSection 0.25s ease-out;
        max-height: 2000px;
        transition: max-height 0.3s ease-out, padding 0.3s ease-out, opacity 0.25s ease-out;
        opacity: 1;
        overflow: visible;
      }

      .control-section.collapsed .section-content {
        max-height: 0;
        padding: 0 16px;
        opacity: 0;
        overflow: hidden;
      }

      @keyframes expandSection {
        from {
          opacity: 0;
          transform: translateY(-5px);
        }
        to {
          opacity: 1;
          transform: translateY(0);
        }
      }

      /* Controles de input - Frosted Style */
      .control-group {
        margin-bottom: 16px;
      }

      .control-group:last-child {
        margin-bottom: 0;
      }

      .control-label {
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-bottom: 10px;
        font-size: 12px;
        color: rgba(255, 255, 255, 0.65);
        font-weight: 500;
      }

      .control-value {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        min-width: 42px;
        height: 22px;
        padding: 0 10px;
        background: rgba(255, 255, 255, 0.12);
        border-radius: 6px;
        font-weight: 600;
        color: rgba(255, 255, 255, 0.95);
        font-size: 11px;
        border: 0.5px solid rgba(255, 255, 255, 0.15);
        letter-spacing: 0.3px;
        font-variant-numeric: tabular-nums;
      }

      #controles input[type=range]{
        width:100%;
        cursor: pointer;
        transition: all 0.3s ease;
      }

      #controles input[type=range]:hover {
        opacity: 1;
      }

      #controles input[type=range]:focus {
        outline: none;
      }

      /* Checkbox - Frosted Style */
      .checkbox-group {
        display: flex;
        align-items: center;
        padding: 10px 12px;
        background: rgba(255, 255, 255, 0.04);
        border-radius: 8px;
        margin-bottom: 8px;
        transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
        cursor: pointer;
        border: 0.5px solid rgba(255, 255, 255, 0.06);
      }

      .checkbox-group:hover {
        background: rgba(255, 255, 255, 0.08);
        border-color: rgba(255, 255, 255, 0.1);
      }

      .checkbox-group input[type=checkbox] {
        width: 16px;
        height: 16px;
        margin-right: 10px;
        cursor: pointer;
        accent-color: rgba(255, 255, 255, 0.9);
      }

      .checkbox-group label {
        flex: 1;
        cursor: pointer;
        font-size: 12px;
        color: rgba(255, 255, 255, 0.75);
        font-weight: 500;
        transition: color 0.2s ease;
      }

      .checkbox-group:hover label {
        color: rgba(255, 255, 255, 0.9);
      }

      /* Propiedades dinámicas - Frosted Style */
      #propiedades {
        width: 100%;
        display: flex;
        flex-direction: column;
        gap: 0;
      }

      #propiedades .bloque-prop{
        padding: 10px 0;
        margin-bottom: 10px;
        animation: slideInDown 0.4s ease-out;
        border-bottom: 0.5px solid rgba(255, 255, 255, 0.06);
      }

      #propiedades .bloque-prop:last-child {
        border-bottom: none;
        margin-bottom: 0;
      }

      #propiedades .titulo-prop{
        font-weight: 600;
        margin-bottom: 8px;
        color: rgba(255, 255, 255, 0.6);
        font-size: 10px;
        text-transform: uppercase;
        letter-spacing: 0.8px;
      }

      #propiedades label{
        display: inline-flex;
        align-items: center;
        padding: 6px 10px;
        margin: 0 6px 6px 0;
        background: rgba(255, 255, 255, 0.08);
        border: 0.5px solid rgba(255, 255, 255, 0.12);
        border-radius: 6px;
        font-size: 11px;
        transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
        cursor: pointer;
        white-space: nowrap;
      }

      #propiedades label:hover {
        background: rgba(255, 255, 255, 0.12);
        border-color: rgba(255, 255, 255, 0.2);
        transform: translateY(-1px);
      }

      #propiedades input[type=checkbox] {
        margin-right: 6px;
        accent-color: rgba(255, 255, 255, 0.9);
        flex-shrink: 0;
      }

      /* Ayuda de teclas - Frosted Style */
      #ayudaTeclas{
        font-size: 11px;
        padding: 12px;
        background: rgba(255, 255, 255, 0.04);
        border-radius: 8px;
        border: 0.5px solid rgba(255, 255, 255, 0.1);
        color: rgba(255, 255, 255, 0.6);
        line-height: 1.7;
        animation: fadeIn 1s ease-out;
      }

      #ayudaTeclas strong {
        color: rgba(255, 255, 255, 0.8);
        font-size: 11px;
        display: block;
        margin-bottom: 6px;
        font-weight: 600;
      }

      /* ===== FROSTED GLASS - Modal 2D ===== */
      #modalOverlay{
        position:fixed;
        top:0;
        left:0;
        width:100vw;
        height:100vh;
        background:rgba(0, 0, 0, 0.3);
        backdrop-filter: blur(20px);
        -webkit-backdrop-filter: blur(20px);
        display:none;
        align-items:center;
        justify-content:center;
        z-index:20;
        animation: fadeIn 0.25s ease-out;
      }

      #modalCaja{
        /* Efecto frosted glass */
        background: rgba(255, 255, 255, 0.08);
        backdrop-filter: blur(40px) saturate(180%);
        -webkit-backdrop-filter: blur(40px) saturate(180%);
        
        border: 0.5px solid rgba(255, 255, 255, 0.18);
        border-radius: 16px;
        box-shadow: 
          0 8px 32px rgba(0, 0, 0, 0.12),
          0 2px 8px rgba(0, 0, 0, 0.08),
          inset 0 0 0 1px rgba(255, 255, 255, 0.05);
        
        max-width:600px;
        max-height:80vh;
        width:90%;
        color:rgba(255, 255, 255, 0.95);
        display:flex;
        flex-direction:column;
        
        /* Animación de entrada */
        animation: scaleIn 0.3s cubic-bezier(0.16, 1, 0.3, 1);
      }

      #modalHeader{
        padding:16px 20px;
        border-bottom:0.5px solid rgba(255, 255, 255, 0.12);
        display:flex;
        justify-content:space-between;
        align-items:center;
        font-size:15px;
        background: rgba(255, 255, 255, 0.03);
        border-radius: 16px 16px 0 0;
      }

      #modalTitulo{
        font-weight:600;
        font-size: 16px;
        color: rgba(255, 255, 255, 0.95);
        letter-spacing: -0.2px;
      }

      #modalCerrar{
        cursor:pointer;
        padding:6px 12px;
        border-radius:6px;
        border:0.5px solid rgba(255, 255, 255, 0.15);
        background: rgba(255, 255, 255, 0.08);
        font-size:12px;
        color: rgba(255, 255, 255, 0.8);
        font-weight: 500;
        transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
      }

      #modalCerrar:hover{
        background: rgba(255, 255, 255, 0.12);
        border-color: rgba(255, 255, 255, 0.2);
        transform: scale(1.02);
      }

      #modalCerrar:active{
        transform: scale(0.98);
        opacity: 0.8;
      }

      #modalContenido{
        padding:20px;
        overflow:auto;
        font-size:14px;
        line-height:1.6;
        animation: fadeIn 0.4s ease-out 0.1s backwards;
      }

      #modalContenido::-webkit-scrollbar {
        width: 8px;
      }

      #modalContenido::-webkit-scrollbar-track {
        background: transparent;
        margin: 4px;
      }

      #modalContenido::-webkit-scrollbar-thumb {
        background: rgba(255, 255, 255, 0.2);
        border-radius: 10px;
        border: 2px solid transparent;
        background-clip: padding-box;
      }

      #modalContenido::-webkit-scrollbar-thumb:hover {
        background: rgba(255, 255, 255, 0.3);
        background-clip: padding-box;
      }

      #modalContenido h2 {
        color: rgba(255, 255, 255, 0.95);
        margin-top: 0;
        font-size: 16px;
        font-weight: 600;
        letter-spacing: -0.2px;
      }

      #modalContenido strong {
        color: rgba(255, 255, 255, 0.9);
        font-weight: 600;
      }

      /* ===== Loader - Frosted Style ===== */
      .loader {
        position: fixed;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 50px;
        height: 50px;
        border: 3px solid rgba(255, 255, 255, 0.15);
        border-top: 3px solid rgba(255, 255, 255, 0.9);
        border-radius: 50%;
        animation: spin 0.8s linear infinite;
        z-index: 100;
        display: none;
      }

      .loader.active {
        display: block;
      }

      /* ===== Efectos adicionales ===== */
      .fade-in {
        animation: fadeIn 0.5s ease-out;
      }

      .scale-in {
        animation: scaleIn 0.5s ease-out;
      }

      .slide-in {
        animation: slideIn 0.5s ease-out;
      }

      /* Sliders - Frosted macOS Style */
      input[type="range"] {
        -webkit-appearance: none;
        appearance: none;
        height: 4px;
        background: rgba(255, 255, 255, 0.15);
        border-radius: 10px;
        outline: none;
        position: relative;
      }

      input[type="range"]::-webkit-slider-thumb {
        -webkit-appearance: none;
        appearance: none;
        width: 16px;
        height: 16px;
        background: rgba(255, 255, 255, 0.95);
        border-radius: 50%;
        cursor: pointer;
        transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
        box-shadow: 0 1px 3px rgba(0, 0, 0, 0.15), 0 1px 2px rgba(0, 0, 0, 0.1);
        border: 0.5px solid rgba(255, 255, 255, 0.2);
      }

      input[type="range"]::-webkit-slider-thumb:hover {
        transform: scale(1.15);
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2), 0 1px 3px rgba(0, 0, 0, 0.15);
      }

      input[type="range"]::-webkit-slider-thumb:active {
        transform: scale(1.05);
      }

      input[type="range"]::-moz-range-thumb {
        width: 16px;
        height: 16px;
        background: rgba(255, 255, 255, 0.95);
        border-radius: 50%;
        cursor: pointer;
        border: 0.5px solid rgba(255, 255, 255, 0.2);
        transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
        box-shadow: 0 1px 3px rgba(0, 0, 0, 0.15), 0 1px 2px rgba(0, 0, 0, 0.1);
      }

      input[type="range"]::-moz-range-thumb:hover {
        transform: scale(1.15);
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2), 0 1px 3px rgba(0, 0, 0, 0.15);
      }

      input[type="range"]::-moz-range-thumb:active {
        transform: scale(1.05);
      }

      /* ===== BOTONES - Frosted macOS Style ===== */
      .btn-action {
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 6px;
        width: 100%;
        padding: 10px 16px;
        margin: 6px 0;
        border: 0.5px solid rgba(255, 255, 255, 0.15);
        border-radius: 8px;
        background: rgba(255, 255, 255, 0.08);
        color: rgba(255, 255, 255, 0.9);
        font-size: 12px;
        font-weight: 500;
        cursor: pointer;
        transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
        text-align: center;
        backdrop-filter: blur(10px);
      }

      .btn-action:hover {
        background: rgba(255, 255, 255, 0.12);
        border-color: rgba(255, 255, 255, 0.2);
        transform: translateY(-1px);
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
      }

      .btn-action:active {
        transform: translateY(0);
        opacity: 0.8;
      }

      .btn-export {
        background: rgba(52, 211, 153, 0.12);
        border-color: rgba(52, 211, 153, 0.2);
        color: rgba(167, 243, 208, 0.95);
      }

      .btn-export:hover {
        background: rgba(52, 211, 153, 0.18);
        border-color: rgba(52, 211, 153, 0.3);
      }

      .btn-import {
        background: rgba(139, 92, 246, 0.12);
        border-color: rgba(139, 92, 246, 0.2);
        color: rgba(196, 181, 253, 0.95);
      }

      .btn-import:hover {
        background: rgba(139, 92, 246, 0.18);
        border-color: rgba(139, 92, 246, 0.3);
      }

      /* Divider - Frosted Style */
      .divider {
        height: 0.5px;
        background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.15), transparent);
        margin: 16px 0;
      }

      /* ===== NOTIFICACIONES TOAST - Frosted Style ===== */
      .toast-container {
        position: fixed;
        top: 24px;
        right: 24px;
        z-index: 9999;
        display: flex;
        flex-direction: column;
        gap: 10px;
        pointer-events: none;
      }

      .toast {
        min-width: 280px;
        max-width: 400px;
        padding: 14px 18px;
        border-radius: 12px;
        background: rgba(255, 255, 255, 0.08);
        backdrop-filter: blur(40px) saturate(180%);
        -webkit-backdrop-filter: blur(40px) saturate(180%);
        border: 0.5px solid rgba(255, 255, 255, 0.18);
        box-shadow: 
          0 8px 32px rgba(0, 0, 0, 0.12),
          0 2px 8px rgba(0, 0, 0, 0.08),
          inset 0 0 0 1px rgba(255, 255, 255, 0.05);
        color: rgba(255, 255, 255, 0.95);
        font-size: 13px;
        font-weight: 500;
        display: flex;
        align-items: center;
        gap: 12px;
        pointer-events: auto;
        animation: toastSlideIn 0.3s cubic-bezier(0.16, 1, 0.3, 1);
      }

      .toast.closing {
        animation: toastSlideOut 0.25s ease-out forwards;
      }

      .toast-icon {
        font-size: 18px;
        line-height: 1;
        flex-shrink: 0;
        opacity: 0.9;
      }

      .toast-message {
        flex: 1;
        line-height: 1.4;
      }

      .toast-success {
        border-left: 2px solid rgba(52, 211, 153, 0.6);
      }

      .toast-error {
        border-left: 2px solid rgba(248, 113, 113, 0.6);
      }

      .toast-info {
        border-left: 2px solid rgba(96, 165, 250, 0.6);
      }

      .toast-warning {
        border-left: 2px solid rgba(251, 191, 36, 0.6);
      }

      @keyframes toastSlideIn {
        from {
          transform: translateX(100px);
          opacity: 0;
        }
        to {
          transform: translateX(0);
          opacity: 1;
        }
      }

      @keyframes toastSlideOut {
        from {
          transform: translateX(0);
          opacity: 1;
        }
        to {
          transform: translateX(100px);
          opacity: 0;
        }
      }

      /* ===== PANEL DE ESTADÍSTICAS LIVE - Frosted Style ===== */
      #estadisticas {
        position: fixed;
        top: 20px;
        right: 20px;
        width: 280px;
        padding: 0;
        
        /* Efecto frosted glass */
        background: rgba(255, 255, 255, 0.08);
        backdrop-filter: blur(40px) saturate(180%);
        -webkit-backdrop-filter: blur(40px) saturate(180%);
        
        border: 0.5px solid rgba(255, 255, 255, 0.18);
        border-radius: 16px;
        box-shadow: 
          0 8px 32px rgba(0, 0, 0, 0.12),
          0 2px 8px rgba(0, 0, 0, 0.08),
          inset 0 0 0 1px rgba(255, 255, 255, 0.05);
        
        font-size: 13px;
        z-index: 9;
        color: #ffffff;
        
        /* Animación de entrada */
        animation: slideInDown 0.5s cubic-bezier(0.16, 1, 0.3, 1);
      }

      .stats-header {
        padding: 16px 20px;
        background: rgba(255, 255, 255, 0.03);
        border-bottom: 0.5px solid rgba(255, 255, 255, 0.12);
        border-radius: 16px 16px 0 0;
        cursor: pointer;
        display: flex;
        align-items: center;
        justify-content: space-between;
        user-select: none;
        transition: all 0.2s ease;
        position: relative;
      }

      .stats-header:active {
        opacity: 0.7;
      }

      .stats-header:hover {
        background: rgba(255, 255, 255, 0.05);
      }

      .stats-title {
        font-size: 14px;
        font-weight: 600;
        color: rgba(255, 255, 255, 0.95);
        margin: 0;
        display: flex;
        align-items: center;
        gap: 8px;
        letter-spacing: -0.2px;
      }

      .stats-toggle {
        font-size: 11px;
        color: rgba(255, 255, 255, 0.4);
        transition: transform 0.25s cubic-bezier(0.16, 1, 0.3, 1), color 0.2s ease;
      }

      .stats-header:hover .stats-toggle {
        color: rgba(255, 255, 255, 0.6);
      }

      #estadisticas.collapsed .stats-toggle {
        transform: rotate(-90deg);
      }

      .stats-content {
        padding: 16px;
        display: flex;
        flex-direction: column;
        gap: 12px;
        max-height: 2000px;
        transition: max-height 0.3s ease-out, padding 0.3s ease-out, opacity 0.25s ease-out;
        opacity: 1;
        overflow: hidden;
      }

      #estadisticas.collapsed .stats-content {
        max-height: 0;
        padding: 0 16px;
        opacity: 0;
      }

      #estadisticas.collapsed {
        border-bottom: none;
      }

      .stat-item {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 12px 14px;
        background: rgba(255, 255, 255, 0.04);
        border: 0.5px solid rgba(255, 255, 255, 0.08);
        border-radius: 10px;
        transition: all 0.25s cubic-bezier(0.16, 1, 0.3, 1);
        animation: fadeIn 0.5s ease-out;
      }

      .stat-item:hover {
        background: rgba(255, 255, 255, 0.08);
        border-color: rgba(255, 255, 255, 0.15);
        transform: translateY(-2px);
      }

      .stat-label {
        display: flex;
        align-items: center;
        gap: 10px;
        font-size: 12px;
        font-weight: 500;
        color: rgba(255, 255, 255, 0.7);
      }

      .stat-icon {
        font-size: 16px;
        width: 24px;
        height: 24px;
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 6px;
        flex-shrink: 0;
      }

      .stat-icon.nodes {
        background: rgba(96, 165, 250, 0.2);
        color: rgba(96, 165, 250, 1);
      }

      .stat-icon.connections {
        background: rgba(52, 211, 153, 0.2);
        color: rgba(52, 211, 153, 1);
      }

      .stat-icon.properties {
        background: rgba(168, 85, 247, 0.2);
        color: rgba(168, 85, 247, 1);
      }

      .stat-icon.fps {
        background: rgba(251, 191, 36, 0.2);
        color: rgba(251, 191, 36, 1);
      }

      .stat-value {
        font-size: 18px;
        font-weight: 700;
        color: rgba(255, 255, 255, 0.95);
        letter-spacing: -0.5px;
        min-width: 50px;
        text-align: right;
        transition: all 0.3s ease;
      }

      .stat-value.updating {
        animation: pulse 0.3s ease;
      }

      .stat-unit {
        font-size: 11px;
        font-weight: 500;
        color: rgba(255, 255, 255, 0.5);
        margin-left: 4px;
      }
    </style>
  </head>
  <body>
    <!-- Loader -->
    <div class="loader active" id="loader"></div>

    <!-- Contenedor de Notificaciones Toast -->
    <div class="toast-container" id="toastContainer"></div>

    <!-- Panel de Estadísticas Live -->
    <div id="estadisticas">
      <div class="stats-header" onclick="toggleEstadisticas()">
        <h2 class="stats-title">
          <span>📊</span>
          <span>Estadísticas Live</span>
        </h2>
        <span class="stats-toggle">▼</span>
      </div>
      <div class="stats-content">
        <div class="stat-item">
          <div class="stat-label">
            <div class="stat-icon nodes">●</div>
            <span>Nodos</span>
          </div>
          <div class="stat-value" id="statNodos">0</div>
        </div>
        <div class="stat-item">
          <div class="stat-label">
            <div class="stat-icon connections">═</div>
            <span>Conexiones</span>
          </div>
          <div class="stat-value" id="statConexiones">0</div>
        </div>
        <div class="stat-item">
          <div class="stat-label">
            <div class="stat-icon properties">◆</div>
            <span>Propiedades</span>
          </div>
          <div class="stat-value" id="statPropiedades">0</div>
        </div>
        <div class="stat-item">
          <div class="stat-label">
            <div class="stat-icon fps">○</div>
            <span>FPS</span>
          </div>
          <div class="stat-value" id="statFPS">
            <span id="statFPSValor">60</span>
            <span class="stat-unit">fps</span>
          </div>
        </div>
      </div>
    </div>

    <!-- Input file oculto para importar -->
    <input type="file" id="fileInput" accept=".json" style="display: none;">

    <!-- Panel de control -->
    <div id="controles">
      <!-- Header del Dashboard -->
      <div class="dashboard-header">
        <h1 class="dashboard-title">
          <span>◆</span>
          <span>Memento</span>
        </h1>
        <p class="dashboard-subtitle">Control Panel</p>
      </div>

      <!-- Contenido con scroll -->
      <div class="dashboard-content">
        
        <!-- Sección: Visualización -->
        <div class="control-section">
          <div class="section-header" onclick="toggleSection(this)">
            <div class="section-title">
              <span class="section-icon">○</span>
              <span>Visualización</span>
            </div>
            <span class="section-toggle">▼</span>
          </div>
          <div class="section-content">
            <div class="control-group">
              <div class="control-label">
                <span>Grosor mínimo</span>
                <span id="grosorMinValor" class="control-value">1</span>
              </div>
              <input id="grosorMin" type="range" min="1" max="10" value="1">
            </div>

            <div class="control-group">
              <div class="control-label">
                <span>Grosor máximo</span>
                <span id="grosorMaxValor" class="control-value">6</span>
              </div>
              <input id="grosorMax" type="range" min="1" max="20" value="6">
            </div>

            <div class="control-group">
              <div class="control-label">
                <span>Transparencia cápsulas</span>
                <span id="opacidadCapsulasValor" class="control-value">25%</span>
              </div>
              <input id="opacidadCapsulas" type="range" min="5" max="100" value="25">
            </div>
          </div>
        </div>

        <!-- Sección: Conexiones -->
        <div class="control-section">
          <div class="section-header" onclick="toggleSection(this)">
            <div class="section-title">
              <span class="section-icon">◇</span>
              <span>Conexiones</span>
            </div>
            <span class="section-toggle">▼</span>
          </div>
          <div class="section-content">
            <div class="control-group">
              <div class="control-label">
                <span>Máx. conexiones</span>
                <span id="maxConexionesValor" class="control-value">2</span>
              </div>
              <input id="maxConexiones" type="range" min="1" max="6" value="2">
            </div>

            <div class="checkbox-group">
              <input id="chkMostrarLineas" type="checkbox" checked>
              <label for="chkMostrarLineas">Mostrar conexiones</label>
            </div>

            <div class="checkbox-group">
              <input id="chkMostrarCapsulas" type="checkbox" checked>
              <label for="chkMostrarCapsulas">Mostrar cápsulas</label>
            </div>
          </div>
        </div>

        <!-- Sección: Propiedades -->
        <div class="control-section">
          <div class="section-header" onclick="toggleSection(this)">
            <div class="section-title">
              <span class="section-icon">◐</span>
              <span>Propiedades</span>
            </div>
            <span class="section-toggle">▼</span>
          </div>
          <div class="section-content">
            <div id="propiedades"></div>
          </div>
        </div>

        <!-- Sección: Navegación -->
        <div class="control-section">
          <div class="section-header" onclick="toggleSection(this)">
            <div class="section-title">
              <span class="section-icon">◎</span>
              <span>Controles</span>
            </div>
            <span class="section-toggle">▼</span>
          </div>
          <div class="section-content">
            <div id="ayudaTeclas">
              <strong>Teclado</strong>
              W / A / S / D — Movimiento<br>
              Q / E — Subir / Bajar<br>
              <strong>Ratón</strong>
              Arrastrar — Mirar alrededor<br>
              Clic — Ver detalles
            </div>
          </div>
        </div>

        <div class="divider"></div>

        <!-- Sección: Gestión de Datos -->
        <div class="control-section">
          <div class="section-header" onclick="toggleSection(this)">
            <div class="section-title">
              <span class="section-icon">◈</span>
              <span>Datos</span>
            </div>
            <span class="section-toggle">▼</span>
          </div>
          <div class="section-content">
            <button class="btn-action btn-export" id="btnExportJSON">
              <span>↓</span>
              <span>Exportar JSON</span>
            </button>
            <button class="btn-action btn-export" id="btnExportCSV">
              <span>↓</span>
              <span>Exportar CSV</span>
            </button>
            <button class="btn-action btn-import" id="btnImportJSON">
              <span>↑</span>
              <span>Importar JSON</span>
            </button>
          </div>
        </div>

      </div>
    </div>

    <!-- Modal 2D -->
    <div id="modalOverlay">
      <div id="modalCaja">
        <div id="modalHeader">
          <div id="modalTitulo">Detalle de nodo</div>
          <button id="modalCerrar">✕ Cerrar</button>
        </div>
        <div id="modalContenido"></div>
      </div>
    </div>

    <!-- Escena A-Frame -->
    <a-scene background="color: #000000">
      <!-- Cielo con gradiente -->
      <a-sky material="shader: gradiente; topColor: #88c8ff; bottomColor: #02041a"></a-sky>

      <!-- Cámara con look-controls + cursor/mouse + raycaster -->
      <a-entity id="rig"
                camera
                look-controls
                position="0 3 15"
                cursor="rayOrigin: mouse; fuse: false"
                raycaster="objects: .clickable; far: 100">
      </a-entity>

      <!-- 💡 SISTEMA DE ILUMINACIÓN DINÁMICA (5 luces animadas) -->
      
      <!-- 🌟 Luz Ambiental Base - Azul suave del cielo con pulsación lenta -->
      <a-entity light="type: ambient; color: #88c8ff; intensity: 0.4"
                animation="property: light.intensity; from: 0.3; to: 0.5; dur: 4000; dir: alternate; loop: true; easing: easeInOutSine">
      </a-entity>
      
      <!-- ✅ Luz Success (Verde) - Energizante, arriba-derecha, pulsación rápida -->
      <a-entity light="type: point; color: #34D399; intensity: 0.6; distance: 30; decay: 2" 
                position="5 6 3"
                animation="property: light.intensity; from: 0.4; to: 0.8; dur: 2500; dir: alternate; loop: true; easing: easeInOutQuad">
      </a-entity>
      
      <!-- ⚠️ Luz Warning (Amarilla) - Cálida, izquierda-frontal, pulsación media -->
      <a-entity light="type: point; color: #FBBF24; intensity: 0.5; distance: 25; decay: 2" 
                position="-6 5 5"
                animation="property: light.intensity; from: 0.3; to: 0.6; dur: 3200; dir: alternate; loop: true; easing: easeInOutSine">
      </a-entity>
      
      <!-- ℹ️ Luz Info (Azul) - Principal focal, centro-atrás, respiración lenta -->
      <a-entity light="type: point; color: #60A5FA; intensity: 0.7; distance: 35; decay: 2" 
                position="0 7 -8"
                animation="property: light.intensity; from: 0.5; to: 0.9; dur: 3800; dir: alternate; loop: true; easing: easeInOutCubic">
      </a-entity>
      
      <!-- 🔥 Luz Accent (Rojo) - Contraste sutil, derecha-atrás, latido rápido -->
      <a-entity light="type: point; color: #F87171; intensity: 0.3; distance: 20; decay: 2" 
                position="7 4 -5"
                animation="property: light.intensity; from: 0.15; to: 0.45; dur: 2000; dir: alternate; loop: true; easing: easeInOutQuad">
      </a-entity>

      <!-- Contenedor de conexiones -->
      <a-entity id="conexiones"></a-entity>

      <!-- Contenedor de nodos -->
      <a-entity id="nodos"></a-entity>
    </a-scene>

    <script>
      const THREE = AFRAME.THREE;

      // ===== FUNCIÓN PARA SECCIONES COLAPSABLES =====
      function toggleSection(headerElement) {
        const section = headerElement.parentElement;
        section.classList.toggle('collapsed');
      }

      // ===== FUNCIÓN PARA PANEL DE ESTADÍSTICAS COLAPSABLE =====
      function toggleEstadisticas() {
        const panel = document.getElementById('estadisticas');
        panel.classList.toggle('collapsed');
      }

      // ===== SISTEMA DE NOTIFICACIONES TOAST =====
      const toastContainer = document.getElementById('toastContainer');

      function mostrarToast(mensaje, tipo = 'info', duracion = 3000) {
        const toast = document.createElement('div');
        toast.className = `toast toast-${tipo}`;
        
        const iconos = {
          success: '✅',
          error: '❌',
          info: 'ℹ️',
          warning: '⚠️'
        };
        
        toast.innerHTML = `
          <span class="toast-icon">${iconos[tipo] || 'ℹ️'}</span>
          <span class="toast-message">${mensaje}</span>
        `;
        
        toastContainer.appendChild(toast);
        
        // Auto-eliminar después de la duración
        setTimeout(() => {
          toast.classList.add('closing');
          setTimeout(() => {
            if (toast.parentElement) {
              toast.parentElement.removeChild(toast);
            }
          }, 300);
        }, duracion);
        
        // Click para cerrar manualmente
        toast.addEventListener('click', () => {
          toast.classList.add('closing');
          setTimeout(() => {
            if (toast.parentElement) {
              toast.parentElement.removeChild(toast);
            }
          }, 300);
        });
      }

      // ===== FUNCIONES DE EXPORTACIÓN =====
      function descargarArchivo(contenido, nombreArchivo, tipoMIME) {
        const blob = new Blob([contenido], { type: tipoMIME });
        const url = URL.createObjectURL(blob);
        const link = document.createElement('a');
        link.href = url;
        link.download = nombreArchivo;
        document.body.appendChild(link);
        link.click();
        document.body.removeChild(link);
        URL.revokeObjectURL(url);
      }

      function exportarJSON() {
        try {
          if (!datosOriginales || datosOriginales.length === 0) {
            mostrarToast('No hay datos para exportar', 'warning');
            return;
          }
          
          const jsonString = JSON.stringify(datosOriginales, null, 2);
          const fecha = new Date().toISOString().split('T')[0];
          const nombreArchivo = `memento-export-${fecha}.json`;
          
          descargarArchivo(jsonString, nombreArchivo, 'application/json');
          mostrarToast(`✨ Exportados ${datosOriginales.length} registros a JSON`, 'success');
        } catch (error) {
          console.error('Error al exportar JSON:', error);
          mostrarToast('Error al exportar JSON: ' + error.message, 'error');
        }
      }

      function exportarCSV() {
        try {
          if (!datosOriginales || datosOriginales.length === 0) {
            mostrarToast('No hay datos para exportar', 'warning');
            return;
          }
          
          // Obtener todas las propiedades únicas
          const propiedades = new Set();
          datosOriginales.forEach(item => {
            if (item.categories) {
              Object.keys(item.categories).forEach(key => propiedades.add(key));
            }
          });
          
          const columnas = Array.from(propiedades).sort();
          
          // Crear encabezados CSV
          let csv = columnas.map(col => `"${col}"`).join(',') + '\n';
          
          // Agregar cada fila de datos
          datosOriginales.forEach(item => {
            const fila = columnas.map(col => {
              const valor = item.categories && item.categories[col] ? item.categories[col] : '';
              // Escapar comillas dobles y envolver en comillas
              return `"${String(valor).replace(/"/g, '""')}"`;
            });
            csv += fila.join(',') + '\n';
          });
          
          const fecha = new Date().toISOString().split('T')[0];
          const nombreArchivo = `memento-export-${fecha}.csv`;
          
          // UTF-8 BOM para compatibilidad con Excel
          const bom = '\uFEFF';
          descargarArchivo(bom + csv, nombreArchivo, 'text/csv;charset=utf-8;');
          mostrarToast(`📊 Exportados ${datosOriginales.length} registros a CSV`, 'success');
        } catch (error) {
          console.error('Error al exportar CSV:', error);
          mostrarToast('Error al exportar CSV: ' + error.message, 'error');
        }
      }

      // ===== FUNCIONES DE IMPORTACIÓN =====
      function validarDatosJSON(datos) {
        if (!Array.isArray(datos)) {
          throw new Error('El archivo debe contener un array de objetos');
        }
        
        if (datos.length === 0) {
          throw new Error('El archivo está vacío');
        }
        
        // Validar estructura de cada elemento
        let validos = 0;
        datos.forEach((item, index) => {
          if (typeof item !== 'object' || item === null) {
            throw new Error(`Elemento ${index + 1} no es un objeto válido`);
          }
          
          // Verificar que tenga al menos categories
          if (!item.categories || typeof item.categories !== 'object') {
            console.warn(`Elemento ${index + 1} no tiene categories válido, se ignorará`);
          } else {
            validos++;
          }
        });
        
        if (validos === 0) {
          throw new Error('Ningún elemento tiene una estructura válida (necesita "categories")');
        }
        
        return validos;
      }

      function importarJSON() {
        const fileInput = document.getElementById('fileInput');
        
        fileInput.onchange = (e) => {
          const file = e.target.files[0];
          if (!file) return;
          
          mostrarToast('⏳ Cargando archivo...', 'info', 2000);
          
          const reader = new FileReader();
          reader.onload = (event) => {
            try {
              const contenido = event.target.result;
              const datos = JSON.parse(contenido);
              
              // Validar datos
              const validos = validarDatosJSON(datos);
              
              // Filtrar solo elementos válidos
              const datosValidos = datos.filter(item => 
                item.categories && typeof item.categories === 'object'
              );
              
              // Recargar la escena con los nuevos datos
              recargarEscenaConDatos(datosValidos);
              
              mostrarToast(
                `✅ Importados ${validos} registros correctamente`, 
                'success', 
                4000
              );
              
            } catch (error) {
              console.error('Error al importar:', error);
              mostrarToast(
                `❌ Error al importar: ${error.message}`, 
                'error', 
                5000
              );
            }
          };
          
          reader.onerror = () => {
            mostrarToast('Error al leer el archivo', 'error');
          };
          
          reader.readAsText(file);
          
          // Limpiar input para permitir seleccionar el mismo archivo de nuevo
          fileInput.value = '';
        };
        
        fileInput.click();
      }

      function recargarEscenaConDatos(nuevosItems) {
        // Limpiar escena actual
        while (nodosContEl.firstChild) {
          nodosContEl.removeChild(nodosContEl.firstChild);
        }
        while (conexionesEl.firstChild) {
          conexionesEl.removeChild(conexionesEl.firstChild);
        }
        
        // Reiniciar estado
        particulas = [];
        conexionesActivadas = false;
        etiquetasSucias = false;
        contadorFrames = 0;
        ultimoTiempo = null;
        
        // Actualizar datos originales
        datosOriginales = nuevosItems;
        
        // Detectar claves de propiedades
        const setClaves = new Set();
        nuevosItems.forEach(item => {
          const cats = item.categories || {};
          Object.keys(cats).forEach(k => setClaves.add(k));
        });
        const claves = Array.from(setClaves);
        
        // Recrear controles y nodos
        crearControlesPropiedades(claves);
        crearNodos3D(nuevosItems);
        
        // Reactivar animaciones y conexiones
        const tiempoAnimacionTotal = (nuevosItems.length * 30) + 800 + 200;
        setTimeout(() => {
          conexionesActivadas = true;
          actualizarConexiones();
          actualizarEstadisticas();
        }, tiempoAnimacionTotal);
        
        // Actualizar estadísticas iniciales
        actualizarEstadisticas();
        
        mostrarToast('🔄 Escena recargada con nuevos datos', 'info', 3000);
      }

      // ---------- Shader gradiente para el cielo ----------
      AFRAME.registerShader('gradiente', {
        schema: {
          topColor:    {type: 'color', default: '#88c8ff'},
          bottomColor: {type: 'color', default: '#02041a'}
        },
        init: function (data) {
          this.uniforms = {
            topColor:    { value: new THREE.Color(data.topColor) },
            bottomColor: { value: new THREE.Color(data.bottomColor) }
          };
          this.material = new THREE.ShaderMaterial({
            uniforms: this.uniforms,
            vertexShader: `
              varying vec3 vWorldPosition;
              void main() {
                vec4 worldPosition = modelMatrix * vec4( position, 1.0 );
                vWorldPosition = worldPosition.xyz;
                gl_Position = projectionMatrix * viewMatrix * worldPosition;
              }
            `,
            fragmentShader: `
              uniform vec3 topColor;
              uniform vec3 bottomColor;
              varying vec3 vWorldPosition;
              void main() {
                float h = normalize(vWorldPosition).y;
                float t = clamp(h * 0.5 + 0.5, 0.0, 1.0);
                vec3 color = mix(bottomColor, topColor, t);
                gl_FragColor = vec4(color, 1.0);
              }
            `,
            side: THREE.BackSide,
            depthWrite: false
          });
        },
        update: function (data) {
          this.uniforms.topColor.value.set(data.topColor);
          this.uniforms.bottomColor.value.set(data.bottomColor);
        }
      });

      // ---------- Componente billboard ----------
      AFRAME.registerComponent('billboard', {
        schema: { target: { type: 'selector' } },
        init: function () {
          this.camEl = this.data.target || document.querySelector('#rig');
        },
        tick: function () {
          if (!this.camEl) return;
          const obj = this.el.object3D;
          const camPos = new THREE.Vector3();
          this.camEl.object3D.getWorldPosition(camPos);
          obj.lookAt(camPos);
        }
      });

      // ---------- Componente cápsula transparente ----------
      AFRAME.registerComponent('transparente-capsula', {
        schema: {
          opacity: { type: 'number', default: 0.25 }
        },
        init: function () {
          const el = this.el;
          const self = this;

          this.applySettings = function () {
            el.object3D.traverse(obj => {
              if (obj.isMesh && obj.material) {
                const m = obj.material;
                m.transparent = true;
                m.opacity = self.data.opacity;
                m.depthWrite = false;
                m.depthTest  = true;
                m.side = THREE.DoubleSide;
                m.needsUpdate = true;
              }
            });
          };

          if (el.object3D) {
            this.applySettings();
          }
          el.addEventListener('object3dset', () => this.applySettings());
        },
        update: function (oldData) {
          if (oldData && oldData.opacity === this.data.opacity) return;
          if (this.applySettings) this.applySettings();
        }
      });

      // ---------- Componente de animación de entrada para nodos ----------
      AFRAME.registerComponent('nodo-animado', {
        schema: {
          delay: { type: 'number', default: 0 }
        },
        init: function () {
          const el = this.el;
          const delay = this.data.delay;
          
          // Iniciar invisible y pequeño
          el.object3D.scale.set(0.01, 0.01, 0.01);
          el.object3D.visible = false;
          
          // Animar después del delay
          setTimeout(() => {
            el.object3D.visible = true;
            const startScale = 0.01;
            const endScale = 1;
            const duration = 800; // ms
            const startTime = Date.now();
            
            const animate = () => {
              const elapsed = Date.now() - startTime;
              const progress = Math.min(elapsed / duration, 1);
              
              // Easing cubic out
              const eased = 1 - Math.pow(1 - progress, 3);
              const currentScale = startScale + (endScale - startScale) * eased;
              
              el.object3D.scale.set(currentScale, currentScale, currentScale);
              
              if (progress < 1) {
                requestAnimationFrame(animate);
              }
            };
            
            animate();
          }, delay);
        }
      });

      // ---------- Utilidades ----------
      function distancia3D(x1,y1,z1,x2,y2,z2){
        const dx = x2 - x1;
        const dy = y2 - y1;
        const dz = z2 - z1;
        return Math.sqrt(dx*dx + dy*dy + dz*dz);
      }

      function hashCadena(str) {
        let hash = 0;
        for (let i = 0; i < str.length; i++) {
          hash = (hash * 31 + str.charCodeAt(i)) | 0;
        }
        return Math.abs(hash);
      }

      const nodosContEl   = document.getElementById("nodos");
      const conexionesEl  = document.getElementById("conexiones");
      const rigEl         = document.getElementById("rig");
      const loaderEl      = document.getElementById("loader");

      // Modal
      const modalOverlay   = document.getElementById("modalOverlay");
      const modalContenido = document.getElementById("modalContenido");
      const modalTitulo    = document.getElementById("modalTitulo");
      const modalCerrar    = document.getElementById("modalCerrar");

      function mostrarModal(titulo, html){
        modalTitulo.textContent = titulo || "Detalle de nodo";
        modalContenido.innerHTML = html || "<p>(Sin contenido)</p>";
        modalOverlay.style.display = "flex";
      }
      function ocultarModal(){
        modalOverlay.style.display = "none";
      }
      modalCerrar.addEventListener("click", ocultarModal);
      modalOverlay.addEventListener("click", (e)=>{
        if (e.target === modalOverlay) ocultarModal();
      });

      // ---------- Parámetros espaciales y físicos ----------
      const LIM_X = 20;
      const LIM_Y = 10;
      const LIM_Z = 20;

      const DISTANCIA_OBJETIVO           = 6;
      const DISTANCIA_MINIMA             = 1.8;
      const DISTANCIA_REPULSION_DISTINTO = 14;

      const K_ATRACCION_FUERTE   = 0.0015;
      const K_ATRACCION_MEDIA    = 0.0009;
      const K_REPULSION_DISTINTO = 0.001;
      const K_REPULSION_CORTA    = 0.06;

      const FRICCION   = 0.93;
      const MAX_FUERZA = 0.05;

      const RADIO_CONEXION         = 12;
      const ACTUALIZAR_LINEAS_CADA = 10;

      // ---------- Controles UI ----------
      let grosorMin = 1;
      let grosorMax = 6;
      let mostrarLineas = true;

      let clavesPropiedades = [];
      let usarEnRelacion    = {};
      let mostrarEnEtiqueta = {};

      let mostrarCapsulas   = true;
      let opacidadCapsulas  = 0.25;

      let maxConexionesPorNodo = 2;
      
      // Variable global para almacenar datos originales
      let datosOriginales = [];

      const sliderMin = document.getElementById("grosorMin");
      const sliderMax = document.getElementById("grosorMax");
      const spanMin   = document.getElementById("grosorMinValor");
      const spanMax   = document.getElementById("grosorMaxValor");
      const chkMostrarLineas = document.getElementById("chkMostrarLineas");
      const divPropiedades   = document.getElementById("propiedades");

      const chkMostrarCapsulas       = document.getElementById("chkMostrarCapsulas");
      const sliderOpacidadCapsulas   = document.getElementById("opacidadCapsulas");
      const spanOpacidadCapsulas     = document.getElementById("opacidadCapsulasValor");

      const sliderMaxConexiones      = document.getElementById("maxConexiones");
      const spanMaxConexiones        = document.getElementById("maxConexionesValor");

      sliderMin.addEventListener("input", () => {
        grosorMin = parseFloat(sliderMin.value);
        spanMin.textContent = sliderMin.value;
        if (grosorMin > grosorMax) {
          grosorMax = grosorMin;
          sliderMax.value = grosorMax;
          spanMax.textContent = grosorMax;
        }
      });

      sliderMax.addEventListener("input", () => {
        grosorMax = parseFloat(sliderMax.value);
        spanMax.textContent = sliderMax.value;
        if (grosorMax < grosorMin) {
          grosorMin = grosorMax;
          sliderMin.value = grosorMin;
          spanMin.textContent = grosorMin;
        }
      });

      sliderMaxConexiones.addEventListener("input", () => {
        maxConexionesPorNodo = parseInt(sliderMaxConexiones.value, 10);
        spanMaxConexiones.textContent = sliderMaxConexiones.value;
        if (conexionesActivadas) {
          actualizarConexiones(); // Actualizar inmediatamente cuando se cambia el valor
        }
      });

      chkMostrarLineas.addEventListener("change", () => {
        mostrarLineas = chkMostrarLineas.checked;
        if (conexionesActivadas) {
          actualizarConexiones(); // Actualizar inmediatamente cuando se cambia el checkbox
        }
      });

      chkMostrarCapsulas.addEventListener("change", () => {
        mostrarCapsulas = chkMostrarCapsulas.checked;
        particulas.forEach(p => {
          if (p.capsulaEl) {
            p.capsulaEl.object3D.visible = mostrarCapsulas;
          }
        });
      });

      sliderOpacidadCapsulas.addEventListener("input", () => {
        const v = parseInt(sliderOpacidadCapsulas.value, 10);
        opacidadCapsulas = v / 100;
        spanOpacidadCapsulas.textContent = v + "%";
        particulas.forEach(p => {
          if (p.capsulaEl) {
            p.capsulaEl.setAttribute("transparente-capsula", "opacity:" + opacidadCapsulas);
          }
        });
      });

      let etiquetasSucias = false;

      function crearControlesPropiedades(claves){
        divPropiedades.innerHTML = "";
        clavesPropiedades = claves.slice();

        // Actualizar contador en el título de la sección
        const seccionPropiedades = document.querySelector('.control-section:has(#propiedades)');
        if (seccionPropiedades) {
          const tituloSpan = seccionPropiedades.querySelector('.section-title span:last-child');
          if (tituloSpan) {
            let contadorBadge = tituloSpan.querySelector('.prop-counter');
            if (claves.length > 0) {
              if (!contadorBadge) {
                contadorBadge = document.createElement('span');
                contadorBadge.className = 'prop-counter';
                tituloSpan.appendChild(contadorBadge);
              }
              contadorBadge.textContent = claves.length;
            } else if (contadorBadge) {
              contadorBadge.remove();
            }
          }
        }

        if (claves.length === 0) {
          // Mostrar mensaje cuando no hay propiedades
          const mensaje = document.createElement('div');
          mensaje.style.cssText = `
            padding: 30px 20px;
            text-align: center;
            color: rgba(255, 255, 255, 0.4);
            font-size: 12px;
            font-style: italic;
          `;
          mensaje.textContent = 'No hay propiedades detectadas';
          divPropiedades.appendChild(mensaje);
          etiquetasSucias = true;
          return;
        }

        clavesPropiedades.forEach((prop, index) => {
          if (!(prop in usarEnRelacion))    usarEnRelacion[prop] = true;
          if (!(prop in mostrarEnEtiqueta)) mostrarEnEtiqueta[prop] = true;

          const bloque = document.createElement("div");
          bloque.className = "bloque-prop";
          bloque.style.animationDelay = (index * 0.05) + 's';

          const titulo = document.createElement("div");
          titulo.className = "titulo-prop";
          titulo.textContent = prop;
          bloque.appendChild(titulo);

          const lblUsar = document.createElement("label");
          const chkUsar = document.createElement("input");
          chkUsar.type = "checkbox";
          chkUsar.checked = usarEnRelacion[prop];
          chkUsar.addEventListener("change", () => {
            usarEnRelacion[prop] = chkUsar.checked;
            particulas.forEach(p => {
              p.fija = false;
              p.estableFrames = 0;
            });
            actualizarEstadisticas();
          });
          lblUsar.appendChild(chkUsar);
          lblUsar.appendChild(document.createTextNode(" Usar en relación"));
          bloque.appendChild(lblUsar);

          const lblMostrar = document.createElement("label");
          const chkMostrar = document.createElement("input");
          chkMostrar.type = "checkbox";
          chkMostrar.checked = mostrarEnEtiqueta[prop];
          chkMostrar.addEventListener("change", () => {
            mostrarEnEtiqueta[prop] = chkMostrar.checked;
            etiquetasSucias = true;
          });
          lblMostrar.appendChild(chkMostrar);
          lblMostrar.appendChild(document.createTextNode(" Mostrar en etiqueta"));
          bloque.appendChild(lblMostrar);

          divPropiedades.appendChild(bloque);
        });

        etiquetasSucias = true;
      }

      // ---------- Datos y nodos ----------
      let particulas = [];
      let numeroParticulas = 0;

      function construirEtiqueta(datosCategorias){
        const lineas = [];
        for (const prop of clavesPropiedades){
          if (!mostrarEnEtiqueta[prop]) continue;
          const val = (datosCategorias[prop] !== undefined && datosCategorias[prop] !== null)
                      ? String(datosCategorias[prop])
                      : "";
          lineas.push(val);
        }
        return lineas.join("\n");
      }

      // Cápsula transparente horizontal:
      // ahora se marcan como .clickable las entidades con geometría
      function crearCapsulaTransparenteHorizontal(){
        const capsula = document.createElement("a-entity");
        capsula.setAttribute("rotation", "0 0 90");
        capsula.setAttribute("transparente-capsula", "opacity:0.25");

        const cilindro = document.createElement("a-cylinder");
        cilindro.setAttribute("radius", 0.7);
        cilindro.setAttribute("height", 1.8);
        cilindro.setAttribute("position", "0 0 0");
        cilindro.setAttribute("class", "clickable");
        capsula.appendChild(cilindro);

        const esferaArriba = document.createElement("a-sphere");
        esferaArriba.setAttribute("radius", 0.7);
        esferaArriba.setAttribute("position", "0 0.9 0");
        esferaArriba.setAttribute("class", "clickable");
        capsula.appendChild(esferaArriba);

        const esferaAbajo = document.createElement("a-sphere");
        esferaAbajo.setAttribute("radius", 0.7);
        esferaAbajo.setAttribute("position", "0 -0.9 0");
        esferaAbajo.setAttribute("class", "clickable");
        capsula.appendChild(esferaAbajo);

        return capsula;
      }

      function crearNodos3D(items){
        particulas = [];
        numeroParticulas = items.length;

        for (let i = 0; i < items.length; i++){
          const item = items[i];
          const categorias    = item.categories || {};
          const contenidoHtml = item.content    || "";

          const x = (Math.random() - 0.5) * LIM_X * 2;
          const y = Math.random() * LIM_Y + 1;
          const z = (Math.random() - 0.5) * LIM_Z * 2;

          const nodo = document.createElement("a-entity");
          nodo.setAttribute("position", `${x} ${y} ${z}`);
          nodo.setAttribute("billboard", "target: #rig");
          
          // Añadir animación de entrada con delay escalonado
          nodo.setAttribute("nodo-animado", `delay: ${i * 30}`);

          const capsula = crearCapsulaTransparenteHorizontal();
          nodo.appendChild(capsula);

          const texto = document.createElement("a-entity");
          texto.setAttribute("text", {
            value: construirEtiqueta(categorias),
            align: "center",
            color: "#ffffff",
            width: 3,
            wrapCount: 20,
            baseline: "center"
          });
          texto.setAttribute("position", "0 0 -1.0");
          texto.setAttribute("class", "clickable"); // también clickable el texto
          nodo.appendChild(texto);

          nodosContEl.appendChild(nodo);

          const pObj = {
            x:x, y:y, z:z,
            vx:(Math.random()-0.5)*0.1,
            vy:(Math.random()-0.5)*0.1,
            vz:(Math.random()-0.5)*0.1,
            ax:0, ay:0, az:0,
            fija:false,
            estableFrames:0,
            datos:categorias,
            contenido:contenidoHtml,
            nodeEl:nodo,
            textEl:texto,
            capsulaEl:capsula
          };

          capsula.object3D.visible = mostrarCapsulas;
          capsula.setAttribute("transparente-capsula", "opacity:" + opacidadCapsulas);

          // click en el nodo completo (evento burbujea desde los hijos .clickable)
          nodo.addEventListener("click", () => {
            zoomACentroDeParticula(pObj);
            const tituloModal = categorias.nombre || "Detalle de nodo";
            mostrarModal(tituloModal, contenidoHtml);
          });

          particulas.push(pObj);
        }
      }

      // ---------- Física 3D ----------
      function pasoFisica(dt){
        const n = numeroParticulas;
        if (n === 0) return;

        for (let i = 0; i < n; i++){
          particulas[i].ax = 0;
          particulas[i].ay = 0;
          particulas[i].az = 0;
        }

        for (let i = 0; i < n; i++){
          const p = particulas[i];
          if (p.fija) continue;

          let fx = 0, fy = 0, fz = 0;

          for (let j = 0; j < n; j++){
            if (i === j) continue;
            const q = particulas[j];

            const d = distancia3D(p.x,p.y,p.z, q.x,q.y,q.z);
            if (d === 0) continue;

            const dx = q.x - p.x;
            const dy = q.y - p.y;
            const dz = q.z - p.z;

            const ux = dx / d;
            const uy = dy / d;
            const uz = dz / d;

            if (d < DISTANCIA_MINIMA){
              const intensidad = (DISTANCIA_MINIMA - d) * K_REPULSION_CORTA;
              fx -= ux * intensidad;
              fy -= uy * intensidad;
              fz -= uz * intensidad;
              continue;
            }

            const propsCoinciden = [];
            let hayPropsRelacionActivas = false;
            for (const prop of clavesPropiedades){
              if (!usarEnRelacion[prop]) continue;
              hayPropsRelacionActivas = true;
              if (p.datos[prop] === q.datos[prop]){
                propsCoinciden.push(prop);
              }
            }

            if (propsCoinciden.length > 1){
              const delta = d - DISTANCIA_OBJETIVO;
              fx += ux * delta * K_ATRACCION_FUERTE;
              fy += uy * delta * K_ATRACCION_FUERTE;
              fz += uz * delta * K_ATRACCION_FUERTE;
            } else if (propsCoinciden.length === 1){
              const delta = d - DISTANCIA_OBJETIVO;
              fx += ux * delta * K_ATRACCION_MEDIA;
              fy += uy * delta * K_ATRACCION_MEDIA;
              fz += uz * delta * K_ATRACCION_MEDIA;
            } else {
              if (d < DISTANCIA_REPULSION_DISTINTO){
                const intensidad = (DISTANCIA_REPULSION_DISTINTO - d) * K_REPULSION_DISTINTO;
                fx -= ux * intensidad;
                fy -= uy * intensidad;
                fz -= uz * intensidad;
              }
            }
          }

          const modF = Math.sqrt(fx*fx + fy*fy + fz*fz);
          if (modF > MAX_FUERZA){
            fx = fx / modF * MAX_FUERZA;
            fy = fy / modF * MAX_FUERZA;
            fz = fz / modF * MAX_FUERZA;
          }

          p.ax = fx;
          p.ay = fy;
          p.az = fz;
        }

        for (let i = 0; i < n; i++){
          const p = particulas[i];
          if (!p.fija){
            p.vx += p.ax;
            p.vy += p.ay;
            p.vz += p.az;

            p.vx *= FRICCION;
            p.vy *= FRICCION;
            p.vz *= FRICCION;

            p.x += p.vx;
            p.y += p.vy;
            p.z += p.vz;

            const REBOTE = -0.5;
            if (p.x > LIM_X){ p.x = LIM_X; p.vx *= REBOTE; }
            if (p.x < -LIM_X){ p.x = -LIM_X; p.vx *= REBOTE; }
            if (p.z > LIM_Z){ p.z = LIM_Z; p.vz *= REBOTE; }
            if (p.z < -LIM_Z){ p.z = -LIM_Z; p.vz *= REBOTE; }
            if (p.y > LIM_Y){ p.y = LIM_Y; p.vy *= REBOTE; }
            if (p.y < 0.5){ p.y = 0.5; p.vy *= REBOTE; }

            const vel  = Math.sqrt(p.vx*p.vx + p.vy*p.vy + p.vz*p.vz);
            const fuer = Math.sqrt(p.ax*p.ax + p.ay*p.ay + p.az*p.az);
            if (vel < 0.02 && fuer < 0.002){
              p.estableFrames++;
              if (p.estableFrames > 60){
                p.fija = true;
                p.vx = p.vy = p.vz = 0;
              }
            } else {
              p.estableFrames = 0;
            }
          }

          p.nodeEl.setAttribute("position", `${p.x} ${p.y} ${p.z}`);

          if (etiquetasSucias){
            p.textEl.setAttribute("text", "value", construirEtiqueta(p.datos));
          }
        }

        if (etiquetasSucias){
          etiquetasSucias = false;
        }
      }

      // ---------- Conexiones 3D ----------
      let conexionesActivadas = false;
      
      function actualizarConexiones(){
        if (!conexionesActivadas) return; // No dibujar hasta que los nodos se hayan animado
        
        conexionesEl.innerHTML = "";
        if (!MostrarLineasGlobal()) return;

        const n = numeroParticulas;
        for (let i = 0; i < n; i++){
          const a = particulas[i];
          const candidatos = [];

          for (let j = i+1; j < n; j++){
            const b = particulas[j];
            const d = distancia3D(a.x,a.y,a.z, b.x,b.y,b.z);
            if (d > RADIO_CONEXION) continue;

            const propsCoinciden = [];
            let hayPropsRelacionActivas = false;
            for (const prop of clavesPropiedades){
              if (!usarEnRelacion[prop]) continue;
              hayPropsRelacionActivas = true;
              if (a.datos[prop] === b.datos[prop]){
                propsCoinciden.push(prop);
              }
            }

            let clave = "ninguna";
            if (propsCoinciden.length === 1){
              clave = propsCoinciden[0];
            } else if (propsCoinciden.length > 1){
              clave = propsCoinciden.slice().sort().join("+");
            } else if (!hayPropsRelacionActivas){
              clave = "sin-prop-relacion";
            }

            const h = hashCadena(clave) % 360;
            const color = `hsl(${h}, 70%, 50%)`;

            candidatos.push({j, d, color});
          }

          candidatos.sort((a,b) => a.d - b.d);
          const limite = Math.min(maxConexionesPorNodo, candidatos.length);
          for (let k = 0; k < limite; k++){
            const c = candidatos[k];
            const b = particulas[c.j];

            const lineaEl = document.createElement("a-entity");
            lineaEl.setAttribute("line", {
              start: `${a.x} ${a.y} ${a.z}`,
              end:   `${b.x} ${b.y} ${b.z}`,
              color: c.color
            });
            conexionesEl.appendChild(lineaEl);
          }
        }
      }

      function MostrarLineasGlobal() {
        return mostrarLineas;
      }

      // ---------- Fly controls ----------
      const flyEstado = {
        adelante:0,
        atras:0,
        izquierda:0,
        derecha:0,
        arriba:0,
        abajo:0
      };
      const VELOCIDAD_FLY = 6;

      window.addEventListener("keydown", (e) => {
        switch(e.key.toLowerCase()){
          case "w": flyEstado.adelante = 1; break;
          case "s": flyEstado.atras    = 1; break;
          case "a": flyEstado.izquierda= 1; break;
          case "d": flyEstado.derecha  = 1; break;
          case "q": flyEstado.arriba   = 1; break;
          case "e": flyEstado.abajo    = 1; break;
        }
      });

      window.addEventListener("keyup", (e) => {
        switch(e.key.toLowerCase()){
          case "w": flyEstado.adelante = 0; break;
          case "s": flyEstado.atras    = 0; break;
          case "a": flyEstado.izquierda= 0; break;
          case "d": flyEstado.derecha  = 0; break;
          case "q": flyEstado.arriba   = 0; break;
          case "e": flyEstado.abajo    = 0; break;
        }
      });

      function actualizarFly(dt){
        const obj = rigEl.object3D;
        const dir = new THREE.Vector3();
        obj.getWorldDirection(dir);
        dir.normalize();

        const up = new THREE.Vector3(0,1,0);
        const right = new THREE.Vector3().crossVectors(dir, up).normalize().negate();

        let move = new THREE.Vector3(0,0,0);

        if (flyEstado.adelante) move.add(dir.clone().multiplyScalar(-1));
        if (flyEstado.atras)    move.add(dir);
        if (flyEstado.derecha)   move.add(right);
        if (flyEstado.izquierda) move.add(right.clone().multiplyScalar(-1));
        if (flyEstado.arriba) move.add(up);
        if (flyEstado.abajo)  move.add(up.clone().multiplyScalar(-1));

        if (move.lengthSq() > 0){
          move.normalize().multiplyScalar(VELOCIDAD_FLY * dt);
          obj.position.add(move);
        }
      }

      // ---------- Zoom suave ----------
      let zoomAnim = null;

      function zoomACentroDeParticula(p){
        const rigPos = rigEl.object3D.position.clone();
        const destino = new THREE.Vector3(p.x, p.y + 0.5, p.z + 5);
        zoomAnim = { from: rigPos, to: destino, t: 0, dur: 1.0 };
      }

      function actualizarZoom(dt){
        if (!zoomAnim) return;
        zoomAnim.t += dt / zoomAnim.dur;
        let t = zoomAnim.t;
        if (t >= 1) t = 1;
        const ease = t < 0.5 ? 2*t*t : -1 + (4 - 2*t)*t;
        const pos = new THREE.Vector3().lerpVectors(zoomAnim.from, zoomAnim.to, ease);
        rigEl.object3D.position.copy(pos);
        if (zoomAnim.t >= 1) zoomAnim = null;
      }

      // ---------- Bucle principal ----------
      let ultimoTiempo = null;
      let contadorFrames = 0;

      // ---------- Estadísticas Live ----------
      let fps = 60;
      let frameCount = 0;
      let lastFpsUpdate = 0;
      let ultimasConexiones = 0;
      
      function actualizarEstadisticas() {
        // Actualizar nodos
        const statNodos = document.getElementById('statNodos');
        if (statNodos && statNodos.textContent !== String(numeroParticulas)) {
          statNodos.textContent = numeroParticulas;
          statNodos.classList.add('updating');
          setTimeout(() => statNodos.classList.remove('updating'), 300);
        }
        
        // Actualizar conexiones
        const numConexiones = conexionesEl ? conexionesEl.children.length : 0;
        const statConexiones = document.getElementById('statConexiones');
        if (statConexiones && numConexiones !== ultimasConexiones) {
          statConexiones.textContent = numConexiones;
          statConexiones.classList.add('updating');
          setTimeout(() => statConexiones.classList.remove('updating'), 300);
          ultimasConexiones = numConexiones;
        }
        
        // Actualizar propiedades habilitadas
        const propsHabilitadas = Object.values(usarEnRelacion).filter(v => v).length;
        const statPropiedades = document.getElementById('statPropiedades');
        if (statPropiedades && statPropiedades.textContent !== String(propsHabilitadas)) {
          statPropiedades.textContent = propsHabilitadas;
          statPropiedades.classList.add('updating');
          setTimeout(() => statPropiedades.classList.remove('updating'), 300);
        }
        
        // FPS se actualiza en el bucle principal
      }
      
      function actualizarFPSDisplay() {
        const statFPSValor = document.getElementById('statFPSValor');
        if (statFPSValor) {
          const fpsRedondeado = Math.round(fps);
          if (statFPSValor.textContent !== String(fpsRedondeado)) {
            statFPSValor.textContent = fpsRedondeado;
          }
        }
      }

      function bucle(tiempoMs){
        if (!ultimoTiempo) ultimoTiempo = tiempoMs;
        const dt = (tiempoMs - ultimoTiempo) / 1000;
        ultimoTiempo = tiempoMs;

        // Calcular FPS
        frameCount++;
        if (tiempoMs - lastFpsUpdate >= 500) { // Actualizar cada 500ms
          fps = frameCount / ((tiempoMs - lastFpsUpdate) / 1000);
          frameCount = 0;
          lastFpsUpdate = tiempoMs;
          actualizarFPSDisplay();
        }

        pasoFisica(dt);
        actualizarFly(dt);
        actualizarZoom(dt);

        contadorFrames++;
        if (contadorFrames % ACTUALIZAR_LINEAS_CADA === 0){
          actualizarConexiones();
          actualizarEstadisticas(); // Actualizar estadísticas cuando se actualizan conexiones
        }

        requestAnimationFrame(bucle);
      }

      // ---------- Event Listeners para Import/Export ----------
      document.getElementById('btnExportJSON').addEventListener('click', exportarJSON);
      document.getElementById('btnExportCSV').addEventListener('click', exportarCSV);
      document.getElementById('btnImportJSON').addEventListener('click', importarJSON);

      // ---------- Carga de datos ----------
      fetch("personas2.json")
        .then(r => r.json())
        .then(items => {
          // Guardar datos originales
          datosOriginales = items;
          const setClaves = new Set();
          items.forEach(item => {
            const cats = item.categories || {};
            Object.keys(cats).forEach(k => setClaves.add(k));
          });
          const claves = Array.from(setClaves);

          crearControlesPropiedades(claves);
          crearNodos3D(items);
          
          // Calcular tiempo total de animación de nodos
          // (número de nodos * 30ms delay) + 800ms de animación + 200ms de margen
          const tiempoAnimacionTotal = (items.length * 30) + 800 + 200;
          
          // Ocultar loader después de cargar
          setTimeout(() => {
            loaderEl.classList.remove('active');
          }, 1000);
          
          // Activar conexiones después de que todos los nodos se hayan animado
          setTimeout(() => {
            conexionesActivadas = true;
            actualizarConexiones(); // Dibujar conexiones por primera vez
            actualizarEstadisticas(); // Actualizar estadísticas iniciales
          }, tiempoAnimacionTotal);
          
          // Actualizar estadísticas de nodos inmediatamente
          actualizarEstadisticas();
          
          requestAnimationFrame(bucle);
        })
        .catch(err => {
          console.error("Error al cargar personas2.json:", err);
          loaderEl.classList.remove('active');
        });
    </script>
  </body>
</html>

```
**personas2.json**
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
    "content": "<h2>Juan (20)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Estudiante<br><strong>Hobbie:</strong> Ajedrez</p>"
  },
  {
    "categories": {
      "nombre": "Juan",
      "hobbie": "Pintura",
      "edad": 20,
      "ciudad": "Valencia",
      "profesion": "Estudiante"
    },
    "content": "<h2>Juan (20)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Estudiante<br><strong>Hobbie:</strong> Pintura</p>"
  },
  {
    "categories": {
      "nombre": "Juan",
      "hobbie": "Fútbol",
      "edad": 20,
      "ciudad": "Valencia",
      "profesion": "Estudiante"
    },
    "content": "<h2>Juan (20)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Estudiante<br><strong>Hobbie:</strong> Fútbol</p>"
  },
  {
    "categories": {
      "nombre": "Juan",
      "hobbie": "Música",
      "edad": 20,
      "ciudad": "Valencia",
      "profesion": "Estudiante"
    },
    "content": "<h2>Juan (20)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Estudiante<br><strong>Hobbie:</strong> Música</p>"
  },
  {
    "categories": {
      "nombre": "Juan",
      "hobbie": "Lectura",
      "edad": 20,
      "ciudad": "Valencia",
      "profesion": "Estudiante"
    },
    "content": "<h2>Juan (20)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Estudiante<br><strong>Hobbie:</strong> Lectura</p>"
  },
  {
    "categories": {
      "nombre": "Juan",
      "hobbie": "Cine",
      "edad": 20,
      "ciudad": "Valencia",
      "profesion": "Estudiante"
    },
    "content": "<h2>Juan (20)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Estudiante<br><strong>Hobbie:</strong> Cine</p>"
  },
  {
    "categories": {
      "nombre": "Julia",
      "hobbie": "Ajedrez",
      "edad": 22,
      "ciudad": "Valencia",
      "profesion": "Diseñadora"
    },
    "content": "<h2>Julia (22)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Diseñadora<br><strong>Hobbie:</strong> Ajedrez</p>"
  },
  {
    "categories": {
      "nombre": "Julia",
      "hobbie": "Pintura",
      "edad": 22,
      "ciudad": "Valencia",
      "profesion": "Diseñadora"
    },
    "content": "<h2>Julia (22)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Diseñadora<br><strong>Hobbie:</strong> Pintura</p>"
  },
  {
    "categories": {
      "nombre": "Julia",
      "hobbie": "Fútbol",
      "edad": 22,
      "ciudad": "Valencia",
      "profesion": "Diseñadora"
    },
    "content": "<h2>Julia (22)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Diseñadora<br><strong>Hobbie:</strong> Fútbol</p>"
  },
  {
    "categories": {
      "nombre": "Julia",
      "hobbie": "Música",
      "edad": 22,
      "ciudad": "Valencia",
      "profesion": "Diseñadora"
    },
    "content": "<h2>Julia (22)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Diseñadora<br><strong>Hobbie:</strong> Música</p>"
  },
  {
    "categories": {
      "nombre": "Julia",
      "hobbie": "Lectura",
      "edad": 22,
      "ciudad": "Valencia",
      "profesion": "Diseñadora"
    },
    "content": "<h2>Julia (22)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Diseñadora<br><strong>Hobbie:</strong> Lectura</p>"
  },
  {
    "categories": {
      "nombre": "Julia",
      "hobbie": "Cine",
      "edad": 22,
      "ciudad": "Valencia",
      "profesion": "Diseñadora"
    },
    "content": "<h2>Julia (22)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Diseñadora<br><strong>Hobbie:</strong> Cine</p>"
  },
  {
    "categories": {
      "nombre": "Jorge",
      "hobbie": "Ajedrez",
      "edad": 25,
      "ciudad": "Madrid",
      "profesion": "Ingeniero"
    },
    "content": "<h2>Jorge (25)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Ingeniero<br><strong>Hobbie:</strong> Ajedrez</p>"
  },
  {
    "categories": {
      "nombre": "Jorge",
      "hobbie": "Pintura",
      "edad": 25,
      "ciudad": "Madrid",
      "profesion": "Ingeniero"
    },
    "content": "<h2>Jorge (25)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Ingeniero<br><strong>Hobbie:</strong> Pintura</p>"
  },
  {
    "categories": {
      "nombre": "Jorge",
      "hobbie": "Fútbol",
      "edad": 25,
      "ciudad": "Madrid",
      "profesion": "Ingeniero"
    },
    "content": "<h2>Jorge (25)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Ingeniero<br><strong>Hobbie:</strong> Fútbol</p>"
  },
  {
    "categories": {
      "nombre": "Jorge",
      "hobbie": "Música",
      "edad": 25,
      "ciudad": "Madrid",
      "profesion": "Ingeniero"
    },
    "content": "<h2>Jorge (25)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Ingeniero<br><strong>Hobbie:</strong> Música</p>"
  },
  {
    "categories": {
      "nombre": "Jorge",
      "hobbie": "Lectura",
      "edad": 25,
      "ciudad": "Madrid",
      "profesion": "Ingeniero"
    },
    "content": "<h2>Jorge (25)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Ingeniero<br><strong>Hobbie:</strong> Lectura</p>"
  },
  {
    "categories": {
      "nombre": "Jorge",
      "hobbie": "Cine",
      "edad": 25,
      "ciudad": "Madrid",
      "profesion": "Ingeniero"
    },
    "content": "<h2>Jorge (25)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Ingeniero<br><strong>Hobbie:</strong> Cine</p>"
  },
  {
    "categories": {
      "nombre": "Jaime",
      "hobbie": "Ajedrez",
      "edad": 27,
      "ciudad": "Madrid",
      "profesion": "Músico"
    },
    "content": "<h2>Jaime (27)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Músico<br><strong>Hobbie:</strong> Ajedrez</p>"
  },
  {
    "categories": {
      "nombre": "Jaime",
      "hobbie": "Pintura",
      "edad": 27,
      "ciudad": "Madrid",
      "profesion": "Músico"
    },
    "content": "<h2>Jaime (27)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Músico<br><strong>Hobbie:</strong> Pintura</p>"
  },
  {
    "categories": {
      "nombre": "Jaime",
      "hobbie": "Fútbol",
      "edad": 27,
      "ciudad": "Madrid",
      "profesion": "Músico"
    },
    "content": "<h2>Jaime (27)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Músico<br><strong>Hobbie:</strong> Fútbol</p>"
  },
  {
    "categories": {
      "nombre": "Jaime",
      "hobbie": "Música",
      "edad": 27,
      "ciudad": "Madrid",
      "profesion": "Músico"
    },
    "content": "<h2>Jaime (27)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Músico<br><strong>Hobbie:</strong> Música</p>"
  },
  {
    "categories": {
      "nombre": "Jaime",
      "hobbie": "Lectura",
      "edad": 27,
      "ciudad": "Madrid",
      "profesion": "Músico"
    },
    "content": "<h2>Jaime (27)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Músico<br><strong>Hobbie:</strong> Lectura</p>"
  },
  {
    "categories": {
      "nombre": "Jaime",
      "hobbie": "Cine",
      "edad": 27,
      "ciudad": "Madrid",
      "profesion": "Músico"
    },
    "content": "<h2>Jaime (27)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Músico<br><strong>Hobbie:</strong> Cine</p>"
  },
  {
    "categories": {
      "nombre": "Jose",
      "hobbie": "Ajedrez",
      "edad": 35,
      "ciudad": "Barcelona",
      "profesion": "Profesor"
    },
    "content": "<h2>Jose (35)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Profesor<br><strong>Hobbie:</strong> Ajedrez</p>"
  },
  {
    "categories": {
      "nombre": "Jose",
      "hobbie": "Pintura",
      "edad": 35,
      "ciudad": "Barcelona",
      "profesion": "Profesor"
    },
    "content": "<h2>Jose (35)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Profesor<br><strong>Hobbie:</strong> Pintura</p>"
  },
  {
    "categories": {
      "nombre": "Jose",
      "hobbie": "Fútbol",
      "edad": 35,
      "ciudad": "Barcelona",
      "profesion": "Profesor"
    },
    "content": "<h2>Jose (35)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Profesor<br><strong>Hobbie:</strong> Fútbol</p>"
  },
  {
    "categories": {
      "nombre": "Jose",
      "hobbie": "Música",
      "edad": 35,
      "ciudad": "Barcelona",
      "profesion": "Profesor"
    },
    "content": "<h2>Jose (35)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Profesor<br><strong>Hobbie:</strong> Música</p>"
  },
  {
    "categories": {
      "nombre": "Jose",
      "hobbie": "Lectura",
      "edad": 35,
      "ciudad": "Barcelona",
      "profesion": "Profesor"
    },
    "content": "<h2>Jose (35)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Profesor<br><strong>Hobbie:</strong> Lectura</p>"
  },
  {
    "categories": {
      "nombre": "Jose",
      "hobbie": "Cine",
      "edad": 35,
      "ciudad": "Barcelona",
      "profesion": "Profesor"
    },
    "content": "<h2>Jose (35)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Profesor<br><strong>Hobbie:</strong> Cine</p>"
  },
  {
    "categories": {
      "nombre": "Julian",
      "hobbie": "Ajedrez",
      "edad": 30,
      "ciudad": "Barcelona",
      "profesion": "Programador"
    },
    "content": "<h2>Julian (30)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Programador<br><strong>Hobbie:</strong> Ajedrez</p>"
  },
  {
    "categories": {
      "nombre": "Julian",
      "hobbie": "Pintura",
      "edad": 30,
      "ciudad": "Barcelona",
      "profesion": "Programador"
    },
    "content": "<h2>Julian (30)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Programador<br><strong>Hobbie:</strong> Pintura</p>"
  },
  {
    "categories": {
      "nombre": "Julian",
      "hobbie": "Fútbol",
      "edad": 30,
      "ciudad": "Barcelona",
      "profesion": "Programador"
    },
    "content": "<h2>Julian (30)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Programador<br><strong>Hobbie:</strong> Fútbol</p>"
  },
  {
    "categories": {
      "nombre": "Julian",
      "hobbie": "Música",
      "edad": 30,
      "ciudad": "Barcelona",
      "profesion": "Programador"
    },
    "content": "<h2>Julian (30)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Programador<br><strong>Hobbie:</strong> Música</p>"
  },
  {
    "categories": {
      "nombre": "Julian",
      "hobbie": "Lectura",
      "edad": 30,
      "ciudad": "Barcelona",
      "profesion": "Programador"
    },
    "content": "<h2>Julian (30)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Programador<br><strong>Hobbie:</strong> Lectura</p>"
  },
  {
    "categories": {
      "nombre": "Julian",
      "hobbie": "Cine",
      "edad": 30,
      "ciudad": "Barcelona",
      "profesion": "Programador"
    },
    "content": "<h2>Julian (30)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Programador<br><strong>Hobbie:</strong> Cine</p>"
  },
  {
    "categories": {
      "nombre": "Laura",
      "hobbie": "Ajedrez",
      "edad": 28,
      "ciudad": "Sevilla",
      "profesion": "Psicóloga"
    },
    "content": "<h2>Laura (28)</h2><p><strong>Ciudad:</strong> Sevilla<br><strong>Profesión:</strong> Psicóloga<br><strong>Hobbie:</strong> Ajedrez</p>"
  },
  {
    "categories": {
      "nombre": "Laura",
      "hobbie": "Pintura",
      "edad": 28,
      "ciudad": "Sevilla",
      "profesion": "Psicóloga"
    },
    "content": "<h2>Laura (28)</h2><p><strong>Ciudad:</strong> Sevilla<br><strong>Profesión:</strong> Psicóloga<br><strong>Hobbie:</strong> Pintura</p>"
  },
  {
    "categories": {
      "nombre": "Laura",
      "hobbie": "Fútbol",
      "edad": 28,
      "ciudad": "Sevilla",
      "profesion": "Psicóloga"
    },
    "content": "<h2>Laura (28)</h2><p><strong>Ciudad:</strong> Sevilla<br><strong>Profesión:</strong> Psicóloga<br><strong>Hobbie:</strong> Fútbol</p>"
  },
  {
    "categories": {
      "nombre": "Laura",
      "hobbie": "Música",
      "edad": 28,
      "ciudad": "Sevilla",
      "profesion": "Psicóloga"
    },
    "content": "<h2>Laura (28)</h2><p><strong>Ciudad:</strong> Sevilla<br><strong>Profesión:</strong> Psicóloga<br><strong>Hobbie:</strong> Música</p>"
  },
  {
    "categories": {
      "nombre": "Laura",
      "hobbie": "Lectura",
      "edad": 28,
      "ciudad": "Sevilla",
      "profesion": "Psicóloga"
    },
    "content": "<h2>Laura (28)</h2><p><strong>Ciudad:</strong> Sevilla<br><strong>Profesión:</strong> Psicóloga<br><strong>Hobbie:</strong> Lectura</p>"
  },
  {
    "categories": {
      "nombre": "Laura",
      "hobbie": "Cine",
      "edad": 28,
      "ciudad": "Sevilla",
      "profesion": "Psicóloga"
    },
    "content": "<h2>Laura (28)</h2><p><strong>Ciudad:</strong> Sevilla<br><strong>Profesión:</strong> Psicóloga<br><strong>Hobbie:</strong> Cine</p>"
  },
  {
    "categories": {
      "nombre": "Luis",
      "hobbie": "Ajedrez",
      "edad": 26,
      "ciudad": "Sevilla",
      "profesion": "Administrador de sistemas"
    },
    "content": "<h2>Luis (26)</h2><p><strong>Ciudad:</strong> Sevilla<br><strong>Profesión:</strong> Administrador de sistemas<br><strong>Hobbie:</strong> Ajedrez</p>"
  },
  {
    "categories": {
      "nombre": "Luis",
      "hobbie": "Pintura",
      "edad": 26,
      "ciudad": "Sevilla",
      "profesion": "Administrador de sistemas"
    },
    "content": "<h2>Luis (26)</h2><p><strong>Ciudad:</strong> Sevilla<br><strong>Profesión:</strong> Administrador de sistemas<br><strong>Hobbie:</strong> Pintura</p>"
  },
  {
    "categories": {
      "nombre": "Luis",
      "hobbie": "Fútbol",
      "edad": 26,
      "ciudad": "Sevilla",
      "profesion": "Administrador de sistemas"
    },
    "content": "<h2>Luis (26)</h2><p><strong>Ciudad:</strong> Sevilla<br><strong>Profesión:</strong> Administrador de sistemas<br><strong>Hobbie:</strong> Fútbol</p>"
  },
  {
    "categories": {
      "nombre": "Luis",
      "hobbie": "Música",
      "edad": 26,
      "ciudad": "Sevilla",
      "profesion": "Administrador de sistemas"
    },
    "content": "<h2>Luis (26)</h2><p><strong>Ciudad:</strong> Sevilla<br><strong>Profesión:</strong> Administrador de sistemas<br><strong>Hobbie:</strong> Música</p>"
  },
  {
    "categories": {
      "nombre": "Luis",
      "hobbie": "Lectura",
      "edad": 26,
      "ciudad": "Sevilla",
      "profesion": "Administrador de sistemas"
    },
    "content": "<h2>Luis (26)</h2><p><strong>Ciudad:</strong> Sevilla<br><strong>Profesión:</strong> Administrador de sistemas<br><strong>Hobbie:</strong> Lectura</p>"
  },
  {
    "categories": {
      "nombre": "Luis",
      "hobbie": "Cine",
      "edad": 26,
      "ciudad": "Sevilla",
      "profesion": "Administrador de sistemas"
    },
    "content": "<h2>Luis (26)</h2><p><strong>Ciudad:</strong> Sevilla<br><strong>Profesión:</strong> Administrador de sistemas<br><strong>Hobbie:</strong> Cine</p>"
  },
  {
    "categories": {
      "nombre": "Lucía",
      "hobbie": "Ajedrez",
      "edad": 24,
      "ciudad": "Bilbao",
      "profesion": "Artista"
    },
    "content": "<h2>Lucía (24)</h2><p><strong>Ciudad:</strong> Bilbao<br><strong>Profesión:</strong> Artista<br><strong>Hobbie:</strong> Ajedrez</p>"
  },
  {
    "categories": {
      "nombre": "Lucía",
      "hobbie": "Pintura",
      "edad": 24,
      "ciudad": "Bilbao",
      "profesion": "Artista"
    },
    "content": "<h2>Lucía (24)</h2><p><strong>Ciudad:</strong> Bilbao<br><strong>Profesión:</strong> Artista<br><strong>Hobbie:</strong> Pintura</p>"
  },
  {
    "categories": {
      "nombre": "Lucía",
      "hobbie": "Fútbol",
      "edad": 24,
      "ciudad": "Bilbao",
      "profesion": "Artista"
    },
    "content": "<h2>Lucía (24)</h2><p><strong>Ciudad:</strong> Bilbao<br><strong>Profesión:</strong> Artista<br><strong>Hobbie:</strong> Fútbol</p>"
  },
  {
    "categories": {
      "nombre": "Lucía",
      "hobbie": "Música",
      "edad": 24,
      "ciudad": "Bilbao",
      "profesion": "Artista"
    },
    "content": "<h2>Lucía (24)</h2><p><strong>Ciudad:</strong> Bilbao<br><strong>Profesión:</strong> Artista<br><strong>Hobbie:</strong> Música</p>"
  },
  {
    "categories": {
      "nombre": "Lucía",
      "hobbie": "Lectura",
      "edad": 24,
      "ciudad": "Bilbao",
      "profesion": "Artista"
    },
    "content": "<h2>Lucía (24)</h2><p><strong>Ciudad:</strong> Bilbao<br><strong>Profesión:</strong> Artista<br><strong>Hobbie:</strong> Lectura</p>"
  },
  {
    "categories": {
      "nombre": "Lucía",
      "hobbie": "Cine",
      "edad": 24,
      "ciudad": "Bilbao",
      "profesion": "Artista"
    },
    "content": "<h2>Lucía (24)</h2><p><strong>Ciudad:</strong> Bilbao<br><strong>Profesión:</strong> Artista<br><strong>Hobbie:</strong> Cine</p>"
  },
  {
    "categories": {
      "nombre": "Leo",
      "hobbie": "Ajedrez",
      "edad": 23,
      "ciudad": "Bilbao",
      "profesion": "Desarrollador"
    },
    "content": "<h2>Leo (23)</h2><p><strong>Ciudad:</strong> Bilbao<br><strong>Profesión:</strong> Desarrollador<br><strong>Hobbie:</strong> Ajedrez</p>"
  },
  {
    "categories": {
      "nombre": "Leo",
      "hobbie": "Pintura",
      "edad": 23,
      "ciudad": "Bilbao",
      "profesion": "Desarrollador"
    },
    "content": "<h2>Leo (23)</h2><p><strong>Ciudad:</strong> Bilbao<br><strong>Profesión:</strong> Desarrollador<br><strong>Hobbie:</strong> Pintura</p>"
  },
  {
    "categories": {
      "nombre": "Leo",
      "hobbie": "Fútbol",
      "edad": 23,
      "ciudad": "Bilbao",
      "profesion": "Desarrollador"
    },
    "content": "<h2>Leo (23)</h2><p><strong>Ciudad:</strong> Bilbao<br><strong>Profesión:</strong> Desarrollador<br><strong>Hobbie:</strong> Fútbol</p>"
  },
  {
    "categories": {
      "nombre": "Leo",
      "hobbie": "Música",
      "edad": 23,
      "ciudad": "Bilbao",
      "profesion": "Desarrollador"
    },
    "content": "<h2>Leo (23)</h2><p><strong>Ciudad:</strong> Bilbao<br><strong>Profesión:</strong> Desarrollador<br><strong>Hobbie:</strong> Música</p>"
  },
  {
    "categories": {
      "nombre": "Leo",
      "hobbie": "Lectura",
      "edad": 23,
      "ciudad": "Bilbao",
      "profesion": "Desarrollador"
    },
    "content": "<h2>Leo (23)</h2><p><strong>Ciudad:</strong> Bilbao<br><strong>Profesión:</strong> Desarrollador<br><strong>Hobbie:</strong> Lectura</p>"
  },
  {
    "categories": {
      "nombre": "Leo",
      "hobbie": "Cine",
      "edad": 23,
      "ciudad": "Bilbao",
      "profesion": "Desarrollador"
    },
    "content": "<h2>Leo (23)</h2><p><strong>Ciudad:</strong> Bilbao<br><strong>Profesión:</strong> Desarrollador<br><strong>Hobbie:</strong> Cine</p>"
  },
  {
    "categories": {
      "nombre": "Lola",
      "hobbie": "Ajedrez",
      "edad": 29,
      "ciudad": "Zaragoza",
      "profesion": "Arquitecta"
    },
    "content": "<h2>Lola (29)</h2><p><strong>Ciudad:</strong> Zaragoza<br><strong>Profesión:</strong> Arquitecta<br><strong>Hobbie:</strong> Ajedrez</p>"
  },
  {
    "categories": {
      "nombre": "Lola",
      "hobbie": "Pintura",
      "edad": 29,
      "ciudad": "Zaragoza",
      "profesion": "Arquitecta"
    },
    "content": "<h2>Lola (29)</h2><p><strong>Ciudad:</strong> Zaragoza<br><strong>Profesión:</strong> Arquitecta<br><strong>Hobbie:</strong> Pintura</p>"
  },
  {
    "categories": {
      "nombre": "Lola",
      "hobbie": "Fútbol",
      "edad": 29,
      "ciudad": "Zaragoza",
      "profesion": "Arquitecta"
    },
    "content": "<h2>Lola (29)</h2><p><strong>Ciudad:</strong> Zaragoza<br><strong>Profesión:</strong> Arquitecta<br><strong>Hobbie:</strong> Fútbol</p>"
  },
  {
    "categories": {
      "nombre": "Lola",
      "hobbie": "Música",
      "edad": 29,
      "ciudad": "Zaragoza",
      "profesion": "Arquitecta"
    },
    "content": "<h2>Lola (29)</h2><p><strong>Ciudad:</strong> Zaragoza<br><strong>Profesión:</strong> Arquitecta<br><strong>Hobbie:</strong> Música</p>"
  },
  {
    "categories": {
      "nombre": "Lola",
      "hobbie": "Lectura",
      "edad": 29,
      "ciudad": "Zaragoza",
      "profesion": "Arquitecta"
    },
    "content": "<h2>Lola (29)</h2><p><strong>Ciudad:</strong> Zaragoza<br><strong>Profesión:</strong> Arquitecta<br><strong>Hobbie:</strong> Lectura</p>"
  },
  {
    "categories": {
      "nombre": "Lola",
      "hobbie": "Cine",
      "edad": 29,
      "ciudad": "Zaragoza",
      "profesion": "Arquitecta"
    },
    "content": "<h2>Lola (29)</h2><p><strong>Ciudad:</strong> Zaragoza<br><strong>Profesión:</strong> Arquitecta<br><strong>Hobbie:</strong> Cine</p>"
  },
  {
    "categories": {
      "nombre": "Andrés",
      "hobbie": "Ajedrez",
      "edad": 31,
      "ciudad": "Valencia",
      "profesion": "Analista de datos"
    },
    "content": "<h2>Andrés (31)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Analista de datos<br><strong>Hobbie:</strong> Ajedrez</p>"
  },
  {
    "categories": {
      "nombre": "Andrés",
      "hobbie": "Pintura",
      "edad": 31,
      "ciudad": "Valencia",
      "profesion": "Analista de datos"
    },
    "content": "<h2>Andrés (31)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Analista de datos<br><strong>Hobbie:</strong> Pintura</p>"
  },
  {
    "categories": {
      "nombre": "Andrés",
      "hobbie": "Fútbol",
      "edad": 31,
      "ciudad": "Valencia",
      "profesion": "Analista de datos"
    },
    "content": "<h2>Andrés (31)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Analista de datos<br><strong>Hobbie:</strong> Fútbol</p>"
  },
  {
    "categories": {
      "nombre": "Andrés",
      "hobbie": "Música",
      "edad": 31,
      "ciudad": "Valencia",
      "profesion": "Analista de datos"
    },
    "content": "<h2>Andrés (31)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Analista de datos<br><strong>Hobbie:</strong> Música</p>"
  },
  {
    "categories": {
      "nombre": "Andrés",
      "hobbie": "Lectura",
      "edad": 31,
      "ciudad": "Valencia",
      "profesion": "Analista de datos"
    },
    "content": "<h2>Andrés (31)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Analista de datos<br><strong>Hobbie:</strong> Lectura</p>"
  },
  {
    "categories": {
      "nombre": "Andrés",
      "hobbie": "Cine",
      "edad": 31,
      "ciudad": "Valencia",
      "profesion": "Analista de datos"
    },
    "content": "<h2>Andrés (31)</h2><p><strong>Ciudad:</strong> Valencia<br><strong>Profesión:</strong> Analista de datos<br><strong>Hobbie:</strong> Cine</p>"
  },
  {
    "categories": {
      "nombre": "Ana",
      "hobbie": "Ajedrez",
      "edad": 21,
      "ciudad": "Madrid",
      "profesion": "Estudiante"
    },
    "content": "<h2>Ana (21)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Estudiante<br><strong>Hobbie:</strong> Ajedrez</p>"
  },
  {
    "categories": {
      "nombre": "Ana",
      "hobbie": "Pintura",
      "edad": 21,
      "ciudad": "Madrid",
      "profesion": "Estudiante"
    },
    "content": "<h2>Ana (21)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Estudiante<br><strong>Hobbie:</strong> Pintura</p>"
  },
  {
    "categories": {
      "nombre": "Ana",
      "hobbie": "Fútbol",
      "edad": 21,
      "ciudad": "Madrid",
      "profesion": "Estudiante"
    },
    "content": "<h2>Ana (21)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Estudiante<br><strong>Hobbie:</strong> Fútbol</p>"
  },
  {
    "categories": {
      "nombre": "Ana",
      "hobbie": "Música",
      "edad": 21,
      "ciudad": "Madrid",
      "profesion": "Estudiante"
    },
    "content": "<h2>Ana (21)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Estudiante<br><strong>Hobbie:</strong> Música</p>"
  },
  {
    "categories": {
      "nombre": "Ana",
      "hobbie": "Lectura",
      "edad": 21,
      "ciudad": "Madrid",
      "profesion": "Estudiante"
    },
    "content": "<h2>Ana (21)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Estudiante<br><strong>Hobbie:</strong> Lectura</p>"
  },
  {
    "categories": {
      "nombre": "Ana",
      "hobbie": "Cine",
      "edad": 21,
      "ciudad": "Madrid",
      "profesion": "Estudiante"
    },
    "content": "<h2>Ana (21)</h2><p><strong>Ciudad:</strong> Madrid<br><strong>Profesión:</strong> Estudiante<br><strong>Hobbie:</strong> Cine</p>"
  },
  {
    "categories": {
      "nombre": "Pablo",
      "hobbie": "Ajedrez",
      "edad": 32,
      "ciudad": "Barcelona",
      "profesion": "Investigador"
    },
    "content": "<h2>Pablo (32)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Investigador<br><strong>Hobbie:</strong> Ajedrez</p>"
  },
  {
    "categories": {
      "nombre": "Pablo",
      "hobbie": "Pintura",
      "edad": 32,
      "ciudad": "Barcelona",
      "profesion": "Investigador"
    },
    "content": "<h2>Pablo (32)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Investigador<br><strong>Hobbie:</strong> Pintura</p>"
  },
  {
    "categories": {
      "nombre": "Pablo",
      "hobbie": "Fútbol",
      "edad": 32,
      "ciudad": "Barcelona",
      "profesion": "Investigador"
    },
    "content": "<h2>Pablo (32)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Investigador<br><strong>Hobbie:</strong> Fútbol</p>"
  },
  {
    "categories": {
      "nombre": "Pablo",
      "hobbie": "Música",
      "edad": 32,
      "ciudad": "Barcelona",
      "profesion": "Investigador"
    },
    "content": "<h2>Pablo (32)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Investigador<br><strong>Hobbie:</strong> Música</p>"
  },
  {
    "categories": {
      "nombre": "Pablo",
      "hobbie": "Lectura",
      "edad": 32,
      "ciudad": "Barcelona",
      "profesion": "Investigador"
    },
    "content": "<h2>Pablo (32)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Investigador<br><strong>Hobbie:</strong> Lectura</p>"
  },
  {
    "categories": {
      "nombre": "Pablo",
      "hobbie": "Cine",
      "edad": 32,
      "ciudad": "Barcelona",
      "profesion": "Investigador"
    },
    "content": "<h2>Pablo (32)</h2><p><strong>Ciudad:</strong> Barcelona<br><strong>Profesión:</strong> Investigador<br><strong>Hobbie:</strong> Cine</p>"
  }
]


```
**worker.js**
```js
// worker.js
// Lógica de física (interacciones y movimiento) en un Web Worker

function distancia2D(x1, y1, x2, y2) {
  const dx = x2 - x1;
  const dy = y2 - y1;
  return Math.sqrt(dx * dx + dy * dy);
}

let particulas = [];
let clavesPropiedades = [];
let usarEnRelacion = {};
let ancho = 0;
let alto  = 0;

onmessage = function(e){
  const datos = e.data;

  if (datos.tipo === "inicializar"){
    particulas = datos.particulas || [];
    clavesPropiedades = datos.clavesPropiedades || [];
    usarEnRelacion = datos.usarEnRelacion || {};
    ancho = datos.ancho || 0;
    alto  = datos.alto  || 0;

    postMessage({ tipo: "iniciado" });
  }
  else if (datos.tipo === "paso"){
    usarEnRelacion    = datos.usarEnRelacion || usarEnRelacion;
    clavesPropiedades = datos.clavesPropiedades || clavesPropiedades;

    calcularPasoFisica();
    postMessage({ tipo: "estado", particulas: particulas });
  }
  else if (datos.tipo === "reactivar"){
    // Quitar estado de "fija" para todas las partículas
    if (particulas) {
      for (let i = 0; i < particulas.length; i++){
        particulas[i].fija = false;
        particulas[i].estableFrames = 0;
      }
    }
  }
};

function calcularPasoFisica(){
  if (!particulas || particulas.length === 0) return;

  const n = particulas.length;

  const rangoGlobal = Math.sqrt(ancho*ancho + alto*alto);

  const distanciaObjetivo          = 120;
  const distanciaMinima            = 70;
  const distanciaRepulsionDistinto = 220;

  const kAtraccionFuerte   = 0.0015;
  const kAtraccionMedia    = 0.0009;
  const kRepulsionDistinto = 0.001;
  const kRepulsionCorta    = 0.06;

  const friccion = 0.93;
  const maxFuerza = 0.05;

  // Reiniciar aceleraciones
  for (let i = 0; i < n; i++){
    particulas[i].ax = 0;
    particulas[i].ay = 0;
  }

  // Calcular fuerzas de interacción
  for (let i = 0; i < n; i++){
    const p = particulas[i];
    if (p.fija) continue;

    let fx = 0;
    let fy = 0;

    for (let j = 0; j < n; j++){
      if (i === j) continue;
      const q = particulas[j];

      let d = distancia2D(p.x, p.y, q.x, q.y);
      if (d === 0 || d > rangoGlobal) continue;

      let dx = q.x - p.x;
      let dy = q.y - p.y;

      let ux = dx / d;
      let uy = dy / d;

      // Repulsión fuerte para evitar solapamiento
      if (d < distanciaMinima){
        let intensidad = (distanciaMinima - d) * kRepulsionCorta;
        fx -= ux * intensidad;
        fy -= uy * intensidad;
        continue;
      }

      // Coincidencias según propiedades activas en relación
      const propsCoinciden = [];
      let hayPropsRelacionActivas = false;
      for (const prop of clavesPropiedades){
        if (!usarEnRelacion[prop]) continue;
        hayPropsRelacionActivas = true;
        if (p.datos[prop] === q.datos[prop]){
          propsCoinciden.push(prop);
        }
      }

      if (propsCoinciden.length > 1){
        // Atracción fuerte (coinciden varias propiedades)
        let delta = d - distanciaObjetivo;
        fx += ux * delta * kAtraccionFuerte;
        fy += uy * delta * kAtraccionFuerte;

      } else if (propsCoinciden.length === 1){
        // Atracción media (coincide una propiedad)
        let delta = d - distanciaObjetivo;
        fx += ux * delta * kAtraccionMedia;
        fy += uy * delta * kAtraccionMedia;

      } else {
        // Sin coincidencias: repulsión suave si está relativamente cerca
        if (d < distanciaRepulsionDistinto){
          let intensidad = (distanciaRepulsionDistinto - d) * kRepulsionDistinto;
          fx -= ux * intensidad;
          fy -= uy * intensidad;
        }
      }
    }

    // Limitar fuerza total
    let modulo = Math.sqrt(fx*fx + fy*fy);
    if (modulo > maxFuerza){
      fx = fx / modulo * maxFuerza;
      fy = fy / modulo * maxFuerza;
    }

    p.ax = fx;
    p.ay = fy;
  }

  // Integrar movimiento y rebotes
  for (let i = 0; i < n; i++){
    const p = particulas[i];
    if (!p.fija){
      // Integrar aceleración -> velocidad
      p.vx += p.ax;
      p.vy += p.ay;

      // Fricción
      p.vx *= friccion;
      p.vy *= friccion;

      // Integrar velocidad -> posición
      p.x += p.vx;
      p.y += p.vy;

      // Rebote con bordes
      const reboteFactor = -0.5;

      if (p.x > ancho){
        p.x = ancho;
        p.vx *= reboteFactor;
      }
      if (p.x < 0){
        p.x = 0;
        p.vx *= reboteFactor;
      }
      if (p.y > alto){
        p.y = alto;
        p.vy *= reboteFactor;
      }
      if (p.y < 0){
        p.y = 0;
        p.vy *= reboteFactor;
      }

      // Comprobar estabilidad para fijar partícula
      const velocidad = Math.sqrt(p.vx*p.vx + p.vy*p.vy);
      const fuerza    = Math.sqrt(p.ax*p.ax + p.ay*p.ay);
      if (velocidad < 0.02 && fuerza < 0.002){
        p.estableFrames = (p.estableFrames || 0) + 1;
        if (p.estableFrames > 60){
          p.fija = true;
          p.vx = 0;
          p.vy = 0;
        }
      } else {
        p.estableFrames = 0;
      }
    }
  }
}

```