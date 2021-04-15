---
description: Se crea una instancia de esta plantilla por malla, que contiene información sobre qué vértices de la malla son duplicados entre sí.
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d62278c206032c9a2dfed6ce9b2cd36c5e7456
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105696064"
---
# <a name="vertexduplicationindices"></a>VertexDuplicationIndices

Se crea una instancia de esta plantilla por malla, que contiene información sobre qué vértices de la malla son duplicados entre sí. Los duplicados se producen cuando un vértice se encuentra en un grupo de suavizado o en un límite de materiales. La finalidad de esta plantilla es permitir que el cargador determine qué vértices que presentan distintos parámetros periféricos son en realidad los mismos vértices en el modelo. Ciertas aplicaciones (por ejemplo, la simplificación de la malla) pueden hacer uso de esta información.

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

-   nIndices: número de índices de vértice. Es el número de vértices de la malla.
-   nOriginalVertices: número de vértices en la malla antes de que se produzca cualquier duplicación.
-   El valor indices \[ n \] contiene el índice del vértice que el vértice \[ n \] de la matriz de vértices de la malla habría tenido si no se hubiera producido ninguna duplicación. Los índices de esta matriz que son iguales, por lo tanto, indican vértices duplicados.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



