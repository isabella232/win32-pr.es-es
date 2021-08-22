---
description: Usado por la plantilla Mesh para definir las caras de una malla. Cada elemento de la matriz nFaceVertexIndices hace referencia a un vértice de malla que se usa para compilar la cara.
ms.assetid: 38c40ebe-eca2-4dd9-95b8-b396225e3050
title: MeshFace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83ea35d1db9e33644638455bc42cc2cbef320f748d96b086037dea6f10607dbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563535"
---
# <a name="meshface"></a>MeshFace

Usado por la [**plantilla Mesh**](mesh.md) para definir las caras de una malla. Cada elemento de la matriz nFaceVertexIndices hace referencia a un vértice de malla que se usa para compilar la cara.

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
-   array DWORD faceVertexIndices \[ nFaceVertexIndices: \] matriz de índices.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



