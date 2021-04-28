---
description: 'FaceAdjacency: se crea una instancia de esta plantilla por malla, con información sobre qué vértices de la malla son duplicados entre sí.'
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: FaceAdjacency
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0508b822f45c6796a793dc4b17caeaa1e30b4c3d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090513"
---
# <a name="faceadjacency"></a><span data-ttu-id="40ba2-103">FaceAdjacency</span><span class="sxs-lookup"><span data-stu-id="40ba2-103">FaceAdjacency</span></span>

<span data-ttu-id="40ba2-104">Se crea una instancia de esta plantilla por malla, con información sobre qué vértices de la malla son duplicados entre sí.</span><span class="sxs-lookup"><span data-stu-id="40ba2-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="40ba2-105">Se duplica el resultado cuando un vértice se encuentra en un límite de material o grupo de suavizado.</span><span class="sxs-lookup"><span data-stu-id="40ba2-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="40ba2-106">El propósito de esta plantilla es permitir que el cargador determine qué vértices que muestran parámetros periféricos diferentes son realmente los mismos vértices del modelo.</span><span class="sxs-lookup"><span data-stu-id="40ba2-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="40ba2-107">Determinadas aplicaciones (simplificación de mallas, por ejemplo) pueden hacer uso de esta información.</span><span class="sxs-lookup"><span data-stu-id="40ba2-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

<span data-ttu-id="40ba2-108">Donde:</span><span class="sxs-lookup"><span data-stu-id="40ba2-108">Where:</span></span>

-   <span data-ttu-id="40ba2-109">nIndices: número de índices de la malla.</span><span class="sxs-lookup"><span data-stu-id="40ba2-109">nIndices - Number of indices in the mesh.</span></span>
-   <span data-ttu-id="40ba2-110">índices \[ nIndices: \] matriz de índices.</span><span class="sxs-lookup"><span data-stu-id="40ba2-110">indices\[nIndices\] - Array of indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="40ba2-111">Consulte también</span><span class="sxs-lookup"><span data-stu-id="40ba2-111">See also</span></span>

<dl> <dt>

<span data-ttu-id="40ba2-112">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="40ba2-112">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



