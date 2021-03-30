---
description: Se crea una instancia de esta plantilla por malla, que contiene información sobre qué vértices de la malla son duplicados entre sí.
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: FaceAdjacency
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2fd0f0b2bb328aa8b5ec39e7481c0b7fd766fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805329"
---
# <a name="faceadjacency"></a><span data-ttu-id="6b95e-103">FaceAdjacency</span><span class="sxs-lookup"><span data-stu-id="6b95e-103">FaceAdjacency</span></span>

<span data-ttu-id="6b95e-104">Se crea una instancia de esta plantilla por malla, que contiene información sobre qué vértices de la malla son duplicados entre sí.</span><span class="sxs-lookup"><span data-stu-id="6b95e-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="6b95e-105">Los duplicados se producen cuando un vértice se encuentra en un grupo de suavizado o en un límite de materiales.</span><span class="sxs-lookup"><span data-stu-id="6b95e-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="6b95e-106">La finalidad de esta plantilla es permitir que el cargador determine qué vértices que presentan distintos parámetros periféricos son en realidad los mismos vértices en el modelo.</span><span class="sxs-lookup"><span data-stu-id="6b95e-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="6b95e-107">Ciertas aplicaciones (por ejemplo, la simplificación de la malla) pueden hacer uso de esta información.</span><span class="sxs-lookup"><span data-stu-id="6b95e-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

<span data-ttu-id="6b95e-108">Donde:</span><span class="sxs-lookup"><span data-stu-id="6b95e-108">Where:</span></span>

-   <span data-ttu-id="6b95e-109">nIndices: número de índices en la malla.</span><span class="sxs-lookup"><span data-stu-id="6b95e-109">nIndices - Number of indices in the mesh.</span></span>
-   <span data-ttu-id="6b95e-110">índices \[ nIndices \] : matriz de índices.</span><span class="sxs-lookup"><span data-stu-id="6b95e-110">indices\[nIndices\] - Array of indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b95e-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b95e-111">See also</span></span>

<dl> <dt>

<span data-ttu-id="6b95e-112">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="6b95e-112">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



