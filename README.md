# Seguimiento_2_FCI2024
Entrega del seguimiento 2, fisica computacional

Desarrollado por: 
Mario José Félix Rojas - Sebastian Gaviria- Jose Luis Torres
1. Plantemiento del problema:
Se tienen dos especies, una de tipo A y otra de tipo B, dentro de las cuales podemos tener funciones de asignación:
$X_{ij} \in {0,1,2}$
Con las siguientes condiciones de supervivencia, muerte y nacimiento:

    * Supervivencia:
        $X_{ij} == 1,2$ y $2<= N_v^{A,B}<=3$ y $N_v^{B,A} \leq 2$, entonces $X_{ij} = 1,2$
    * Muerte: 
        $X_{ij} == 1,2$ y $N_v^{A,B} >3$ o $N_v^{A,B} <2$ o $N_v^{B,A}>2$, entonces $X_{ij}=0$
    * Nacimiento:
        $X_{ij}==0$ y $N_v^{A,B}==3$ y $N_v^{B,A}<=2$, entonces $X_{ij}=1,2$
2. Modificación del problema:

    * Implementación del juego de la vida con dos especies 
    * Modificar una de las reglas:
        - Condición de nacimiento: Se puede cambiar los números requeridos para que una célula muerta nazca como cécula tipo A o B.
        - Condición de muerte: se puede decidir incrementar la competencia; cambiar la condición de que si una célula tiene pocos vecinos de otro tipo de célula entonces muere. Ejemplo, si una célula tipo A tiene solo un vecino tipo B, muere.
        - COndición adicional de competencia: se puede incluir una condición adicional en la que una célula se alimente de otra para incluir una dinámica de cazador-presa. Por ejemplo, si una célula tipo A está rodeada por dos células B esta cambia a ser célula de tipo B. Sería similar a considerar que las células B fagocitaron la célula A y se produjeron una nueva célula B en su lugar.

## Entregables:

1. Obtener las distribuciones (histogramas normalizados a la unidad) del número de células A y B para todo el histórico de 1000 iteraciones. 

2. Considere el sistema como descrito por el estado $N_A$ y $N_B$, donde $N_A$ es el número de células tipo A y $N_B$ es el número de células tipo B. Si llamamos a $N_T$ el número total de casillas del tablero del juego, tenga en cuenta que $N_A+N_B<=N_T$. De la misma forma el número de células muertas es $N_T-N_A-N_B$. Además, tenga presente que como las dos especies de células interactúan es previsible que la probabilidad de encontrar un número de células A no sea independiente de encontrar un número de células B, en otras palabras $N_A$ y $N_B$ están correlacionados, y, por lo tanto, lo mejor es utilizar la probabilidad 2-dimensional como distribución de probabilidad de los estados del sistema y no las probabilidades marginales de cada variable separadamente.

3. Utilizando las distribuciones obtenidas en el punto 1 y teniendo en cuenta lo señalado en el punto 4, utilice el algoritmo de Metrópolis para generar una serie de estados del sistema

4. Grafique la probabilidad 2-dimensional de los estados generados con el algoritmo de Metrópolis y muestre cualitativamente que la distribución obtenida es similar a la del punto 1.

Entregas:
1. El código desarrollado.
2. Los gráficos pedidos.
