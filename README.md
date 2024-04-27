# Seguimiento_2_FCI2024
Entrega del seguimiento 2, fisica computacional

Desarrollado por: 
Mario José Félix Rojas - Sebastian Gaviria
1. Plantemiento del problema:
Se tienen dos especies, una de tipo A y otra de tipo B, dentro de las cuales podemos tener funciones de asignación:
$X_{ij} \in {0,1,2}$
Con las siguientes condiciones de supervivencia, muerte y nacimiento:

    * Supervivencia:
        $X_{ij} == 1,2$ y $2<= N_v^{A,B}<=3 y $N_v^{B,A} \leq 2$, entonces $X_{ij} = 1,2$
    * Muerte: 
        $X_{ij} == 1,2$ y $N_v^{A,B} >3$ o $N_v^{A,B} <2$ o $N_v^{B,A}>2$, entonces $X_{ij}=0$
    * Nacimiento:
        $X_{ij}==0 y $N_v^{A,B}==3$ y $N_v^{B,A}<=2$, entonces $X_{ij}=1,2$
2. Modificación del problema:

    * Implementación del juego de la vida con dos especies 
    * Modificar una de las reglas:
        - Condición de nacimiento: Se puede cambiar los números requeridos para que una célula muerta nazca como cécula tipo A o B.
        - Condición de muerte: se puede decidir incrementar la competencia; cambiar la condición de que si una célula tiene pocos vecinos de otro tipo de célula entonces muere. Ejemplo, si una célula tipo A tiene solo un vecino tipo B, muere.
        - COndición adicional de competencia: se puede incluir una condición adicional en la que una célula se alimente de otra para incluir una dinámica de cazador-presa. Por ejemplo, si una célula tipo A está rodeada por dos células B esta cambia a ser célula de tipo B. Sería similar a considerar que las células B fagocitaron la célula A y se produjeron una nueva célula B en su lugar.
