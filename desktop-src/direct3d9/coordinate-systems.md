---
description: 'Normalmente, las aplicaciones de gráficos 3D usan dos tipos de sistemas de coordenadas cartesianos: a la izquierda y a la derecha.'
ms.assetid: 268c3024-85a5-4fd5-b575-e126dd4be97c
title: Sistemas de coordenadas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e47b87ae6374d68b8c836dfb4818781e83e77c288f7bf05b121dbb4426c9aad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857585"
---
# <a name="coordinate-systems-direct3d-9"></a>Sistemas de coordenadas (Direct3D 9)

Normalmente, las aplicaciones de gráficos 3D usan dos tipos de sistemas de coordenadas cartesianos: a la izquierda y a la derecha. En ambos sistemas de coordenadas, el eje X positivo apunta a la derecha y el eje Y positivo apunta hacia arriba. Puede recordar en qué dirección apunta el eje Z positivo señalando los dedos de la mano izquierda o derecha en la dirección X positiva y en curling en la dirección Y positiva. La dirección en la que apunta el control, ya sea hacia usted o lejos de usted, es la dirección en la que apunta el eje Z positivo para ese sistema de coordenadas. En la ilustración siguiente se muestran estos dos sistemas de coordenadas.

![ilustración de los sistemas de coordenadas cartesianos de mano izquierda y derecha](images/leftrght.png)

Direct3D usa un sistema de coordenadas a la izquierda. Si va a portear una aplicación basada en un sistema de coordenadas de mano derecha, debe realizar dos cambios en los datos pasados a Direct3D.

-   Voltee el orden de los vértices de triángulo para que el sistema los recoste en el sentido de las agujas del reloj desde la parte delantera. En otras palabras, si los vértices son v0, v1, v2, pásenlos a Direct3D como v0, v2, v1.
-   Use la matriz de vistas para escalar el espacio del mundo en -1 en la dirección z. Para ello, voltee el signo del miembro \_ 31, 32, 33 y 34 de la estructura \_ \_ \_ [**D3DMATRIX**](d3dmatrix.md) que se usa para la matriz de vistas.

Para obtener lo que equivale a un mundo de derechas, use las funciones [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md) y [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) para definir la transformación de proyección. Sin embargo, tenga cuidado de usar la función [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) correspondiente, invertir el orden de búsqueda de caras inversas y configurar los mapas del cubo en consecuencia.

Aunque las coordenadas de mano izquierda y derecha son los sistemas más comunes, hay una variedad de otros sistemas de coordenadas que se usan en el software 3D. Por ejemplo, no es inusual que las aplicaciones de modelado 3D usen un sistema de coordenadas en el que el eje Y apunta hacia el visor o fuera de él, y el eje Z apunta hacia arriba.

Formalmente, la orientación de un conjunto de vectores base (es decir, un sistema de coordenadas) se puede encontrar al calcular el determinante de la matriz definida por el conjunto concreto de vectores base. Si el determinante es positivo, se dice que la base está orientada "positivamente" (o a la derecha). Si el determinante es negativo, se dice que la base está orientada "negativamente" (o a la izquierda). Para obtener una explicación de lo que es determinante, consulte cualquier recurso de álgebra lineal.

De forma informal, puede usar la "regla de derecha/izquierda" para determinar si un conjunto determinado de vectores base forman un sistema de coordenadas a la derecha o a la izquierda.

Las operaciones esenciales realizadas en objetos definidos en un sistema de coordenadas 3D son la traducción, la rotación y el escalado. Puede combinar estas transformaciones básicas para crear una matriz de transformación. Para obtener más información, [vea Transformaciones (Direct3D 9).](transforms.md)

Al combinar estas operaciones, los resultados no son conmutativos; el orden en el que se multiplican las matrices es importante.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistemas de coordenadas y geometría](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



