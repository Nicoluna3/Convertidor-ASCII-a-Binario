# Convertidor-ASCII-a-Binario

### ■ Objetivo: 
### Programa que convierte caracteres alfanuméricos ASCII a su respectivo valor en Binario

#### ■	Problema que resuelve
Este programa permite convertir cualquier caracter alfanumércio ASCII a un valor Binario, con el propósito
de facilitar el cotejo de resultados de ejercicios hechos tanto por alumnos como de profesores.
De igual forma puede ser utilizado para la elaboración de reactivos referentes a este tema ya sea para diseñar 
ejercicios como examenes por parte del profesor.

#### ■ Lenguaje utilizado:
Se considero el lenguaje de programación Julia, por ser un programa novedoso para mí y de alto rendimiento.

#### ■  Tema que ayuda a comprender:
Sera utilizado para la asignatura de Taller de Cómputo, perteneciente al Colegio de Ciencias y Humanidades de la Universidad Nacional Autónoma de México, correspondiente a la Unidad 2 para el aprendizaje que prentende "Explicar la representación y cuantificación de la información en los diferentes dispositivos digitales, mediante la conversion del código ASCII a un sistema Binario.


### ■  Justificación:
### Se pretende que el uso de este programa sea de caracter "comprobativo o verificativo" principalmente, es decir para comprobar y verificar resultados de ejercicios propuestos en clase y fuera de clase, al igual que para el diseño de reactivos. Debido a la diferencia de lo que se ofrece actualmente en "Internet" que es el convertir valores decimales a valores binarios, "ESTE PROGRAMA CONVIERTE UNA CADENA DE CARACTERES ASCII ALFANUMERICOS A BINARIO", lo cual lo hace UNICO en su TIPO, al convertir un conjunto de caracteres directamente y no uno por uno, pero además ahorra tiempo en la tarea de identificar el "valor numérico" desde una Tabla ASCII para luego convertirlo a su valor respectivo en Binario.

#### ■ Descripción
##### Aquí esta el Directorio SÓLO de carcateres alfanuméricos de la Tabla ASCII, pero pueden anexarse más caracteres de otro tipo
##### (numéricos y especiales)
   
tableAscii = Dict("A" => 65, "B" => 66, "C" => 67, "D" => 68, "E" => 69, "F" => 70, "G" => 71,"H" => 72, 
"I" => 73, "J" => 74, "K" => 75, "L" => 76, "M" => 77, "N" => 78,
"O" => 79, "P" => 80, "Q" => 81, "R" => 82, "S" => 83, "T" => 84,"U" => 85, 
"V" => 86, "W" => 87, "X" => 88, "Y" => 89, "Z" => 90, "a" => 97, "b" => 98, "c" => 99, "d" => 100, 
"e" => 101, "f" => 102, "g" => 103, "h" => 104, "i" => 105, "j" => 106, "k" => 107, "l" => 108, "m" => 109, "n" => 110,
"o" => 111, "p" => 112, "q" => 113, "r" => 114, "s" => 115, "t" => 116,"u" => 117, "v" => 118, "w" => 119, "x" => 120, 
"y" => 121, "z" => 122)

##### Sigue el código que convierte estos caracteres a su valor respectivo en Binario

function convertDecBinary(valorIngresado :: Int)  
binario_str = ""  
while valorIngresado > 1
residuo = valorIngresado % 2
resultadoTruncado = trunc(Int64, residuo)       
binario_str = string(resultadoTruncado) * binario_str
valorIngresado = valorIngresado / 2
end
return binario_str == "" ? "0" : binario_str
end

#### ■ Ejemplo:  
#### En este caso es con la palabra "HOLA"
dato = ["H","O","L","A"]

i = 1
while i <= length(dato)
    datos = dato[i]
    representaBinaria = convertDecBinary(tableAscii[dato[i]])
    println("Para '$datos' su valor en Binario es: $representaBinaria")
    i += 1
end

# -----------------------------------------------------------
#### ■  El resultado al correr el programa es:
Para 'H' su valor en Binario es: 1001000
Para 'O' su valor en Binario es: 1001111
Para 'L' su valor en Binario es: 1001100
Para 'A' su valor en Binario es: 1000001

#### ESTA ES LA PRIMERA ETAPA DE 3 ETAPAS PARA ESTE PROGRAMA.
### 1 (CODIGO FUENTE) --> 2 (iNTERFAZ DE USUARO) --> 3 (PROGRAMA EJECUTABLE PARA PC Y CELULAR) 
#### ANEXO AVANCES de estas etapas en repositorio SRC






