---
description: Define una malla definida por las revisiones de Bézier. La primera matriz es una lista de vértices y la segunda define las revisiones de la malla mediante la indexación en la matriz de vértices.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcdefac9799736c796aef7cbb7222ab1942540d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536820"
---
# <a name="patchmesh"></a>PatchMesh

Define una malla definida por las revisiones de Bézier. La primera matriz es una lista de vértices y la segunda define las revisiones de la malla mediante la indexación en la matriz de vértices.

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
-   vertices \[ nVertices \] : matriz de vértices. Consulte [**Vector**](vector.md).
-   nPatches: número de revisiones.
-   patches \[ nPatches \] : matriz de revisiones. Consulte [**patch**](patch.md).
-   \[ ... \] -Aquí puede usarse cualquier plantilla de archivo. x. Esto hace que la arquitectura sea extensible.

Las revisiones usan los vértices de la matriz de vértices como puntos de control para cada revisión. Se trata de una plantilla heredada. La plantilla de malla de parches más reciente es [**PatchMesh9**](patchmesh9.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



