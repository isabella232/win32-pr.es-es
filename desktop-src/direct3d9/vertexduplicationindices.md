---
description: 'VertexDuplicationIndices: se crea una instancia de esta plantilla por malla, que incluye información sobre qué vértices de la malla son duplicados entre sí.'
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a9ac9b43e0aa05d75727e24bb4677ef0b21fcb41366800185551c48f5fb76f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290340"
---
# <a name="vertexduplicationindices"></a>VertexDuplicationIndices

Se crea una instancia de esta plantilla por malla, con información sobre qué vértices de la malla son duplicados entre sí. Los duplicados se duplican cuando un vértice se encuentra en un límite de material o grupo de suavizado. El propósito de esta plantilla es permitir que el cargador determine qué vértices que muestran parámetros periféricos diferentes son realmente los mismos vértices del modelo. Ciertas aplicaciones (simplificación de mallas, por ejemplo) pueden usar esta información.

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

Donde:

-   nIndices: número de índices de vértices. Este es el número de vértices de la malla.
-   nOriginalVertices: número de vértices en la malla antes de que se produzca cualquier duplicación.
-   Los índices de valor n contiene el índice de vértices que el vértice n de la matriz de vértices de la malla habría tenido si no se hubiera producido \[ \] ninguna \[ \] duplicación. Los índices de esta matriz que son iguales, por lo tanto, indican vértices duplicados.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



