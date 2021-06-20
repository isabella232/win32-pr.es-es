---
description: PatchMesh define una malla definida por revisiones de Bézier, incluida una lista de vértices y las revisiones de la malla mediante la indexación en la matriz de vértices.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabb3846246c7fb76a7146baf0b30bd9730fe24b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404718"
---
# <a name="patchmesh"></a>PatchMesh

Define una malla definida por revisiones de Bézier. La primera matriz es una lista de vértices y la segunda define las revisiones de la malla mediante la indexación en la matriz de vértices.

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

 

 



