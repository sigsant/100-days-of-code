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
 
