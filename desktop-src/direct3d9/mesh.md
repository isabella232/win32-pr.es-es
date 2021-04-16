---
description: Define una malla simple. La primera matriz es una lista de vértices y la segunda matriz define las caras de la malla mediante la indexación en la matriz de vértices.
ms.assetid: vs|directx_sdk|~\mesh.htm
title: En malla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced60785a5f013db7fc26e4d203119a160953b65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494278"
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
-   los vértices del vector de matriz \[ nVertices \] -matriz de vértices, cada uno de tipo vector. Consulte [**Vector**](vector.md).
-   nFaces: número de caras.
-   array MeshFace Face \[ nFaces \] -Array of Faces, cada una de tipo MeshFace. Vea [**MeshFace**](meshface.md).
-   \[ ... \] -Aquí puede usarse cualquier plantilla de archivo. x. Esto hace que la arquitectura sea extensible. Normalmente se usan plantillas de [**material**](material.md) y [**TextureFilename**](texturefilename.md) .

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



