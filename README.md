# SpaceInvaders
_Juego simple sobre consola del cl�sico 4 en raya para jugar contra el ordenador o 2 jugadores_

---------------

El algoritmo utilizado para el juego del ordenador est� basado en el algoritmo del MiniMax con poda alfa beta. El programa est� desarrollado �ntegramente en C. Para compilarlo, basta con ejecutar en la carpeta del programa:

```
gcc -o 4enRaya.exe src/*.c
```

##Estructura del c�digo

El c�digo (todo �l en la carpeta **src/**) se ha dividido en un **main.c** y tres librer�as:
>  - **gamestuff.c**: contiene  funciones caracter�sticas del juego del 4 en raya en particular (como se decide una victoria, tama�o del tablero, como se aplica una tirada, funci�n heur�stica, etc).
>  - **minimaxvar.c**: contiene todas las funciones del algoritmo MiniMax. El _var_ hace referencia a que de hecho es una ligera variante del MiniMax, dividiendo el valor heur�stico de una partida mediante aumenta la profundidad del �rbol de decisi�n (esto hace que el ordenador opte antes por jugadas que le sean favorables lo antes posible).
>  - **highscores.c**: contiene funciones para el registro de r�cords.

## Advertencia

> **_El juego ha sido desarrollado en Windows y para Windows!!_**
> _Si se desea implementar en Linux, antes se deben cambiar tres cosas en el c�digo:_

> - Cambiar los "system("cls")" por "system("clear")".
> - Cambiar las funciones de la librer�a "conio.h" -getch(),gectche()- que no se tienen de forma predeterminada a Linux.
> - Cambiar las funciones Beep() -que hacen un ruidito cuando se presiona una tecla incorrecta- de la librer�a "Windows.h".

>_El juego no ha sido testeado en Mac OSX._


_Desarrollado por Mart�n Campos para la asignatura de 'Programaci� Avan�ada' del grado de Matem�ticas de la Universitat Aut�noma de Barcelona_