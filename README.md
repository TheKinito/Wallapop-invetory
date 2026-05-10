# 🔄 FlipTracker

Aplicación web para gestionar compraventas de productos en Wallapop (o cualquier plataforma de segunda mano). Sin servidor, sin base de datos — funciona directamente en el navegador.

## ✨ Funcionalidades

### 📦 Ventas
- Registra productos con precio de compra, venta y repuestos usados
- Múltiples repuestos por producto con cantidad (descuenta stock automáticamente)
- Beneficio neto y margen calculados en tiempo real
- Estados: En stock / Vendido / Reparando
- Búsqueda y filtrado del historial
- Edición y eliminación de cualquier entrada
- Exportación a CSV

### 🗄️ Inventario
- Gestión de repuestos con stock inicial, usados y stock actual
- Precio por unidad y valor total del stock
- El stock se actualiza automáticamente al vincular repuestos a ventas

### 📊 Resumen
- Capital invertido, facturado y beneficio neto
- ROI, margen medio y tasa de éxito
- Top 5 productos por beneficio
- Distribución por estado con barras visuales
- Análisis financiero detallado

### ⬆ Importar Excel
- Importa directamente desde tu hoja de cálculo `.xlsx`
- Detecta automáticamente las columnas (Producto, Compra, Venta, Repuesto, Estado…)
- Vincula repuestos del inventario por nombre
- Opción de añadir a datos existentes o reemplazar todo

## 🚀 Uso

No necesita instalación ni servidor. Simplemente abre `index.html` en tu navegador.

```bash
# Opción 1: abrir directamente
open index.html

# Opción 2: servidor local rápido (Python)
python3 -m http.server 8080
# luego visita http://localhost:8080

# Opción 3: servidor local rápido (Node)
npx serve .
```

## 💾 Almacenamiento

Los datos se guardan en el `localStorage` del navegador. No se envía nada a ningún servidor. Para hacer copia de seguridad usa el botón **⬇ CSV**.

## 📁 Estructura

```
fliptracker/
├── index.html      # Aplicación completa (HTML + CSS + JS en un solo archivo)
└── README.md
```

## 🌐 Deploy en GitHub Pages

1. Sube el repositorio a GitHub
2. Ve a **Settings → Pages**
3. En *Source* selecciona `main` / `root`
4. Tu app estará disponible en `https://tu-usuario.github.io/fliptracker`

## 🛠 Tecnologías

- HTML5 / CSS3 / JavaScript vanilla
- [SheetJS (xlsx)](https://sheetjs.com/) — lectura de archivos Excel (cargado desde CDN)
- Google Fonts — Syne + JetBrains Mono
- `localStorage` para persistencia de datos

## 📋 Formato del Excel para importación

### Hoja de ventas
| Producto | Precio compra | Repuesto usado | Coste reparación | Precio venta | Estado | Observaciones |
|----------|--------------|---------------|-----------------|-------------|--------|---------------|

### Hoja de inventario
| Repuesto | Stock Inicial | Usados | Stock Actual | Precio Unidad |
|---------|--------------|--------|-------------|--------------|

## 📄 Licencia

MIT — libre para uso personal y comercial.
