# 💻 Tarea 2: Exploración de Arquitecturas de Computación Emergentes

Este repositorio contiene la investigación sobre diversas arquitecturas de computación avanzadas y emergentes, enfocándose en sus principios, historia, ventajas y desventajas. 
El objetivo es proporcionar un panorama completo de estas tecnologías que están definiendo el futuro del campo

---

##  📑 Contenido

1. [Primer Punto: Computación Cuántica](#primer-punto-computación-cuántica)  
- Definición de computación Cuántica
- Arquitectura y partes clave
- Historia de la computación cuántica, ventajas y desventajas
- Conceptos como superposición, entrelazamiento, compuertas cuánticas, etc...

3. [Segundo Punto: Computación Neuromórfica](#segundo-punto-computación-neuromórfica)  
- Definición computador neuromórfico
- Arquitectura, funcionamiento, ventajas y desventajas
- Hardware utilizado en la computación neuromórfica
- Tipos de computación neuromórfica

4. [Tercer Punto: Ordenadores Biológicos](#tercer-punto-ordenadores-biológicos)  
- Definición de ordenadores biológicos
- Arquitectura, tipos y principales hitos

5. [Cuarto Punto: Arquitectura de Computación Heterogénea](#cuarto-punto-Arquitectura-de-computación-heterogénea)
- Definición de arquitectura de computación heterogénea
- Historia, ventajas y desventajas

6. [Quinto Punto: Arquitectura de Computación de Borde](#cuarto-punto-Arquitectura-de-computación-heterogénea)
- Definición de arquitectura de computación de borde
- Historia, ventajas y desventajas

---
## 1) Computación cuántica
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

### 1.2) 🏗️ **ARQUITECTURA**
La arquitectura de una computadora cuántica no se limita a procesar información: es un sistema altamente especializado que protege los estados cuánticos frágiles contra la decoherencia y traduce las 
instrucciones clásicas en operaciones físicas a nivel cuántico.

### **1. El Stack Arquitectónico Híbrido**

- **Las computadoras cuánticas son sistemas híbridos:** combinan componentes clásicos y cuánticos en un stack de múltiples capas.

- **Procesador Anfitrión (Host Processor):** ejecuta el software de alto nivel y compila los algoritmos cuánticos en instrucciones de bajo nivel.

- **Plano de Control y Medición:** convierte esas instrucciones en pulsos físicos (microondas, láseres) y procesa las señales de salida de los cúbits.

- **Plano de Datos Cuánticos (Quantum Data Plane):** alberga la Unidad de Procesamiento Cuántico (QPU), donde residen los cúbits físicos y se realizan las operaciones cuánticas.

📌 Este flujo traduce el lenguaje digital clásico en señales físicas y, tras la medición, lo devuelve al dominio clásico. La fidelidad de esta traducción determina el rendimiento del sistema.

### **La Materialización del Cúbit: Plataformas Físicas en Competencia**

No existe una única forma de construir un cúbit. Varias tecnologías físicas compiten para convertirse en la plataforma dominante, cada una con un conjunto único de ventajas y desafíos en términos de velocidad, estabilidad y escalabilidad.

- ***Cúbits Superconductores:*** Actualmente, es la tecnología líder, utilizada por empresas como IBM y Google. Se basan en circuitos eléctricos fabricados con materiales superconductores como el aluminio, enfriados a temperaturas extremadamente bajas. Utilizan un componente no lineal llamado unión Josephson para crear niveles de energía discretos y desiguales, comportándose como un "átomo artificial" cuyos dos niveles más bajos pueden usarse como los estados ∣0⟩ y ∣1⟩ de un cúbit. El tipo más común se conoce como "transmon".

- ***Iones Atrapados:*** Este enfoque utiliza átomos individuales que han sido ionizados (se les ha quitado un electrón) y son confinados en el vacío mediante campos electromagnéticos generados por un chip. Los estados del cúbit se codifican en los niveles de energía electrónicos hiperfinos del ion, que son extremadamente estables. Empresas como IonQ y Quantinuum lideran esta tecnología.

- ***Cúbits Fotónicos:*** Utilizan partículas de luz, fotones, como cúbits. La información cuántica se puede codificar en propiedades como la polarización (horizontal/vertical) o la ruta que sigue el fotón. Su principal ventaja es que son muy resistentes a la decoherencia y pueden operar a temperatura ambiente, lo que simplifica enormemente la infraestructura.

- ***Átomos Neutros:*** Una tecnología emergente y prometedora que utiliza átomos sin carga eléctrica, atrapados individualmente en el espacio mediante "pinzas ópticas", que son rayos láser muy enfocados. Los estados del cúbit se definen por los estados electrónicos del átomo.

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

