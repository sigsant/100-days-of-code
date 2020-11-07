# #100DaysOfCode Log - Round 1 - Sigsant

**Meta:** Realizar una app CRUD por linea de comandos

*Link para futuras referencias* https://www.reddit.com/r/dailyprogrammer/comments/pihtx/intermediate_challenge_1

*Link del proyecto*: https://github.com/sigsant/go-event-planning

**Tecnología usada:** Golang

**Conocimientos previos:** Principiante - Conocimientos básicos en Golang.


## Log

### R1D1 : 3 de Noviembre de 2020

**Enlaces útiles**
  * https://golangdocs.com/reading-and-writing-csv-files-in-golang
  * https://golangcode.com/write-data-to-a-csv-file/
  * https://www.golanglearn.com/converting-csv-data-to-json-in-golang/ (¿futuras referencias en caso de convertir JSON?)
 

**Progreso de aprendizaje de hoy**
Estoy aprendiendo el guardado de datos en ficheros CSV y cómo añadir nuevas líneas. Del mismo modo estoy empezando a implementar en mis proyectos los módulos para
el uso de funciones y structs, para evitar la acumulación de datos en el fichero principal del programa.

**Recordatorios**
Refactorizar y limpiar los módulos para usarlo en otros submódulos menores y agrupados según su uso como componente. Evitar juntar los structs y
funciones al menos que sea necesario hacerlo.

**Progreso de la app**
 * El usuario puede seleccionar las opciones básicas del programa. Incluye un pequeño control para saber si la opción está disponible o no.
 * El usuario puede crear eventos. Éstos se guardan tanto internamente en la memoria del programa y en un fichero csv en el directorio.
 * Se realiza un formato de hora en caso de las horas y minutos contengan un dígito. 
 * Se realiza un formato de texto para que sea legible el evento tanto en el array 2D como en el fichero csv.
 
 
 ### R1D2 : 4 de Noviembre de 2020

**Enlaces útiles**
  * https://medium.com/@moriagape/how-to-read-csv-files-in-golang-a-quiz-app-b5c8891207a0
  * https://joneisen.me/programming/2013/06/23/golang-and-default-values.html
  
 
**Progreso de aprendizaje de hoy**
 Después de mirar la documentación oficial de Golang, no he podido encontrar una manera de obtener un formato de salida que permita mostrar los datos
 del fichero CSV en pantalla. Por suerte he encontrado una pequeña guía  que me ha servido de base para la solución a este problema que he enlazado 
 en la sección de arriba. La solución era asociar un struct que indicase las partes que compone con cada apartado del fichero CSV,
 tal como puede verse en mi [Gist](https://gist.github.com/sigsant/ceda6ae549caf910d9fbe978df1d81cc.js)
 
Por otra parte he decido añadir la posibilidad de que el usuario defina el nombre del fichero que se creará o, en caso de ya existir, manipular desde el 
programa si no está de acuerdo con el nombre por defecto "planning.csv". 
En relación a este problema, he notado que tiendo a complejizar los problemas, en lugar de buscar soluciones muchos más sencillas. Originalmente había considerado
crear valores por defecto en los argumentos de la función de abrir/crear fichero para reflejar el cambio de nombre del usuario. 
Al no existir esta opción en Golang debido a que dificulta el mantenimiento del código, al contrario que en Javascript o Python, he tenido que modificar
el enfoque del problema y aplicar el paquete flag.

He agregado un enlace con respecto a este problema con otras soluciones a partir de cambios en el esqueleto del struct o bien mediante el empleo de argumentos
variádicos.

**Recordatorios**
Al contrario que en otros lenguajes, he encontrado mucho más útil leer las notas y la documentación de cada módulo que compone el lenguaje desde el [Repositorio
oficial de Github](https://github.com/golang/go/tree/be943df58860e7dec008ebb8d68428d54e311b94/src) que desde la página web. Ayuda a entender la lógica del lenguaje y cómo se relaciona cada proceso cuando se invoca una función/interface.

**Progreso de la app**
 * Muestra en un formato legible todos los datos guardados en un fichero CSV. 
 * Añadido flag de apertura de fichero:  -csv nombre-del-fichero
 * Bugfixes y modularizacion de código en otros paquetes.
 
 ### R1D3 : 6 de Noviembre de 2020


**Progreso de aprendizaje de hoy**
No pude actualizar ayer debido a que no había avanzado nada en la aplicación. Pensaba diferentes maneras de como eliminar una línea de un fichero CSV a partir del siguiente flujo: 

> Archivo CSV --> Conversión a Array multidimensional [][]string a partir de un struct --> eliminación del index del array ([x][]) --> conversión del array modificado a CSV.

Actualmente me encuentro en el tercer paso y veo que no tengo muy claro el concepto de punteros y su uso en los structs. Entre ayer y hoy estuve mirando algunos paquetes de terceros para entender como ha sido resuelto este problema. No logré entender bien el concepto de "marshall"/"unmarshall" que emplean, por lo que tendré mirar tutoriales/guías/documentación para consolidar conocimientos.

Por otra parte, he estado considerando mirar a largo plazo la posibilidad de crear una interfaz gráfica (fyne parece fácil de entender) o, con casi toda seguridad, emplear una interfaz web usando Golang como Back-end y React para Front-end. Tal como encuentro la situación dudo que hasta febrero como muy pronto empiece a trabajar en esta idea hasta que mire los frameworks existentes en este lenguaje de programación.


 
