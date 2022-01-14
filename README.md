# ejercicio_1102.sh

##### Literal 1

- Primero nos ubicamos en la carpeta con los datos que nos solicita el ejercicio, en este caso:

Dell@DellG7Andres MINGW64 ~

$ cd Documents/
 
Dell@DellG7Andres MINGW64 ~/Documents

$ cd practica\ bio/CSB-master

Dell@DellG7Andres MINGW64 ~/Documents/practica bio/CSB-master

$ cd unix/

Dell@DellG7Andres MINGW64 ~/Documents/practica bio/CSB-master/unix

$ cd data

- Luego, vamos a ver la estructura del archivo solicitado en el ejercicio con el comando:

Dell@DellG7Andres MINGW64 ~/Documents/practica bio/CSB-master/unix/data

$ head -n 3 Gesquiere2011_data.csv

maleID  GC      T
1       66.9    64.57
1       51.09   35.57


- Ahora lo que nos pide el ejercicio es extraer todas las filas en las que la primera columna sea 3 o 27 y contarlas para lo que utilizamos:

Dell@DellG7Andres MINGW64 ~/Documents/practica bio/CSB-master/unix/data

$ cut -f 1 Gesquiere2011_data.csv | grep -c -w 3

61


Dell@DellG7Andres MINGW64 ~/Documents/practica bio/CSB-master/unix/data

$ cut -f 1 Gesquiere2011_data.csv | grep -c -w 27

5

- Aqui terminaria el literal 1


##### Literal 2

- Para esta parte el ejercicio nos pide imprimir como entrada el nombre del archivo y la identificación del individuo,y devolver el número de registros para esa identificación para lo cual utilizamos: 


Dell@DellG7Andres MINGW64 ~/Documents/practica bio/CSB-master/unix/data

$ bash count_baboons.sh Gesquiere2011_data.csv 27

5



##### Literal 3

- Para esta esta parte del ejercicio nos pide obtener el número de veces que cada individuo fue muestreado, para lo cual utilizamos: 


Dell@DellG7Andres MINGW64 ~/Documents/practica bio/CSB-master/unix/data

$ myIDS=`tail -n +2 Gesquiere2011_data.csv | cut -f 1 | sort -n | uniq` 


Dell@DellG7Andres MINGW64 ~/Documents/practica bio/CSB-master/unix/data

$ for id in $myIDS

> do

>     mycounts=`bash count_baboons.sh Gesquiere2011_data.csv $id`

>     echo "ID:" $id "counts:" $mycounts

> done

ID: 1 counts: 10

ID: 2 counts: 2

ID: 3 counts: 61

ID: 4 counts: 46

ID: 5 counts: 28

ID: 6 counts: 7

ID: 7 counts: 5

ID: 8 counts: 17

ID: 9 counts: 4

ID: 10 counts: 21

ID: 11 counts: 26

ID: 12 counts: 23

ID: 13 counts: 16

ID: 14 counts: 1

ID: 15 counts: 40

ID: 16 counts: 31

ID: 17 counts: 3

ID: 18 counts: 4

ID: 19 counts: 3

ID: 20 counts: 4

ID: 21 counts: 12

ID: 22 counts: 5

ID: 23 counts: 36

ID: 24 counts: 35

ID: 25 counts: 35

ID: 26 counts: 22

ID: 27 counts: 5

ID: 29 counts: 33

ID: 30 counts: 63

ID: 31 counts: 1

ID: 32 counts: 3

ID: 33 counts: 1

ID: 34 counts: 16

ID: 35 counts: 5

ID: 36 counts: 39

ID: 37 counts: 38

ID: 38 counts: 1

ID: 39 counts: 3

ID: 40 counts: 32

ID: 41 counts: 53

ID: 42 counts: 5

ID: 43 counts: 2

ID: 44 counts: 56

ID: 45 counts: 1

ID: 46 counts: 24

ID: 47 counts: 34

ID: 48 counts: 23

ID: 49 counts: 19

ID: 50 counts: 21

ID: 51 counts: 25

ID: 52 counts: 6

ID: 53 counts: 3

ID: 54 counts: 22

ID: 55 counts: 20

ID: 56 counts: 41

ID: 57 counts: 46

ID: 58 counts: 1

ID: 59 counts: 25

ID: 60 counts: 51

ID: 61 counts: 20

ID: 62 counts: 13

ID: 63 counts: 35

ID: 64 counts: 34

ID: 65 counts: 38

ID: 66 counts: 20

ID: 67 counts: 1

ID: 68 counts: 10

ID: 69 counts: 22

ID: 70 counts: 33

ID: 71 counts: 5

ID: 72 counts: 2

ID: 73 counts: 10

ID: 74 counts: 1

ID: 75 counts: 15

ID: 76 counts: 39

ID: 77 counts: 2

ID: 78 counts: 29

ID: 79 counts: 4

ID: 80 counts: 35

ID: 81 counts: 1

ID: 82 counts: 27

ID: 83 counts: 2

ID: 84 counts: 11

ID: 85 counts: 1

ID: 86 counts: 39

ID: 87 counts: 18

ID: 88 counts: 46

ID: 89 counts: 25

ID: 90 counts: 24

ID: 91 counts: 32

ID: 92 counts: 1

ID: 93 counts: 7

ID: 94 counts: 25

ID: 95 counts: 71

ID: 96 counts: 17

ID: 97 counts: 17

ID: 98 counts: 5

ID: 99 counts: 2

ID: 100 counts: 13

ID: 101 counts: 26

ID: 102 counts: 15

ID: 103 counts: 26

ID: 104 counts: 29

ID: 105 counts: 6

ID: 106 counts: 46

ID: 107 counts: 7

ID: 108 counts: 41

ID: 109 counts: 28

ID: 110 counts: 3

ID: 111 counts: 24

ID: 112 counts: 3

ID: 113 counts: 1

ID: 114 counts: 1

ID: 115 counts: 1

ID: 116 counts: 14

ID: 118 counts: 23

ID: 119 counts: 1

ID: 120 counts: 42

ID: 121 counts: 12

ID: 122 counts: 9

ID: 123 counts: 39

ID: 124 counts: 1

ID: 125 counts: 39

ID: 126 counts: 15

ID: 127 counts: 13



## FIN
