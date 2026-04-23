# Arquitectura de un Sistema Experto

## 1. Adquisición de Conocimiento
Esta es la fase de entrada, donde el sistema "aprende" o recibe la información necesaria para operar.

* **¿Qué es?:** El proceso de recolectar datos y reglas de fuentes externas.
* **¿Para qué sirve?:** Para alimentar la base del sistema con la experiencia humana y datos del entorno.
* **¿Cómo funciona?:**
    * **Experto / Cognimátic:** El experto humano entrega su saber al "Ingeniero del Conocimiento" (Cognimátic), quien traduce el lenguaje humano a reglas lógicas.
    * **Sensores / Bases de datos:** Entradas automáticas de información técnica o histórica.

> **Ejemplo:** En un sistema de diagnóstico médico, un oncólogo (Experto) explica que "si hay una mancha tipo X en la radiografía, hay un 80% de probabilidad de lesión". El ingeniero traduce esto en una regla de código.

---

## 2. Representación del Conocimiento
Es donde reside la inteligencia y los datos del sistema, estructurados para ser procesados.

* **¿Qué es?:** El almacén donde se guarda el saber y los hechos actuales.
* **¿Para qué sirve?:** Para diferenciar entre lo que el sistema "sabe del mundo" y lo que "sabe del caso actual".
* **¿Cómo funciona?:**
    * **Base de Conocimiento:** Contiene reglas permanentes (Ej: "Todos los mamíferos tienen pelo").
    * **Base de Hechos (Memoria de trabajo):** Contiene datos efímeros del caso específico (Ej: "Este animal tiene pelo").

> **Ejemplo:** En un sistema bancario, la Base de Conocimiento tiene la regla "No dar crédito si la deuda supera el 30% del sueldo". La Base de Hechos registra que "Juan Pérez gana $1,000 y debe $500".

---

## 3. Tratamiento del Conocimiento (El Cerebro)
Aquí es donde ocurre el razonamiento lógico para llegar a una solución.

* **¿Qué es?:** El motor lógico que procesa la información.
* **¿Para qué sirve?:** Para aplicar las reglas de la base de conocimiento a los hechos actuales y obtener una conclusión.
* **¿Cómo funciona?:**
    * **Motor de Inferencia:** Es el componente que "piensa". Une el hecho con la regla (Si A entonces B).
    * **Módulo de Explicaciones:** Justifica el porqué de la decisión.

> **Ejemplo:** El Motor de Inferencia ve que Juan Pérez debe el 50% de su sueldo. Cruza este dato con la regla de crédito y decide: "Denegar crédito". El Módulo de Explicaciones genera el mensaje: "Crédito denegado porque su nivel de endeudamiento excede el límite permitido".

---

## 4. Utilización del Conocimiento
Es la capa externa que interactúa con el mundo real y el usuario final.

* **¿Qué es?:** Los canales de comunicación y ejecución de acciones.
* **¿Para qué sirve?:** Para entregar resultados al usuario o realizar cambios físicos en el entorno.
* **¿Cómo funciona?:**
    * **Interfaz de Usuario:** Pantallas, menús o chats donde el usuario hace consultas.
    * **Subsistema de Ejecución:** Realiza acciones automáticas (enviar correos, cerrar válvulas, etc.).

> **Ejemplo:** Un usuario entra a una App de diagnóstico (Interfaz), responde preguntas y recibe la receta. Si es un sistema industrial, el sistema podría cerrar automáticamente una válvula de gas al detectar una anomalía (Ejecución).

---

## Resumen del Flujo de Información

* **El Experto (La Fuente):** Su función es proveer la sabiduría y experiencia acumulada. *Ejemplo: un mecánico experto explica que "si el motor vibra de cierta forma, es porque le falta aceite".*
* **La Base de Conocimiento (El Almacén):** Es donde se guardan las reglas generales de forma permanente. *Ejemplo: se almacena la regla lógica "Si hay Vibración, entonces la causa es Falta de Aceite".*
* **La Base de Hechos (La Realidad Actual):** Registra los datos específicos del momento o del caso. *Ejemplo: "El sensor detecta que el motor está vibrando en este preciso instante".*
* **El Motor de Inferencia (El Razonamiento):** Es el componente que conecta los puntos. *Ejemplo: Analiza que como el motor vibra (hecho) y la regla dice que eso significa falta de aceite (conocimiento), la conclusión es que falta aceite.*
* **La Interfaz y el Usuario (La Comunicación):** Es el medio por el cual el sistema le habla al humano. *Ejemplo: El sistema envía un mensaje diciendo: "Señor usuario, el diagnóstico es falta de aceite; por favor, rellene el depósito".*
