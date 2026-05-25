# Caracterizacion-Panel-Solar-con-STM32
# Diseño e implementación de un convertidor Buck alimentado mediante panel solar con control basado en STM32 y sistema de protección integrado

## Descripción

Este proyecto consiste en el diseño e implementación de un convertidor DC-DC tipo Buck alimentado por un panel solar de 450 W. El sistema incorpora una fuente auxiliar de 5 V para alimentar la etapa de control, un microcontrolador STM32 encargado del control PWM y un conjunto de protecciones eléctricas para garantizar la operación segura.

---

## Objetivo general

Diseñar e implementar un sistema de conversión DC-DC tipo Buck alimentado mediante un panel solar de 450 W, incorporando una fuente auxiliar de 5V para el circuito de control y un microcontrolador STM32 encargado de regular el funcionamiento y aplicar protecciones.

---

## Objetivos específicos

- Caracterizar el comportamiento del panel solar mediante una fuente DC controlada.
- Diseñar un convertidor Buck para operación con entrada solar.
- Diseñar una fuente auxiliar de 5V.
- Implementar protecciones mediante STM32.
- Diseñar el esquema eléctrico y PCB en KiCad.

---

## Especificaciones del panel solar

| Parámetro | Valor |
|------------|--------|
| Voltaje máxima potencia | 44.6V |
| Corriente máxima potencia | 10.09A |
| Potencia máxima | 450W |

---

## Protecciones implementadas

### Sobrevoltaje

Condición:

Vin > 50V

Acción:

- Desactivar PWM
- Activar alarma LED

### Sobrecorriente

Condición:

I > 10A

Acción:

- Desactivar MOSFET

### Temperatura

Condición:

T > 80°C

Acción:

- Reducir duty cycle
- Apagar sistema

### Bajo voltaje

Condición:

Vin < 15V

Acción:

- Desactivar convertidor

### Cortocircuito

Acción:

- PWM = 0%

---

## Variables monitoreadas

ADC1 → Voltaje del panel

ADC2 → Corriente del panel

ADC3 → Voltaje de salida

ADC4 → Temperatura

PWM → Control del convertidor Buck

---

## Software utilizado

- KiCad
- STM32CubeIDE

---

## Resultados esperados

- Regulación estable del convertidor Buck
- Fuente auxiliar funcional de 5V
- Curvas I-V y P-V del panel
- Protecciones automáticas
- PCB funcional
- Código y documentación disponibles
