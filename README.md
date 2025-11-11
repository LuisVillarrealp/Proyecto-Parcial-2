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
Codigo1.  “num = int(input("Este es un conversor de decimal a binario de 8 bits. Ingrese un número decimal (0-99): "))”
Al principio pedimos un numero al usuario entre 0 y 99
2. “if 0 <= num <= 99:”
Después con ese número vemos si está dentro del rango si es así, el programa comienza a convertirlo a binario
3.  binario = ""
Se crea una cadena vacía donde se irán guardando los bits (0 y 1) que forman el número binario.
Empieza vacía porque el número aún no ha sido convertido.
4. “n = num”
Se hace una copia del número ingresado en otra variable (n) para no modificar la original durante las operaciones.
5. “while n > 0:”
Este bucle se repite mientras el número sea mayor que cero.
En cada vuelta se obtiene un bit del número binario.
6. “binario = str(n % 2) + binario”
Aquí se calcula el residuo de dividir n entre 2 (n % 2), que puede ser 0 o 1.
Ese residuo representa un bit del número binario.
Se convierte a texto (str()) y se agrega al inicio de la cadena binario.
7. “n //= 2”
Luego se divide n entre 2 usando división entera (//) para continuar con el siguiente bit.
El proceso se repite hasta que n llega a 0.

8. “binario = binario.zfill(8)”
    Si el número binario tiene menos de 8 dígitos, se añaden ceros a la izquierda
9. “print("El número", num, "en binario (8 bits) es:", binario)”
    Muestra el número que el ususario dio junto con su binario de 8 bits.
10. “else:
    print("Este número no es permitido, ingresa uno de 2 digitos ")”
    Mensaje si el número no está en el rango


