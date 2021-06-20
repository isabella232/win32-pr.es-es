---
description: PatchMesh9 define una malla definida por las revisiones de Bézier, incluida una lista de vértices y las revisiones de la malla mediante la indexación en la matriz de vértices.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811e593117f2ec57a4718ea8078d96bcea87e71f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404708"
---
# <a name="patchmesh9"></a><span data-ttu-id="54cc8-103">PatchMesh9</span><span class="sxs-lookup"><span data-stu-id="54cc8-103">PatchMesh9</span></span>

<span data-ttu-id="54cc8-104">Define una malla definida por las revisiones de Bézier.</span><span class="sxs-lookup"><span data-stu-id="54cc8-104">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="54cc8-105">La primera matriz es una lista de vértices y la segunda matriz define las revisiones de la malla mediante la indexación en la matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="54cc8-105">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

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

<span data-ttu-id="54cc8-106">Donde:</span><span class="sxs-lookup"><span data-stu-id="54cc8-106">Where:</span></span>

-   <span data-ttu-id="54cc8-107">Tipo: tipo de malla de revisión: rectángulo, triángulo o N revisiones.</span><span class="sxs-lookup"><span data-stu-id="54cc8-107">Type - Patch mesh type: rectangle, triangle, or N-patch.</span></span>
-   <span data-ttu-id="54cc8-108">Degree: grado de las variables de la ecuación de curva.</span><span class="sxs-lookup"><span data-stu-id="54cc8-108">Degree - Degree of the variables in the curve equation.</span></span>
-   <span data-ttu-id="54cc8-109">Base: tipo base de una superficie de revisión de orden superior.</span><span class="sxs-lookup"><span data-stu-id="54cc8-109">Basis - Basis type of a high-order patch surface.</span></span>
-   <span data-ttu-id="54cc8-110">nVertices: número de vértices.</span><span class="sxs-lookup"><span data-stu-id="54cc8-110">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="54cc8-111">vértices \[ nVertices: \] matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="54cc8-111">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="54cc8-112">Vea [**Vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="54cc8-112">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="54cc8-113">nPatches: número de revisiones.</span><span class="sxs-lookup"><span data-stu-id="54cc8-113">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="54cc8-114">patches \[ nPatches: \] matriz de revisiones.</span><span class="sxs-lookup"><span data-stu-id="54cc8-114">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="54cc8-115">Consulte [**Revisión**](patch.md)de .</span><span class="sxs-lookup"><span data-stu-id="54cc8-115">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="54cc8-116">\[ ... \] - Cualquier plantilla de archivo .x se puede usar aquí.</span><span class="sxs-lookup"><span data-stu-id="54cc8-116">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="54cc8-117">Esto hace que la arquitectura sea extensible.</span><span class="sxs-lookup"><span data-stu-id="54cc8-117">This makes the architecture extensible.</span></span>

<span data-ttu-id="54cc8-118">Las revisiones usan los vértices de la matriz de vértices como puntos de control para cada revisión.</span><span class="sxs-lookup"><span data-stu-id="54cc8-118">The patches use the vertices in the array of vertices as the control points for each patch.</span></span>

## <a name="see-also"></a><span data-ttu-id="54cc8-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="54cc8-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="54cc8-120">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="54cc8-120">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



