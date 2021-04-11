---
description: La interpolación de vértices mezcla dos posiciones proporcionadas por el usuario (o normales).
ms.assetid: vs|directx_sdk|~\vertex_tweening.htm
title: Interpolación de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a5458e384fa69b91b1eab1623fb526d514591f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274731"
---
# <a name="vertex-tweening-direct3d-9"></a><span data-ttu-id="57b34-103">Interpolación de vértices (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="57b34-103">Vertex Tweening (Direct3D 9)</span></span>

<span data-ttu-id="57b34-104">La interpolación de vértices mezcla dos posiciones proporcionadas por el usuario (o normales).</span><span class="sxs-lookup"><span data-stu-id="57b34-104">Vertex tweening blends two user-provided positions (or normals).</span></span> <span data-ttu-id="57b34-105">La intercalación es mutuamente excluyente de la fusión de vértices con pesos.</span><span class="sxs-lookup"><span data-stu-id="57b34-105">Tweening is mutually exclusive from vertex blending with weights.</span></span> <span data-ttu-id="57b34-106">La intercalación se realiza antes de la iluminación y el recorte, y se habilita estableciendo D3DRS \_ VERTEXBLEND en D3DVBF \_ intercalación.</span><span class="sxs-lookup"><span data-stu-id="57b34-106">Tweening is performed before lighting and clipping, and is enabled by setting D3DRS\_VERTEXBLEND to D3DVBF\_TWEENING.</span></span> <span data-ttu-id="57b34-107">La posición del vértice resultante se calcula mediante:</span><span class="sxs-lookup"><span data-stu-id="57b34-107">The resulting vertex position is computed by:</span></span>


```
POSITION = POSITION1 * (1.0 - TWEENFACTOR) + POSITION2 * TWEENFACTOR
```



<span data-ttu-id="57b34-108">Se usa el mismo enfoque para calcular las normales.</span><span class="sxs-lookup"><span data-stu-id="57b34-108">The same approach is used for calculating normals.</span></span> <span data-ttu-id="57b34-109">Para obtener más información, vea [usar la interpolación de vértices (Direct3D 9)](using-vertex-tweening.md).</span><span class="sxs-lookup"><span data-stu-id="57b34-109">For more information, see [Using Vertex Tweening (Direct3D 9)](using-vertex-tweening.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="57b34-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="57b34-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57b34-111">Combinación de geometría</span><span class="sxs-lookup"><span data-stu-id="57b34-111">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 



