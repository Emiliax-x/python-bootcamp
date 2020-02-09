
# python-bootcamp
Python bootcamp material


Here is all the notes I did during my Python Bootcamp course. 


#### 

COMMAND PROMPT

buscar: cmd (command prompt)->insertar:
cd->directorio actual
dir->contenidos del directorio
cd (nombre carpeta del dir)->abre la carpeta seleccionada
cd ..->regresa al directorio (Sales de la carpeta seleccionada)
cls->limpia la pantalla
Si sólo aparece: >>
colocar quit() y vuele a pedir directorio

---------------------------------------------------------------------------

STRINGS 

input("?")-> Espera que se ingrese un número y se entrega en forma de texto
int()-> Convierte un texto en número no decimal
float()-> Convierte un texto en número decimal
import random-> Permite utulizar el siguiente código
random.randint(,)-> Elige un número al azar en un intervalo cerrado
str()-> Convierte un número a texto
,-> Misma función que str() pero deja dos espacios
if :-> Condición
else :-> Segunda condición en caso de que no se cumpla la primera
maximo_numero-> Elige el número más grande, el códido es sólo "max"
minimo_numero-> Elige el número más pequeño, el código es sólo "min"
#Ejemplo de lo anterior: print("Maximo", maximo_numero)
elif-> Condiciones dentro de if
print("1/t1")-> /t permite avanzar un tab hacia adelante, deja un espacio
print("1/n2")-> /n permite escribir lo que resta en la línea de abajo 
a=a+b es lo mismo que a+=b
import math->importa operaciones matemáticas, ej:
math.radians(x)->convierte ángulos en radianes
math.sin(x)->calcula el seno de los radianes
math.cos(x)->calcula el coseno de los radianes
math.sqrt(x)->calcula la raíz cuadrada: math.sqrt(16)
from math import*->importa igual todas las operaciones pero se ahorra el escribir el "math":
sqrt(16)->sin el math
randint(1,100)->sin el math
math.pi->entrega el valor de pi
math.e->entrega el valor de eulet

FUNCIONES

def->define funciones, ejemplo: def área_círculo(r): 'donde área_círculo es el nombre de la función, (r) es el parámetro y los dos puntos actuán como el if'
#ejemplo 1:
def área_circulo(r):
    x=math.pi*(r**2)
    return x
#def área_triángulo(a,b,c):
     s=(a+b+c)/2
     área=math.sqrt(s*(s-a)*(s-b)*(s-c)
     return área
return->devuelve el valor que se le indica
type(x)->indica que tipo de variable es

LISTAS

Lista=[]*n
Lista.append[m]->agrega un valor m al final de la lista "Lista"
Lista.insert(0,"hola")->agrega a la lista "Lista" el valor hola (o cualquier numero, frase, plabara) en la posición 0 (o cualquier posición).
Lista=[0]*5+[1]*3+["hola"]*7-> crea una lista con la cantidad de veces multiplicada de todos los valores.
Lista=[1,2,3]*100-> muestra 100 veces repetidas la lista [1,2,3.....1,2,3], en total 300 casilleros.
s="hola como estas"->continua abajo
Lista=s.split()->convierte una variable a una lista separado por comas cada ve que hay un espacio.
c=' '->un espacio, puede ser lo que sea pero estará entremedio de los valores de la lista.
c.join(Lista)->convierte una lista en un strig nuevo con un espacio de separación. 
lista.remove(i)->elimina primera aparicion del elemento de la lista, si no existe este elemento, me arroja un error.
list(range(n,m+1))->me genera una lista con rango n hasta m.
lista.pop(indice)->elimina el elemento de la posicion indice y lo retorna.
x[n][m]->accede al dato que se encuentra en una lista dentro de una lista, retorna el valor m de la lista a que se encuentra en la lista n. 
También se puede ver como que n es la fila de la matriz y m son las columnas.
M[[0 for x in range(m)] for x in range(n)]->crea una matriz de m columanas de ceros con n filas de ceros.
len(M)->numero de filas
len(M[0])->numero de columnas 
for x in matriz->x toma la primera columna de la matriz.
print("hola",end="")-> end="" hace lo que se le pide después de imprimir, evita que el print se salte una lnea con el siguiente print.
print(M)->imprime cada columna de una matriz hacia el lado.
imprimir(M)->imprime las filas de la matriz hacia abajo.
n.find('')->Encuentra la primera posicion de la letra o fagmento dentro de un string.
n.rfind('')->Encuentra el índice más alto donde se encuentra una letra o fragmento y retorna su posicion menos 1.
n.count('')->Cuenta cuantas veces aparece un string dentro de una frase o palabra.
n.replace(" "," ")-> Reemplaza el primer string puesto en la función por el segundo string.
n.upper()->Entrega todo el string n es mayúscula.
n.lower()->Entrega todo el string n en minúscula.
n.isalpha()->Dice si el string se encuentra dentro del abecedario.
archivo=open("")->Reconoce un archivo que se encuentra dentro de la misma carpeta que estoy trabajando.
archivo.readlines()->Entrega una lista con cada una de las lineas del archivo. Estas lineas vienen con \n porque existe un salto de lineas en el arcivo original.
archico=open(" ",encoding="Latin-1")->Reconoce un archivo que tiene tildes.
lista[a].strip()->Elimina los saltos de lineas (elimina el "\n").
>>Las listas funcionan de manera diferente con las funciones<<
lista.count(i)->Cuenta cuantos elementos i aparecen en la lista.

CLASS

class (Nombre de mi clase):
def__init__(a,b)->Todos los métodos de una clase reciben como primer parámetro "self". Ejemplo: def__iit__(self,a,b), 
este self es una referencia al objeto en el cual estoy trabajando.
def__init_(self,a,b):
    self.x=a
    self.y=b
isinstance(x,int)-> Esta función revisa que el parámetro x sea del tipo int (o cualquiera que yo coloque) y retorna True o False.
def __init__(self,a=0,b=0):-> Si un punto no revise parámetros, se retornar por defecto los valores de a y b.
lista.index('')->arroja cantidad de apariciones del elemento en la lista.                         
string.startswith(x)-> si el string comienza con el elemento x.
#Para elegir la cantidad de decimales:
"{:.nf}".format(numero)  --> n es la cantidad de decimales
'string {}'.format() ----> f'string {}'  #lo mismo

DICTIONARIES:

my_dict = {key1: value1, key2: value2, key3: [value3]}
my_dict[key2] = value2
my_dict[key3]['anyelement'] = [element of value3]
my_dict[key3]['anystring'].upper() --> se pueden agregar funciones directas
#para agregar algo simplemente debe escribirse una nueva key con su value: my_dict[key4] = [value4] --> se agrega al final
#para cambiar un valor es lo mismo que antes, se escribe la key y se iguala al nuevo value
my_dict.keys()  ---> entrega lista de todas las keys
my_dict.values() ---> entrega lista de todos los values
my_dict.items() ---> entrega lista de tuplas con las keys y los alues correspondientes

TUPLES:

#Funciona igual que una lista pero no se oueden modificar su interior

t = (value1,value2,...)
t[-1] = valuefinal

MAP:
map(funcion,elemento)
filter(funcion,elemento)
Si quiero  hacer una funcion que retorne un elemento modificado, sólo debe usarse:
square = lambda num: num**2  (un ejemplo)
otra forma: list(map(lambda num: num**2, mynums))

Object Oriented Programming (OOP):

class NameClass():
      
   #acá van los atributos ya definidos por la clase, rj:
   type_attribute = any_int

   def __init__(self,attribute):
           self.my_attribute = attribute

   def __str__(self):  ---> le da un string que se pueda imprimir al llamar a la clase
      print(string_representacion)
 
   def __len__(self):  ---> entrega un numero si se pregunta por len(b), b = NameClass()

   def __del__(self): ---> del b --> borra el objeto creado

   #OPERATIONS/ACTIONS ----> Methods
   
   def methods(self):
      print(something)

   def other_method(self,method1,method2):
       self.method1 = method1
       self.method2 = method2

#Mezclar dos clase: class Animal():  y class Dog(Animal)  --> los atributos de Animal están incorporados a la clase Dog
