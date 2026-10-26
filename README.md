# Calculadora de costo de impresiones 3D

Página web estática (un solo archivo, sin dependencias) que calcula el costo real y el precio de venta sugerido de una impresión 3D.

## Uso

Abre `index.html` en cualquier navegador y elige tu país en el selector de moneda (todos los países hispanohablantes y Brasil). Los valores se guardan automáticamente en el navegador.

## Qué calcula

| Concepto | Fórmula |
|---|---|
| Material | peso (g) × precio del rollo ÷ peso del rollo (g) |
| Electricidad | consumo (W) ÷ 1000 × horas × precio del kWh |
| Desgaste | costo de la impresora ÷ vida útil (h) × horas |
| Mantenimiento | costo por hora × horas |
| Fallos | (material + electricidad + desgaste + mantenimiento) × (1 ÷ (1 − tasa) − 1) |
| Mano de obra | minutos de trabajo ÷ 60 × valor de la hora |
| Costo total | suma de todo lo anterior + insumos extra |
| Precio de venta | (costo × (1 + margen)) ÷ (1 − impuestos/comisiones) |

Si se imprimen varias piezas en el mismo trabajo, ingresa el peso y tiempo totales y la cantidad: se muestra también el precio por unidad.
