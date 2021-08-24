---
description: PatchMesh define una malla definida por las revisiones de Bézier, incluida una lista de vértices y las revisiones de la malla mediante la indexación en la matriz de vértices.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3bc3c243fb42014ba18aac134ea008d5818e249a601858be6724d5a0fd7310
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746925"
---
# <a name="patchmesh"></a>PatchMesh

Define una malla definida por las revisiones de Bézier. La primera matriz es una lista de vértices y la segunda matriz define las revisiones de la malla mediante la indexación en la matriz de vértices.

``` syntax
template PatchMesh
{
    < D02C95CC-EDBA-4305-9B5D-1820D7704BBF >
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
}
```

Donde:

-   nVertices: número de vértices.
-   vértices \[ nVertices: \] matriz de vértices. Vea [**Vector**](vector.md).
-   nPatches: número de revisiones.
-   patches \[ nPatches: \] matriz de revisiones. Consulte [**Revisión**](patch.md)de .
-   \[ ... \] - Cualquier plantilla de archivo .x se puede usar aquí. Esto hace que la arquitectura sea extensible.

Las revisiones usan los vértices de la matriz de vértices como puntos de control para cada revisión. Se trata de una plantilla heredada. La plantilla de malla de revisión más reciente [**es PatchMesh9.**](patchmesh9.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



