---
description: 'Normalmente, las aplicaciones de gráficos 3D usan dos tipos de sistemas de coordenadas cartesianos: zurdo y zurdo.'
ms.assetid: 268c3024-85a5-4fd5-b575-e126dd4be97c
title: Sistemas de coordenadas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb9fa389b2bf11bec9ee4f8053bbeb4c822f422
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696098"
---
# <a name="coordinate-systems-direct3d-9"></a>Sistemas de coordenadas (Direct3D 9)

Normalmente, las aplicaciones de gráficos 3D usan dos tipos de sistemas de coordenadas cartesianos: zurdo y zurdo. En ambos sistemas de coordenadas, el eje x positivo apunta a la derecha y el eje y positivo apunta hacia arriba. Puede recordar en qué dirección apunta el eje z positivo apuntando los dedos de la mano izquierda o derecha en la dirección x positiva y dirigiendolos en la dirección y positiva. La dirección en la que se encuentra el punto de control, ya sea hacia delante o fuera, es la dirección en la que apunta el eje z positivo para ese sistema de coordenadas. En la ilustración siguiente se muestran estos dos sistemas de coordenadas.

![Ilustración de los sistemas de coordenadas cartesiano de la izquierda y la mano derecha](images/leftrght.png)

Direct3D usa un sistema de coordenadas de la mano izquierda. Si va a migrar una aplicación que se basa en un sistema de coordenadas de la mano derecha, debe realizar dos cambios en los datos pasados a Direct3D.

-   Gire el orden de los vértices del triángulo para que el sistema los Recorra hacia la derecha desde la parte delantera. En otras palabras, si los vértices son V0, V1, V2, páselo a Direct3D como V0, V2, v1.
-   Use la matriz de vista para escalar el espacio universal en-1 en la dirección z. Para ello, voltee el signo del \_ miembro 31, \_ 32, \_ 33 y \_ 34 de la estructura [**D3DMATRIX**](d3dmatrix.md) que usa para la matriz de la vista.

Para obtener las cantidades que se van a usar en un mundo con una mano, use las funciones [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md) y [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) para definir la transformación de proyección. Sin embargo, tenga cuidado de usar la función [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) correspondiente, invierta el orden de selección de caras inversas y diseñe los mapas de cubos según corresponda.

Aunque las coordenadas de la izquierda y la mano derecha son los sistemas más comunes, hay varios sistemas de coordenadas que se usan en el software 3D. Por ejemplo, no es inusual que las aplicaciones de modelado 3D utilicen un sistema de coordenadas en el que el eje y apunte hacia el espectador o fuera de él, y el eje z apunta hacia arriba.

Formalmente, la orientación de un conjunto de vectores de base (es decir, un sistema de coordenadas) puede encontrarse en el cálculo del determinante de la matriz definida por el conjunto determinado de vectores de base. Si el determinante es positivo, se dice que la base está "positiva" (o diestro). Si el determinante es negativo, se dice que la base está orientada negativamente (o diestro). Para obtener una explicación de lo que es un determinante, consulte cualquier recurso de álgebra lineal.

De manera informativa, puede usar la "regla de mano derecha/izquierda" para determinar si un conjunto determinado de vectores de base forma un sistema de coordenadas de la mano derecha o izquierda.

Las operaciones esenciales realizadas en los objetos definidos en un sistema de coordenadas 3D son la conversión, la rotación y el escalado. Puede combinar estas transformaciones básicas para crear una matriz de transformación. Para obtener más información, vea [transformaciones (Direct3D 9)](transforms.md).

Cuando se combinan estas operaciones, los resultados no son conmutables; el orden en el que se multiplican las matrices es importante.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistemas de coordenadas y geometría](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



