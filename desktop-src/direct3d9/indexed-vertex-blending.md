---
description: La mezcla de vértices indizados amplía la compatibilidad de mezcla de vértices en Direct3D para permitir el uso de matrices para la fusión.
ms.assetid: d320cb8a-48b6-4a53-a051-d50f239c1aa3
title: Fusión de vértices indizados (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cfe7b45831317fdf9e92525ed74bbd27323e99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494290"
---
# <a name="indexed-vertex-blending-direct3d-9"></a>Fusión de vértices indizados (Direct3D 9)

La mezcla de vértices indizados amplía la compatibilidad de mezcla de vértices en Direct3D para permitir el uso de matrices para la fusión. Se hace referencia a estas matrices mediante el uso de un índice de matriz. Estos índices se proporcionan en cada vértice y hacen referencia a una paleta de hasta 256 matrices. Cada índice es de 8 bits y cada vértice puede tener hasta cuatro índices, lo que permite mezclar cuatro matrices por vértice. Los índices se empaquetan en un valor DWORD. Dado que los índices se especifican en función de cada vértice, hasta 12 matrices pueden afectar a un solo triángulo y cualquier matriz de la paleta puede afectar a los vértices de una llamada a Draw. Este enfoque tiene las ventajas siguientes.

-   Permite que más matrices afecten a un solo triángulo.
-   Permite que se pasen más triángulos combinados en la misma llamada a Draw.
-   Hace que la mezcla de vértices sea independiente de los índices de triángulo. Esto permite que las mallas progresivas funcionen junto con la combinación de vértices.

Una desventaja de este enfoque es que no funciona con primitivas de superficie curvada cuando se produce teselación antes del procesamiento de vértices.

En el diagrama siguiente se muestra cómo pueden afectar cuatro matrices a un vértice. Cada vértice tiene hasta cuatro índices, por lo que se pueden mezclar cuatro matrices por vértice. El diagrama utiliza las matrices indizadas en 0, 2, 5 y 6.

![diagrama de fusión de vértices indexados con 4 de 256 matrices disponibles](images/dword1.png)

En el diagrama siguiente se muestra cómo hasta 12 matrices pueden afectar a un triángulo. Con los índices especificados en cada vértice, hasta 12 matrices pueden afectar al triángulo.

![diagrama de la mezcla de vértices indexados para un triángulo mediante 12 de 256 matrices disponibles](images/dword2.png)

La ecuación siguiente determina el caso general de cómo afectan las matrices a un vértice.

![ecuación de la mezcla de vértices indexados](images/indexedvblend.png)

El <sub>modelo</sub> V es la posición del vértice del espacio del modelo de entrada. Index0.. Index3 son los índices de matriz por vértice empaquetados en un valor DWORD. M \[ \] es la matriz de matrices mundiales que se indexan en. b ₀... b ₂ son los pesos de la mezcla. El<sub>mundo</sub> V es la posición del vértice del espacio del mundo de salida.

Para obtener más información sobre la mezcla de vértices indizados, vea [usar la combinación de vértices indizada (Direct3D 9)](using-indexed-vertex-blending.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Combinación de geometría](geometry-blending.md)
</dt> </dl>

 

 



