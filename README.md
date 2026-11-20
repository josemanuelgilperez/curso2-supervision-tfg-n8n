# Supervisión de un TFG con n8n e IA

Repositorio público de demostración para la sesión 5 del curso **Automatización y agentes de IA para la docencia universitaria (nivel intermedio)** de la UCLM.

## Enlaces públicos

- Repositorio: <https://github.com/josemanuelgilperez/curso2-supervision-tfg-n8n>
- Proyecto: <https://github.com/users/josemanuelgilperez/projects/9>
- Caso suficiente (`F0-01`): <https://github.com/josemanuelgilperez/curso2-supervision-tfg-n8n/issues/1>
- Caso incompleto (`F0-02`): <https://github.com/josemanuelgilperez/curso2-supervision-tfg-n8n/issues/2>
- Caso sin entregable (`F0-03`): <https://github.com/josemanuelgilperez/curso2-supervision-tfg-n8n/issues/3>

## Finalidad

El repositorio representa un TFG ficticio organizado mediante issues de GitHub. Cada issue describe una fase, identifica un entregable y establece criterios de aceptación. El workflow de n8n deberá:

1. Recibir la URL de un issue.
2. Leer su estructura y localizar el entregable solicitado.
3. Comprobar de forma determinista si el archivo existe.
4. Valorar su contenido frente a los criterios del issue con ayuda de IA.
5. Validar la respuesta de la IA.
6. Seleccionar una acción dentro de un conjunto cerrado.
7. Generar un informe sin modificar GitHub.

## Casos disponibles

| Código | Situación preparada | Resultado general esperado |
| --- | --- | --- |
| `F0-01` | El entregable existe y cubre los criterios principales. | `marcar_fase_preparada` |
| `F0-02` | El entregable existe, pero es claramente incompleto. | `solicitar_cambios` |
| `F0-03` | El issue solicita un archivo que no existe. | `indicar_entregables_faltantes` |

Los resultados esperados sirven para comprobar el comportamiento del workflow. La redacción exacta del informe puede variar, pero la acción final debe pertenecer al conjunto autorizado.

## Estructura

- `.github/ISSUE_TEMPLATE/`: plantilla utilizada para las fases del TFG.
- `docs/entregas/`: entregables ficticios disponibles.
- `casos/issues/`: copias de los cuerpos usados para crear los issues públicos.
- `casos/resultados_esperados.json`: oráculo de prueba de los tres casos.

## Uso docente

El contenido es completamente ficticio. El repositorio no contiene datos personales, trabajos reales de estudiantes, credenciales ni información confidencial. Durante la práctica, los workflows deben trabajar únicamente en modo de lectura.

