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
# <a name="patchmesh9"></a><span data-ttu-id="25476-104">PatchMesh9</span><span class="sxs-lookup"><span data-stu-id="25476-104">PatchMesh9</span></span>

<span data-ttu-id="25476-105">Define una malla definida por las revisiones de Bézier.</span><span class="sxs-lookup"><span data-stu-id="25476-105">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="25476-106">La primera matriz es una lista de vértices y la segunda define las revisiones de la malla mediante la indexación en la matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="25476-106">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

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

<span data-ttu-id="25476-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="25476-107">Where:</span></span>

-   <span data-ttu-id="25476-108">Tipo: tipo de malla de revisión: rectángulo, triángulo o N-patch.</span><span class="sxs-lookup"><span data-stu-id="25476-108">Type - Patch mesh type: rectangle, triangle, or N-patch.</span></span>
-   <span data-ttu-id="25476-109">Grado de grado de las variables en la ecuación de curva.</span><span class="sxs-lookup"><span data-stu-id="25476-109">Degree - Degree of the variables in the curve equation.</span></span>
-   <span data-ttu-id="25476-110">Tipo base de una superficie de revisión de orden superior.</span><span class="sxs-lookup"><span data-stu-id="25476-110">Basis - Basis type of a high-order patch surface.</span></span>
-   <span data-ttu-id="25476-111">nVertices: número de vértices.</span><span class="sxs-lookup"><span data-stu-id="25476-111">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="25476-112">vertices \[ nVertices \] : matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="25476-112">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="25476-113">Consulte [**Vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="25476-113">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="25476-114">nPatches: número de revisiones.</span><span class="sxs-lookup"><span data-stu-id="25476-114">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="25476-115">patches \[ nPatches \] : matriz de revisiones.</span><span class="sxs-lookup"><span data-stu-id="25476-115">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="25476-116">Consulte [**patch**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="25476-116">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="25476-117">\[ ... \] -Aquí puede usarse cualquier plantilla de archivo. x.</span><span class="sxs-lookup"><span data-stu-id="25476-117">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="25476-118">Esto hace que la arquitectura sea extensible.</span><span class="sxs-lookup"><span data-stu-id="25476-118">This makes the architecture extensible.</span></span>

<span data-ttu-id="25476-119">Las revisiones usan los vértices de la matriz de vértices como puntos de control para cada revisión.</span><span class="sxs-lookup"><span data-stu-id="25476-119">The patches use the vertices in the array of vertices as the control points for each patch.</span></span>

## <a name="see-also"></a><span data-ttu-id="25476-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="25476-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="25476-121">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="25476-121">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



