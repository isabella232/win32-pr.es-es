---
description: Si no se enciende con un sombreador de vértices o un sombreador de píxeles, puede optar por usar el motor de iluminación en el tiempo de ejecución.
ms.assetid: vs|directx_sdk|~\lighting_state.htm
title: Estado de iluminación (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74f0e7b7ec4a8bcf0ee27c9bc1e643536819d8fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705193"
---
# <a name="lighting-state-direct3d-9"></a><span data-ttu-id="6ee7b-103">Estado de iluminación (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6ee7b-103">Lighting State (Direct3D 9)</span></span>

<span data-ttu-id="6ee7b-104">Si no se enciende con un sombreador de vértices o un sombreador de píxeles, puede optar por usar el motor de iluminación en el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="6ee7b-104">If you do not light with a vertex shader or a pixel shader, you may choose to use the lighting engine in the runtime.</span></span> <span data-ttu-id="6ee7b-105">El motor de iluminación requiere que los datos del vértice contengan normales por vértice; los vértices sin datos normales generarán un producto DOT de cero en todos los cálculos de iluminación.</span><span class="sxs-lookup"><span data-stu-id="6ee7b-105">The lighting engine requires that the vertex data contains per-vertex normals; vertices without normal data will generate a dot product of zero in all lighting computations.</span></span> <span data-ttu-id="6ee7b-106">Los cálculos de iluminación se describen con más detalle en [matemáticas de iluminación (Direct3D 9)](mathematics-of-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="6ee7b-106">The lighting calculations are covered in more detail in [Mathematics of Lighting (Direct3D 9)](mathematics-of-lighting.md).</span></span>

<span data-ttu-id="6ee7b-107">Para habilitar el motor de iluminación, use:</span><span class="sxs-lookup"><span data-stu-id="6ee7b-107">To enable the lighting engine, use:</span></span>


```
SetRenderState(D3DRS_LIGHTING, TRUE); 
```



## <a name="related-topics"></a><span data-ttu-id="6ee7b-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6ee7b-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ee7b-109">Estados de representación</span><span class="sxs-lookup"><span data-stu-id="6ee7b-109">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



