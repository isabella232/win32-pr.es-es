---
description: Se crea una instancia de esta plantilla por cada malla.
ms.assetid: ac5289c6-989c-43b4-9190-ac8f831a05f0
title: SkinWeights
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759239a3a7ec8ebb608cf9ede6624105cee321b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536814"
---
# <a name="skinweights"></a><span data-ttu-id="e49a4-103">SkinWeights</span><span class="sxs-lookup"><span data-stu-id="e49a4-103">SkinWeights</span></span>

<span data-ttu-id="e49a4-104">Se crea una instancia de esta plantilla por cada malla.</span><span class="sxs-lookup"><span data-stu-id="e49a4-104">This template is instantiated on a per-mesh basis.</span></span> <span data-ttu-id="e49a4-105">Dentro de una malla, aparecerá una secuencia de n instancias de esta plantilla, donde n es el número de huesos (fotogramas de archivo X) que influyen en los vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="e49a4-105">Within a mesh, a sequence of n instances of this template will appear, where n is the number of bones (X file frames) that influence the vertices in the mesh.</span></span> <span data-ttu-id="e49a4-106">Cada instancia de la plantilla define básicamente la influencia de un hueso determinado en la malla.</span><span class="sxs-lookup"><span data-stu-id="e49a4-106">Each instance of the template basically defines the influence of a particular bone on the mesh.</span></span> <span data-ttu-id="e49a4-107">Hay una lista de índices de vértices y una lista de pesos correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e49a4-107">There is a list of vertex indices, and a corresponding list of weights.</span></span>

``` syntax
template SkinWeights 
{ 
    < 6F0D123B-BAD2-4167-A0D0-80224F25FABB > 
    STRING transformNodeName; 
    DWORD nWeights; 
    array DWORD vertexIndices[nWeights]; 
    array float weights[nWeights]; 
    Matrix4x4 matrixOffset; 
} 
```

<span data-ttu-id="e49a4-108">Donde:</span><span class="sxs-lookup"><span data-stu-id="e49a4-108">Where:</span></span>

-   <span data-ttu-id="e49a4-109">El nombre del hueso cuya influencia se está definiendo es transformNodeName y nWeights es el número de vértices afectados por este hueso.</span><span class="sxs-lookup"><span data-stu-id="e49a4-109">The name of the bone whose influence is being defined is transformNodeName, and nWeights is the number of vertices affected by this bone.</span></span>
-   <span data-ttu-id="e49a4-110">Los vértices afectados por este hueso están contenidos en vertexIndices y las ponderaciones de cada uno de los vértices afectados por este hueso están contenidas en pesos.</span><span class="sxs-lookup"><span data-stu-id="e49a4-110">The vertices influenced by this bone are contained in vertexIndices, and the weights for each of the vertices influenced by this bone are contained in weights.</span></span>
-   <span data-ttu-id="e49a4-111">La matriz matrixOffset transforma los vértices de la malla en el espacio del hueso.</span><span class="sxs-lookup"><span data-stu-id="e49a4-111">The matrix matrixOffset transforms the mesh vertices to the space of the bone.</span></span> <span data-ttu-id="e49a4-112">Cuando se concatena a la transformación del hueso, esto proporciona las coordenadas de espacio universal de la malla según se ve afectada por el hueso.</span><span class="sxs-lookup"><span data-stu-id="e49a4-112">When concatenated to the bone's transform, this provides the world space coordinates of the mesh as affected by the bone.</span></span> <span data-ttu-id="e49a4-113">Vea [**Matrix4x4**](matrix4x4.md).</span><span class="sxs-lookup"><span data-stu-id="e49a4-113">See [**Matrix4x4**](matrix4x4.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e49a4-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="e49a4-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="e49a4-115">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="e49a4-115">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



