# Estrategia Quant: Acumulación Basada en VIX y EWO vs Buy & Hold

Este proyecto implementa una estrategia de *trading cuantitativo* en **Python puro**, sin librerías externas para gráficos ni indicadores técnicos. Funciona directamente en **consola (modo texto)** y es compatible con **Windows**.

## 🧠 Objetivo

Evaluar si es más rentable **acumular acciones** bajo dos condiciones específicas en lugar de aplicar la estrategia pasiva de **Buy & Hold semanal**.

### Las condiciones de compra son:

1. **VIX en zona de sobreventa** (color verde en TradingView).
2. **EWO negativo** (color rojo, indica tendencia bajista).

Cuando ambas condiciones se cumplen en el cierre de un día, se simula una compra. Se comparan los resultados con Buy & Hold.

## 📊 Indicadores usados

### VIX – Índice de Volatilidad
- Se interpreta como señal de compra cuando está en zona de sobreventa.
- Se convierte desde `vix.pine.txt` a `vix.py`.

### EWO – Elliott Wave Oscillator
- Diferencia entre EMA(5) y EMA(35).
- Si el valor es negativo, hay tendencia bajista.
- Se convierte desde `ewo.pine.txt` a `ewo.py`.

Ambos indicadores se reescriben manualmente en Python sin librerías externas.

## ⚙️ Requisitos

- Python 3.10 o superior
- Librerías estándar:
  - `datetime`
  - `csv`
  - `yfinance` (para obtener datos diarios)

Instalación de dependencias:

```bash
pip install yfinance
