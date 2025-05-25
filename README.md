# Proyecto de Optimización de Cobranza Domiciliada para Credifiel

# 🧾 Análisis y Optimización de Estrategias de Cobranza Domiciliada

## 📌 Objetivo General

Diseñar una estrategia de cobranza inteligente que:

- *Clasifique a los clientes* por su comportamiento de pago.
- *Ajuste automáticamente la estrategia de cobro* (emisora, canal, horario) según el perfil.
- *Optimice el beneficio esperado*, reduciendo costos en buenos pagadores y priorizando rapidez en los malos.
- Visualice patrones entre *monto del pagare y capital* para entender si hay una relación con el cumplimiento.

## 📊 Análisis Inicial: Pagos por Crédito

- Se consolidó una base donde cada fila representa un intento de cobro.
- Se calculó el *porcentaje pagado* por crédito:

  # 🧠 Resumen del Modelo de Clasificación y Optimización de Cobranza

Desarrollamos un modelo que clasifica a los clientes según su historial de pago y asigna automáticamente la estrategia de cobranza más eficiente. El objetivo es minimizar los costos por comisiones bancarias y el tiempo de respuesta de cada intento, ya que la empresa paga comisión incluso si el cobro falla.

## 🧩 Clasificación de Clientes

- *Confiable*: 0 fallos → estrategia gratis, lenta (6 días)
- *Tentativo*: 1 fallo → estrategia rápida, cara
- *Desconfiable*: 2 fallos → estrategia intermedia
- *Stand-by*: 3 o más fallos → no se cobra (a menos que haya intervención manual)

## ⚙️ Optimización Matemática (ILP)

Se utilizó un modelo de Programación Lineal Entera para seleccionar la estrategia de menor costo y tiempo permitida por cliente, según su categoría.

- *Función objetivo*: minimizar (costo + λ * tiempo)
- *Restricciones*: una sola estrategia válida por cliente

## ✅ Resultado

- Reducción de costos por cobros fallidos
- Clasificación automática y trazable
- Asignación óptima de emisoras bancarias según el riesgo
