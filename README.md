# Tarea 2. Modelos de probabilidad discretos y contínuos.

## Matemáticas para Ciencia de Datos (2026-2)

**Integrantes:**
- Carlos Iván Sotomayor Samaniego
- Horacio Araiza Gonzáles

## Descripción

Proyecto académico dedicado a la resolución de problemas de probabilidad mediante procedimientos matemáticos y su implementación en Python con Jupyter Notebook. La libreta desarrolla los primeros nueve ejercicios de la Tarea 2, utilizando las distribuciones binomial y de Poisson.

## Objetivos

- Identificar la distribución de probabilidad adecuada para cada problema.
- Definir las variables aleatorias y sus parámetros.
- Calcular probabilidades puntuales, acumuladas y complementarias.
- Implementar las fórmulas matemáticas en Python y presentar los resultados en formato decimal y porcentual.

## Contenido

| Ejercicio | Problema | Distribución |
|---|---|---|
| 1 | Selección de trabajadoras de una empresa | Binomial |
| 2 | Juguetes defectuosos en un lote | Binomial |
| 3 | Reacciones negativas en pruebas médicas | Binomial |
| 4 | Demanda del servicio de urgencias de un hospital | Poisson |
| 5 | Efectividad de un detergente | Binomial |
| 6 | Errores en declaraciones fiscales del SAT | Binomial |
| 7 | Fallos de componentes electrónicos | Poisson |
| 8 | Llegada de mensajes a un servidor | Poisson |
| 9 | Pañuelos defectuosos en una caja | Binomial |

En el ejercicio 6 se interpreta la variable aleatoria como el número de declaraciones con errores dentro de un grupo fijo de diez declaraciones, debido a la ambigüedad del enunciado original.

## Fundamento matemático

### Distribución binomial

Modela el número de éxitos en un conjunto de ensayos independientes con una probabilidad de éxito constante.

$$P(X=x)=\binom{n}{x}p^x(1-p)^{n-x}$$

Donde $n$ es el número de ensayos, $p$ es la probabilidad de éxito y $x$ es el número de éxitos.

### Distribución de Poisson

Modela el número de eventos que ocurren en un intervalo determinado, suponiendo una tasa constante e independencia de los eventos en intervalos disjuntos.

$$P(X=x)=\frac{e^{-\lambda}\lambda^x}{x!}$$

Donde $\lambda$ es el número promedio de eventos en el intervalo y $x$ es el número de eventos observados.

Para calcular probabilidades acumuladas se suman las probabilidades individuales. También se utiliza la regla del complemento cuando simplifica el cálculo.

## Estructura del proyecto

```text
.
├── README.md
└── Tarea_2_Modelos_de_probabilidad.ipynb
```

## Tecnologías y requisitos

- Python 3.8 o superior.
- Jupyter Notebook, JupyterLab o Google Colab.
- Módulo estándar `math` (`comb`, `exp` y `factorial`).
- Markdown y LaTeX para documentar los procedimientos matemáticos.

No se requieren bibliotecas externas para realizar los cálculos.

## Instalación y ejecución

Para ejecutar la libreta localmente, instalar Jupyter Notebook si aún no está disponible:

```bash
python -m pip install notebook
```

Desde el directorio del proyecto, ejecutar:

```bash
jupyter notebook Tarea_2_Modelos_de_probabilidad.ipynb
```

Ejecutar todas las celdas en orden desde el menú de Jupyter. La primera celda de código define las funciones reutilizadas en los ejercicios. También es posible abrir el archivo `.ipynb` directamente en Google Colab o Visual Studio Code con soporte para Jupyter.

## Implementación

La libreta incluye tres funciones auxiliares:

| Función | Descripción |
|---|---|
| `binomial(n, p, x)` | Calcula la probabilidad binomial puntual. |
| `poisson(lam, x)` | Calcula la probabilidad de Poisson puntual. |
| `mostrar(prob)` | Imprime la probabilidad decimal y porcentual. |

Cada ejercicio contiene el planteamiento, la identificación de la distribución, los parámetros, las fórmulas, el desarrollo matemático y una celda de código para obtener el resultado numérico.

## Alcance

La tarea original comprende 20 ejercicios. Esta versión del proyecto resuelve únicamente los ejercicios 1 al 9; los restantes no están implementados en la libreta.

## Conclusión

El proyecto permite aplicar los modelos binomial y de Poisson a situaciones concretas y relacionar el desarrollo matemático con el cálculo computacional reproducible mediante Python.
