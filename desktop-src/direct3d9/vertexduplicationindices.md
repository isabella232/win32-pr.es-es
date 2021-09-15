---
description: 'VertexDuplicationIndices: se crea una instancia de esta plantilla por malla, que incluye información sobre qué vértices de la malla son duplicados entre sí.'
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b33a8c5fca4f479eec6e9864d4528d4e3e4a1e32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360532"
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

 

 



