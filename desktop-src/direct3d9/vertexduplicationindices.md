---
description: 'VertexDuplicationIndices: se crea una instancia de esta plantilla por malla, con información sobre qué vértices de la malla son duplicados entre sí.'
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b33a8c5fca4f479eec6e9864d4528d4e3e4a1e32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090183"
---
# <a name="vertexduplicationindices"></a><span data-ttu-id="02c2c-103">VertexDuplicationIndices</span><span class="sxs-lookup"><span data-stu-id="02c2c-103">VertexDuplicationIndices</span></span>

<span data-ttu-id="02c2c-104">Se crea una instancia de esta plantilla por malla, con información sobre qué vértices de la malla son duplicados entre sí.</span><span class="sxs-lookup"><span data-stu-id="02c2c-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="02c2c-105">Se duplica el resultado cuando un vértice se encuentra en un límite de material o grupo de suavizado.</span><span class="sxs-lookup"><span data-stu-id="02c2c-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="02c2c-106">El propósito de esta plantilla es permitir que el cargador determine qué vértices que muestran parámetros periféricos diferentes son realmente los mismos vértices del modelo.</span><span class="sxs-lookup"><span data-stu-id="02c2c-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="02c2c-107">Determinadas aplicaciones (simplificación de mallas, por ejemplo) pueden hacer uso de esta información.</span><span class="sxs-lookup"><span data-stu-id="02c2c-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

<span data-ttu-id="02c2c-108">Donde:</span><span class="sxs-lookup"><span data-stu-id="02c2c-108">Where:</span></span>

-   <span data-ttu-id="02c2c-109">nIndices: número de índices de vértices.</span><span class="sxs-lookup"><span data-stu-id="02c2c-109">nIndices - Number of vertex indices.</span></span> <span data-ttu-id="02c2c-110">Este es el número de vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="02c2c-110">This is the number of vertices in the mesh.</span></span>
-   <span data-ttu-id="02c2c-111">nOriginalVertices: número de vértices de la malla antes de que se produzca cualquier duplicación.</span><span class="sxs-lookup"><span data-stu-id="02c2c-111">nOriginalVertices - Number of vertices in the mesh before any duplication occurs.</span></span>
-   <span data-ttu-id="02c2c-112">Los índices de valor n contiene el índice de vértices que el vértice n de la matriz de vértices de la malla habría tenido si no se hubiera producido \[ \] ninguna \[ \] duplicación.</span><span class="sxs-lookup"><span data-stu-id="02c2c-112">The value indices\[n\] holds the vertex index that vertex\[n\] in the vertex array for the mesh would have had if no duplication had occurred.</span></span> <span data-ttu-id="02c2c-113">Los índices de esta matriz que son iguales, por lo tanto, indican vértices duplicados.</span><span class="sxs-lookup"><span data-stu-id="02c2c-113">Indices in this array that are the same, therefore, indicate duplicate vertices.</span></span>

## <a name="see-also"></a><span data-ttu-id="02c2c-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="02c2c-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="02c2c-115">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="02c2c-115">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



