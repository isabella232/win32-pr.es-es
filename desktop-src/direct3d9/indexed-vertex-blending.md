---
description: La combinación de vértices indexada amplía la compatibilidad con la mezcla de vértices en Direct3D para permitir que las matrices se utilicen para la mezcla.
ms.assetid: d320cb8a-48b6-4a53-a051-d50f239c1aa3
title: Mezcla de vértices indexados (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3d45e3ff72a33cd21265d1e4aa25e237e2a73e473914898d5c1057316d4ca0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728717"
---
# <a name="indexed-vertex-blending-direct3d-9"></a>Mezcla de vértices indexados (Direct3D 9)

La combinación de vértices indexada amplía la compatibilidad con la mezcla de vértices en Direct3D para permitir que las matrices se utilicen para la mezcla. Se hace referencia a estas matrices mediante un índice de matriz. Estos índices se proporcionan por vértice y hacen referencia a una paleta de hasta 256 matrices. Cada índice es de 8 bits y cada vértice puede tener hasta cuatro índices, lo que permite combinar cuatro matrices por vértice. Los índices se empaquetan en una DWORD. Dado que los índices se especifican por vértice, hasta 12 matrices pueden afectar a un solo triángulo y cualquier matriz de la paleta puede afectar a los vértices de una llamada a draw. Este enfoque tiene las siguientes ventajas.

-   Permite que más matrices afecten a un solo triángulo.
-   Permite pasar más triángulos combinados en la misma llamada a draw.
-   Hace que la combinación de vértices sea independiente de los índices de triángulo. Esto permite que las mallas progresivas funcionen junto con la combinación de vértices.

Una desventaja de este enfoque es que no funciona con primitivas de superficie curva cuando se produce la teselación antes del procesamiento de vértices.

En el diagrama siguiente se muestra cómo cuatro matrices pueden afectar a un vértice. Cada vértice tiene hasta cuatro índices, por lo que se pueden combinar cuatro matrices por vértice. El diagrama usa las matrices indizadas en 0, 2, 5 y 6.

![diagrama de mezcla de vértices indexados mediante 4 de 256 matrices disponibles](images/dword1.png)

En el diagrama siguiente se muestra cómo hasta 12 matrices pueden afectar a un triángulo. Si se usan índices especificados por vértice, hasta 12 matrices pueden afectar al triángulo.

![diagrama de mezcla de vértices indexados para un triángulo mediante 12 de 256 matrices disponibles](images/dword2.png)

La ecuación siguiente determina el caso general de cómo las matrices tienen efecto en un vértice.

![ecuación de combinación de vértices indexados](images/indexedvblend.png)

El modelo <sub>V es</sub> la posición del vértice del espacio del modelo de entrada. Index0.. Index3 son los índices de matriz por vértice empaquetados en una DWORD. M \[ \] es la matriz de matrices del mundo en las que se indexa. b₀.. b3 son los pesos de mezcla. V<sub>world es</sub> la posición del vértice del espacio del mundo de salida.

Para obtener más información sobre la combinación de vértices indexados, vea [Using Indexed Vertex Blending (Direct3D 9)](using-indexed-vertex-blending.md)(Uso de la combinación de vértices indexados [Direct3D 9]).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mezcla de geometría](geometry-blending.md)
</dt> </dl>

 

 



