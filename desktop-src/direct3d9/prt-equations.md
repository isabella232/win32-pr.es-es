---
description: Para entender completamente un sombreador que implementa PRT, es útil derivar la fórmula que utiliza el sombreador para calcular el Radiance de salida.
ms.assetid: 66876e9e-cde1-4d04-9b31-30be1c115e6b
title: Ecuaciones de PRT (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65559fada82fda7f7eed1c7d05543883a06a19e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152435"
---
# <a name="prt-equations-direct3d-9"></a>Ecuaciones de PRT (Direct3D 9)

Para entender completamente un sombreador que implementa PRT, es útil derivar la fórmula que utiliza el sombreador para calcular el Radiance de salida.

Para empezar, la siguiente ecuación es la ecuación general para calcular las radiances de salida resultantes de la iluminación directa en un objeto difuso con iluminación distanl arbitraria.

![ecuación del Radiance de salida resultante de la iluminación directa en un objeto difuso con iluminación distanl arbitraria](images/prt-theory-eq1.png)

donde:



| Parámetro     | Descripción                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------|
| RP            | El Radiance de salida en el vértice p. Se evalúa en cada vértice de la malla.                                   |
| p<sub>d</sub> | Albedo de la superficie.                                                                              |
| pi            | Constante que se usa como factor de normalización de ahorro de energía.                                        |
| L (s)          | Entorno de iluminación (Radiance de origen).                                                             |
| VP ₍ s ₎         | Una función de visibilidad binaria para el punto p. Es 1 si el punto puede ver la luz, 0 en caso contrario.             |
| HNP ₍ s ₎        | El término del coseno de la ley de Lambert. Igual a Max ((NP · s), 0), donde NP es la superficie normal en el punto p. |
| s             | La variable que se integra en la esfera.                                                           |



 

Con las funciones de base esféricas, como los armónicos esféricos, la ecuación siguiente se aproxima al entorno de iluminación.

![ecuación del entorno de iluminación](images/prt-theory-eq2.png)

donde:



| Parámetro        | Descripción                                              |
|------------------|----------------------------------------------------------|
| L (s)             | Entorno de iluminación (Radiance de origen).              |
| i                | Entero que suma el número de funciones de base. |
| O                | El orden de los armónicos esféricos.                        |
| l<sub>i</sub>    | Un coeficiente.                                           |
| Y<sub>i (s)</sub> | Función de base en la esfera.                     |



 

La colección de estos coeficientes, L ', proporciona una aproximación óptima para las funciones L (s) con las funciones de base Y. Al sustituir y distribuir, se produce la siguiente ecuación.

![ecuación del Radiance de salida después de sustituir l (s) y distribuir](images/prt-theory-eq3.png)

La parte entera de Y<sub>i (s)</sub>VP ₍ s ₎ HNP ₍ s ₎ es un coeficiente de transferencia t<sub>PI</sub> que el simulador calcula para cada vértice de la malla. Al sustituir esto, se produce la siguiente ecuación.

![ecuación del Radiance de salida después de sustituir el coeficiente de transferencia](images/prt-theory-eq4.png)

Si se cambia a notación vectorial, se produce la siguiente ecuación sin comprimir para calcular el Radiance de salida de cada canal.

![ecuación del Radiance de salida después de cambiar a notación vectorial](images/prt-theory-eq5.png)

donde:



| Parámetro     | Descripción                                                                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RP            | El Radiance de salida en el vértice p.                                                                                                                                                      |
| p<sub>d</sub> | Albedo de la superficie.                                                                                                                                                          |
| CG            | Vector de l<sub>i</sub>y es la proyección de la Radiance de origen en las funciones de base de armónico esférica. Se trata de un vector de pedido ² de coeficientees armónicos esféricos. |
| Supervisor            | Vector de transferencia de pedido ² para el vértice p. El simulador divide los coeficientes de transferencia por p.                                                                                       |



 

Ambos vectores son un vector de pedido ² de coeficientees armónicos esféricos, por lo que se debe tener en cuenta que se trata simplemente de un producto punto. Dependiendo del orden, el punto puede ser caro, por lo que se puede usar la compresión. Un algoritmo denominado análisis de componentes principales en clúster (CPCA) comprime de forma eficaz los datos. Esto permite el uso de una aproximación armónica esférica de orden superior, lo que da como resultado sombras más nítidas.

CPCA proporciona la siguiente ecuación para aproximarse al vector de transferencia.

![ecuación del vector de transferencia aproximado](images/prt-theory-eq6.png)

donde:



| Parámetro      | Descripción                                          |
|----------------|------------------------------------------------------|
| Supervisor             | Vector de transferencia para el vértice p.                    |
| MK             | La media del clúster k.                              |
| j              | Entero que suma el número de vectores PCA. |
| N              | El número de vectores PCA.                           |
| en<sub>blanco</sub> | Peso del PCA de JTH para el punto p.                      |
| B<sub>KJ</sub> | Vector de base del PCA de JTH para el clúster k.              |



 

Un clúster es simplemente un número de vértices que comparten el mismo vector medio. A continuación se describe cómo obtener la media del clúster, las ponderaciones del PCA, los vectores de base del PCA y los identificadores de clúster de los vértices.

La sustitución de estas dos ecuaciones produce:

![ecuación del Radiance de salida después de sustituir el vector de transferencia](images/prt-theory-eq7.png)

A continuación, la distribución del producto DOT produce la siguiente ecuación.

![ecuación del Radiance de salida después de distribuir el producto de punto](images/prt-theory-eq8.png)

Dado que ambos (MK · L ') y (B<sub>KJ</sub>· L ') son constantes por vértice, el ejemplo calcula estos valores con la CPU y los pasa como constantes en el sombreador de vértices; Dado que los cambios en w<sub>PJ</sub> para cada vértice, el ejemplo almacena estos datos por vértice en el búfer de vértices.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transferencia Radiance precalculada](precomputed-radiance-transfer.md)
</dt> </dl>

 

 



