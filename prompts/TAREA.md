# Tarea: Mi prompt profesional

## Funcionalidad elegida

Sistema de Registro de Clientes en Java Swing con tabla visual y validaciones.

## Version 1: prompt basico

```text
Crea un sistema de registro de clientes en Java.
```

Qué cambié: Se solicitó únicamente la idea general sin dar contexto de interfaz ni estructura.

Por qué: Para evaluar qué tipo de respuesta genera la IA sin ninguna restricción.

Qué mejoró: La respuesta generó una clase por consola simple, pero carecía de interfaz gráfica, validaciones y organización.

## Version 2

Crea un sistema de registro de clientes en Java Swing. El usuario debe poder ingresar Nombre, Correo y Telefono. Valida que el correo tenga @.

Qué cambié: Se especificó la tecnología (Java Swing), los campos de entrada y una validación de correo.

Por qué: Para obligar a la IA a generar una interfaz gráfica utilizable con al menos un filtro de datos.

Qué mejoró: La IA entregó un formulario visual funcional, pero todo en un solo archivo desordenado y sin mostrar los datos registrados.

## Version 3: prompt final

Actúa como un desarrollador Java Senior con experiencia en arquitectura Swing. Crea un sistema de registro de clientes para una tienda comercial. La interfaz debe permitir ingresar Nombre, Correo y Teléfono, y mostrar los clientes registrados en una tabla (JTable).

Ejemplo de entrada válida:
Nombre: Juan Pérez | Correo: juan@gmail.com | Teléfono: 987654321

Restricciones:

- No uses librerías externas (solo paquetes nativos javax.swing y java.awt).
- Valida que el correo contenga '@' y que el teléfono contenga solo números de 9 dígitos.
- Muestra los mensajes de error o éxito con JOptionPane.
- Separa el código en dos clases: Cliente (modelo) y VentanaCliente (interfaz).
- Muestra una breve explicación antes del código.

## Componentes del prompt final

| Componente                  | Texto en el prompt                                                                                     |
| --------------------------- | ------------------------------------------------------------------------------------------------------ |
| **Rol**                     | Actúa como un desarrollador Java Senior con experiencia en arquitectura Swing                          |
| **Instrucción**             | Crea un sistema de registro de clientes (...) y mostrar los clientes registrados en una tabla (JTable) |
| **Contexto**                | Para una tienda comercial                                                                              |
| **Ejemplos**                | Nombre: Juan Pérez \| Correo: juan@gmail.com \| Teléfono: 987654321                                    |
| **Formato / Restricciones** | No usar librerías externas, validación de correo/teléfono, uso de JOptionPane y división en 2 clases   |

## Evaluacion del resultado

| Criterio de evaluación                                                | Cumple (Sí / No) |
| --------------------------------------------------------------------- | ---------------- |
| ¿Usa Java Swing sin depender de librerías externas?                   | Sí               |
| ¿Muestra los registros acumulados en un JTable?                       | Sí               |
| ¿Valida el formato del correo y del teléfono usando JOptionPane?      | Sí               |
| ¿Aplica separación de responsabilidades en 2 clases (Modelo y Vista)? | Sí               |

## Errores que evite

1. **Ser demasiado general:** En la versión 1 no se especificó si era consola o interfaz gráfica. Se evitó definiendo explícitamente los campos (Nombre, Correo, Teléfono) y el componente visual `JTable`.
2. **No indicar el formato:** En las primeras versiones no se definió la estructura interna del código. Se evitó exigiendo la separación en dos clases específicas (`Cliente` y `VentanaCliente`).
