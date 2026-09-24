# Checkpoint 1 — Agente de ventas para ferretería y bazar

Workflow de n8n que recibe consultas mediante un Chat Trigger y las procesa con un AI Agent conectado a OpenAI Chat Model.

## Funcionamiento

* El agente atiende consultas comerciales siguiendo un System Prompt con rol, objetivos y restricciones.
* Tiene un límite de 7 iteraciones por ejecución.
* Puede activar Gmail como herramienta para derivar solicitudes que requieren atención de un vendedor.
* Un segundo nodo Gmail, conectado a la salida del agente, envía un reporte con el ID de ejecución, la consulta, la respuesta y las acciones realizadas.

## Validación

Se realizó una prueba manual de solicitud de cotización. El agente activó la herramienta Gmail, el reporte de observabilidad se envió y el workflow finalizó correctamente.

## Archivo de entrega

[checkpoint1_matias_lema.json](checkpoint1_matias_lema.json)

El archivo contiene la configuración exportada del workflow. Para ejecutarlo en otra instancia de n8n es necesario configurar credenciales propias de OpenAI y Gmail.
