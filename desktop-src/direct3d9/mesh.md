---
description: Define una malla simple. La primera matriz es una lista de vértices y la segunda matriz define las caras de la malla mediante la indexación en la matriz de vértices.
ms.assetid: vs|directx_sdk|~\mesh.htm
title: En malla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ce4cf6fb6a3eee3417a7d0fe1594164c1e22df9d118f4f995955f8070fc015
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119240745"
---
# <a name="mesh"></a>En malla

Define una malla simple. La primera matriz es una lista de vértices y la segunda matriz define las caras de la malla mediante la indexación en la matriz de vértices.

``` syntax
template Mesh
{
    <3D82AB44-62DA-11CF-AB39-0020AF71E433>
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nFaces;
    array MeshFace faces[nFaces];
    [...]
}
```

Donde:

-   nVertices: número de vértices.
-   array Vector vertices \[ nVertices: \] matriz de vértices, cada uno de tipo Vector. Vea [**Vector**](vector.md).
-   nFaces: número de caras.
-   array MeshFace faces \[ nFaces \] : matriz de caras, cada una de tipo MeshFace. Vea [**MeshFace**](meshface.md).
-   \[ ... \] - Cualquier plantilla de archivo .x se puede usar aquí. Esto hace que la arquitectura sea extensible. [**Normalmente se**](material.md) usan las plantillas Material [**y TextureFilename.**](texturefilename.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



