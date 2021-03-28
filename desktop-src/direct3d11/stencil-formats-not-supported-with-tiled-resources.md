---
title: Formatos de estarcido no compatibles con recursos en mosaico
description: Los formatos que contienen la galería de símbolos no se admiten con recursos en mosaico.
ms.assetid: 1B675245-F21F-47B5-B3B4-C8307DAC575B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce07b64e54808a2b4b730f6ed9c5321956f6bf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075001"
---
# <a name="stencil-formats-not-supported-with-tiled-resources"></a><span data-ttu-id="f83c3-103">Formatos de estarcido no compatibles con recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="f83c3-103">Stencil formats not supported with tiled resources</span></span>

<span data-ttu-id="f83c3-104">Los formatos que contienen la galería de símbolos no se admiten con recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="f83c3-104">Formats that contain stencil aren't supported with tiled resources.</span></span>

<span data-ttu-id="f83c3-105">Los formatos que contienen la Galería \_ de símbolos incluyen el formato dxgi \_ D24 \_ UNORM \_ S8 \_ uint (y los formatos relacionados en la familia R24G8) y el \_ formato dxgi \_ D32 \_ float \_ S8X24 \_ uint (y los formatos relacionados en la familia R32G8X24).</span><span class="sxs-lookup"><span data-stu-id="f83c3-105">Formats that contain stencil include DXGI\_FORMAT\_D24\_UNORM\_S8\_UINT (and related formats in the R24G8 family) and DXGI\_FORMAT\_D32\_FLOAT\_S8X24\_UINT (and related formats in the R32G8X24 family).</span></span>

<span data-ttu-id="f83c3-106">Algunas implementaciones almacenan la profundidad y la galería de símbolos en asignaciones independientes mientras que otras las almacenan juntas.</span><span class="sxs-lookup"><span data-stu-id="f83c3-106">Some implementations store depth and stencil in separate allocations while others store them together.</span></span> <span data-ttu-id="f83c3-107">La administración de mosaicos para los dos esquemas tendría que ser diferente, y ninguna API única puede abstraer o racionalizar las diferencias.</span><span class="sxs-lookup"><span data-stu-id="f83c3-107">Tile management for the two schemes would have to be different, and no single API can abstract or rationalize the differences.</span></span> <span data-ttu-id="f83c3-108">Se recomienda que el hardware futuro admita superficies de estarcido y profundidad independientes, cada una de las cuales se organiza por separado.</span><span class="sxs-lookup"><span data-stu-id="f83c3-108">We recommend for future hardware to support independent depth and stencil surfaces, each independently tiled.</span></span> <span data-ttu-id="f83c3-109">la profundidad de bits de 32 tendría iconos de 128x128 y la galería de símbolos de 8 bits tendría iconos de 256x256.</span><span class="sxs-lookup"><span data-stu-id="f83c3-109">32 bit depth would have 128x128 tiles, and 8 bit stencil would have 256x256 tiles.</span></span> <span data-ttu-id="f83c3-110">Por lo tanto, las aplicaciones tendrían que vivir con la alineación de la forma de mosaico entre la profundidad y la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="f83c3-110">Therefore, applications would have to live with tile shape misalignment between depth and stencil.</span></span> <span data-ttu-id="f83c3-111">Pero ya existe el mismo problema con los distintos formatos de superficie de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="f83c3-111">But the same problem exists with different render target surface formats already.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f83c3-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f83c3-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f83c3-113">Proceso cruzado y uso compartido de dispositivos entre recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="f83c3-113">Tiled resource cross process and device sharing</span></span>](tiled-resource-cross-process-and-device-sharing.md)
</dt> </dl>

 

 




