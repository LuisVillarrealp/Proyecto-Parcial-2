# Proyecto-Parcial-2
En este repositorio se encuentra el codigo de python para transformar un numero decimal de 2 cifras a binario de 8 digitos.
Integrantes del grupo
Luis Villarreal
Byron Buitron
Jonathan Mullo
Descripcion
Este programa en Python convierte un número decimal de dos cifras (0–99) a binario de 8 bits, aplicando el algoritmo de divisiones sucesivas entre 2.
El código solicita un número al usuario, obtiene los residuos de cada división, forma el número binario en orden inverso y finalmente lo rellena con ceros a la izquierda hasta completar 8 bits.
Como se hizo en codespaces
1. Abrir el repositorio en GitHub.  
2. Presionar el botón Code  Open with Codespaces  Create Codespace on main.  
3. Crear el contenedor de python.  
4. Una vez abierto el entorno, ejecutar el siguiente comando en la terminal python --version, para revisar si esta instalado correctamente.
5. Crear un archivo con el codigo y ejecutarlo.
Codigo
1.  num = int(input("Este es un conversos de decimal a binario de 8 bits. 
    Ingrese un número     decimal (0-99): "))
    Al principio pedimos un numero al usuario entre 0 y 99
2. if 0 <= num <= 99:
    Despues con ese numero vemos si esta dentro del rango si es asi, el programa comienza a convertirlo a binario
3.  binario = ""
    n = num
    while n > 0:
        binario = str(n % 2) + binario
        n //= 2
    El número se divide entre 2 repetidamente:
    Se toma el residuo (n % 2) para obtener el bit correspondiente.
    Se añade ese bit al inicio de la cadena binario.
    Se actualiza n dividiendo entre 2.
4. binario = binario.zfill(8)
    Si el número binario tiene menos de 8 dígitos, se añaden ceros a la izquierda
5. print("El número", num, "en binario (8 bits) es:", binario)
    Muestra el número que el ususario dio junto con su binario de 8 bits.
6. else:
    print("Este numero no es permitido, ingresa uno de 2 digitos ")
    Mensaje si el número no está en el rango

