---
description: Cada cara de una malla tiene un vector normal de unidad demente, como se muestra en la ilustración siguiente.
ms.assetid: 86e2a460-7b58-4612-8f72-5a4e864ceb58
title: Vectores normales de cara y vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78087ffecbd7157d68ccfb9667392f5148c96191388c1b7886c16f771066ba30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069265"
---
# <a name="face-and-vertex-normal-vectors-direct3d-9"></a>Vectores normales de cara y vértice (Direct3D 9)

Cada cara de una malla tiene un vector normal de unidad demente, como se muestra en la ilustración siguiente. La dirección del vector viene determinada por el orden en que se definen los vértices y por si el sistema de coordenadas es de derecha o izquierda. La cara normal apunta lejos del lado frontal de la cara. En Direct3D, solo está visible la parte delantera de una cara. Una cara frontal es en la que los vértices se definen en el orden de las agujas del reloj.

![ilustración de un vector normal para una cara frontal](images/nrmlvect.png)

Cualquier cara que no sea una cara frontal es una cara posterior. Direct3D no siempre representa caras; por lo tanto, se dice que las caras traseras están en la selección. Puede cambiar el modo de selección para representar caras de nuevo si lo desea. Consulte [Estado de la selección (Direct3D 9)](culling-state.md) para obtener más información.

Direct3D usa las normales de unidad de vértice para efectos de sombreado, iluminación y texturización de Gouraud. En la ilustración siguiente se muestran las normales de ejemplo.

![ilustración de normales de vértice](images/vertnrml.png)

Al aplicar sombreado de Gouraud a un polígono, Direct3D usa las normales de vértice para calcular el ángulo entre la fuente de luz y la superficie. Calcula los valores de color e intensidad de los vértices y los interpola para cada punto en todas las superficies de la primitiva. Direct3D calcula el valor de intensidad de la luz mediante el ángulo . Cuando mayor sea el ángulo, menor será la luz en la superficie.

Si va a crear un objeto plano, establezca las normales de vértice para que apunten a la superficie, como se muestra en la ilustración siguiente.

![ilustración de una superficie plana formada por dos triángulos con normales de vértice](images/flatvert.png)

Sin embargo, es más probable que el objeto se conste de franjas de triángulo y que los triángulos no sean coplanares. Una manera sencilla de lograr un sombreado suave en todos los triángulos de la franja es calcular primero el vector normal de la superficie para cada cara poligonal a la que está asociado el vértice. El vértice normal se puede establecer para hacer un ángulo igual con cada superficie normal. Sin embargo, este método podría no ser lo suficientemente eficaz para primitivas complejas.

Este método se ilustra en el diagrama siguiente, en el que se muestran dos superficies, S1 y S2 que se han visto en el perímetro anterior. Los vectores normales para S1 y S2 se muestran en azul. El vector normal del vértice se muestra en rojo. El ángulo que realiza el vector normal del vértice con la normal de superficie de S1 es el mismo que el ángulo entre el vértice normal y el normal de la superficie de S2. Cuando estas dos superficies se encienden y sombrean con sombreado de Gouraud, el resultado es un borde suave sombreado y redondeado suave entre ellas.

![diagrama de dos superficies (s1 y s2) y sus vectores normales y vector normal de vértice](images/gvert.png)

Si el vértice normal se inclina hacia una de las caras a las que está asociado, hace que la intensidad de la luz aumente o disminuya para los puntos de esa superficie, en función del ángulo que haga con la fuente de luz. En el diagrama siguiente se muestra un ejemplo. Una vez más, estas superficies se ven en el perímetro. El vértice normal se inclina hacia S1, lo que hace que tenga un ángulo más pequeño con la fuente de luz que si el vértice normal tuviera ángulos iguales a los normales de la superficie.

![diagrama de dos superficies (s1 y s2) con un vector normal de vértice que se inclina hacia una cara](images/gvert2.png)

Puede usar el sombreado de Gouraud para mostrar algunos objetos en una escena 3D con bordes nítidos. Para ello, duplique los vectores normales del vértice en cualquier intersección de caras en las que se requiera un borde nítido, como se muestra en la ilustración siguiente.

![ilustración de vectores normales de vértice duplicados en bordes nítidos](images/shade1.png)

Si usa los métodos DrawPrimitive para representar la escena, defina el objeto con bordes nítidos como una lista de triángulos, en lugar de una franja de triángulo. Al definir un objeto como una franja de triángulo, Direct3D lo trata como un único polígono compuesto por varias caras triangulares. El sombreado gouraud se aplica tanto en cada cara del polígono como entre las caras adyacentes. El resultado es un objeto que se sombrea sin problemas de cara a cara. Dado que una lista de triángulos es un polígono compuesto por una serie de caras triangulares desconexas, Direct3D aplica sombreado de Gouraud en cada cara del polígono. Sin embargo, no se aplica de cara a cara. Si dos o más triángulos de una lista de triángulos son adyacentes, parece que tienen un borde nítido entre ellos.

Otra alternativa es cambiar al sombreado plano al representar objetos con bordes nítidos. Se trata, desde el punto de vista computacional, del método más eficaz, pero puede dar lugar a objetos de la escena que no se representan de forma tan realista como los objetos sombreados por Gouraud.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistemas de coordenadas y geometría](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



