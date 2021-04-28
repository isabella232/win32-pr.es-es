---
description: 'FaceAdjacency: se crea una instancia de esta plantilla por malla, con información sobre qué vértices de la malla son duplicados entre sí.'
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: FaceAdjacency
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0508b822f45c6796a793dc4b17caeaa1e30b4c3d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090513"
---
# <a name="faceadjacency"></a>FaceAdjacency

Se crea una instancia de esta plantilla por malla, con información sobre qué vértices de la malla son duplicados entre sí. Se duplica el resultado cuando un vértice se encuentra en un límite de material o grupo de suavizado. El propósito de esta plantilla es permitir que el cargador determine qué vértices que muestran parámetros periféricos diferentes son realmente los mismos vértices del modelo. Determinadas aplicaciones (simplificación de mallas, por ejemplo) pueden hacer uso de esta información.

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

Donde:

-   nIndices: número de índices de la malla.
-   índices \[ nIndices: \] matriz de índices.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



