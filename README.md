# reto-10
# 1 algoritmo que calcule promedio de reales 
```
n : int = int(input("Ingrese la cantidad de números reales que va a introducir: ")) #Se le pide al usuario la cantidad de números reales que va a introducir a la lista
nLista = [] #Creamos una lista vacía
for i in range(n): #Aplicamos ciclo for en rango de n
    i: float = float(input("Ingrese los número reales que usted quiera: ")) #Se le pide al usuario que ingrese el número que quiera. Esto sucederá dependiendo del número de reales que va a ingresea, esto gracias al ciclo for
    nLista.append(i) #Cada vez ingresamos el valor introducido a la lista
print(nLista)

promedio = sum(nLista)/n #Para sacar el promedio usamos la sum() con la lista que creamos sobre n = el número de reales que se introdujeron en la lista
print("El promedio de los valores de la lista es igual a", promedio) #Imprimimos

```
# 2 Algoritmo que calcule promedio arreglo de dos enteros 
#Inicializamos estas variables para solo poner por cada lista dos elementos, uno que corresponderá al eje x y otro al eje y; esto para cada vector
pM : int = 2
pN : int = 2
pMLista = []
pNLista = []
#Ponemos en las listas los elementos anteriormente comentados
for M in range(pM):
    M : float = float(input("Ingrese las coordenadas del punto pM, teniendo en cuenta que el primer valor que agregue será el del eje x y después el del eje y: "))
    pMLista.append(M) #Los añadimos a las listas
for N in range(pN):
    N : float = float(input("Ingrese las coordenadas del punto pN, teniendo en cuenta que el primer valor que agregue será el del eje x y después el del eje y: "))
    pNLista.append(N) #Los añadimos a las listas
print(pMLista, pNLista, sep=", ") #Imprimimos vectores, realmente esta parte se hizo para la facilidad del usuario al ver sus vectores; teniendo en cuenta que se le explica el eje X y el eje Y

print("Tenga en cuenta que la primera lista se refiera al primer vector y la segunda lista se refiere al segundo vector. El primer valor de cada lista se refiere al valor de la coordenada en el eje x, el segundo valor se refiere al valor de la coordenada en el eje y.")

#Creamos listas; una para los valores del eje x y otra para los valores del eje Y
ejeXLista = []
ejeYLista = []
#Pedimos que se ingresen datos de la siguiente manera como está descrita
x1 : float = float(input("Ingrese el valor del eje x del primer vector que usted ingresó al inicio: "))
x2 : float = float(input("Ingrese el valor del eje x del segundo vector que usted ingresó al inicio: "))
y1 : float = float(input("Ingrese el valor del eje y del primer vector que usted ingresó al inicio: "))
y2 : float = float(input("Ingrese el valor del eje y del segundo vector que usted ingresó al inicio: "))
#Agregamos a las listas
ejeXLista.append(x1)
ejeXLista.append(x2)
ejeYLista.append(y1)
ejeYLista.append(y2)

#Creamos una función en la que se calcule el producto punto
def calcularProductoPunto(ejeXLista, ejeYLista):
    #Creamos un ciclo for para que se pueda multiplicar los elementos de la lista del eje X
    producto1 = 1

    for numero1 in ejeXLista:
        producto1 = producto1 * numero1
    
    #Creamos un ciclo for para que se pueda multiplicar los elementos de la lista del eje Y
    producto2 = 1

    for numero2 in ejeYLista:
        producto2 = producto2 * numero2

    #Sumamos los resultados, y nos da la respuesta
    productoPunto = producto1 + producto2
    return productoPunto
    
if __name__ == "__main__":

    resultado = calcularProductoPunto(ejeXLista, ejeYLista)
    print(ejeXLista, ejeYLista, sep=", ")
    print("El resultado de producto punto de los vectores es", resultado) #Imprimimos la respuesta

    
 
