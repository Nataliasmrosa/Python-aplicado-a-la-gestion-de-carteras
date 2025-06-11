# Python aplicado a la gestión de carteras
Microcredencial universitaria de Python aplicado a la gestión de carteras, impartida por la Universidad Autónoma de Madrid.



Repositorio con el trabajo final del curso **Python Aplicado a la Gestión de Carteras**, enfocado en el diseño de estrategias de inversión adaptadas al nuevo escenario económico global ante un posible segundo mandato de Donald Trump.

## Objetivo

Desarrollar una cartera de inversión con fundamentos cuantitativos que responda a cambios macroeconómicos vinculados al regreso de Trump, combinando:

- Análisis de factores de riesgo (modelo de Fama-French)
- Simulaciones Monte Carlo
- Backtesting histórico
- Análisis cualitativo del contexto político-económico

## Metodología y Desarrollo

### 1. Selección y Ponderación de Activos

Se optó por invertir en fondos en lugar de activos individuales, debido a su diversificación automática, gestión profesional y simplicidad operativa. Para la selección se aplicaron criterios de exposición a factores de mercado y baja correlación histórica (≤ 0.6).

**Criterios de selección:**
- Exposición a sectores potencialmente beneficiados por políticas trumpistas (energía, defensa)
- ETFs con baja correlación entre sí
- Inclusión de activos refugio (oro, deuda a corto plazo)

Las ponderaciones se asignaron de forma equiponderada, considerando esta estrategia como la más eficiente para la construcción inicial de la cartera.

### 2. Diseño de la Cartera

Se utilizaron datos de precios diarios desde enero de 2020 hasta abril de 2025. Para reducir el ruido de corto plazo, se tomaron precios semanales cada miércoles, evitando efectos de inicio o cierre de semana.

**Factores de mercado incluidos (modelo Fama-French):**
- **Mkt-RF:** Exceso de rentabilidad del mercado
- **SMB:** Prima por tamaño (small minus big)
- **HML:** Prima por valor (high minus low)
- **RF:** Tasa libre de riesgo

### 3. Backtesting Histórico

Se evaluó el desempeño de la cartera en distintos entornos de mercado:

| Escenario        | Período           | Rentabilidad | Volatilidad |
|------------------|-------------------|--------------|-------------|
| Bull Market      | 2023-01 a 2024-12 | +18.7%       | 12.4%       |
| Bear Market      | 2020-03 a 2020-12 | -5.2%        | 24.1%       |
| Escenario Trump 1| 2025-01 a 2025-06 | +9.4%        | 15.8%       |

### 4. Gestión de Riesgos

Se implementó una simulación de Monte Carlo con 100,000 iteraciones para modelar posibles escenarios futuros. Además, se calcularon las siguientes métricas:

- **VaR mensual al 95%:** -7.4%
- **CVaR mensual al 95%:** -9.1%
