# Algoritmos Genéticos y Técnicas de Aprendizaje Automático para el Entrenamiento de Agentes Inteligentes en Videojuegos Arcade

**Autores:** Bartolucci Gino, Joaquín Bates, Francisco Mendiburu

**Institución:** Universidad Tecnológica Nacional Facultad Regional Rosario, Algoritmos Genéticos

## Resumen

Este trabajo se origina en la intersección de dos campos científicos altamente relevantes en la actualidad: el aprendizaje automático y los algoritmos genéticos. El presente estudio se centra en el juego arcade "Breakout", donde los agentes controlan una paleta para lograr rebotar una pelota y eliminar una pared compuesta de bloques dispuestos en la parte superior de la pantalla. Aunque este juego puede parecer simple, presenta un entorno interactivo y dinámico con desafíos significativos debido a su naturaleza impredecible y rápida. El objetivo principal de este trabajo es investigar cómo la combinación de algoritmos genéticos y técnicas de aprendizaje automático, específicamente NeuroEvolution of Augmenting Topologies (NEAT), puede llevar a la creación de agentes que superen el rendimiento humano en el juego.

## Palabras Clave

Algoritmos genéticos, crossover, redes neuronales, topologías, deep learning.

## Introducción

El problema a resolver radica en desarrollar estrategias automatizadas que permitan a los agentes aprender y adaptarse en tiempo real para maximizar su puntuación en el juego Breakout. Esto implica la identificación de funciones de aptitud adecuadas, la representación eficiente del espacio de búsqueda y la adaptación de operadores genéticos para mantener la diversidad de soluciones. Además, se explorará cómo las redes neuronales, optimizadas mediante NEAT, pueden mejorar la toma de decisiones de los agentes en un entorno de juego interactivo y desafiante.

## Marco Teórico

### Introducción al Aprendizaje Automático y Algoritmos Genéticos

El aprendizaje automático, definido como una rama de la inteligencia artificial, permite a los sistemas computacionales aprender patrones y tomar decisiones a partir de datos, mejorando su rendimiento con la experiencia. Los algoritmos genéticos, por otro lado, son una técnica de optimización inspirada en la evolución biológica, que utiliza operadores genéticos como selección, mutación y crossover para mejorar soluciones candidatas en un espacio de búsqueda.

### Redes Neuronales en el Contexto del Problema

Dentro del campo del aprendizaje automático, las redes neuronales han emergido como una herramienta poderosa para abordar problemas complejos y no lineales, como la toma de decisiones en videojuegos. En el contexto de la investigación sobre el entrenamiento de agentes inteligentes en videojuegos arcade, las redes neuronales ofrecen la capacidad de aprender representaciones y estrategias adaptativas directamente de los datos del juego. La evolución de la topología de las redes neuronales a través de algoritmos genéticos, como NEAT, permite la adaptación de la arquitectura y el rendimiento del agente a lo largo del tiempo, mejorando su capacidad para enfrentar los desafíos cambiantes del juego.

### Topología en una Red Neuronal

La topología en una red neuronal se refiere a la estructura y disposición de las neuronas y conexiones en capas dentro del modelo. Es la configuración espacial que determina cómo las neuronas están conectadas entre sí, influyendo en la capacidad de la red para aprender y generalizar patrones complejos. Una topología puede ser profunda, con varias capas interconectadas, o más superficial con menos capas, y puede incluir conexiones recurrentes o saltos directos entre capas.

## Elección de NEAT en el Proyecto

La elección de utilizar NEAT (NeuroEvolution of Augmenting Topologies) se fundamenta en su potencial para abordar problemas de optimización en entornos complejos y dinámicos como los videojuegos. La combinación de algoritmos genéticos y redes neuronales a través de NEAT permite la evolución de la topología, adaptación de la arquitectura y el rendimiento del agente a lo largo del proceso de evolución. Su adopción en el entrenamiento de agentes en videojuegos donde las estrategias pueden ser altamente variables presenta una oportunidad prometedora para resolver los desafíos de optimización y toma de decisiones.

## Enfoque del Proyecto

El enfoque se basa en la idea de que un agente aprende a tomar decisiones óptimas al interactuar con su entorno y recibir recompensas por sus acciones. En el contexto de los videojuegos, los agentes aprenden a través de ensayo y error, ajustando sus acciones para maximizar las recompensas acumuladas a lo largo del tiempo. A medida que los agentes exploran y toman decisiones, ajustan sus políticas de acción para mejorar su desempeño en el juego.

NEAT permite la evolución de estrategias de juego a través de la adaptación tanto de la topología como de los pesos de las redes neuronales que guían las acciones del agente. Esto proporciona una solución eficaz para entrenar agentes capaces de anticipar la trayectoria de la pelota, optimizar la posición de la paleta y lograr puntuaciones sobresalientes. La aplicación de algoritmos genéticos y redes neuronales mediante NEAT en el juego Breakout puede llevar a la generación de agentes altamente competentes, capaces de superar el rendimiento humano. Este enfoque ha explorado la adaptabilidad de las topologías neuronales y la optimización de políticas de acción.

## Concreción del Modelo

### Descripción de la Implementación Técnica

El stack tecnológico seleccionado comprende Python como lenguaje de programación principal, junto con la biblioteca NEAT para entrenar el modelo de IA y la biblioteca PYGAME para crear el entorno de juego Breakout. Python proporciona una plataforma versátil y dinámica para el desarrollo de IA, mientras que la biblioteca NEAT ofrece un marco robusto para evolucionar redes neuronales y optimizar su estructura. La biblioteca PYGAME, por su parte, nos permite crear una interfaz de juego para poder acceder de manera sencilla a la información del entorno esencial para probar nuestro modelo y validar el rendimiento del agente de IA.

### Entorno del Juego Breakout

El mismo consistirá en una paleta que deberá moverse en el eje x para hacer rebotar una pelota sobre sí y así destruir una serie de bloques ubicados en la parte superior de la pantalla. El objetivo del juego es eliminar la mayor cantidad de bloques posible sin dejar que la pelota toque el suelo. La paleta se puede controlar con una interfaz de entrada, como las teclas de flecha o una palanca de juego.

### Estructura General del Entrenamiento del Agente

El entrenamiento del agente se realiza mediante algoritmos genéticos y NEAT. Se genera una población inicial de 50 genes, cada uno representando una red neuronal con una topología única. Cada gen es un conjunto de información que describe la estructura y los pesos de la red neuronal. El juego se ejecuta para cada gen, y el rendimiento del agente se evalúa en términos de puntuación y habilidad para evitar que la pelota toque el suelo. Luego, se aplican operadores genéticos, como mutación y crossover, para generar una nueva generación de genes. Este proceso se repite durante múltiples generaciones hasta que los agentes logren un rendimiento satisfactorio en el juego.

### Estructura Común de las Redes Neuronales

Todas las redes neuronales en la población comparten una estructura común, que consta de una capa de entrada y una capa de salida. La capa de entrada recibe información crítica del juego, como la posición de la pelota, la posición de la paleta y la disposición de los bloques. La capa de salida toma decisiones en tiempo real, como la velocidad y la dirección de movimiento de la paleta. La adaptación de la topología y los pesos de las conexiones dentro de estas redes neuronales a lo largo del entrenamiento permite a los agentes aprender estrategias efectivas para jugar Breakout.

## Operadores Genéticos

Como parte del algoritmo NEAT, se implementan operadores genéticos que influyen en la evolución de los genes y las redes neuronales. Estos operadores incluyen mutación y crossover.

### Mutación

La mutación introduce variabilidad en las redes neuronales al realizar cambios aleatorios en la topología, como agregar o eliminar nodos y conexiones. La mutación es fundamental para explorar nuevas estrategias y evitar que el algoritmo quede atrapado en óptimos locales.

### Crossover

El crossover combina información genética de dos genes parentales para crear un nuevo gen hijo. Esto permite la transferencia de características exitosas de los padres a la siguiente generación. El crossover juega un papel importante en la explotación de soluciones prometedoras y la mejora del rendimiento de los agentes.

## Cálculo de la Aptitud del Agente

La aptitud de un agente se calcula en función de su desempeño en el juego Breakout. Las medidas de aptitud incluyen la puntuación obtenida durante una partida y la habilidad para evitar que la pelota toque el suelo. Un agente con una alta aptitud logra puntuaciones más altas y mantiene la pelota en juego durante más tiempo. Estas métricas objetivas proporcionan una forma cuantitativa de evaluar y comparar el rendimiento de los agentes en diferentes generaciones.

## Resultados y Rendimiento

A lo largo de las generaciones, se observa una mejora constante en el fitness de los agentes. Esto sugiere que los agentes aprenden a desempeñarse mejor a medida que avanzan en el proceso de entrenamiento. La adaptación de la topología y los pesos de las redes neuronales a través de NEAT permite a los agentes encontrar estrategias efectivas para jugar Breakout, lo que se refleja en un aumento en la puntuación y la capacidad de mantener la pelota en juego.

## Problemática: Impacto de la Variabilidad del Juego en el Desempeño de Agentes con Fitness Elevado

La variabilidad en el juego puede afectar a los agentes con un alto nivel de fitness. Esto plantea la pregunta de si el alto fitness se debe a la idoneidad particular de su proceso de entrenamiento o si los agentes son capaces de adaptarse a desafíos variables.

## Evaluación del Interrogante a través de Pruebas Iterativas

Se llevaron a cabo pruebas iterativas para determinar si el rendimiento de los agentes con alto fitness se mantenía en diferentes situaciones de juego. Estas pruebas consistieron en ajustar parámetros del juego, como la velocidad de la pelota o la disposición de los bloques, y evaluar si los agentes entrenados podían adaptarse con éxito a estas condiciones cambiantes.

## Resultados

Los resultados de las pruebas iterativas mostraron que el rendimiento de los agentes con alto fitness estaba relacionado con la cantidad de generaciones de entrenamiento más que con la idoneidad particular de las condiciones de entrenamiento originales. Los agentes que habían experimentado un mayor número de generaciones de entrenamiento tendían a adaptarse mejor a los cambios en el juego y mantenían un rendimiento sólido en diferentes situaciones.

## Conclusiones Preliminares

Los resultados subrayan la importancia de un entrenamiento extenso y diversificado en la formación de agentes inteligentes capaces de enfrentar desafíos variables en entornos de juego. La adaptabilidad de las redes neuronales entrenadas a través de NEAT permite a los agentes ajustar sus estrategias y políticas de acción para abordar desafíos cambiantes, lo que es fundamental para el éxito en juegos como Breakout.

## Trabajos Relacionados

Investigaciones previas han utilizado NEAT para entrenar agentes en juegos como Super Mario y Flappy Bird. Estos estudios han demostrado el potencial de NEAT para abordar una variedad de juegos y desafíos de optimización.

## Conclusión y Trabajos Futuros

En conclusión, este estudio demuestra que la combinación de algoritmos genéticos y NEAT puede mejorar significativamente el rendimiento de los agentes en juegos como Breakout. Se ha explorado con éxito la adaptabilidad de las topologías neuronales y la optimización de políticas de acción a través de procesos evolutivos. Como trabajos futuros, se sugiere investigar estrategias de entrenamiento más avanzadas para superar el rendimiento humano en juegos más complejos y desafiantes. Además, la exploración de hiperparámetros y la transferencia de conocimiento a otros juegos son áreas prometedoras de investigación en el campo de la inteligencia artificial aplicada a los videojuegos.

## Agradecimientos

Agradecemos a la profesora Daniela Díaz y al profesor Víctor Lombardo por su orientación y apoyo en este proyecto de investigación. También a la Universidad Tecnológica Nacional por proporcionar el entorno académico y los recursos necesarios para llevar a cabo esta investigación.

## Referencias

[1] Mitchell, T. M. (1997). Machine Learning. McGraw-Hill.

[2] Holland, J. H. (1975). Adaptation in natural and artificial systems. University of Michigan Press.

[3] LeCun, Y., Bengio, Y., & Hinton, G. (2015). Deep learning. Nature, 521(7553), 436-444.

[4] Goodfellow, I., Bengio, Y., & Courville, A. (2016). Deep learning. MIT press.

[5] Nielsen, M. A. (2015). Neural networks and deep learning: A textbook. Determination Press.

[6] Stanley, K. O., & Miikkulainen, R. (2002). Evolving neural networks through augmenting topologies. Evolutionary computation, 10(2), 99-127.

[7] Sutton, R. S., & Barto, A. G. (2018). Reinforcement learning: An introduction. MIT press.

[8] Togelius, J., Yannakakis, G. N., & Stanley, K. O. (2009). Preface to the special issue on evolutionary and player-adaptive games. IEEE Transactions on Computational Intelligence and AI in Games, 1(1), 1-2.

[9] Xie, H., & Zhong, L. (2017). Playing flappy bird with NEAT. In Proceedings of the 2017 IEEE Symposium Series on Computational Intelligence (SSCI) (pp. 1-6).
