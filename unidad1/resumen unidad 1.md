# Síntesis de la Unidad 1: Circuitos de Corriente Directa

---

## Semana 01: Fundamentos de la Electricidad y el Circuito como Sistema

### Magnitudes eléctricas básicas

| Magnitud | Símbolo | Definición | Fórmula | Unidad |
|---|---|---|---|---|
| Carga | Q | Propiedad fundamental de los materiales (cantidad de electrones en exceso o déficit) | — | Culombio (C) |
| Corriente | I | Flujo de carga por unidad de tiempo | I = Q/t | Amperio (A) |
| Voltaje | V | Diferencia de potencial entre dos puntos | V = W/Q | Volt (V) |
| Resistencia | R | Dificultad que encuentra la corriente al pasar por un material | — | Ohm (Ω) |
| Conductancia | G | Facilidad con que pasa la corriente | G = 1/R | Siemens (S) |

### Clasificación de materiales

Los materiales se clasifican según la cantidad de electrones de valencia que tienen:

- **Conductores:** de 1 a 3 electrones de valencia (ejemplo: cobre).
- **Semiconductores:** 4 electrones de valencia (ejemplo: silicio).
- **Aislantes:** de 5 a 8 electrones de valencia (ejemplo: vidrio).

### Circuito eléctrico

Sistema formado por una **fuente de alimentación**, **conductores**, **carga** y **elemento de control**. Tiene que ser un circuito cerrado.

### Tipos de circuitos

- **Circuito cerrado:** el conductor está cerrado y por él circula corriente.
- **Circuito abierto:** no hay corriente (I = 0).
- **Cortocircuito:** circuito cerrado con resistencia muy pequeña (casi 0) y por él pasa una corriente peligrosa.

### Instrumentación

- **Amperímetro:** se coloca en **serie**.
- **Voltímetro:** se coloca en **paralelo**.
- **Óhmetro:** se usa con el circuito desconectado (desenergizado).

---

## Semana 02: Resistencia, Ley de Ohm, Potencia y Energía

### Factores que afectan a la resistencia

En un conductor:

$$R = \rho \cdot \frac{L}{A}$$

Depende de:

- La resistividad (ρ) del material.
- La longitud (L).
- El área transversal (A) del conductor.
- La temperatura (T), a través del coeficiente α.

### Ley de Ohm

En los elementos óhmicos (con resistencia constante) existe una relación lineal entre voltaje y corriente:

$$V = I \cdot R$$

### Potencia y Efecto Joule

La potencia es la rapidez con que se transforma la energía:

$$P = V \cdot I = I^2 \cdot R = \frac{V^2}{R} \quad [W]$$

Toda la potencia disipada en una resistencia se convierte en calor (**Efecto Joule**).

### Energía y selección de componentes

- La energía es el consumo de potencia en el tiempo: **E = P · t** [J] o [kWh].
- Para evitar fallos térmicos en los componentes resistivos hay que tener un margen de seguridad: el componente debe soportar al menos el doble de la potencia disipada.

$$P_{nom} \geq 2P$$

---

## Semana 03: Circuitos en Serie, LVK y Divisor de Tensión

### Características de un circuito en serie

- Solo hay un camino cerrado.
- Todos los elementos están en serie, por lo que por todos ellos circula la **misma corriente**.

### Resistencia equivalente

$$R_{eq} = R_1 + R_2 + \dots + R_n$$

Es mayor que el valor de la resistencia más alta.

### Ley de Voltajes de Kirchhoff (LVK)

- En todo lazo cerrado la suma de los voltajes es cero: **∑V = 0**.
- Equivalente: las subidas de tensión son iguales a las caídas de tensión: **∑subidas = ∑caídas**.
- Es una ley de **conservación de la energía**.

### Divisor de tensión

Permite repartir el voltaje entre los elementos en proporción a sus resistencias:

$$V_x = E \cdot \frac{R_x}{R_{eq}}$$

### Fuentes reales

Las fuentes reales tienen una resistencia interna (R<sub>int</sub>). Al entregar corriente, la tensión en bornes baja:

$$V_t = E - I \cdot R_{int}$$

---

## Semana 04: Circuitos en Paralelo, LCK y Divisor de Corriente

### Características de un circuito en paralelo

Todos los elementos están entre los mismos dos nodos, por lo que tienen el **mismo voltaje**.

### Ley de Corrientes de Kirchhoff (LCK)

- En todo nodo la suma de corrientes que entran es igual a la suma de corrientes que salen: **∑I<sub>entrantes</sub> = ∑I<sub>salientes</sub>**.
- Es una ley de **conservación de la carga**.

### Resistencia equivalente

$$\frac{1}{R_{eq}} = \sum \frac{1}{R_k} \qquad (G_{eq} = \sum G_k)$$

Es menor que el valor de la resistencia más baja.

Para 2 elementos:

$$R_{eq} = \frac{R_1 \cdot R_2}{R_1 + R_2}$$

### Divisor de corriente

Permite repartir la corriente en función inversa de la resistencia:

$$I_x = I \cdot \frac{R_{eq}}{R_x}$$

Para 2 elementos:

$$I_1 = I \cdot \frac{R_2}{R_1 + R_2}$$

---

## Semana 05: Redes en Serie-Paralelo (Circuitos Mixtos)

### Reglas para determinar conexiones

- **Serie:** dos elementos están en serie si comparten un nodo (único) y en ese nodo no confluyen otras ramas.
- **Paralelo:** dos elementos están en paralelo si están entre los mismos dos nodos.

### Estrategia para resolver circuitos mixtos (reducción e ida/vuelta)

1. **Reducción:** reducir el circuito paso a paso. Se etiquetan los nodos y se buscan pares válidos para reducir. Así se obtiene la resistencia equivalente total (R<sub>eq</sub>) y la corriente que entrega la fuente:

   $$I = \frac{V_s}{R_{eq}}$$

2. **Vuelta:** se regresa sobre los bloques reducidos.
   - En los **paralelos** se marca el voltaje (V → I).
   - En los **series** se marca la corriente (I → V).

### Transformación de fuentes reales

Una fuente real de tensión (V<sub>s</sub> en serie con R<sub>s</sub>) es equivalente a una fuente real de corriente (I<sub>s</sub> en paralelo con R<sub>s</sub>):

$$I_s = \frac{V_s}{R_s}$$

### Comprobación final

Hay que verificar que todo esté bien calculado:

- Se cumplen las leyes de Kirchhoff (**LVK** y **LCK**).
- Se cumple el balance global de potencias:

$$P_{fuente} = \sum P_{resistencias}$$
