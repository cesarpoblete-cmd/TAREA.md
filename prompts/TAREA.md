# Tarea: Mi prompt avanzado 

## Tarea elegida 
Generar casos de prueba unitarios y funcionales para un módulo de registro de usuarios en una aplicación web (validación de correo electrónico, contraseña segura, campos obligatorios y correos duplicados).
## Version 1: prompt basico 

```text
Genera casos de prueba para el registro de usuarios de una pagina web.
```
* **Técnica agregada:** Ninguna (prompt directo).
* **Por qué:** Punto de partida para medir la respuesta inicial.
* **Qué mejoró:** Dio una lista muy genérica, desordenada y sin datos de prueba reales.

## Version 2 
```text
Actúa como Ingeniero QA Senior. Genera casos de prueba para el registro de usuarios (campos: nombre, email único y password de mínimo 8 caracteres). Divide la respuesta en:
1. Casos positivos
2. Casos negativos
3. Casos borde
```
* **Técnica agregada:** Ninguna (prompt directo / zero-shot básico).
* **Por qué:** Es el punto de partida inicial para evaluar qué responde la IA sin contexto técnico ni restricciones.
* **Qué mejoró:** Al ser la primera versión, la respuesta fue muy general y desordenada; entregó una lista simple con viñetas sin distinguir entre casos positivos o negativos ni definir datos de entrada exactos.

## Version 3: prompt final 
```text
Actúa como Ingeniero QA Senior. Genera casos de prueba para el registro de usuarios (campos: nombre, email único y password de mínimo 8 caracteres). Divide la respuesta en:
1. Casos positivos
2. Casos negativos
3. Casos borde
```

* **Técnica agregada:** Role Prompting y Prompt Estructurado.
* **Por qué:** Para obtener criterio técnico y clasificar los escenarios.
* **Qué mejoró:** Separó bien los tipos de prueba e incluyó validaciones de límites, pero seguía en formato de texto largo.

## Tecnicas usadas en el prompt final 

| Técnica | Parte del prompt donde se aplica |
| :--- | :--- |
| **Role Prompting** | *"Actúa como Ingeniero QA Senior."* |
| **Prompt Estructurado** | División en bloques: objetivo, pasos, ejemplo y reglas finales. |
| **Chain of Thought** | Lista numerada *"Pasos"* antes de generar la tabla. |
| **Few-Shot** | Tabla de ejemplo con el caso `CP-01`. |
| **Autocrítica** | Última regla pidiendo revisar si faltó algún caso de seguridad. |


## Evaluacion del resultado 


| Criterio | ¿Cumple? (Sí / No) |
| :--- | :--- |
| ¿Usó terminología técnica adecuada de QA? | Sí |
| ¿Respetó el formato exacto de tabla Markdown? | Sí |
| ¿Incluyó datos JSON válidos y códigos HTTP? | Sí |
| ¿La autocrítica detectó casos faltantes? | Sí |


## Por que elegi estas tecnicas

Elegí estas técnicas porque en pruebas de software se necesita precisión y un formato estándar. El rol de QA y la estructura evitaron respuestas vagas; Chain of Thought ordenó el análisis de validaciones; Few-Shot aseguró una tabla lista para copiar, y la autocrítica permitió detectar casos límite de seguridad que suelen omitirse.