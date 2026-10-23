
# 🚌 Sistema de Control de Gestión y Reportería de Taller de Buses (3-Way Match)

![Excel](https://img.shields.io/badge/Excel-Advanced-green?style=flat&logo=microsoft-excel)
![Data Analysis](https://img.shields.io/badge/Role-Data%20Analyst%20%7C%20Control%20de%20Gesti%C3%B3n-blue)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Contexto del Proyecto
Este prototipo de portafolio aborda la problemática real de control operativo y financiero de una **PYME subcontratista** dedicada a la mantención y reparación de buses, la cual presta servicios a una empresa de transporte de mayor escala (**la Mandante**).

### 🚨 Problemática de Negocio Detectada
La PYME presentaba severos problemas de cuadratura financiera y trazabilidad entre los documentos del ciclo comercial:
1. **Descalce entre Presupuestos y Órdenes de Compra (OC):** Trabajos ejecutados con presupuestos aprobados que no contaban con la OC respaldatoria emitida por la mandante.
2. **Brechas de Facturación:** Órdenes de compra recibidas con montos distintos a los cotizados inicialmente por los mecánicos.
3. **Falta de visibilidad por técnico/vendedor:** Dificultad para determinar qué mecánico o responsable generaba las desviaciones en los presupuestos.

---

## 💡 Solución Desarrollada (`Control_Taller_Buses_V8.xlsx`)
Se diseñó un modelo analítico integral en Microsoft Excel (sin uso de macros/VBA, priorizando tablas estructuradas y fórmulas dinámicas avanzadas) enfocado en la **auditoría de triangulación (3-Way Match)**:

$$\text{Presupuesto Aprobado} \iff \text{Orden de Compra (OC)} \iff \text{Factura Emitida}$$

### 🎯 Módulos Destacados del Sistema

1. **Dashboard de Cuadre Mandante (`Control_Mandante`):**
   * Matriz de trazabilidad 1 a 1 entre `ID Presupuesto` $\rightarrow$ `ID OC` $\rightarrow$ `ID Factura`.
   * Evaluador automático de triangulación con clasificación de estados (`CUADRADO (3-WAY OK)`, `DESCUADRE DE MONTOS`, `Falta OC Mandante`).
   * Filtros interactivos por **Mes**, **Cliente**, **Estado de Cuadre** y **Mecánico Responsable**.

2. **Dashboard de Productividad de Mecánicos (`Dashboard_Mecanicos`):**
   * Evaluación de rendimiento individual para los 8 técnicos/vendedores del taller (incluyendo a *Andrea Salinas*).
   * Matriz comparativa de OTs ejecutadas por especialidad (Preventivo, Correctivo, Siniestro).
   * Tarjetas ejecutivas con métricas dobles: **Mecánico más productivo** (con total de OTs), **Mayor Facturación** (monto en CLP) y **Mayor Margen Generado** (monto en CLP y % de participación sobre el taller).

3. **Dashboard Visual y Tendencias (`Dashboard_Graficos`):**
   * Gráfico de barras verticales con la **Evolución de Facturación Mensual ($)**.
   * Gráfico de torta/anillo con la **Participación Porcentual en la Facturación por Técnico**.

4. **Auditoría Económica y Control de Calidad de Datos:**
   * Eliminación de ceros ficticios en repuestos y mano de obra sin precio registrado (`Alerta_Dato`).
   * Distinción estricta entre *Margen Confirmado* y *Pendiente de Validación*.

---

## 🛠️ Herramientas y Funciones de Excel Utilizadas
* **Funciones Lógicas y de Búsqueda:** `SUMIFS`, `COUNTIFS`, `AVERAGEIFS`, `INDEX` + `MATCH`, `RANK`, `IF` + `AND` + `OR`.
* **Estructura de Datos:** Tablas Estructuradas (`T_OrdenesTrabajo`, `T_DetalleOT`, `T_RendimientoMecanicos`), Listas Desplegables con Validación de Datos, Rangos Dinámicos.
* **Modelamiento:** Control de fechas (`WEEKNUM`, `YEAR`, `MONTH`), reglas de negocio de cobranza y vencimiento.

---

## 📂 Descarga e Instrucciones de Uso
1. Descarga el libro en Excel: [`Control_Taller_Buses_V8.xlsx`](./Control_Taller_Buses_V8.xlsx).
2. Abre el archivo en Excel (compatibilidad total para Office 2016+ / Microsoft 365).
3. Navega a la pestaña **`Control_Mandante`** e interactúa con las celdas amarillas superiores para filtrar la información.

---

**Autor:** Ramón Muñoz  
**Rol:** Analista de Datos / Especialista en Control de Gestión  
**Contacto / LinkedIn:** [Enlace a tu LinkedIn]
