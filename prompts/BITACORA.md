# Bitacora de prompts

Laboratorio 06: Fundamentos de Ingenieria de Prompts.
Herramienta de IA usada: Gemini

## Ejercicio 2: Tokens y ventana de contexto

| Texto                              | Caracteres | Tokens |
| ---------------------------------- | ---------- | ------ |
| Los estudiantes programan en Java. | 34         | 7      |
| The students program in Java.      | 29         | 6      |
| desafortunadamente                 | 18         | 4      |

## Ejercicio 3: Temperatura

### Resultados del Simulador en Java

| Temperatura | Nombres generados (5 intentos)                        | Comportamiento observado                                                                |
| ----------- | ----------------------------------------------------- | --------------------------------------------------------------------------------------- |
| **0**       | BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec | 100% determinista. Siempre elige la opción con el puntaje más alto.                     |
| **0.5**     | BiblioTec, LibroYa, PrestaLibro, BiblioTec, BiblioTec | Selecciona principalmente la opción más probable con ligeras variaciones.               |
| **1.0**     | BiblioTec, BiblioTec, BiblioTec, LibroYa, PrestaLibro | Variabilidad moderada y balanceada.                                                     |
| **1.8**     | LectoGo, BiblioTec, PaginaLibre, LibroYa, LibroYa     | Alta creatividad e impredecibilidad; selecciona opciones con baja probabilidad inicial. |

**Conclusión:**

- **Temperatura baja (0.0 - 0.2):** Recomendada para código y datos exactos, ya que elimina la aleatoriedad[cite: 1].
- **Temperatura alta (0.8 - 1.8):** Recomendada para lluvia de ideas, nombres y redacción creativa[cite: 1].

## Ejercicio 4: Prompt vago vs estructurado

| Criterio                            | Prompt vago | Prompt estructurado |
| ----------------------------------- | ----------- | ------------------- |
| Menciona el objetivo del sistema    | No          | Si                  |
| Menciona a los usuarios principales | No          | Si                  |
| Tiene exactamente 3 funcionalidades | No          | Si                  |
| Esta en 3 parrafos                  | No          | Si                  |
| Lo usaria en un informe real        | No          | Si                  |

## Ejercicio 5: Anatomia de un prompt

### 1. Identificación de los componentes del prompt

| Componente  | Texto de mi prompt                                                                                   |
| ----------- | ---------------------------------------------------------------------------------------------------- |
| Rol         | Actua como desarrollador Java.                                                                       |
| Instruccion | Crea un programa en Java usando una clase Producto con los atributos codigo, nombre, precio y stock. |
| Contexto    | para gestionar los productos de una tienda.                                                          |
| Ejemplo     | Usa este estilo para los metodos: getPrecio(), setPrecio(double precio).                             |
| Formato     | Explica primero la estructura de la clase y luego presenta el codigo Java.                           |

---

### 2. Cambios observados por nivel

- **Nivel 1:** La IA genera un código genérico cualquiera (ej. un "Hola Mundo" o una calculadora simple)[cite: 1].
- **Nivel 2 (+ Rol):** Aplica mejores prácticas de un desarrollador Java en la estructura general del código[cite: 1].
- **Nivel 3 (+ Contexto):** Adapta la solución específicamente a la gestión de productos de una tienda[cite: 1].
- **Nivel 4 (+ Instrucción):** Crea la clase `Producto` con los 4 atributos exactos solicitados (`codigo`, `nombre`, `precio`, `stock`).
- **Nivel 5 (+ Formato y Ejemplo):** Separa la explicación conceptual antes del código y utiliza la convención solicitada para los métodos getter/setter[cite: 1].

## Ejercicio 6: Del prompt basico al profesional

## Ejercicio 6: Del prompt basico al profesional

### 1. Evaluación del Prompt Profesional

| Qué revisar                                            | Cumple (Sí / No) |
| ------------------------------------------------------ | ---------------- |
| ¿Está escrito en Java y usa Swing?                     | Sí               |
| ¿Pide correo y contraseña?                             | Sí               |
| ¿Explica el funcionamiento antes o después del código? | Sí               |
| ¿El código está organizado en clases?                  | Sí               |
| ¿Valida los datos que ingresa el usuario?              | Sí               |

---

### 2. Prompt final con iteraciones

```text
Prompt inicial:
Actua como desarrollador Java. Crea un ejemplo de login para una aplicacion de escritorio utilizando Swing. El usuario debe ingresar correo y contrasena. Explica brevemente el funcionamiento y presenta el codigo organizado por clases.

Prompt de mejora (iteración):
Mejora el codigo anterior con estas restricciones: no uses librerias externas, valida que el correo contenga @ y que la contrasena tenga al menos 8 caracteres, y muestra los mensajes con JOptionPane.
```

- [Bitacora de prompts](prompts/BITACORA.md)
