# 🔄 FlipTracker + ⚡ RepairLab

Aplicación web fusionada para gestionar compraventas de segunda mano en Wallapop, con asistente IA de reparación integrado.

## ✨ Funcionalidades

### 🔄 FlipTracker (gestión de negocio)
- **📦 Ventas** — Registra productos con precio de compra, venta y repuestos. Calcula beneficio y ROI automáticamente.
- **🗄️ Inventario** — Gestión de repuestos con stock. Se descuenta automáticamente al vincular a ventas.
- **🔧 Taller** — Componentes con alertas de stock mínimo.
- **🛒 Pedidos** — Lista de compra pendiente vinculada al taller.
- **📊 Resumen** — ROI, margen medio, top productos, análisis financiero completo.
- Importar desde Excel `.xlsx`, exportar a CSV.

### ⚡ RepairLab (búsqueda e IA)
- **🔍 Buscador** — Búsqueda real en Wallapop vía API Playwright con filtros de precio, estado y orden. Detecta posibles daños automáticamente y estima % de beneficio.
- **🤖 Asistente IA** — Claude analiza el producto con tus datos de inventario: diagnóstico, guía paso a paso, componentes necesarios, beneficio potencial.

## 🗄️ Base de datos

Usa **Supabase** (PostgreSQL) para sincronización en tiempo real. Tablas necesarias:
- `ventas`
- `inventario`
- `inventario_componentes`
- `lista_compra`

## 🔍 API de búsqueda (Playwright)

Para que el buscador funcione necesitas desplegar la API de scraping por separado:
👉 [wallapop-api](https://github.com/TU_USUARIO/wallapop-api)

Una vez desplegada en Railway, actualiza en `index.html`:
```javascript
const API_URL = 'https://TU-API.railway.app';
```

## 🚀 Despliegue

**Opción 1 — Vercel (recomendado, gratis):**
1. Conecta este repo en [vercel.com](https://vercel.com)
2. Deploy automático en cada push a `main`

**Opción 2 — GitHub Pages:**
1. Settings → Pages → Source: `main` / `root`
2. Disponible en `https://tu-usuario.github.io/fliptracker-repairlab`

**Opción 3 — Local:**
```bash
open index.html
# o
npx serve .
```

## 🛠 Tecnologías

- HTML5 / CSS3 / JavaScript vanilla
- [Supabase](https://supabase.com) — base de datos en tiempo real
- [Claude API](https://anthropic.com) — asistente IA de reparación
- [SheetJS](https://sheetjs.com) — importación de Excel
- Google Fonts — Syne + JetBrains Mono

## 📄 Licencia

MIT
