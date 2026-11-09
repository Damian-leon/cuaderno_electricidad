# Resumen de la Unidad 1: Circuitos de Corriente Directa

---

### **Semana 01: Fundamentos de la Electricidad y el Circuito como Sistema**
* **Magnitudes eléctricas básicas**: La **carga ($Q$)** es una propiedad fundamental de la materia medida en culombios (C). La **corriente ($I$)** es la tasa de flujo de carga por unidad de tiempo ($I = \frac{Q}{t}$) en amperios (A). El **voltaje ($V$)** es la diferencia de potencial o energía por unidad de carga entre dos puntos ($V = \frac{W}{Q}$) en voltios (V). La **resistencia ($R$)** representa la oposición al flujo de corriente en ohmios ($\Omega$), mientras que la **conductancia ($G = \frac{1}{R}$)** mide la facilidad de conducción en siemens (S).
* **Clasificación de materiales**: Según sus electrones de valencia, los materiales se dividen en **conductores** (1 a 3 e⁻, ej. cobre), **semiconductores** (4 e⁻, ej. silicio) y **aislantes** (5 a 8 e⁻, ej. vidrio).
* **El circuito eléctrico**: Consta de fuente, conductores, carga y elemento de control en un camino cerrado. Puede estar **cerrado** (circula corriente), **abierto** ($I = 0$) o en **cortocircuito** (camino de resistencia casi nula con corriente peligrosa).
* **Instrumentación**: El amperímetro se conecta en **serie**, el voltímetro en **paralelo** y el óhmetro con el circuito **desenergizado** y desasociado.

---

### **Semana 02: Resistencia, Ley de Ohm, Potencia y Energía**
* **Factores de la resistencia**: En un conductor, $R = \frac{\rho \cdot L}{A}$, donde depende de la resistividad ($\rho$), la longitud ($L$), el área transversal ($A$) y la temperatura ($T$) mediante el coeficiente $\alpha$.
* **Ley de Ohm**: Establece la relación lineal $V = I \cdot R$, válida exclusivamente para **elementos óhmicos** con resistencia constante.
* **Potencia y Efecto Joule**: La potencia es la velocidad de transformación de energía ($P = V \cdot I = I^2 \cdot R = \frac{V^2}{R}$) en vatios (W). Por el **efecto Joule**, toda la potencia disipada en una resistencia se transforma en calor.
* **Energía y selección de componentes**: La energía consumida es $E = P \cdot t$ (en julios o kWh). Para evitar fallas térmicas, los componentes resistivos se seleccionan con un margen de seguridad donde su potencia nominal cumple $P_{nom} \ge 2 \cdot P$.

---

### **Semana 03: Circuitos en Serie, LVK y Divisor de Tensión**
* **Propiedades de la red en serie**: Existe una única trayectoria cerrada, por lo que circula la **misma corriente ($I$)** a través de todos los elementos.
* **Resistencia equivalente**: Se calcula como $R_{eq} = R_1 + R_2 + \dots + R_n$, siendo $R_{eq}$ estrictamente mayor que la resistencia individual más grande ($R_{eq} > R_{max}$).
* **Ley de Voltajes de Kirchhoff (LVK)**: Basada en la conservación de la energía, establece que la suma algebraica de los voltajes en cualquier lazo cerrado es cero ($\sum V = 0$ o $\sum \text{subidas} = \sum \text{caidas}$).
* **Divisor de tensión y fuentes reales**: Reparte el voltaje proporcionalmente: $V_x = E \cdot \frac{R_x}{R_{eq}}$. En fuentes reales con resistencia interna ($R_{int}$), el voltaje en terminales decae al entregar corriente: $V_t = E - I \cdot R_{int}$.

---

### **Semana 04: Circuitos en Paralelo, LCK y Divisor de Corriente**
* **Propiedades de la red en paralelo**: Todos los elementos están conectados entre los mismos dos nodos, compartiendo el **mismo voltaje ($V$)**.
* **Ley de Corrientes de Kirchhoff (LCK)**: Basada en la conservación de la carga, establece que en cualquier nodo la suma de corrientes entrantes es igual a la de salientes ($\sum I_{entrantes} = \sum I_{salientes}$).
* **Resistencia equivalente**: Cumple $\frac{1}{R_{eq}} = \sum \frac{1}{R_k}$ o $G_{eq} = \sum G_k$, siendo $R_{eq}$ siempre menor que la menor resistencia de la red. Para dos ramas: $R_{eq} = \frac{R_1 \cdot R_2}{R_1 + R_2}$.
* **Divisor de corriente**: Distribuye la corriente inversamente a la resistencia: $I_x = I \cdot \frac{R_{eq}}{R_x}$ (para dos ramas, $I_1 = I \cdot \frac{R_2}{R_1 + R_2}$).

---

### **Semana 05: Redes en Serie-Paralelo (Circuitos Mixtos)**
* **Criterios de conexión por nodos**:
  * **Serie**: Dos elementos comparten un **nodo exclusivo** sin que concurra una tercera rama.
  * **Paralelo**: Dos elementos están conectados exactamente entre los **mismos dos nodos**.
* **Estrategia de reducción e ida/vuelta**:
  1. **Reducción progresiva**: Identificar y combinar pares válidos por etapas etiquetando nodos hasta hallar la resistencia equivalente total ($R_{eq}$) y la corriente entregada por la fuente ($I = \frac{V_s}{R_{eq}}$).
  2. **Reconstrucción**: Volver sobre los bloques simplificados asignando voltajes en bloques en paralelo ($V \to I$) y corrientes en bloques en serie ($I \to V$).
* **Conversión de fuentes reales**: Una fuente real de voltaje ($V_s$ en serie con $R_s$) es equivalente exteriormente a una fuente real de corriente ($I_s = \frac{V_s}{R_s}$ en paralelo con la misma $R_s$).
* **Verificación final**: Todo cálculo debe ser auditado mediante LVK, LCK y el balance global de potencias ($P_{fuente} = \sum P_{resistencias}$).
