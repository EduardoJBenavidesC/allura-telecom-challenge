# allura-telecom-challenge
Proyecto para especialización en Data Science

Ecosistema Digital B2B: Optimización de ROAS y Eficiencia de Ventas.

1. Propósito del Proyecto

   Este proyecto despliega una solución de Data Science orientada a la transformación de centros de costos en centros de beneficios mediante el análisis 
   avanzado de fuga de clientes (Churn). A través de una capa de Master Data Management (MDM), el sistema identifica patrones críticos de abandono para 
   optimizar el Retorno de la Inversión Publicitaria (ROAS) y mejorar la Sales Efficiency, permitiendo que los equipos comerciales se enfoquen en leads
   de alta rentabilidad.

2. Estructura del MDM (Dominios de Datos).
   
   El pipeline procesa una arquitectura de datos jerárquica (JSON) normalizada en tres dimensiones estratégicas:
   
   Customer Domain: Atributos demográficos y perfiles de usuario.
   Account & Financial Domain: Gestión de contratos, métodos de facturación y métricas de cargo (Charges_Monthly, Contract).
   Services Domain: Portafolio técnico que incluye conectividad, seguridad y servicios de valor agregado.

4. Instalación y Dependencias
   Para asegurar la correcta ejecución del análisis y la visualización de los modelos de propensión, se requiere el siguiente entorno:

   Pandas: Motor principal para la normalización de JSON anidado y manipulación de DataFrames.
   NumPy: Gestión de lógica computacional y tratamiento de nulos financieros.
   Matplotlib: Infraestructura base para la generación de gráficos ejecutivos.
   Seaborn: Visualización estadística avanzada para mapas de calor y densidades KDE.

5. Metodología Analítica (Pipeline de Trabajo).
   
   El notebook sigue una línea analítica rigurosa dividida en:

   Ingesta Progresiva: Carga y json_normalize de estructuras complejas con separadores de jerarquía (_).
   Auditoría de Integridad: Verificación de unicidad de customerID y saneamiento de registros con latencia (tenure 0).
   Saneamiento de Datos: Imputación lógica de cargos basada en el ciclo de vida del cliente.
   Optimización Estructural: Implementación de tipos category para maximizar la velocidad de procesamiento.
   Análisis de Propensión (EDA): Evaluación bivariada y de densidad para identificar umbrales críticos de fuga.
   Determinación de Drivers: Cálculo de correlación de Pearson para aislar variables de riesgo y retención.

6. Hallazgos Estratégicos para la Toma de Decisiones.
   
  Segmento de Riesgo Crítico: El contrato mes a mes (account_Contract_Month-to-month) es el principal predictor de fuga.
  Impacto de Servicios: La fibra óptica, a pesar de su alto valor, presenta correlación positiva con el abandono si no está asociada a contratos de l/p.
  Palancas de Retención: Los contratos de 1 y 2 años actúan como estabilizadores del ecosistema, reduciendo drásticamente la tasa de Churn.

7. Soluciones y Escalabilidad.
   
  Blindaje Técnico: Protocolo de certificación del Target que valida la pureza de los datos antes del modelado.
  Integración CRM: Nomenclatura estandarizada por prefijos para una sincronización fluida con sistemas de ventas y CRM.

**Notas del Desarrollador**

  Este proyecto ha sido diseñado bajo estándares profesionales de consultoría, priorizando la interpretación de datos para la generación de valor financiero y 
  eliminando el ruido técnico.
