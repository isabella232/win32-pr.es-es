---
description: Lo usa la plantilla de malla para definir las caras de una malla. Cada elemento de la matriz nFaceVertexIndices hace referencia a un vértice de malla que se usa para crear la superficie.
ms.assetid: 38c40ebe-eca2-4dd9-95b8-b396225e3050
title: MeshFace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a9e8b73efb214f7a767d986830cccc83ee6cbc1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151977"
---
# <a name="meshface"></a>MeshFace

Lo usa la plantilla de [**malla**](mesh.md) para definir las caras de una malla. Cada elemento de la matriz nFaceVertexIndices hace referencia a un vértice de malla que se usa para crear la superficie.

``` syntax
template MeshFace
{
    < 3D82AB5F-62DA-11cf-AB39-0020AF71E433 >
    DWORD nFaceVertexIndices;
    array DWORD faceVertexIndices[nFaceVertexIndices];
} 
```

Donde:

-   nFaceVertexIndices: número de índices.
-   array DWORD faceVertexIndices \[ nFaceVertexIndices \] : matriz de índices.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



