# 💻 Tarea 2: Exploración de Arquitecturas de Computación Emergentes

Este repositorio contiene la investigación sobre diversas arquitecturas de computación avanzadas y emergentes, enfocándose en sus principios, historia, ventajas y desventajas. 
El objetivo es proporcionar un panorama completo de estas tecnologías que están definiendo el futuro del campo

---

## 📑 Contenido

1. [Primer Punto: Computación Cuántica](#primer-punto-computación-cuántica)  
   - Definición de computación Cuántica
   - Arquitectura y partes clave
   - Historia de la computación cuántica, ventajas y desventajas
   - Conceptos como superposición, entrelazamiento, compuertas cuánticas, etc...

2. [Segundo Punto: Computación Neuromórfica](#segundo-punto-computación-neuromórfica)  
   - Definición computador neuromórfico
   - Arquitectura, funcionamiento, ventajas y desventajas
   - Hardware utilizado en la computación neuromórfica
   - Tipos de computación neuromórfica

3. [Tercer Punto: Ordenadores Biológicos](#tercer-punto-ordenadores-biológicos)  
   - Definición de ordenadores biológicos
   - Arquitectura, tipos y principales hitos

4. [Cuarto Punto: Arquitectura de Computación Heterogénea](#cuarto-punto-Arquitectura-de-computación-heterogénea)
   - Definición de arquitectura de computación heterogénea
   - Historia, ventajas y desventajas

5. [Quinto Punto: Arquitectura de Computación de Borde](#cuarto-punto-Arquitectura-de-computación-heterogénea)
   - Definición de arquitectura de computación de borde
   - Historia, ventajas y desventajas

---
# 1) Computación cuántica
### 1.1) **¿Qué es?**
La computación cuántica es un tipo de informática que utiliza principios de la mecánica cuántica para resolver problemas muy complejos que las computadoras clásicas no pueden resolver.
Este tipo de computación es un paradigma que se diferencia de la computacion clasica ya que se basa en uso de quibit en vez de bits, gracias a esto se dan nuevos estados los
cuales pasan de ser dos a ser cuatro, esto abre infinidad de posibilidades en la resolucion de problemas altamente complejos, así como la creación de nuevos algoritmos porque
se crean nuevas compuertas lógicas que permiten analizar problemas con diferentes complejidades creando grandes expectativas frente a este paradigma.

Con apenas ~30 qubits se alcanza un espacio de estados comparable a un supercomputador de 10 teraflops, aunque obtener la respuesta correcta exige diseñar algoritmos que controlen la probabilidad de medida. 

![Image](https://github.com/user-attachments/assets/e17b4efa-c094-47aa-9d93-9f676a4c85ec)

📌 Principios físicos clave

- ***Superposición:*** un qubit puede estar en combinación lineal de |0⟩ y |1⟩; los algoritmos explotan ese paralelismo para evaluar funciones “en todos los puntos simultáneamente” antes de medir. 
- ***Entrelazamiento:*** correlaciones no clásicas entre qubits  
- ***Interferencia cuántica:*** las amplitudes pueden sumarse o anularse; muchos procedimientos “hacen desaparecer” los términos no deseados por interferencia destructiva y amplifican el deseado 
- ***Medición probabilística:*** medir colapsa la superposición y entrega un único resultado; por eso los algoritmos transforman el estado para que la respuesta correcta tenga alta probabilidad 
- ***Decoherencia:*** el acoplamiento con el entorno destruye la coherencia y la información; es el gran reto práctico de la tecnología.

---

## 1.2) 🏗️ **ARQUITECTURA**
La arquitectura de una computadora cuántica no se limita a procesar información: es un sistema altamente especializado que protege los estados cuánticos frágiles contra la decoherencia y traduce las 
instrucciones clásicas en operaciones físicas a nivel cuántico.

### **1. El Stack Arquitectónico Híbrido**

- **Las computadoras cuánticas son sistemas híbridos:** combinan componentes clásicos y cuánticos en un stack de múltiples capas.

- **Procesador Anfitrión (Host Processor):** ejecuta el software de alto nivel y compila los algoritmos cuánticos en instrucciones de bajo nivel.

- **Plano de Control y Medición:** convierte esas instrucciones en pulsos físicos (microondas, láseres) y procesa las señales de salida de los cúbits.

- **Plano de Datos Cuánticos (Quantum Data Plane):** alberga la Unidad de Procesamiento Cuántico (QPU), donde residen los cúbits físicos y se realizan las operaciones cuánticas.

📌 Este flujo traduce el lenguaje digital clásico en señales físicas y, tras la medición, lo devuelve al dominio clásico. La fidelidad de esta traducción determina el rendimiento del sistema.

### **2. La Materialización del Cúbit: Arquitectura física**

No existe una única forma de construir un cúbit. Varias tecnologías físicas compiten para convertirse en la plataforma dominante, cada una con un conjunto único de ventajas y desafíos en términos de velocidad, estabilidad y escalabilidad.

- **Cúbits Superconductores:** Actualmente, es la tecnología líder, utilizada por empresas como IBM y Google. Se basan en circuitos eléctricos fabricados con materiales superconductores como el aluminio, enfriados a temperaturas extremadamente bajas. Utilizan un componente no lineal llamado unión Josephson para crear niveles de energía discretos y desiguales, comportándose como un "átomo artificial" cuyos dos niveles más bajos pueden usarse como los estados ∣0⟩ y ∣1⟩ de un cúbit. El tipo más común se conoce como "transmon".

- **Iones Atrapados:** Este enfoque utiliza átomos individuales que han sido ionizados (se les ha quitado un electrón) y son confinados en el vacío mediante campos electromagnéticos generados por un chip. Los estados del cúbit se codifican en los niveles de energía electrónicos hiperfinos del ion, que son extremadamente estables. Empresas como IonQ y Quantinuum lideran esta tecnología.

- **Cúbits Fotónicos:** Utilizan partículas de luz, fotones, como cúbits. La información cuántica se puede codificar en propiedades como la polarización (horizontal/vertical) o la ruta que sigue el fotón. Su principal ventaja es que son muy resistentes a la decoherencia y pueden operar a temperatura ambiente, lo que simplifica enormemente la infraestructura.

- **Átomos Neutros:** Una tecnología emergente y prometedora que utiliza átomos sin carga eléctrica, atrapados individualmente en el espacio mediante "pinzas ópticas", que son rayos láser muy enfocados. Los estados del cúbit se definen por los estados electrónicos del átomo.

A continuación, se presenta una tabla comparativa que resume las características clave de las principales plataformas de cúbits.

| **Característica**       | **Superconductores**            | **Iones Atrapados**           | **Fotónicos**          | **Átomos Neutros**        |
| ------------------------ | ------------------------------- | ----------------------------- | ---------------------- | ------------------------- |
| **Base Física**          | Circuitos con uniones Josephson | Estados electrónicos de iones | Propiedades de fotones | Estados de átomos neutros |
| **Método de Control**    | Microondas                      | Láseres                       | Óptica lineal          | Pinzas ópticas            |
| **Velocidad de Puerta**  | Muy alta (ns)                   | Lenta (μs)                    | Altísima (c)           | Media (μs)                |
| **Tiempo de Coherencia** | Corto (μs)                      | Muy largo (s–min)             | Muy largo              | Largo (s)                 |
| **Fidelidad**            | Alta (>99.9%)                   | Muy alta (>99.99%)            | Media                  | Alta (>99.5%)             |
| **Conectividad**         | Local                           | Todos con todos               | Difícil                | Reconfigurable            |
| **Desafíos**             | Ruido, criogenia                | Escalabilidad                 | Interacción de fotones | Carga/detección           |

### **Control y Medición: La Orquestación de los Estados Cuánticos**

Manipular un cúbit equivale a realizar una operación lógica, lo que se logra aplicando pulsos de energía cuidadosamente calibrados para guiar la evolución de su estado cuántico.

〰️ Para los cúbits superconductores, esto se hace mediante pulsos de microondas. Se envían señales de microondas a una frecuencia de resonancia específica del cúbit 
(generalmente en el rango de 5-10 GHz) a través de cables coaxiales que llegan hasta el chip. La duración, forma y fase de estos pulsos determinan con precisión la rotación del estado del cúbit en la Esfera de Bloch.

💥 Para los iones atrapados y átomos neutros, se utilizan láseres de alta precisión. Un conjunto de láseres se enfoca en los átomos individuales para enfriarlos, mantenerlos en su lugar y, lo más importante, inducir transiciones entre sus niveles de energía internos para ejecutar las operaciones cuánticas.

📏 El paso final de cualquier algoritmo cuántico es la medición, que extrae la respuesta del cálculo. Este proceso es fundamentalmente probabilístico y destructivo: fuerza al cúbit a "elegir" uno de los estados base, ∣0⟩ o ∣1⟩, colapsando la superposición. Para los cúbits superconductores, una técnica común es acoplar el cúbit a un circuito resonador. El estado del cúbit (sea ∣0⟩ o ∣1⟩) altera ligeramente la frecuencia de resonancia del circuito. 
Al enviar una señal de microondas de "lectura" y medir la fase de la señal transmitida, se puede inferir el estado del cúbit con alta probabilidad.

### El entorno operativo es un reto enorme:

Los superconductores requieren temperaturas más bajas que el espacio interestelar, alcanzadas con criostatos de dilución.

Los sistemas ópticos y de iones necesitan aislamiento de vibraciones, ruido electromagnético y partículas externas.

La complejidad de esta infraestructura es uno de los principales obstáculos para la masificación de las computadoras cuánticas.

👉👉👉 Imagen 3: Sistema de criogenia y control cuántico

### 🧠 La Arquitectura Lógica: El Lenguaje de la Computación Cuántica
---
Mientras que la arquitectura física se ocupa del hardware, la arquitectura lógica define el conjunto de operaciones y la estructura abstracta utilizada para programar una computadora cuántica. 
Este es el dominio de las puertas, los circuitos y los algoritmos, el lenguaje con el que se instruye a los cúbits para que realicen cálculos.
Sobre los cúbits físicos se construye la **capa lógica**, que define cómo se programan los algoritmos.

- **Puertas cuánticas:** operaciones unitarias reversibles como X, Y, Z, Hadamard (H) y CNOT.  
- **Circuitos cuánticos:** secuencias organizadas de puertas para ejecutar algoritmos.  
- **Algoritmos representativos:**  
  - **Shor (1994):** factorización de enteros, amenaza a RSA.  
  - **Grover (1996):** búsqueda en bases de datos no estructuradas, con aceleración cuadrática.  
  - **QFT (Quantum Fourier Transform):** pieza clave en varios algoritmos.  

👉👉👉 *Imagen 5: Ejemplo de circuito cuántico con puertas H y CNOT*  

### 5. Corrección de errores y cúbits lógicos

Los cúbits son inestables y altamente sensibles al entorno. Para mantener la confiabilidad se usan **códigos de corrección de errores cuánticos (QEC):**

- **Tipos de errores comunes:**  
  - *Bit-flip* (0 ↔ 1).  
  - *Phase-flip* (∣+⟩ ↔ ∣−⟩).  
  - Errores continuos generados por ruido ambiental.  

- **Redundancia:** un cúbit lógico requiere decenas o cientos de cúbits físicos.  
- **Ejemplos:**  
  - **Código de Shor (1995):** protege un cúbit lógico usando 9 cúbits físicos.  
  - **Código de superficie (Surface Code):** más usado hoy por su escalabilidad en superconductores.  

👉👉👉 *Imagen 6: Corrección de errores cuánticos mediante cúbits ancilla*  

## 1.3)📜 Breve Historia de la Computación Cuántica
La computación cuántica se perfila como una de las revoluciones tecnológicas más significativas, prometiendo resolver problemas que hoy son intratables para las supercomputadoras más potentes. 
A continuación, se desglosan sus conceptos fundamentales, su historia, sus capacidades y los obstáculos que enfrenta.

Aunque sus raíces teóricas se hunden en los descubrimientos de Max Planck y Albert Einstein a principios del siglo XX, la idea de la computación cuántica comenzó a tomar forma en la década de 1980.   

**Años 80:** El físico Richard Feynman propuso que un ordenador basado en principios cuánticos podría simular eficientemente sistemas cuánticos, una tarea extremadamente difícil para las computadoras clásicas. 
En 1985, David Deutsch formalizó el concepto de una máquina cuántica universal.   

**Años 90:** Se produjeron avances algorítmicos cruciales. En 1994, Peter Shor desarrolló un algoritmo capaz de factorizar números grandes de manera exponencialmente más rápida que cualquier método clásico, 
lo que representa una amenaza para la criptografía actual. Dos años más tarde, Lov Grover presentó un algoritmo que acelera significativamente la búsqueda en bases de datos no estructuradas.   

**Siglo XXI:** La teoría comenzó a materializarse. En 2001, IBM y la Universidad de Stanford ejecutaron por primera vez el algoritmo de Shor, factorizando el número 15. En 2011, D-Wave Systems vendió la primera
computadora cuántica comercial. Un hito importante llegó en 2019, cuando Google afirmó haber alcanzado la "supremacía cuántica" con su procesador Sycamore, que realizó un cálculo en minutos que a una supercomputadora clásica le llevaría miles de años.   

## ⚖️ Ventajas y Desventajas

La computación cuántica no pretende reemplazar a la clásica, sino **complementarla** en tareas específicas donde ofrece ventajas exponenciales.

| **Ventajas** | **Desventajas** |
|--------------|-----------------|
| 🚀 **Velocidad exponencial** en problemas como factorización (Shor) y simulación molecular. | ⚠️ **Fragilidad de los cúbits**: son sensibles al ruido y la decoherencia. |
| 🔀 **Procesamiento paralelo** gracias a la superposición, explorando muchas posibilidades simultáneamente. | ❄️ **Requisitos de hardware extremos**: criogenia y equipos costosos. |
| 🧠 **Resolución de problemas complejos**: optimización, nuevos materiales, fármacos, IA y machine learning. | 🧮 **Corrección de errores en desarrollo**: requiere muchos cúbits físicos para un cúbit lógico. |
| 💾 **Mayor capacidad de memoria cuántica** con bajo consumo energético. | 📏 **Escalabilidad difícil**: aumentar cúbits manteniendo calidad es un desafío. |

---
## 1.4) 🌌 Principios Fundamentales
El poder de la computación cuántica reside en su capacidad para aprovechar fenómenos del mundo subatómico que no tienen equivalente en la experiencia cotidiana.   

### Superposición
Es la capacidad de un cúbit (la unidad básica de información cuántica) de existir en múltiples estados a la vez. Mientras que un bit clásico solo puede ser 0 o 1, un cúbit puede ser una combinación de ambos estados simultáneamente hasta que se mide. 
Esta propiedad es la que permite el paralelismo cuántico, donde un registro de    

n cúbits puede representar 2^n  valores al mismo tiempo.  

### Entrelazamiento
El entrelazamiento es una conexión profunda y "fantasmal" entre dos o más cúbits. Cuando están entrelazados, el estado de un cúbit está instantáneamente correlacionado con el estado del otro, sin importar la distancia que los separe. Medir uno de los cúbits 
determina de inmediato el resultado de la medición del otro. Este fenómeno es esencial para realizar cálculos cuánticos complejos y para la comunicación cuántica segura.   

### Interferencia Cuántica

Al igual que las ondas pueden sumarse o anularse, los algoritmos cuánticos utilizan la interferencia para manipular las probabilidades de los estados de los cúbits. El objetivo es diseñar el cálculo de tal manera que las rutas que llevan a soluciones incorrectas
se cancelen entre sí (interferencia destructiva), mientras que las rutas que conducen a la respuesta correcta se refuercen (interferencia constructiva), aumentando la probabilidad de medir el resultado deseado.   

### Medición Probabilística
La medición es el acto de observar un cúbit para extraer un resultado clásico (un 0 o un 1). Este proceso es inherentemente probabilístico. Al medir un cúbit en superposición, su estado "colapsa" a uno de los estados base con una probabilidad determinada por su estado 
cuántico justo antes de la medición. Este colapso es irreversible y destruye la superposición, lo que significa que no se pueden observar todos los estados a la vez; el arte de los algoritmos cuánticos es maximizar la probabilidad de que el estado colapse en la respuesta correcta.   

### El Desafío de la Decoherencia

La decoherencia es el mayor enemigo de la computación cuántica. Es el proceso por el cual un cúbit pierde sus propiedades cuánticas (como la superposición y el entrelazamiento) debido a interacciones no deseadas con su entorno, como fluctuaciones de temperatura, 
vibraciones o campos electromagnéticos. Esta interacción es como un "ruido" que introduce errores en los cálculos y degrada la información cuántica. Gran parte de la ingeniería de hardware cuántico se centra en aislar los cúbits para retrasar la decoherencia el 
tiempo suficiente para realizar un cálculo útil.  

--- 

## 📡 Tipos de Comunicación Cuántica
La comunicación cuántica utiliza los principios cuánticos para transmitir información de formas nuevas y, sobre todo, más seguras. Los principales protocolos incluyen:   

**Distribución Cuántica de Claves (QKD):** Es la aplicación más madura. Permite a dos partes generar y compartir una clave de cifrado secreta con la garantía de que cualquier intento de espionaje será detectado. Esto se debe a que el acto de medir un estado cuántico
(como un fotón) lo altera inevitablemente, alertando a los usuarios de la presencia de un intruso. El protocolo BB84 es uno de los más conocidos.   

**Protocolos Emergentes:** Se están desarrollando otros protocolos para tareas específicas, como la transferencia ajena cuántica (transferir información sin que el remitente sepa qué dato se eligió), el lanzamiento de monedas cuánticas (para generar aleatoriedad segura
entre dos partes que no confían la una en la otra) y las firmas digitales cuánticas.   

## Compuertas Cuánticas
Las compuertas cuánticas son las operaciones fundamentales que se aplican a los cúbits para ejecutar un algoritmo, análogas a las puertas lógicas (AND, OR, NOT) en la computación clásica. Sin embargo, a diferencia de muchas puertas clásicas, las cuánticas son siempre 
reversibles. Se representan matemáticamente como matrices unitarias que rotan el estado del cúbit.   

A continuación, se presentan algunas de las compuertas más importantes:

| **Compuerta** | **Símbolo** | **Función Principal** |
|---------------|-------------|------------------------|
| Pauli-X (NOT) | X           | Invierte el estado del cúbit. |
| Pauli-Z       | Z           | Aplica un cambio de fase. |
| Hadamard      | H           | Crea superposición uniforme a partir de un estado base. |
| CNOT (NOT Controlada) | CNOT | Genera entrelazamiento. Aplica X al cúbit objetivo si el cúbit de control está en 1. |


