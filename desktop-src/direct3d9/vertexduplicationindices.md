---
description: Se crea una instancia de esta plantilla por malla, que contiene información sobre qué vértices de la malla son duplicados entre sí.
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d62278c206032c9a2dfed6ce9b2cd36c5e7456
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105696064"
---
# <a name="vertexduplicationindices"></a><span data-ttu-id="3bbe8-103">VertexDuplicationIndices</span><span class="sxs-lookup"><span data-stu-id="3bbe8-103">VertexDuplicationIndices</span></span>

<span data-ttu-id="3bbe8-104">Se crea una instancia de esta plantilla por malla, que contiene información sobre qué vértices de la malla son duplicados entre sí.</span><span class="sxs-lookup"><span data-stu-id="3bbe8-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="3bbe8-105">Los duplicados se producen cuando un vértice se encuentra en un grupo de suavizado o en un límite de materiales.</span><span class="sxs-lookup"><span data-stu-id="3bbe8-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="3bbe8-106">La finalidad de esta plantilla es permitir que el cargador determine qué vértices que presentan distintos parámetros periféricos son en realidad los mismos vértices en el modelo.</span><span class="sxs-lookup"><span data-stu-id="3bbe8-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="3bbe8-107">Ciertas aplicaciones (por ejemplo, la simplificación de la malla) pueden hacer uso de esta información.</span><span class="sxs-lookup"><span data-stu-id="3bbe8-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

<span data-ttu-id="3bbe8-108">Donde:</span><span class="sxs-lookup"><span data-stu-id="3bbe8-108">Where:</span></span>

-   <span data-ttu-id="3bbe8-109">nIndices: número de índices de vértice.</span><span class="sxs-lookup"><span data-stu-id="3bbe8-109">nIndices - Number of vertex indices.</span></span> <span data-ttu-id="3bbe8-110">Es el número de vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="3bbe8-110">This is the number of vertices in the mesh.</span></span>
-   <span data-ttu-id="3bbe8-111">nOriginalVertices: número de vértices en la malla antes de que se produzca cualquier duplicación.</span><span class="sxs-lookup"><span data-stu-id="3bbe8-111">nOriginalVertices - Number of vertices in the mesh before any duplication occurs.</span></span>
-   <span data-ttu-id="3bbe8-112">El valor indices \[ n \] contiene el índice del vértice que el vértice \[ n \] de la matriz de vértices de la malla habría tenido si no se hubiera producido ninguna duplicación.</span><span class="sxs-lookup"><span data-stu-id="3bbe8-112">The value indices\[n\] holds the vertex index that vertex\[n\] in the vertex array for the mesh would have had if no duplication had occurred.</span></span> <span data-ttu-id="3bbe8-113">Los índices de esta matriz que son iguales, por lo tanto, indican vértices duplicados.</span><span class="sxs-lookup"><span data-stu-id="3bbe8-113">Indices in this array that are the same, therefore, indicate duplicate vertices.</span></span>

## <a name="see-also"></a><span data-ttu-id="3bbe8-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="3bbe8-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="3bbe8-115">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="3bbe8-115">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



