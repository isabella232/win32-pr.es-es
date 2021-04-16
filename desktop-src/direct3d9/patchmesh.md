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
# <a name="patchmesh"></a><span data-ttu-id="b438a-104">PatchMesh</span><span class="sxs-lookup"><span data-stu-id="b438a-104">PatchMesh</span></span>

<span data-ttu-id="b438a-105">Define una malla definida por las revisiones de Bézier.</span><span class="sxs-lookup"><span data-stu-id="b438a-105">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="b438a-106">La primera matriz es una lista de vértices y la segunda define las revisiones de la malla mediante la indexación en la matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="b438a-106">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

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

<span data-ttu-id="b438a-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="b438a-107">Where:</span></span>

-   <span data-ttu-id="b438a-108">nVertices: número de vértices.</span><span class="sxs-lookup"><span data-stu-id="b438a-108">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="b438a-109">vertices \[ nVertices \] : matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="b438a-109">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="b438a-110">Consulte [**Vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="b438a-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="b438a-111">nPatches: número de revisiones.</span><span class="sxs-lookup"><span data-stu-id="b438a-111">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="b438a-112">patches \[ nPatches \] : matriz de revisiones.</span><span class="sxs-lookup"><span data-stu-id="b438a-112">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="b438a-113">Consulte [**patch**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="b438a-113">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="b438a-114">\[ ... \] -Aquí puede usarse cualquier plantilla de archivo. x.</span><span class="sxs-lookup"><span data-stu-id="b438a-114">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="b438a-115">Esto hace que la arquitectura sea extensible.</span><span class="sxs-lookup"><span data-stu-id="b438a-115">This makes the architecture extensible.</span></span>

<span data-ttu-id="b438a-116">Las revisiones usan los vértices de la matriz de vértices como puntos de control para cada revisión.</span><span class="sxs-lookup"><span data-stu-id="b438a-116">The patches use the vertices in the array of vertices as the control points for each patch.</span></span> <span data-ttu-id="b438a-117">Se trata de una plantilla heredada.</span><span class="sxs-lookup"><span data-stu-id="b438a-117">This is a legacy template.</span></span> <span data-ttu-id="b438a-118">La plantilla de malla de parches más reciente es [**PatchMesh9**](patchmesh9.md).</span><span class="sxs-lookup"><span data-stu-id="b438a-118">The latest patch mesh template is [**PatchMesh9**](patchmesh9.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b438a-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="b438a-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="b438a-120">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="b438a-120">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



