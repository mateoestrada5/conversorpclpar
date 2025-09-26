# 💱 Conversor de Monedas CLP → USD → ARS

Una aplicación web moderna para convertir pesos chilenos (CLP) a dólares estadounidenses (USD) y pesos argentinos (ARS) con cotizaciones en tiempo real.

![Conversor de Monedas](https://img.shields.io/badge/Status-Active-brightgreen) ![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white) ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?logo=tailwind-css&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## ✨ Características

- 🔄 **Cotizaciones en tiempo real** desde APIs oficiales
- ⚡ **Conversión instantánea** con formato de números localizados
- 🔧 **Configuración manual** de cotizaciones como respaldo
- 🌟 **Interfaz tipo dashboard** compacta y elegante
- 🔔 **Notificaciones toast** para mejor UX

## 🚀 Demo

Simplemente abre `index.html` en tu navegador favorito. No requiere instalación ni servidor.

## 🛠️ Tecnologías Utilizadas

- **HTML5** - Estructura semántica
- **Tailwind CSS** - Framework CSS utilitario vía CDN
- **JavaScript ES6+** - Lógica de conversión y APIs
- **Montserrat Font** - Tipografía moderna de Google Fonts
- **CSS Glassmorphism** - Efectos de cristal con backdrop-blur

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