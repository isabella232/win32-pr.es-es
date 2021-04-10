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
# <a name="meshface"></a><span data-ttu-id="f198c-104">MeshFace</span><span class="sxs-lookup"><span data-stu-id="f198c-104">MeshFace</span></span>

<span data-ttu-id="f198c-105">Lo usa la plantilla de [**malla**](mesh.md) para definir las caras de una malla.</span><span class="sxs-lookup"><span data-stu-id="f198c-105">Used by the [**Mesh**](mesh.md) template to define a mesh's faces.</span></span> <span data-ttu-id="f198c-106">Cada elemento de la matriz nFaceVertexIndices hace referencia a un vértice de malla que se usa para crear la superficie.</span><span class="sxs-lookup"><span data-stu-id="f198c-106">Each element of the nFaceVertexIndices array references a mesh vertex used to build the face.</span></span>

``` syntax
template MeshFace
{
    < 3D82AB5F-62DA-11cf-AB39-0020AF71E433 >
    DWORD nFaceVertexIndices;
    array DWORD faceVertexIndices[nFaceVertexIndices];
} 
```

<span data-ttu-id="f198c-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="f198c-107">Where:</span></span>

-   <span data-ttu-id="f198c-108">nFaceVertexIndices: número de índices.</span><span class="sxs-lookup"><span data-stu-id="f198c-108">nFaceVertexIndices - Number of indices.</span></span>
-   <span data-ttu-id="f198c-109">array DWORD faceVertexIndices \[ nFaceVertexIndices \] : matriz de índices.</span><span class="sxs-lookup"><span data-stu-id="f198c-109">array DWORD faceVertexIndices\[nFaceVertexIndices\] - Array of indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="f198c-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="f198c-110">See also</span></span>

<dl> <dt>

<span data-ttu-id="f198c-111">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="f198c-111">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



