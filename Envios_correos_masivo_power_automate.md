

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

iNPUTS : @{items('Apply_to_each')?['CORREOS']}

*FILTER ARRAY*

![image](https://github.com/Miguelapp10/-Microsoft_Power_Platform/assets/114699192/d314e24a-a90a-4c17-bdf7-a544e7a5e7b9)

Aqui filtrara los datos que corresponde segun SELECT y COMPOSE_4.
*Create HTML table*

![image](https://github.com/Miguelapp10/-Microsoft_Power_Platform/assets/114699192/250f6616-9ae3-41fb-9d12-adb01e02b959)

EN VALUE: @{item()['BULTO']} y @{formatDateTime(item()['FECHA'],'dd-MM-yyyy')}

*COMPOSE 5*

![image](https://github.com/Miguelapp10/-Microsoft_Power_Platform/assets/114699192/88a3f2a8-609c-44c3-aa6b-da52c6a89b8a)

Aqui le das formato a la tabla HTML

*SEND AN EMAIL 

![image](https://github.com/Miguelapp10/-Microsoft_Power_Platform/assets/114699192/98413d7f-fef1-4689-afe0-e97388a7b02f)

Aqui pones los datos que has puestos en cada cada compose 2,3 y 4.

![image](https://github.com/Miguelapp10/-Microsoft_Power_Platform/assets/114699192/fe435aba-8437-4665-99aa-3a28a4f38a06)


![image](https://github.com/Miguelapp10/-Microsoft_Power_Platform/assets/114699192/489a6b95-0783-4db5-8802-d22952c7ff0b)

Aqui pones si deseas agregar los archivos de excel y la sensibilidad


