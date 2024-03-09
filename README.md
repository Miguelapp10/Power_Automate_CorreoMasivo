#  Power automate // Envio de correos masivos para proveedores o clientes
Esta automatizacion de flujo de caja sobre envio de correo para proveedores y/o clientes nos permitio lo siguiente:

- Power Automate automatiza tareas repetitivas de envío de correos electrónicos, lo que ahorra tiempo y recursos humanos.
- Reducción de la carga de trabajo manual, permitiendo que el personal se enfoque en tareas más estratégicas y de mayor valor.
- Permite la personalización del contenido de los correos electrónicos en función de variables o datos específicos, lo que mejora la relevancia y la personalización para cada destinatario.
- Power Automate permite programar el envío de correos electrónicos en momentos específicos, lo que garantiza la entrega oportuna de información relevante.
- Ofrece un control detallado sobre la ejecución de los flujos de trabajo, incluida la capacidad de establecer condiciones y reglas.
- Proporciona capacidades de seguimiento y monitorización para evaluar el rendimiento de los flujos de trabajo.
-  Facilita la identificación de posibles problemas o áreas de mejora en los procesos de envío de correos masivos.
-  Contribuye a garantizar el cumplimiento de políticas y procedimientos al seguir flujos de trabajo predefinidos y consistentes.
- Minimiza el riesgo de errores humanos al estandarizar y automatizar procesos.

A continuacion le mostrare el flujo que elabore:

*RECURRENCE*

![image](https://github.com/Miguelapp10/-Microsoft_Power_Platform/assets/114699192/afa17b9c-f681-4f6c-b666-60fdedd20dfa)

Esta permite programar la ejecución de un flujo de trabajo en intervalos regulares y predefinidos. En otras palabras, puedes configurar una tarea para que se repita automáticamente a intervalos específicos, como cada día, semana, mes, etc.

*LIST ROWS PRESENT IN A TABLE*

![image](https://github.com/Miguelapp10/-Microsoft_Power_Platform/assets/114699192/c348bb07-b1a6-422c-93d3-e29aa94005ca)

Si en el caso deseas enviar informacion no repetidas del dia ayer se debera agregar una formula en el excel la siguiente codicion:
![image](https://github.com/Miguelapp10/-Microsoft_Power_Platform/assets/114699192/9df90673-0c2f-48af-bade-f0cf21a6926e)

Muy importante! 
En pagination siempre poner 5000 para que el flujo pueda las 5000 primeras filas del excel web.
![image](https://github.com/Miguelapp10/-Microsoft_Power_Platform/assets/114699192/04fd4dce-a485-40ed-98e7-9d7c6c46967f)

*SELECT*

![image](https://github.com/Miguelapp10/-Microsoft_Power_Platform/assets/114699192/93040a5d-1c6d-4162-89a9-2ba3e0b50fd4)

*COMPOSE*

![image](https://github.com/Miguelapp10/-Microsoft_Power_Platform/assets/114699192/6e8bd1b9-b686-45f8-9678-90b3c63dca6a)

iNPUTS : @{union(body('Select'),body('Select'))}

![image](https://github.com/Miguelapp10/-Microsoft_Power_Platform/assets/114699192/c277c880-56ca-4817-8e03-d16b690d6535)

En el compose 2,3 y 4 van los datos que has seleccionado en SELECT.

Por ejemplo:

*COMPOSE 4*

![image](https://github.com/Miguelapp10/-Microsoft_Power_Platform/assets/114699192/680fd9ac-bf34-4938-8456-4d5e2593de2e)



