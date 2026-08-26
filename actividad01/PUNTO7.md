# RESUMEN DE LOS DOS PDF.

## 1. INGENIERIA DEL CONOCIMIENTO.

### CONCEPTOS FUNDAMENTALES.
* El conocimiento en la Inteligencia Artificial se interpreta como la combinación de estructuras de datos y procedimientos interpretativos que confieren un comportamiento inteligente para modelar el mundo real[cite: 4].
* El conocimiento puede ser declarativo (hechos o atributos de un objeto) o procedural (conjunto de reglas que los expertos usan para solucionar problemas).
* El Ingeniero de Conocimiento (ICO) es el especialista informático encargado de extraer el conocimiento del experto humano e implementarlo correctamente en un sistema informático.
* El Experto Humano es la persona de reconocido prestigio que aporta su experiencia, mientras que el Usuario es quien utilizará el sistema interactuando con la base de conocimiento.

### INGENIERIA DEL CONOCIMIENTO. (IC)
* La Ingeniería del Conocimiento es la disciplina de la IA encargada de la adquisición, representación, validación, inferencia y explicación del conocimiento.
* Su objetivo principal es construir aplicaciones informáticas y sistemas expertos en dominios donde el conocimiento no está bien estructurado, es inconsistente o incompleto.
* Los procesos fundamentales que interactúan en la IC son: Adquisición del conocimiento, Representación del conocimiento, Validación, Inferencia, y Explicación y Justificación.

### ADQUISICION DEL CONOCIMIENTO.
* Es el proceso central para crear sistemas expertos, y consiste en extraer conocimiento de fuentes estáticas (documentos, libros) o dinámicas (expertos humanos).
* Se compone de cinco etapas formales: Identificación del problema, Entendimiento de los conceptos, Formalización (organización para la representación), Implementación (creación de prototipos) y Pruebas para validar la precisión del conocimiento.
* Los métodos de adquisición se dividen en manuales, destacando las entrevistas (estructuradas, semiestructuradas, no estructuradas) y el análisis de protocolos para rastrear los pensamientos del experto.
* También existen métodos semiautomatizados, que brindan soporte computacional mediante editores e interfaces, tanto para el experto humano como para el ingeniero de conocimiento.
* Finalmente, los métodos automatizados, como la inducción de reglas mediante algoritmos (ej. ID3) o el aprendizaje automático, buscan extraer patrones directamente de matrices de datos, minimizando la intervención humana.

### REPRESENTACION DEL CONOCIMIENTO. (KR)
* La representación del conocimiento organiza la información extraída en esquemas lógicos que la computadora pueda almacenar, manipular e interpretar.
* Un buen esquema de representación debe ser sencillo, fácil de modificar, transparente para detectar incoherencias, independiente y relacional.
* Los esquemas incluyen reglas de lógica simbólica, divididas en lógica proposicional (uso de operadores booleanos como conjunción y disyunción) y lógica de predicados (uso de constantes, variables y cuantificadores).
* Otras estructuras fundamentales son las redes semánticas (nodos y enlaces que representan relaciones como "ES-UN"), los árboles de decisiones, los gráficos conceptuales y los marcos (frames o slots) que agrupan propiedades jerárquicas de un objeto.

---

## 2. RESUMEN DE SISTEMAS EXPERTOS BASADOS EN REGLAS.

### LA BASE DEL CONOCIMIENTO
* Los sistemas basados en reglas son la metodología más sencilla y eficiente dentro de los sistemas expertos para tratar situaciones deterministas y de control.
* El sistema opera utilizando "Hechos", que son datos dinámicos almacenados en la memoria de trabajo, y "Reglas", que constituyen la información estática y permanente alojada en la base de conocimiento.
* Una regla es una afirmación lógica que consta de una "premisa" (antecedente lógico tras la palabra "si") y una "conclusión" (consecuente tras la palabra "entonces"), las cuales pueden conectarse con operadores lógicos.
* Las reglas complejas pueden someterse a mecanismos de sustitución para simplificarlas, transformando reglas compuestas en conjuntos equivalentes de reglas simples para facilitar su procesamiento computacional.

### EL MOTOR DE INFERENCIA.
* Es el componente central encargado de procesar los hechos de la memoria de trabajo y aplicar las reglas para derivar lógicamente nuevas conclusiones.
* Para obtener conclusiones simples, utiliza reglas de inferencia clásicas como el *Modus Ponens*, que se mueve hacia adelante afirmando que si una premisa es cierta, la conclusión también lo es.
* También emplea la regla del *Modus Tollens*, que se mueve hacia atrás estipulando que si la conclusión de una regla es falsa, entonces su premisa es obligatoriamente falsa.
* Para derivar conclusiones compuestas que involucren múltiples reglas, el motor utiliza el "Mecanismo de Resolución", el cual combina y simplifica expresiones lógicas paso a paso.

### ESTRATEGIAS DE ENCADENAMIENTO.
* El "Encadenamiento de reglas" es un algoritmo que avanza desde los hechos conocidos, ejecutando reglas cuyas premisas son ciertas para deducir nuevos datos, repitiendo el ciclo hasta que no es posible obtener más conclusiones.
* El "Encadenamiento orientado a un objetivo" (o encadenamiento hacia atrás) funciona de manera inversa, partiendo de un nodo objetivo deseado y navegando por las reglas para verificar si los hechos iniciales respaldan dicha meta.
* Si la información es insuficiente durante el encadenamiento orientado a un objetivo, el algoritmo interrumpe el proceso para preguntar directamente al usuario por el valor de los datos faltantes requeridos.

### CONTROL DE COHERENCIA Y EXPLICACION.
* El control de coherencia es estrictamente necesario para evitar que el sistema procese reglas contradictorias o acepte combinaciones de hechos imposibles, lo cual generaría un comportamiento poco satisfactorio y conclusiones absurdas.
* Los "valores no factibles" que contradicen el conjunto de reglas deben ser detectados y eliminados automáticamente de las listas de opciones del usuario antes de que se ingresen al sistema.
* La coherencia total se asegura actualizando la base de conocimiento y evaluando la información continuamente tras la incorporación de cada nuevo hecho aislado.
* Por último, los sistemas basados en reglas facilitan la tarea del "Subsistema de explicación", permitiendo justificar los resultados al mostrarle al usuario el listado exacto de reglas activas que se utilizaron para alcanzar cada conclusión.