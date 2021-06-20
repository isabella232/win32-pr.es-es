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
# <a name="patchmesh"></a><span data-ttu-id="da800-103">PatchMesh</span><span class="sxs-lookup"><span data-stu-id="da800-103">PatchMesh</span></span>

<span data-ttu-id="da800-104">Define una malla definida por revisiones de Bézier.</span><span class="sxs-lookup"><span data-stu-id="da800-104">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="da800-105">La primera matriz es una lista de vértices y la segunda define las revisiones de la malla mediante la indexación en la matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="da800-105">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

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

<span data-ttu-id="da800-106">Donde:</span><span class="sxs-lookup"><span data-stu-id="da800-106">Where:</span></span>

-   <span data-ttu-id="da800-107">nVertices: número de vértices.</span><span class="sxs-lookup"><span data-stu-id="da800-107">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="da800-108">vértices \[ nVertices: \] matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="da800-108">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="da800-109">Vea [**Vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="da800-109">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="da800-110">nPatches: número de revisiones.</span><span class="sxs-lookup"><span data-stu-id="da800-110">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="da800-111">patches \[ nPatches: \] matriz de revisiones.</span><span class="sxs-lookup"><span data-stu-id="da800-111">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="da800-112">Consulte [**Revisión**](patch.md)de .</span><span class="sxs-lookup"><span data-stu-id="da800-112">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="da800-113">\[ ... \] - Cualquier plantilla de archivo .x se puede usar aquí.</span><span class="sxs-lookup"><span data-stu-id="da800-113">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="da800-114">Esto hace que la arquitectura sea extensible.</span><span class="sxs-lookup"><span data-stu-id="da800-114">This makes the architecture extensible.</span></span>

<span data-ttu-id="da800-115">Las revisiones usan los vértices de la matriz de vértices como puntos de control para cada revisión.</span><span class="sxs-lookup"><span data-stu-id="da800-115">The patches use the vertices in the array of vertices as the control points for each patch.</span></span> <span data-ttu-id="da800-116">Se trata de una plantilla heredada.</span><span class="sxs-lookup"><span data-stu-id="da800-116">This is a legacy template.</span></span> <span data-ttu-id="da800-117">La plantilla de malla de revisión más reciente [**es PatchMesh9.**](patchmesh9.md)</span><span class="sxs-lookup"><span data-stu-id="da800-117">The latest patch mesh template is [**PatchMesh9**](patchmesh9.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="da800-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="da800-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="da800-119">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="da800-119">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



