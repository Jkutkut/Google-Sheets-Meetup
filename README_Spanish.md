# Google-Sheets-Meetup

### Objetivo del projecto:

Tener una manera fácil de organizar una reunión de cualquier tipo en un periodo de tiempo definido.

Dado el comienzo de un mes (Date of reference, celda B1 en la Hoja Principal), las funciones aquí presentadas nos permiten visualizar posibles fechas para realizar la reunión en ese periodo de tiempo.

Cada usuario debe tener una hoja personal para que el script funcione (duplicando la hoja del administrador del archivo, puesto que funcionan de la misma manera).

Cuando todo está rellenado de manera correcta, la hoja principal ("Main") mostrará el calendario con la cantidad de usuarios disponibles cada día, de acuerdo con el criterio definido en la función "peopleReady" de el archivo customfunctions.js.


## Contenido
Contiene dos funciones con las siguientes características:

*· DIACALENDARIO*: genera de manera dinámica un calendario basado en una Fecha de referencia ("Date of reference").

   En mi caso, uso esta función para que me enseñe el nº de cada día del mes.

     `=DIACALENDARIO($B$1;$Q$6;$Q$5;FILA();COLUMNA();DIASEM(FIN.MES($B$1; -1);2);DIA(FIN.MES($B$1;0)))`

*peopleReady*: Comprueba el resto de hojas en el documento para contar la cantidad de usuarios disponibles ese día.
   
   La manera de usar esta función es la siguiente:
      
      `=peopleReady(FILA();COLUMNA())`

*#Nota1:*
   El formato del día de la semana (Lunes, L, M...) también se puede cambiar desde ajustes:

   Siendo el último número de la función el día de la semana (ej: 1 = Lunes, 2 = Martes...)   
      
      `=INDIRECTO("Main!" & Main!$Q$7 & 1)`
      
*#Nota2:*
   Para hacer la aparienza más atractiva, se ha usado formato condicional, El uso o no de este formato no afecta a la lógica del programa


Demostración de del funcionamiento:

![EgMain](https://github.com/Jkutkut/Google-Sheets-Meetup/blob/master/resources/MeetupEgMain.png)
![egSheets](https://github.com/Jkutkut/Google-Sheets-Meetup/blob/master/resources/Google_sheet_demo_sheets.png)
![Settings](https://github.com/Jkutkut/Google-Sheets-Meetup/blob/master/resources/Google_sheet_settings.png)
![sheetRoot](https://github.com/Jkutkut/Google-Sheets-Meetup/blob/master/resources/Google_sheet_demoRoot.png)
![sheetUser1](https://github.com/Jkutkut/Google-Sheets-Meetup/blob/master/resources/Google_sheet_demoUser1.png)