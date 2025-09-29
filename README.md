# 💱 Conversor de Monedas Pro

Un conversor de monedas moderno y completo que permite conversiones bidireccionales entre **Peso Chileno (CLP)**, **Dólar Estadounidense (USD)** y **Peso Argentino (ARS)** con funcionalidades avanzadas.

![Conversor de Monedas Pro](https://img.shields.io/badge/Version-2.0-brightgreen) ![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white) ![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?logo=tailwind-css&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## 🌟 Características Principales

### 🔄 **Conversión Bidireccional**
- Convierte entre cualquier par de monedas: CLP ↔ USD ↔ ARS
- Selección intuitiva de moneda origen y destino
- Botón de intercambio rápido entre monedas
- Montos rápidos adaptativos según la moneda seleccionada

### 🎨 **Interfaz Moderna**
- Diseño inspirado en Apple con **Tailwind CSS**
- Layout de dashboard horizontal optimizado
- **Tema claro/oscuro** con persistencia
- Completamente **responsivo** para móviles y desktop
- Animaciones suaves y transiciones fluidas

### 📊 **Funcionalidades Avanzadas**
- **📈 Gráfico de tendencias**: Visualización de cotizaciones de los últimos 7 días
- **📝 Historial de conversiones**: Guarda las últimas 10 conversiones realizadas
- **🧮 Calculadora integrada**: Entrada numérica con botones
- **⚡ Montos rápidos**: Botones predeterminados (100K, 500K, 1M, 5M para CLP)
- **🔔 Alertas de precio**: Notificaciones cuando las cotizaciones cambien
- **📤 Función compartir**: Comparte resultados por WhatsApp, email, redes sociales
- **💾 Persistencia**: Guarda historial, alertas y configuraciones en localStorage

### 🌐 **APIs y Datos en Tiempo Real**
- **DolarAPI**: Cotizaciones oficiales USD → ARS
- **Mindicador**: Cotizaciones oficiales USD → CLP
- Actualización automática al cargar la página
- Opción de cotizaciones manuales para casos especiales
- Sistema de notificaciones para feedback del usuario

## 🚀 Uso

### Acceso Directo
Simplemente abre `index.html` en tu navegador web.

### Servidor Local
```bash
# Clona el repositorio
git clone https://github.com/mateoestrada5/conversorpclpar.git
cd conversorpclpar

# Inicia un servidor HTTP local
python3 -m http.server 8080

# Abre en tu navegador
# http://localhost:8080
```

## 📱 Cómo Usar

1. **Selecciona las monedas**: Elige moneda origen y destino en los dropdowns
2. **Ingresa el monto**: Escribe la cantidad o usa los botones de montos rápidos
3. **Convierte**: Presiona el botón "Convertir" para obtener el resultado
4. **Explora**: 
   - Ve el historial de conversiones anteriores
   - Consulta el gráfico de tendencias
   - Configura alertas de precio
   - Comparte resultados

## 🛠️ Tecnologías

- **HTML5**: Estructura semántica y moderna
- **Tailwind CSS**: Framework de CSS utility-first para diseño rápido
- **JavaScript ES6+**: Funcionalidades modernas (async/await, localStorage)
- **Chart.js**: Visualización de datos para gráficos de tendencias
- **Font: Montserrat**: Tipografía moderna de Google Fonts

## 🌐 APIs Utilizadas

| API | Propósito | URL |
|-----|-----------|-----|
| **DolarAPI** | Cotización USD → ARS | `https://dolarapi.com/v1/dolares/oficial` |
| **Mindicador** | Cotización USD → CLP | `https://mindicador.cl/api/dolar` |

## 📁 Estructura del Proyecto

```
conversorpclpar/
├── index.html          # Aplicación principal (SPA)
├── README.md           # Documentación del proyecto
└── .git/              # Control de versiones
```

## ⚡ Funcionalidades Técnicas

### Conversión Bidireccional
```javascript
// Ejemplo de conversión CLP → ARS
function calcularConversion(monto, desde, hacia) {
  // Convertir todo a USD primero
  let montoUSD = monto;
  if (desde === 'CLP') montoUSD = monto / cotizacionClp;
  
  // Convertir de USD a moneda destino
  if (hacia === 'ARS') return montoUSD * cotizacionArs;
}
```

### Persistencia de Datos
- `localStorage` para historial de conversiones
- `localStorage` para configuración de alertas
- `localStorage` para tema claro/oscuro
- `localStorage` para historial de cotizaciones (gráfico)

### Características de UX
- **Formato de miles**: Separación automática con puntos (ej: 1.000.000)
- **Validación en tiempo real**: Verificación de inputs
- **Notificaciones toast**: Feedback inmediato al usuario
- **Estados de carga**: Indicadores durante la carga de APIs
- **Manejo de errores**: Fallbacks cuando las APIs no responden

## 🎯 Casos de Uso

### Para Individuos
- Conversiones rápidas para viajes o compras online
- Seguimiento de tendencias cambiarias
- Alertas para decisiones de inversión

### Para Empresas
- Cálculos de precios internacionales
- Planificación de importaciones/exportaciones
- Análisis de variaciones cambiarias

## 🔄 Historial de Versiones

### v2.0 (Actual)
- ✅ Conversión bidireccional entre CLP, USD, ARS
- ✅ Interfaz moderna inspirada en Apple
- ✅ Gráfico de tendencias con Chart.js
- ✅ Historial de conversiones
- ✅ Calculadora integrada
- ✅ Sistema de alertas
- ✅ Función compartir
- ✅ Tema claro/oscuro

### v1.0 (Inicial)
- ✅ Conversión básica CLP → USD → ARS
- ✅ Integración con APIs
- ✅ Interfaz básica con Tailwind

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Para cambios importantes:

1. Fork del proyecto
2. Crea una rama para tu feature (`git checkout -b feature/nueva-funcionalidad`)
3. Commit tus cambios (`git commit -am 'Agrega nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/nueva-funcionalidad`)
5. Abre un Pull Request

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Ver `LICENSE` para más detalles.

## 👨‍💻 Autor

**Mateo Estrada**
- GitHub: [@mateoestrada5](https://github.com/mateoestrada5)

## 🙏 Agradecimientos

- **DolarAPI** por proporcionar cotizaciones en tiempo real de Argentina
- **Mindicador** por las cotizaciones oficiales de Chile
- **Tailwind CSS** por el framework de diseño
- **Chart.js** por las visualizaciones de datos

---

⭐ **¡Dale una estrella al proyecto si te resulta útil!** ⭐

## 📊 APIs Utilizadas

| Moneda | API | Endpoint |
|--------|-----|----------|
| 🇦🇷 ARS | DolarAPI | `https://dolarapi.com/v1/dolares/oficial` |
| 🇨🇱 CLP | Mindicador | `https://mindicador.cl/api/dolar` |

## 🎯 Funcionalidades

### 💹 Cotizaciones Automáticas
- Carga automática al iniciar la aplicación
- Botón de actualización manual
- Indicadores visuales de estado (cargando/éxito/error)
- Valores por defecto en caso de fallo de API

### 🔄 Conversión de Monedas
- Input con formato de miles automático (1.000.000)
- Validación de entrada
- Conversión CLP → USD → ARS
- Resultado visual con banderas y colores

### ⚙️ Configuración Manual
- Override de cotizaciones automáticas
- Inputs numéricos para USD→CLP y USD→ARS
- Persistencia durante la sesión
- Timestamp de última actualización

## 💻 Estructura del Proyecto

```
conversorpclpar/
├── index.html          # Aplicación principal
└── README.md          # Este archivo
```

## 🎨 Diseño

### Layout Dashboard
- **3 columnas principales**: Cotizaciones | Convertir | Configuración
- **Sección de resultados**: Centrada con 60% de ancho
- **Header sticky**: Con navegación fija
- **Cards flotantes**: Con efectos glassmorphism

### Paleta de Colores
- **Apple Gray**: `#f5f5f7` - Fondo principal
- **Apple Dark**: `#1d1d1f` - Textos principales  
- **Apple Blue**: `#007aff` - Elementos interactivos
- **Apple Green**: `#30d158` - Confirmaciones/éxito

### Responsive Design
- **Desktop**: Grid de 3 columnas
- **Tablet**: Grid adaptativo
- **Móvil**: Columna única apilada

## 🔧 Personalización

### Cambiar APIs
```javascript
// En la función cargarCotizaciones()
const responseArs = await fetch("TU_NUEVA_API_ARS");
const responseClp = await fetch("TU_NUEVA_API_CLP");
```

### Modificar Colores
```javascript
// En el tailwind.config
colors: {
  'apple-gray': '#tu-color',
  'apple-blue': '#tu-color',
  // ...
}
```

### Agregar Nuevas Monedas
1. Actualizar la función `convertir()`
2. Agregar nueva API en `cargarCotizaciones()`  
3. Modificar el HTML de resultado

## 📱 Compatibilidad

- ✅ Chrome 90+
- ✅ Firefox 88+  
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Mobile browsers

## 🤝 Contribuir

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add: nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 👤 Autor

**Mateo Estrada** - [@mateoestrada5](https://github.com/mateoestrada5)

## 🙏 Agradecimientos

- [DolarAPI](https://dolarapi.com/) por los datos del peso argentino
- [Mindicador](https://mindicador.cl/) por los datos del peso chileno  

---

⭐ ¡No olvides darle una estrella al proyecto si te fue útil!