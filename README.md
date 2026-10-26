# Calculadora de costo de impresiones 3D

Página web estática (un solo archivo, sin dependencias) que calcula el costo real y el precio de venta sugerido de una impresión 3D.

## Uso

Abre `index.html` en cualquier navegador y elige tu país en el selector de moneda (todos los países hispanohablantes y Brasil). Los valores se guardan automáticamente en el navegador.

## Productos y presupuestos

- **Mis productos:** guarda la configuración actual con el nombre de la pieza y vuelve a cargarla cuando quieras.
- **Enviar presupuesto:** completa tu negocio, el cliente y notas, y envíalo por WhatsApp, por email, con el menú de compartir del celular o como PDF (Imprimir → Guardar como PDF).

Todo se guarda solo en el navegador del dispositivo (no hay servidor).

## Publicar en Vercel

Es un sitio estático, no necesita configuración:

1. Entra en <https://vercel.com/new> e inicia sesión con GitHub.
2. Importa el repositorio `calculadora-de-impresiones-3d`.
3. Framework Preset: **Other**. Deja vacíos Build Command y Output Directory.
4. Pulsa **Deploy**.

## Consumo de la impresora

Elige tu modelo en la lista (Bambu Lab, Creality, Prusa, Anycubic, Elegoo, Artillery y de resina) para cargar su consumo promedio aproximado, o elige **Personalizada** e ingresa los watts. Las configuraciones personalizadas se pueden guardar con un nombre y aparecen en **Mis impresoras**.

## Qué calcula

| Concepto | Fórmula |
|---|---|
| Material | peso (g) × precio del rollo ÷ peso del rollo (g) |
| Electricidad | consumo (W) ÷ 1000 × horas × precio del kWh |
| Desgaste | costo de la impresora ÷ vida útil (h) × horas |
| Mantenimiento | costo por hora × horas |
| Fallos | (material + electricidad + desgaste + mantenimiento) × (1 ÷ (1 − tasa) − 1) |
| Mano de obra | minutos de trabajo ÷ 60 × valor de la hora |
| Costo total | suma de todo lo anterior + insumos extra (+ envío, si es gratis para el cliente) |
| Precio de venta | (costo × (1 + margen)) ÷ (1 − impuestos/comisiones) (+ envío, si lo paga el cliente) |

Si se imprimen varias piezas en el mismo trabajo, ingresa el peso y tiempo totales y la cantidad: se muestra también el precio por unidad.
