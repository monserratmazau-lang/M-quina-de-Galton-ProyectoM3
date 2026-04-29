# Máquina-de-Galton-ProyectoM3
Simulación de la Máquina de Galton

#Simulación de la Campana de Galton

#Se descargan los paquetes necesarios para generar números aleatorios y graficar
import random
import matplotlib.pyplot as plt

#Función para simular la caída de las canicas 
def simular_canicas(num_canicas, num_niveles):
    resultados = [0] * (num_niveles + 1)

    for _ in range(num_canicas):
        posicion = 0
        for _ in range(num_niveles):
            if random.random() < 0.5:
                posicion += 1
        resultados[posicion] += 1

    return resultados

#Función para graficar los resultados
def graficar_resultados(resultados):
    plt.bar(range(len(resultados)), resultados, color='blue')
    plt.xlabel('Distribución de Canicas')
    plt.ylabel('Cantidad de Canicas')
    plt.title('Simulación de la Máquina de Galton')
    plt.show()

#Simulación y graficación
resultados = simular_canicas(3000, 12)
graficar_resultados(resultados)


#Reflexión de los aprendizajes a lo largo de este módulo
Cada vez comprendo más los elementos y herramientas que Python nos ofrece son muy prácticas y lógicas. La impresión que me ha dejado el curso es muy buena hasta el momento. Algo que me gusta es que con las hábilidades y modalidades de trabajo de cada profesor se enriquece la enseñanza y cada uno de nostros tiene la oportunidad de formar nuestra forma de programar.
Me parece que con suficiente práctica y analisis de las clases y demás herramientas que nos han brindado, me sera posible comenzar a dominar lo básico de este basto, completo e intuitivo lenguaje.



