# problemanum197
Repositorio donde se trabajará la resolució de la actividad de sintesis A4 llamado "Problema 197"

---

## Funciones

Dividiremos el proyecto en 2 funciones, cada función cumplirá cada requisito que nos piden.

X -> f(x) = X' (Ilia Arcas)
También haremos la inversa: X' -> f(x') = X 

X' -> f(x)' = X'' (Esteban Antiñolo)
También haremos la inversa: X'' -> f(x'') = X' 


---

### X -> f(x) = X' 
#### Logica de ejecución
- Se nos pide que: 
Dado una sucesión de caracteres, separar en sucesiones mas pequeñas las cuales utilizaremos vocales para delemitar cada una de ellas.

Para poder saber cuando nos encontramos una vocal, podemos determinar las vocales en un Array o hacer las validaciones de si la letra es una vocal o no, mientras leemos la cadena de caracteres. 

La manera que considero mas eficiente, es determinar en una array y luego, comparar si la letra de la cadena de caracteres, pertenece a esta lista o no. 

Antes de analizar si hay vocales o no, debemos determinar una metodo para poder leer todos los caracteres y como nos piden que tenemos que remplazar la cadena de caracteres de consonantes por su imagen especular, debemos guardar todos los caracteres en una variable antes de la vcal.

Diagrama de flujo + Pseudocodigo:

1. Guardar en una array los caracteres que usaremos como delimitadores(Vocales).

> Array Vocales = [a,e,i,o,u]

2. Buscar la longitud de caracteres de la cadena de entrada y guardarlo en una variable.

> Variable LongitudCadena = función contar(Cadena)

3. Dividir la cadena de caracteres y guardar los caracteres en un array. 

> Array Caracteres[] = función cortar (Cadena)

4. Recorrer cada elemento de la array de caracteres 

> Foreach Caracter in Caracteres[]{}

5. Analizar si el caracter que estamos leyendo es Vocal o no (Si pertenece a la array de vocales) recorriendo el array principal de las vocales. 

> Foreach Vocal in Vocales[]{
> 	if (Caracter = Vocal){}
> }

6. Analizamos 2 situaciones
	1. Si el caracter NO es vocal:
		1. Guardamos el caracter en una variable
	2. Si el caracter es vocal:
		1. Cojemos el caracter o los caracteres guardados en la variable
		2. Lo invertimos
> if (Caracter != vocal){
> 	Variable CadenaConsonantes .= Caracter
> }
> else{
> 	Variable CadenaInvertida = funcion Invertir(CadenaConsonantes)
> } 



### X'-> f(x)' = X''
#### Logica de ejecución
- Se nos pide que:
Dada una cadena de caracteres, mostrar el primer y el último carácter, después el segundo y el penúltimo, y así sucesivamente hasta que se crucen los contadores.

Para poder hacer esto, primero debemos determinar la longitud de la cadena de caracteres y separar todos los caracteres en un array, de esta manera podremos acceder a cada posición de la cadena.

La manera que considero más eficiente es utilizar dos contadores, uno que empiece en la posición 0 y otro en la última posición del array, que corresponde a la longitud de la cadena menos 1.

Mientras los contadores no se crucen, iremos mostrando el carácter de la primera posición y el de la última. Después, aumentaremos en 1 el contador inicial y disminuiremos en 1 el contador final, repitiendo el proceso hasta que el contador inicial sea mayor que el contador final.
