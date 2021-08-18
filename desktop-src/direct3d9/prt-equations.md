---
description: Para comprender completamente un sombreador que implementa PRT, resulta útil derivar la fórmula que usa el sombreador para calcular el brillo de salida.
ms.assetid: 66876e9e-cde1-4d04-9b31-30be1c115e6b
title: Ecuaciones PRT (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd3dc716349ce46d4e678f0e408e5c964eb5f01d633649e3d512db6115c0267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798202"
---
# <a name="prt-equations-direct3d-9"></a>Ecuaciones PRT (Direct3D 9)

Para comprender completamente un sombreador que implementa PRT, resulta útil derivar la fórmula que usa el sombreador para calcular el brillo de salida.

Para empezar, la ecuación siguiente es la ecuación general para calcular la radiancia de salida resultante de la iluminación directa en un objeto difuso con una iluminación lejana arbitraria.

![ecuación del brillo de salida resultante de la iluminación directa en un objeto difuso con iluminación arbitraria lejana](images/prt-theory-eq1.png)

donde:



| Parámetro     | Descripción                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------|
| Rp            | El brillo de salida en el vértice p. Se evalúa en cada vértice de la malla.                                   |
| p<sub>d</sub> | Albedo de la superficie.                                                                              |
| pi            | Constante que se usa como factor de normalización de la energía.                                        |
| L(s)          | Entorno de iluminación (brillo de origen).                                                             |
| Vp₍s₎         | Una función de visibilidad binaria para el punto p. Es 1 si el punto puede ver la luz, 0 si no es así.             |
| Hnp₍s₎        | Término de coseno de la ley de Lambert. Igual a max((Np· s), 0), donde Np es la superficie normal en el punto p. |
| s             | Variable que se integra en la esfera.                                                           |



 

Mediante el uso de funciones de base esférica, como los armónicos esféricos, la siguiente ecuación se aproxima al entorno de iluminación.

![ecuación del entorno de iluminación](images/prt-theory-eq2.png)

donde:



| Parámetro        | Descripción                                              |
|------------------|----------------------------------------------------------|
| L(s)             | Entorno de iluminación (brillo de origen).              |
| i                | Entero que suma el número de funciones base. |
| O                | Orden de los armónicos esféricos.                        |
| l<sub>i</sub>    | Coeficiente.                                           |
| Y<sub>i(s)</sub> | Alguna función base sobre la esfera.                     |



 

La colección de estos coeficientes, L', proporciona la aproximación óptima para la función L(s) con las funciones base Y(s). La sustitución y distribución produce la siguiente ecuación.

![ecuación de la salida después de sustituir l(s) y distribuir](images/prt-theory-eq3.png)

La integral de Y<sub>i(s)</sub>Vp₍s₎Hnp₍s₎ es un coeficiente de transferencia t<sub>pi</sub> que el simulador precompute para cada vértice de la malla. Al sustituir esto, se produce la siguiente ecuación.

![ecuación del resultado de salida después de sustituir el coeficiente de transferencia](images/prt-theory-eq4.png)

Al cambiar esto a la notación vectorial, se produce la siguiente ecuación sin comprimir para calcular la radiancia de salida de cada canal.

![ecuación del resultado de salida después de cambiar a la notación vectorial](images/prt-theory-eq5.png)

donde:



| Parámetro     | Descripción                                                                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rp            | El brillo de salida en el vértice p.                                                                                                                                                      |
| p<sub>d</sub> | Albedo de la superficie.                                                                                                                                                          |
| L'            | El vector de l<sub>i</sub>, y es la proyección de la radiancia de origen en las funciones de base de armónica esférica. Se trata de un vector de orden de coeficientes de armónico esféricos. |
| Tp            | Vector de transferencia order' para el vértice p. El simulador divide los coeficientes de transferencia por p.                                                                                       |



 

Ambos vectores son un vector de orden de coeficientes esféricos, por lo que debe tener en cuenta que se trata simplemente de un producto de puntos. Según el orden, el punto puede ser costoso, por lo que se puede usar la compresión. Un algoritmo denominado Clustered Principal Component Analysis (DAXA) comprime los datos de forma eficaz. Esto permite el uso de una aproximación armónica esférica de orden superior que da como resultado sombras más nítidas.

LA ASE proporciona la ecuación siguiente para aproximar el vector de transferencia.

![ecuación del vector de transferencia aproximado](images/prt-theory-eq6.png)

donde:



| Parámetro      | Descripción                                          |
|----------------|------------------------------------------------------|
| Tp             | Vector de transferencia para el vértice p.                    |
| Mk             | La media del clúster k.                              |
| j              | Entero que suma el número de vectores PCA. |
| N              | Número de vectores PCA.                           |
| w<sub>pj</sub> | Peso de PCA jth para el punto p.                      |
| B<sub>kj</sub> | Vector de base de PCA jth para el clúster k.              |



 

Un clúster es simplemente un número de vértices que comparten el mismo vector medio. A continuación se explica cómo obtener la media del clúster, los pesos de PCA, los vectores de base de PCA y los identificadores de clúster de los vértices.

La sustitución de estas dos ecuaciones produce:

![ecuación del resultado de salida después de sustituir el vector de transferencia](images/prt-theory-eq7.png)

Después, la distribución del producto por puntos produce la siguiente ecuación.

![ecuación del resultado de salida después de distribuir el producto de punto](images/prt-theory-eq8.png)

Porque ambos (Mk· L') y (B<sub>kj</sub>· L') son constantes por vértice, el ejemplo calcula estos valores con la CPU y los pasa como constantes al sombreador de vértices. dado que w<sub>pj</sub> cambia para cada vértice, el ejemplo almacena estos datos por vértice en el búfer del vértice.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transferencia de radiancia precalutada](precomputed-radiance-transfer.md)
</dt> </dl>

 

 



