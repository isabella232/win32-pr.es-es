---
description: Cada cara de una malla tiene un vector normal de unidad perpendicular, tal como se muestra en la siguiente ilustración.
ms.assetid: 86e2a460-7b58-4612-8f72-5a4e864ceb58
title: Vectores normales de cara y vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e0ef6fd8eba85b770cbfe71477655ddbafd8ee7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104566488"
---
# <a name="face-and-vertex-normal-vectors-direct3d-9"></a>Vectores normales de cara y vértice (Direct3D 9)

Cada cara de una malla tiene un vector normal de unidad perpendicular, tal como se muestra en la siguiente ilustración. La dirección del vector viene determinada por el orden en el que se definen los vértices y por si el sistema de coordenadas es una mano derecha o izquierda. La cara normal apunta fuera del lado frontal de la cara. En Direct3D, solo está visible la parte frontal de una cara. Una cara frontal es aquella en la que los vértices se definen en el orden de las agujas del reloj.

![Ilustración de un vector normal para una cara frontal](images/nrmlvect.png)

Cualquier cara que no sea una cara frontal es una cara trasera. Direct3D no siempre representa caras inversas; por lo tanto, se dice que los rostros se seleccionan. Si lo desea, puede cambiar el modo de selección de datos para que represente caras. Consulte [Estado de selección de datos (Direct3D 9)](culling-state.md) para obtener más información.

Direct3D usa las normales de unidad de vértices para los efectos de sombreado Gouraud, iluminación y textura. En la ilustración siguiente se muestran las normales de ejemplo.

![Ilustración de las normales de vértice](images/vertnrml.png)

Al aplicar el sombreado Gouraud a un polígono, Direct3D usa las normales de vértice para calcular el ángulo entre la fuente de luz y la superficie. Calcula los valores de color y intensidad de los vértices y los interpola para cada punto de todas las superficies primitivas. Direct3D calcula el valor de la intensidad de la luz mediante el ángulo. Cuanto mayor sea el ángulo, menos luz se iluminará en la superficie.

Si va a crear un objeto plano, establezca el valor normal del vértice en el punto perpendicular a la superficie, tal como se muestra en la siguiente ilustración.

![Ilustración de una superficie plana compuesta por dos triángulos con normales de vértice](images/flatvert.png)

Sin embargo, lo más probable es que el objeto esté formado por franjas de triángulo y que los triángulos no sean coplanos. Una manera sencilla de lograr un sombreado suave en todos los triángulos de la franja es calcular primero el vector normal de la superficie para cada cara poligonal a la que está asociado el vértice. El vértice normal se puede establecer para crear un ángulo igual con cada superficie normal. Sin embargo, es posible que este método no sea lo suficientemente eficaz para primitivas complejas.

Este método se muestra en el siguiente diagrama, que muestra dos superficies, S1 y S2 que se han encontrado en el borde anterior. Los vectores normales para S1 y S2 se muestran en azul. El vector normal del vértice se muestra en rojo. El ángulo que el vector normal de vértice realiza con la superficie normal de S1 es el mismo que el del vértice normal y el normal de la superficie de S2. Cuando estas dos superficies están iluminadas y sombreadas con el sombreado Gouraud, el resultado es un borde con un sombreado suave y con una curvatura suave.

![diagrama de dos superficies (S1 y S2) y sus vectores normales y vector normal de vértice](images/gvert.png)

Si el vértice normal se inclina hacia uno de los rostros con el que está asociado, hace que la intensidad de la luz aumente o disminuya para los puntos de la superficie, dependiendo del ángulo que realice con la fuente de luz. En el diagrama siguiente se muestra un ejemplo. De nuevo, estas superficies aparecen en el borde. El vértice normal se inclina hacia S1, lo que hace que tenga un ángulo más pequeño con la fuente de luz que si el vértice normal tuviera ángulos iguales con las normales de la superficie.

![diagrama de dos superficies (S1 y S2) con un vector normal de vértice que se inclina hacia una cara](images/gvert2.png)

Puede usar el sombreado Gouraud para mostrar algunos objetos en una escena 3D con bordes nítidos. Para ello, duplique los vectores normales de vértices en cualquier intersección de caras en las que se requiera un borde nítido, como se muestra en la siguiente ilustración.

![Ilustración de vectores normales de vértices duplicados en bordes agudos](images/shade1.png)

Si usa los métodos DrawPrimitive para representar la escena, defina el objeto con bordes nítidos como una lista de triángulos, en lugar de una franja de triángulo. Al definir un objeto como una franja de triángulo, Direct3D lo trata como un único polígono compuesto por varias caras triangulares. El sombreado Gouraud se aplica tanto en cada cara del polígono como entre caras adyacentes. El resultado es un objeto que se sombrea suavemente de la superficie a la superficie. Dado que una lista de triángulos es un polígono compuesto por una serie de caras triangular discontinuas, Direct3D aplica sombreado Gouraud en cada cara del polígono. Sin embargo, no se aplica de la esfera a la superficie. Si dos o más triángulos de una lista de triángulo son adyacentes, parecen tener un borde nítido entre ellos.

Otra alternativa es cambiar a sombreado plano al representar objetos con bordes nítidos. Este es el método más eficaz, pero puede dar lugar a que los objetos de la escena no se representen de forma realista como los objetos con sombreado Gouraud.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistemas de coordenadas y geometría](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



