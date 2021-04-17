---
description: Define una malla definida por las revisiones de Bézier. La primera matriz es una lista de vértices y la segunda define las revisiones de la malla mediante la indexación en la matriz de vértices.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b3d8232fe8c83358feb216acfb45a7877d7acb9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105696096"
---
# <a name="patchmesh9"></a>PatchMesh9

Define una malla definida por las revisiones de Bézier. La primera matriz es una lista de vértices y la segunda define las revisiones de la malla mediante la indexación en la matriz de vértices.

``` syntax
template PatchMesh9
{
    < B9EC94E1-B9A6-4251-BA18-94893F02C0EA >
    DWORD Type;
    DWORD Degree;
    DWORD Basis;
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
} 
```

Donde:

-   Tipo: tipo de malla de revisión: rectángulo, triángulo o N-patch.
-   Grado de grado de las variables en la ecuación de curva.
-   Tipo base de una superficie de revisión de orden superior.
-   nVertices: número de vértices.
-   vertices \[ nVertices \] : matriz de vértices. Consulte [**Vector**](vector.md).
-   nPatches: número de revisiones.
-   patches \[ nPatches \] : matriz de revisiones. Consulte [**patch**](patch.md).
-   \[ ... \] -Aquí puede usarse cualquier plantilla de archivo. x. Esto hace que la arquitectura sea extensible.

Las revisiones usan los vértices de la matriz de vértices como puntos de control para cada revisión.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



