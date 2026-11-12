# Análisis de ventas y dashboard en Excel

**Proyecto de práctica · Excel · 2026**

Autor: Angel Regino

![Dashboard de ventas](dashboard.png)

---

## 1. El problema

Una tienda de electrónica, muebles y papelería quiere entender **de dónde viene su dinero** y **qué tan estables son sus ventas**, para decidir en qué productos enfocarse.

Preguntas de negocio:
1. ¿Cuánto vende la tienda y cuál es el ticket promedio?
2. ¿Qué productos, regiones y vendedores generan más dinero?
3. ¿Cómo cambian las ventas mes a mes?
4. ¿Qué riesgos tiene el negocio?

## 2. Los datos

Datos de práctica de **120 ventas** (enero a junio de 2026), con fecha, región, vendedor, producto, categoría, cantidad y precio. El archivo tiene 6 hojas:

| Hoja | Contenido |
|---|---|
| **Dashboard** | KPIs, gráficos y conclusiones en una sola pantalla |
| **Ventas** | Los datos de cada venta, con columnas calculadas (total, costo, comisión, total en USD, mes) |
| **Costos** | Costo unitario de cada producto (tabla de consulta) |
| **Vendedores** | Nivel y % de comisión de cada vendedor (tabla de consulta) |
| **Resumen** | Indicadores, preguntas de negocio con su fórmula y ventas por producto |
| **Dinámica** | Tabla dinámica de ventas por mes y categoría |

## 3. Lo que hice

- **Columnas calculadas:** total por venta y conversión a dólares con un tipo de cambio fijo (referencias absolutas `$`).
- **BUSCARX:** traje el costo de cada producto y la comisión de cada vendedor desde otras tablas, como un JOIN. Detecté un vendedor que no estaba registrado y lo manejé con un mensaje claro en lugar de un error `#N/D`.
- **CONTAR.SI, SUMAR.SI y sus versiones .CONJUNTO:** respondí preguntas con una o varias condiciones (por ejemplo, ventas de Electrónica en la región Norte).
- **Tablas dinámicas:** ventas por región, vendedor, producto y mes.
- **Formato condicional:** resalté las ventas mayores a $10,000 y apliqué una escala de colores por producto.
- **Gráficos:** columnas para comparar productos y líneas para ver la tendencia por mes.
- **Dashboard:** 3 KPIs, 2 gráficos y conclusiones.

**Herramienta:** Microsoft Excel (Excel en línea / Microsoft 365). BUSCARX requiere Excel 365 o 2021.

## 4. Lo que descubrí

- **La Laptop es el producto estrella:** genera el **50% de las ventas** ($450,000 de $901,695).
- **Principio de Pareto:** el **20% de las ventas** (las mayores a $10,000) genera el **66% del dinero**.
- **Electrónica es la categoría más grande y la más volátil:** pasó de $27,600 en abril a $206,400 en mayo. En abril, Muebles la rebasó.
- **Vender más veces no es vender más dinero:** Carlos hizo más ventas (20), pero Sofía generó más dinero ($157,450) porque vende más laptops.

### Recomendaciones
1. Mantener las laptops como motor del negocio, cuidando su inventario y precio con proveedores.
2. Impulsar Muebles, que es más estable, y la venta de accesorios junto con cada laptop (audífonos, mochilas).
3. Evaluar a los vendedores por monto y ticket promedio, no solo por número de ventas.
4. Registrar a la vendedora Valeria en la tabla de comisiones (dato faltante detectado).
