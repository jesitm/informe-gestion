# Informe de gestión de ventas · Power BI + Python

Dashboard comparativo de gestión construido a partir de 10 años de ventas de una empresa con sucursales en varias ciudades. Los datos se recibieron en archivos CSV (productos, precios y medios de pago); los limpié y modelé con Python y armé el tablero en Power BI para responder preguntas de negocio sobre sucursales, productos y medios de pago.

> **Contexto:** caso práctico del curso de Data Science de Henry / proyecto individual .

## Problema de negocio

La empresa necesita un informe que detalle:

- la **rentabilidad de cada sucursal**,
- el **desempeño del equipo de ventas**,
- el **ranking de marcas y productos** que comercializa,

para tomar decisiones sobre la apertura o el cierre de sucursales y las alianzas con marcas, entre otras.

## Datos

| Fuente | Contenido | Período |
| --- | --- | --- |
| Archivos CSV | Ventas con información de productos, precios y medios de pago, por sucursal y ciudad | 10 años |

[cantidad de registros: 30,000, cantidad de sucursales: 6 y de productos: 40 ]

## Proceso

**1. Preparación de datos (ETL, Python y Power Query)**
- Importación de 1 archivo CSV
- Limpieza: Completitud de los datos, formatos de fechas entre otros
- Modelado relacional: Productos, Clientes, Sucursales, Facturas, Detalle de Facturas, Ciudades, Vendedores, Marcas y Método de Pago

**2. Análisis exploratorio (Python)**
- Análisis de ventas por sucursal, producto, marca y medio de pago con Pandas, Matplotlib y Seaborn
- Definición de indicadores clave (KPI)

**3. Dashboard (Power BI)**
- Tarjetas de KPI y vistas comparativas por sucursal, marca, producto y medio de pago
- Medidas en DAX: [COMPLETAR: 2 o 3 medidas principales, por ejemplo ventas totales, participación %, ranking]

## Hallazgos y recomendaciones

| Hallazgo | Recomendación |
| --- | --- |
| **Medellín lidera las ventas**: concentra el 44,45% del total y se mantiene estable a lo largo de los años | Consolidar y proteger la sucursal líder |
| **Pereira (12,4%) y Cali (12,35%)** generan bajas ganancias con poco porcentaje de participación en las ventas, no lograron una posición fuerte en los últimos 10 años | Realizar un estudio de mercado en la zona antes de decidir sobre su continuidad |
| **Las tarjetas de crédito y débito** son los medios de pago más usados; el efectivo es el menos usado | Lanzar campañas promocionales para reducir aún más el uso de efectivo |
| **Los productos del puesto 35 al 40** son los de menor venta | Discontinuarlos y sumar productos similares a los 5 más vendidos |

## Capturas del informe

**Medellín, líder en ventas**

![Líder en ventas](images/01-lider-ventas.png)

**Participación y evolución de las ventas (44,45% del total, estable en el tiempo)**

![Evolución de ventas](images/02-evolucion-ventas.png)

**Pereira y Cali: sucursales de baja rentabilidad**

![Pereira](images/03-pereira.png)
![Cali](images/04-cali.png)

**Comparación de ventas por marca**

![Ventas por marca](images/05-marcas.png)

**Medios de pago**

![Medios de pago](images/06-medios-de-pago.png)

**Ranking de productos**

![Ranking de productos](images/07-ranking-productos.png)

## Estructura del repositorio

```text
management-report/
├── README.md
├── data/            # datos de muestra o descripción de las columnas
├── notebooks/       # limpieza y análisis exploratorio (Python)
├── powerbi/         # archivo .pbix del informe
└── images/          # capturas del dashboard
```

## Herramientas

- **Lenguaje:** Python
- **Análisis y visualización:** Pandas, Matplotlib, Seaborn
- **Business Intelligence:** Power BI, Power Query, DAX Studio

## Autora

**Lic. Inf. Jessica Torres Molina** · Consultora de datos · Power BI, SQL y Python
[LinkedIn](https://www.linkedin.com/in/jessicatorresmolina/) · [GitHub](https://github.com/jesitm)
