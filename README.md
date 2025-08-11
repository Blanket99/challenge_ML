# Análisis Predictivo de Churn - TelecomX LATAM

## Resumen

Este proyecto presenta un análisis completo de churn prediction para TelecomX LATAM, implementando técnicas avanzadas de Machine Learning para identificar clientes en riesgo, cuantificar factores de deserción y desarrollar estrategias de retención basadas en datos. 

Resultados: Identificación de factores críticos que permiten reducir el churn del 26.6% actual al 19-22% mediante estrategias dirigidas con un ROI del 315%

## Objetivos del Proyecto

- Análisis Predictivo: Desarrollar modelos ML para predecir churn con 81.6% de precisión
- Identificación de Factores: Cuantificar variables que más influyen en la deserción
- Estrategias de Retención: Generar recomendaciones actionables por segmento de riesgo
- Informe: Crear dashboard completo para stakeholders y C-level
- Implementación: Roadmap de 12 meses con métricas de seguimiento

## Estructura del Proyecto

```
challenge_ML/
├── TelecomX_LATAM.ipynb                # Pipeline ML completo (4 algoritmos)
├── Informe_Churn_TelecomX.ipynb        # Informe con estrategias
├── TelecomX_Limpio.csv                 # Dataset limpio y procesado
└── README.md                          
```

## Metodología y Pipeline

### 1. Extracción y Preparación de Datos (ETL)
- Fuente: Dataset TelecomX con 7,032 clientes y 22 variables
- Formato: JSON → CSV procesado con limpieza completa
- Variables: Demográficas, servicios, facturación, comportamiento

### 2. Limpieza y Transformación Avanzada
- Estandarización: Normalización de strings y formatos
- Ingeniería de Features: Creación de variables derivadas (tenure_group, charges_group)
- Encoding: One-hot encoding para variables categóricas
- Balanceo: Implementación de SMOTE para clases desbalanceadas

### 3. Modelado de Machine Learning
- Algoritmos evaluados: Random Forest, Logistic Regression, KNN, Decision Tree
- Métrica principal: F1-Score (balanceando precision y recall)
- Mejor modelo: Random Forest con 81.6% accuracy y 70.3% F1-Score
- Validación: Cross-validation y métricas múltiples

### 4. Análisis de Factores y Correlaciones
- Análisis de correlación: Identificación de variables más influyentes
- Segmentación por riesgo: Alto, Medio, Bajo riesgo basado en factores clave
- Feature importance: Cuantificación de impacto de cada variable

### 5. Desarrollo de Estrategias de Negocio
- Segmentación estratégica: Programas diferenciados por perfil de riesgo
- ROI analysis: Cálculo de retorno de inversión por estrategia
- Timeline de implementación: Roadmap de 12 meses con fases

## Hallazgos Principales (Datos Reales)

### Tasa General de Churn
- Tasa actual: 26.6% de los clientes abandonan el servicio
- Distribución: 1,873 clientes con churn de 7,032 total
- Impacto financiero: Pérdida significativa que justifica inversión en retención

### TOP 4 Factores Más Influyentes (Análisis de Correlación)
1. Tenure (Permanencia): 0.354 correlación - Factor #1
   - Clientes 0-12 meses: 47.7% churn (CRÍTICO)
   - Clientes 36+ meses: 11.9% churn
   
2. Charges.Total: 0.199 correlación
   - Mayor inversión total → menor probabilidad de churn
   
3. Cuentas_Diarias: 0.193 correlación
   - Patrón de uso frecuente reduce deserción
   
4. Charges.Monthly: 0.193 correlación
   - Cargos medio-alto: 36.8% churn (mayor riesgo)

### Contratos: Factor Decisivo
- Month-to-month: 42.7% churn (3x mayor riesgo)
- One year: 11.3% churn
- Two year: 2.8% churn (mayor retención)

### Métodos de Pago: Impacto Crítico
- Electronic check: 45.3% churn (mayor riesgo)
- Credit card (automatic): 15.3% churn
- Bank transfer (automatic): 16.7% churn
- Insight: Automatización reduce churn en 66%

### Rendimiento del Modelo ML
- Mejor algoritmo: Random Forest
- Accuracy: 81.6%
- F1-Score: 70.3%
- Capacidad predictiva: Identifica 70%+ clientes en riesgo

## Estrategias de Retención (Data-Driven)

### ALTO RIESGO: Clientes Nuevos (0-12 meses) - 47.7% churn
Estrategias:
1. Programa de Bienvenida Extendido (ROI: 320%)
   - Seguimiento personalizado primeros 6 meses
   - Soporte técnico prioritario
   - Verificación de satisfacción 30/60/90 días

2. Incentivos de Permanencia
   - Descuentos progresivos por contratos largos
   - Migración asistida de month-to-month a anual
   - Bonificaciones por débito automático

### RIESGO MEDIO: Cargos Elevados - 36.8% churn
Estrategias:
1. Programa VIP (ROI: 280%)
   - Gestor de cuenta dedicado
   - Reportes de valor personalizado
   - Servicios premium incluidos

2. Justificación de Valor
   - Dashboard de beneficios utilizados
   - Comparativas con competencia
   - Flexibilidad de downgrade temporal

### BAJO RIESGO: Contratos Largos - 2.8% churn
Estrategias:
1. Programa de Lealtad (ROI: 250%)
   - Recompensas por permanencia
   - Early access nuevos servicios
   - Cross-selling inteligente

### Impacto Proyectado
- Reducción de churn: 15-25% (objetivo: 19.9-22.6%)
- ROI promedio: 315%
- Timeline: 12 meses de implementación
- Beneficio anual: $2.5M - $4.2M

## Plan de Implementación (12 meses)

### FASE 1: Implementación Inmediata (0-3 meses)
- Sistema de alertas tempranas ML
- Programa bienvenida para clientes nuevos
- Campaña migración a débito automático
- Objetivo: 5% reducción churn

### FASE 2: Programas Diferenciados (3-6 meses)
- Programa VIP para alto valor
- Personalización de ofertas
- Optimización onboarding fibra óptica
- Objetivo: 15% reducción churn acumulada

### FASE 3: Optimización Continua (6-12 meses)
- Automatización ML en producción
- A/B testing de estrategias
- Refinamiento de modelos
- Objetivo: 25% reducción churn total

### FASE 4: Mejora Continua (12+ meses)
- Expansión a otros productos
- Optimización basada en resultados
- Objetivo: 35% reducción churn sostenida

## Métricas de Éxito y KPIs

### KPIs Primarios
- Churn Rate: Reducción del 26.6% → 19.9-22.6% (meta: -20%)
- Customer Lifetime Value: Incremento del 20-30%
- Net Promoter Score: Mejora de 15+ puntos
- Early Detection: Identificar 70%+ clientes en riesgo antes de churning

### KPIs Secundarios
- Contratos Largos: Incremento del 35% en adopción
- Débito Automático: Incremento del 50% en adopción
- Time to Value: Reducción del 40% en onboarding
- Support CSAT: Mejora del 25% en satisfacción

### Métricas de Negocio
- ROI de Retención: 315% promedio
- Revenue Impact: $2.5M - $4.2M anual
- Cost per Retention: <30% del CLV del cliente

## Stack Tecnológico

### Análisis y Machine Learning
- Python 3.8+: Lenguaje principal
- Pandas: Manipulación y análisis de datos
- Scikit-learn: Modelos ML (Random Forest, Logistic Regression, KNN, Decision Tree)
- NumPy: Computación numérica optimizada
- Imbalanced-learn (SMOTE): Balanceo de clases

### Visualización y Reporting
- Matplotlib: Gráficos base y personalización
- Seaborn: Visualizaciones estadísticas elegantes
- Jupyter Notebooks: Ambiente de desarrollo interactivo
- Plotly (opcional): Dashboards interactivos

### Datos y Procesamiento
- JSON/CSV: Formatos de entrada
- Pandas: ETL y feature engineering
- One-hot encoding: Variables categóricas
- Feature scaling: Normalización para ML

## Entregables del Proyecto

### 1. TelecomX_LATAM.ipynb
Pipeline completo de Machine Learning
- Análisis exploratorio de datos
- Preprocesamiento y feature engineering
- Entrenamiento y evaluación de 4 modelos ML
- Análisis de importancia de características
- Métricas de rendimiento detalladas

### 2. Informe_Churn_TelecomX.ipynb
Informe ejecutivo para stakeholders
- Contexto de negocio y problemática
- Factores críticos con visualizaciones
- Estrategias de retención por segmento
- Dashboard ejecutivo con ROI
- Plan de implementación de 12 meses
- Conclusiones y próximos pasos

### 3. Documentación Técnica
- TelecomX_diccionario.md: Descripción de variables
- TelecomX_Limpio.csv: Dataset procesado listo para análisis
- README.md: Documentación completa del proyecto

## Cómo Ejecutar el Proyecto

### Prerrequisitos
```bash
pip install pandas numpy scikit-learn matplotlib seaborn imbalanced-learn jupyter
```

### Ejecución
1. Pipeline ML: Abrir `TelecomX_LATAM.ipynb` y ejecutar todas las celdas
2. Informe Ejecutivo: Abrir `Informe_Churn_TelecomX.ipynb` para ver análisis completo
3. Exploración Inicial: `analisis.ipynb` para análisis exploratorio

### Outputs Esperados
- 6+ visualizaciones con insights de negocio
- Modelo Random Forest entrenado con 81.6% accuracy
- Ranking de factores más influyentes en churn
- Estrategias de retención con ROI calculado
- Dashboard ejecutivo con métricas clave

---
