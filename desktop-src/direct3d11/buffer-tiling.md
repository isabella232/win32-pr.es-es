---
title: Mosaico de búfer
description: Un recurso de búfer se divide en mosaicos de 64 KB, con un espacio vacío en el último mosaico si el tamaño no es múltiplo de 64 KB.
ms.assetid: 979EFCF3-1FE1-412A-A19D-F1B1CF86423B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fafa009e554499822c90c8fb6c0c8f34e47f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904636"
---
# <a name="buffer-tiling"></a><span data-ttu-id="9d828-103">Mosaico de búfer</span><span class="sxs-lookup"><span data-stu-id="9d828-103">Buffer tiling</span></span>

<span data-ttu-id="9d828-104">Un recurso de [búfer](overviews-direct3d-11-resources-buffers.md) se divide en mosaicos de 64 KB, con un espacio vacío en el último mosaico si el tamaño no es múltiplo de 64 KB.</span><span class="sxs-lookup"><span data-stu-id="9d828-104">A [Buffer](overviews-direct3d-11-resources-buffers.md) resource is divided into 64KB tiles, with some empty space in the last tile if the size is not a multiple of 64KB.</span></span>

<span data-ttu-id="9d828-105">Los búferes estructurados no deben tener ninguna restricción en el intervalo que se va a colocar en mosaico.</span><span class="sxs-lookup"><span data-stu-id="9d828-105">Structured buffers must have no constraint on the stride to be tiled.</span></span> <span data-ttu-id="9d828-106">Sin embargo, las posibles optimizaciones de rendimiento en el hardware para el uso de [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) se pueden sacrificar haciéndolos en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="9d828-106">But possible performance optimizations in hardware for using [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) can be sacrificed by making them tiled in the first place.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d828-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9d828-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d828-108">Cómo se organiza en mosaico el área de un recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="9d828-108">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 