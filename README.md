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

<img width="743" height="408" alt="Image" src="https://github.com/user-attachments/assets/11af99fc-c6ca-474d-a57d-8075b0b844e7" />

> - Qbit vs Bit

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

![Image](https://github.com/user-attachments/assets/b337783b-85d8-4f81-b5d9-416e93c43b26)

> - Sistema de criogenia y control cuántico

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

<img width="633" height="381" alt="Image" src="https://github.com/user-attachments/assets/d868ed5b-cac7-47c6-a9dc-e78617446e1f" />

> - Ejemplo de circuito cuántico con puertas H y CNOT 

### 5. Corrección de errores y cúbits lógicos

Los cúbits son inestables y altamente sensibles al entorno. Para mantener la confiabilidad se usan **códigos de corrección de errores cuánticos (QEC):**

- **Tipos de errores comunes:**  
  - *Bit-flip* (0 ↔ 1).  
  - *Phase-flip* (∣+⟩ ↔ ∣−⟩).  
  - Errores continuos generados por ruido ambiental.  

- **Redundancia:** un cúbit lógico requiere decenas o cientos de cúbits físicos.  
- **Ejemplos:**  
  - **Código de Shor (1995):** protege un cúbit lógico usando 9 cúbits físicos.
    
<img src="https://github.com/user-attachments/assets/9b7c51c3-a45c-4155-b73b-d47f0b115d43" width="800"> 

 > - (Codigo de Shor)
    
  - **Código de superficie (Surface Code):** más usado hoy por su escalabilidad en superconductores.
  
 <img width="850" height="293" alt="Image" src="https://github.com/user-attachments/assets/82be1c94-90cf-4494-8693-cc961b8829bd" />
 
 > - (Codigo de superficie)


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

![Image](https://github.com/user-attachments/assets/f89d2bbd-f96d-4f74-a2d7-d062df5571de)

 > - (Compuertas comunes)

---
---

# 2) 🧠 Computación Neuromórfica

La **computación neuromórfica** diseña hardware y software inspirados en el **cerebro**: neuronas y sinapsis que intercambian **pulsos (spikes)** de manera **asíncrona** y **event-driven**. El objetivo es procesar percepción y control en **tiempo real** con **muy bajo consumo** energético, ejecutando **Redes Neuronales de Disparos** (*Spiking Neural Networks, SNN*).


<img src="https://github.com/user-attachments/assets/b6018afd-ebbe-4b25-b940-60be5cc8bb69" width="700"> 


 > - (Redes neuronales de disparos)

---

## ¿Cómo funciona? (Arquitectura y principios)

1. **Modelo de neurona y sinapsis**  
   - Neuronas tipo *Integrate-and-Fire (LIF)* acumulan corriente sináptica; cuando superan un umbral, **emiten un spike**.  
   - Sinapsis ponderan los spikes con **pesos** y **delays**; algunas admiten **plasticidad local** (p.ej., **STDP**).

2. **Codificación por eventos**  
   - En lugar de muestrear todo el tiempo, las neuronas **solo se activan cuando hay información**.  
   - Los spikes viajan como **direcciones** (no como valores analógicos) mediante **AER – Address-Event Representation**.

3. **Paralelismo masivo y asíncrono**  
   - Miles/millones de neuronas operan en paralelo, **sin reloj global** (o con relojes locales).  
   - La comunicación usa redes en chip (**NoC**) o routers jerárquicos especializados.

4. **Memoria “cerca del cómputo”**  
   - Los **pesos sinápticos** residen junto a las neuronas (SRAM, RRAM, PCM…), reduciendo movimiento de datos y energía.

5. **Aprendizaje**  
   - *On-chip*: reglas locales (STDP, homeostasis).  
   - *Off-chip*: se entrena con métodos clásicos y se **mapea** al chip (cuantización/digitalización de pesos y tiempos).

![Image](https://github.com/user-attachments/assets/0046994c-9aea-4bf6-8587-222dcfa45566)

 > - (Neuronas LIF)


![Image](https://github.com/user-attachments/assets/da18a75d-b596-4621-8d25-2c6bddbd1334)

 > - (STDP, o «plasticidad dependiente del tiempo de espiga» (Spike-Timing-Dependent Plasticity),
>  - Es un mecanismo biológico y un modelo de aprendizaje que modifica la fuerza de las conexiones sinápticas entre neuronas según el momento preciso en que los potenciales(o espigas) de las neuronas pre- y postsinápticas ocurren de acción)

---

## Componentes de hardware (¿qué se usa?)

- **Núcleos neuromórficos**: bancos de neuronas y sinapsis (digitales, analógicos o mixtos).  
- **Memoria sináptica local**: SRAM, **memristores/RRAM**, **PCM**, a veces *crossbars* para cómputo en-memoria.  
- **Red de interconexión**: routers AER / NoC para enrutar spikes.  
- **SoC de soporte**: microcontrolador, temporizadores, I/O sensorial (cámaras dinámicas, micrófonos), conversores si son mixtos.  
- **Software**: SDK/compiladores (**Lava**, **NxSDK**, **PyNN**), librerías de mapeo y herramientas de conversión ANN→SNN.

### Hardware representativo

| Plataforma | Tipo de implementación | Escala/Enfoque | Notas |
|---|---|---|---|
| **IBM TrueNorth** | Digital, evento-dirigido | 1M neuronas / 256M sinapsis (a gran escala) | Ultra-bajo consumo; programación con *corelets*. |
| **Intel Loihi / Loihi 2** | Digital, con plasticidad on-chip | Núcleos programables con aprendizaje local | SDK **Lava**; soporte para constraints temporales. |
| **SpiNNaker (U. Manchester)** | Many-core ARM (simulación de SNN) | Hasta ~1M núcleos en clúster | Flexibilidad alta; útil para neurociencia. |
| **BrainScaleS (Heidelberg)** | Analógico/mixed-signal acelerado en tiempo | Aceleración ×10³ del tiempo biológico | Muy rápido para dinámica neuronal. |
| **Crossbars memristivos** | Analógico en-memoria | Alta densidad sináptica | Variabilidad del dispositivo es un reto. |


<img src="https://github.com/user-attachments/assets/64d65973-57d3-4f33-bca1-3f3593b88b63" width="300"> 
       
<img src="https://github.com/user-attachments/assets/2c828f75-f445-4650-aa60-8f4e52701fc6" width="430">

<img src="https://github.com/user-attachments/assets/1b4c428b-b336-4256-a158-90431136e48b" width="300">
   
<img src="https://github.com/user-attachments/assets/a74cf1ff-ac4c-4391-82bb-5a7c29a54b6c" width="430"> 

<img src="https://github.com/user-attachments/assets/d4492353-6fe4-463b-a77c-a8757c2bf052" width="300"> 


---

## Ventajas y desventajas

| ✅ Ventajas | ⚠️ Desventajas |
|---|---|
| **Eficiencia energética** (pJ por evento) gracias al procesamiento por eventos y memoria cercana. | **Programación compleja**: las SNN y su tooling aún son menos maduros que ANN/GPU. |
| **Baja latencia** y **tiempo real** para percepción/actuación (robótica, edge). | **Precisión limitada** en analógico/mixto; **variabilidad** de dispositivos no-volátiles. |
| **Escalabilidad biológicamente plausible** con paralelismo masivo asíncrono. | **Portabilidad del modelo** entre chips no estandarizada (diferencias de hardware). |
| **Aprendizaje local** (STDP, reglas Hebbianas) y operación continua *on-line*. | **Herramientas y ecosistema** aún en consolidación; conversión ANN→SNN no siempre óptima. |

---

## Tipos de computación neuromórfica

1. **Digital evento-dirigida** (TrueNorth, Loihi): determinista, reprogramable, buena para edge e investigación aplicada.  
2. **Analógica / Mixta** (BrainScaleS, ASICs con ADC/DAC): dinámica natural muy rápida y eficiente, pero más sensible al ruido.  
3. **En-memoria con dispositivos no volátiles** (RRAM/PCM/memristores en *crossbars*): alta densidad sináptica; retos de variabilidad y endurance.  
4. **Basada en FPGA/Many-core** (SpiNNaker, prototipos): gran flexibilidad para simulación a gran escala y educación.  
5. **Neuromórfica fotónica** (emergente): usa interferómetros/laser para spikes; promete muy alta velocidad con baja latencia.


---

## Arquitectura de un computador neuromórfico (resumen estructural)

- **Capa sensorial**: cámaras de visión por eventos (DVS), micrófonos, sensores IMU.  
- **Capa de cómputo**: núcleos con neuronas LIF y sinapsis (pesos, delays, plasticidad opcional).  
- **Red en chip**: routers AER jerárquicos que garantizan baja latencia y QoS de spikes.  
- **Capa de aprendizaje**: reglas locales (STDP) u orquestación externa para *off-chip training*.  
- **Interfaces**: PCIe/Ethernet/UART, control por CPU anfitrión, APIs (Lava/PyNN).  


<img src="https://github.com/user-attachments/assets/4c9a77a8-8396-4fca-9794-d992973fd3c5" width="600"> 

 > - (Diagrama de bloques de un SoC neuromórfico completo)

---

## Casos de uso típicos

- **Percepción en tiempo real**: visión por eventos, seguimiento de objetos, detección de gestos.  
- **Robótica y control**: navegación, SLAM neuromórfico, control motor reactivo.  
- **IoT y Edge AI**: analítica local con ultra-bajo consumo y alta privacidad.  
- **Neurociencia computacional**: simulación de redes a gran escala con dinámica biológica.

---
---

# 3) 🧬 Computación Biológica

La **computación biológica** utiliza sistemas y procesos de organismos vivos (ADN, ARN, proteínas, células) para **almacenar, procesar y transmitir información**. Su enfoque es aprovechar las propiedades moleculares y bioquímicas para resolver problemas de forma paralela y con densidad de información extraordinaria.


<img src="https://github.com/user-attachments/assets/27a2deab-4867-4cb1-abf1-fa96ea7cb17b" width="600"> 

---

## Arquitectura de un ordenador biológico

Un ordenador biológico no se compone de transistores y chips, sino de **moléculas y reacciones biológicas** que actúan como elementos lógicos y de memoria.

1. **Capa de codificación genética**  
   - La información se representa mediante **secuencias de bases nitrogenadas** (A, T, C, G).  
   - Estas secuencias pueden codificar datos binarios o instrucciones.  

2. **Procesamiento molecular**  
   - En lugar de puertas lógicas electrónicas, se utilizan **reacciones químicas** como hibridación de ADN, plegamiento de ARN o unión proteína-ligando.  
   - Los resultados de estas reacciones definen la salida de la operación.  

3. **Memoria biológica**  
   - El ADN ofrece una **capacidad de almacenamiento masiva**: un gramo puede contener hasta **215 petabytes** de información.  

4. **Output (salida)**  
   - Puede ser una molécula sintetizada, un cambio estructural o una señal biológica detectable.  


<img src="https://github.com/user-attachments/assets/45ffe3b3-59e4-48d6-9f90-ffa6a24df81a" width="600"> 

 > - (Arquitectura de un ordenador biológico, codificación de datos en ADN, procesamiento molecular y el almacenamiento masivo de información)
---

## Tipos de computación biológica

1. **Computación basada en ADN**
<img src="https://github.com/user-attachments/assets/b5440270-9037-4254-8a52-0709575cc92f" width="150"> 
   
   - Pionera en los años 90 con Leonard Adleman.  
   - Utiliza reacciones de ADN para resolver problemas complejos, como el **problema del camino hamiltoniano**.  
   
2. **Computación en células vivas (Biocomputación sintética)**  
<img src="https://github.com/user-attachments/assets/146b4484-5a97-4e20-8f83-39eaa3563dd1" width="150"> 

   - Reprograma organismos mediante biología sintética para que actúen como **procesadores vivos**.  
   - Ejemplo: bacterias que detectan contaminantes o generan respuestas programadas.
     
3. **Computación molecular híbrida**
<img src="https://github.com/user-attachments/assets/77e881a9-e4d6-4257-b085-eab36ee60c1d" width="150"> 

   - Integra moléculas biológicas con sistemas electrónicos tradicionales.  
   - Promete dispositivos bioelectrónicos con mayor densidad de almacenamiento.  

---
El hito más relevante y un caso de estudio ejemplar en este campo es el CL1 de la empresa australiana Cortical Labs, presentado como la primera computadora biológica comercial del mundo. Su arquitectura es una fusión de elementos biológicos y electrónicos, 
representando un avance significativo en la intersección de la biología y la tecnología.   

La estructura del CL1 se basa en una arquitectura híbrida que integra los siguientes componentes :   

- Componentes Biológicos: Utiliza neuronas reales cultivadas a partir de células madre humanas que funcionan como las unidades de procesamiento.   

- Interfaz Híbrida: Un chip de silicio actúa como la interfaz crucial, enviando y recibiendo impulsos eléctricos para establecer una comunicación bidireccional entre las células vivas y el hardware.   

- Sistema de Soporte Vital: Para mantener vivas y funcionales las neuronas, el sistema está alojado en una unidad de soporte vital que proporciona un entorno controlado, suministrando una solución rica en nutrientes y
 manteniendo una temperatura y pH óptimos durante al menos seis meses.   

- Sistema Operativo biOS: Un software especializado, desarrollado por Cortical Labs, interactúa con las neuronas vivas. Este sistema operativo permite a los usuarios ejecutar código traduciendo un lenguaje de muy alto nivel en una secuencia de estímulos eléctricos,
 que a su vez moldea el comportamiento biológico de las neuronas para ajustarse a una especificación dada.

## Principales hitos históricos

- **1994:** Leonard Adleman resuelve un problema matemático (camino hamiltoniano) utilizando ADN como soporte de cálculo.  
- **Década de 2000:** avances en almacenamiento de información en ADN, con demostraciones de codificación de imágenes, textos y videos.  
- **2012:** Harvard almacena un libro de 53.000 palabras en ADN.  
- **2017:** investigadores codifican un sistema operativo completo y una película en ADN.  
- **Actualidad:** desarrollo de **biocomputadoras celulares** capaces de tomar decisiones en organismos vivos.  

---

## Ventajas y desventajas

| ✅ Ventajas | ⚠️ Desventajas |
|---|---|
| **Densidad de almacenamiento altísima** (millones de veces mayor que el silicio). | **Lentitud** en comparación con la computación clásica. |
| **Procesamiento paralelo masivo** gracias a reacciones moleculares. | **Errores bioquímicos** durante síntesis y lectura de ADN. |
| **Biocompatibilidad**: ideal para aplicaciones médicas y biotecnológicas. | **Costos altos** en síntesis y secuenciación de ADN. |
| **Durabilidad**: el ADN puede conservar información durante miles de años. | **Dificultad de escalabilidad práctica** para uso masivo. |

---

## Aplicaciones principales

- **Medicina personalizada:** diagnósticos y tratamientos basados en biocomputadoras celulares.  
- **Biotecnología:** organismos programados para detectar o responder a estímulos ambientales.  
- **Almacenamiento de datos:** uso de ADN como memoria de ultra-alta densidad.  
- **Criptografía y seguridad:** codificación genética resistente a ataques tradicionales.  


---
# 4) 🔀 Computación Heterogénea

La **computación heterogénea** integra **diferentes tipos de procesadores** dentro de un mismo sistema (CPU, GPU, FPGA, ASIC, TPU, e incluso QPU), de modo que cada uno se encarga de las tareas para las que está mejor optimizado. 
Su objetivo es **maximizar el rendimiento y la eficiencia energética**, superando las limitaciones de las arquitecturas homogéneas tradicionales.

<img src="https://github.com/user-attachments/assets/25ca988e-edf1-4d73-a5e1-86d9eabab878" width="350"> 
<img src="https://github.com/user-attachments/assets/0be5dfcb-1159-443f-af7e-8b92e8217c08" width="350"> 


---

## Breve historia

- **Década de 1990:** primeras combinaciones de CPU con coprocesadores gráficos para acelerar operaciones matemáticas.  
- **2000s:** auge de las GPU programables y su integración en supercomputadores.  
- **2010s:** consolidación de la **High-Performance Computing (HPC)** heterogénea con arquitecturas híbridas CPU–GPU.  
- **Actualidad:** integración de múltiples aceleradores (GPU, TPU, FPGA, QPU) en sistemas de **exascale computing**, servidores en la nube e incluso dispositivos de borde.



---

## Arquitectura de un sistema heterogéneo

1. **CPU (Central Processing Unit)**  
   - Generalista, controla el flujo y tareas de coordinación.  
   - Maneja tareas secuenciales y de control lógico.  

2. **GPU (Graphics Processing Unit)**  
   - Masivamente paralela, ideal para cargas de trabajo en IA, simulaciones y procesamiento de gráficos.  

3. **FPGA (Field-Programmable Gate Array)**  
   - Reconfigurable, permite implementar arquitecturas personalizadas para acelerar algoritmos específicos.  

4. **TPU (Tensor Processing Unit)**  
   - Diseñada por Google para aprendizaje automático y redes neuronales profundas.  

5. **QPU (Quantum Processing Unit)** *(emergente)*  
   - Procesadores cuánticos integrados en ecosistemas híbridos (ejemplo: IBM Q Experience).  

6. **Interconexión de alto rendimiento**  
   - Buses, NoC (Network on Chip) y memorias compartidas/unificadas que permiten comunicación eficiente entre los distintos procesadores.  

<img src="https://github.com/user-attachments/assets/2086621c-ca50-40e6-b84e-ce72edb0a54e" width="550"> 

 > - (Segunda generacion arquitectura heterogenea)

---

## Ventajas y desventajas

| ✅ Ventajas | ⚠️ Desventajas |
|---|---|
| **Alto rendimiento**: cada procesador ejecuta la tarea para la que fue diseñado. | **Complejidad de programación**: requiere librerías, compiladores y APIs específicas. |
| **Eficiencia energética**: menor consumo frente a CPUs puras para cargas intensivas. | **Costos de desarrollo elevados** para hardware y software especializado. |
| **Flexibilidad**: integración de múltiples aceleradores según la aplicación. | **Problemas de compatibilidad** entre diferentes arquitecturas y estándares. |
| **Escalabilidad**: fundamental en supercomputación y centros de datos modernos. | **Curva de aprendizaje** pronunciada para desarrolladores. |

---

## Aplicaciones principales

- **Inteligencia Artificial y Machine Learning** (entrenamiento y despliegue de modelos a gran escala).  
- **Big Data y análisis masivo de información**.  
- **Simulaciones científicas**: clima, biología molecular, astrofísica.  
- **Industria del entretenimiento**: renderizado gráfico y efectos visuales.  
- **Supercomputación (HPC)**: sistemas híbridos CPU–GPU–FPGA que lideran el ranking TOP500.  


---
---

# 5) 🌐 Computación de Borde (Edge Computing)

La **computación de borde** consiste en procesar datos **cerca de la fuente donde se generan** (sensores, cámaras, dispositivos IoT), en lugar de enviarlos a un centro de datos o la nube. Esto reduce la **latencia**, 
el **consumo de ancho de banda** y mejora la **privacidad**. Es una arquitectura clave para aplicaciones en **tiempo real** como vehículos autónomos, industria 4.0 y ciudades inteligentes.

<img src="https://github.com/user-attachments/assets/ac6e650d-da8b-4959-b55d-6ef295a6cb6d" width="550"> 

---

## Historia

- **Década de 1990 – 2000:** surge el concepto de *Content Delivery Networks (CDN)*, acercando contenido a los usuarios para reducir latencia.  
- **2010s:** con el auge del IoT y el 5G, el borde se convierte en un enfoque para procesar datos localmente.  
- **Actualidad:** Edge Computing es un pilar de arquitecturas distribuidas, integrándose con **cloud computing**, **IA** y **computación heterogénea**.  

---

## Arquitectura de la computación de borde

1. **Dispositivos finales (IoT, móviles, sensores)**  
   - Generan datos de forma continua.  
   - Algunos incluyen capacidad básica de cómputo.  

2. **Nodos de borde (Edge Nodes/Gateways)**  
   - Procesan y filtran información cerca de la fuente.  
   - Pueden ejecutar modelos de IA y análisis en tiempo real.  

3. **MEC (Multi-access Edge Computing)**  
   - Estándar impulsado por 5G que habilita servicios de baja latencia en la red de acceso.  

4. **Capa de orquestación y nube híbrida**  
   - El procesamiento más pesado y almacenamiento masivo aún se realiza en la nube.  
   - El borde actúa como **primer filtro** para datos críticos y en tiempo real.  

👉 *Imagen E3 (Borde): Diagrama de arquitectura — Dispositivos → Edge Nodes → Nube.*

---

## Ventajas y desventajas

| ✅ Ventajas | ⚠️ Desventajas |
|---|---|
| **Baja latencia**: procesamiento local inmediato. | **Costo de infraestructura**: requiere nodos distribuidos. |
| **Menor tráfico de red**: se reduce la cantidad de datos enviados a la nube. | **Mantenimiento complejo**: más dispositivos que mantener y actualizar. |
| **Privacidad y seguridad**: datos sensibles permanecen cerca de la fuente. | **Recursos limitados**: los nodos de borde tienen menos potencia que un datacenter. |
| **Resiliencia**: operaciones locales continúan incluso con mala conexión a internet. | **Estandarización incompleta** en plataformas de edge. |

---

## Aplicaciones principales

- **Vehículos autónomos**: decisiones inmediatas de frenado, navegación y seguridad.  
- **Ciudades inteligentes**: gestión de tráfico, alumbrado, monitoreo ambiental.  
- **Industria 4.0**: control de maquinaria, mantenimiento predictivo en tiempo real.  
- **Salud digital**: monitoreo de pacientes con baja latencia y mayor privacidad.  
- **Realidad aumentada/virtual (AR/VR)**: experiencias inmersivas con baja latencia gracias al 5G.  

<img src="https://github.com/user-attachments/assets/981b9356-9b81-4a96-801e-b96f163ae0a2" width="550"> 


---

