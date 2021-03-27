---
title: Comportamiento de rasterizador con iconos sin asignar
description: En esta sección se describe el comportamiento de rasterizador con mosaicos no asignados.
ms.assetid: 3477A621-7051-4585-AB58-523EE64CDC5C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54230321f4286b92a3444e3f74167ee7b8711c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996773"
---
# <a name="rasterizer-behavior-with-non-mapped-tiles"></a><span data-ttu-id="06bb7-103">Comportamiento de rasterizador con iconos sin asignar</span><span class="sxs-lookup"><span data-stu-id="06bb7-103">Rasterizer behavior with non-mapped tiles</span></span>

<span data-ttu-id="06bb7-104">En esta sección se describe el comportamiento de rasterizador con mosaicos no asignados.</span><span class="sxs-lookup"><span data-stu-id="06bb7-104">This section describes rasterizer behavior with non-mapped tiles.</span></span>

## <a name="depthstencilview"></a><span data-ttu-id="06bb7-105">DepthStencilView</span><span class="sxs-lookup"><span data-stu-id="06bb7-105">DepthStencilView</span></span>

<span data-ttu-id="06bb7-106">El comportamiento de las lecturas y escrituras de la vista de galería de símbolos de profundidad (DSV) depende del nivel de compatibilidad de hardware.</span><span class="sxs-lookup"><span data-stu-id="06bb7-106">Behavior of depth stencil view (DSV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="06bb7-107">Para ver un desglose de los requisitos, consulte el comportamiento general de lectura y escritura para [los niveles de características de los recursos en mosaico](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="06bb7-107">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span>

<span data-ttu-id="06bb7-108">Este es el comportamiento ideal:</span><span class="sxs-lookup"><span data-stu-id="06bb7-108">Here is the ideal behavior:</span></span>

<span data-ttu-id="06bb7-109">Si un mosaico no se asigna en DepthStencilView, el valor devuelto de la profundidad de lectura es 0, que se introduce en las operaciones configuradas para el valor de lectura de profundidad.</span><span class="sxs-lookup"><span data-stu-id="06bb7-109">If a tile isn't mapped in the DepthStencilView, the return value from reading depth is 0, which is then fed into whatever operations are configured for the depth read value.</span></span> <span data-ttu-id="06bb7-110">Las escrituras en el icono de profundidad que falta se quitan.</span><span class="sxs-lookup"><span data-stu-id="06bb7-110">Writes to the missing depth tile are dropped.</span></span> <span data-ttu-id="06bb7-111">Esta definición ideal para el control de escritura no es necesaria en el [nivel 2](tier-2.md); las escrituras en mosaicos no asignados pueden acabar en una memoria caché que las lecturas posteriores podrían recogerse.</span><span class="sxs-lookup"><span data-stu-id="06bb7-111">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="rendertargetview"></a><span data-ttu-id="06bb7-112">RenderTargetView</span><span class="sxs-lookup"><span data-stu-id="06bb7-112">RenderTargetView</span></span>

<span data-ttu-id="06bb7-113">El comportamiento de las lecturas y escrituras de la vista de destino de representación (RTV) depende del nivel de compatibilidad de hardware.</span><span class="sxs-lookup"><span data-stu-id="06bb7-113">Behavior of render target view (RTV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="06bb7-114">Para ver un desglose de los requisitos, consulte el comportamiento general de lectura y escritura para [los niveles de características de los recursos en mosaico](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="06bb7-114">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span>

<span data-ttu-id="06bb7-115">En todas las implementaciones, los distintos RTVs (y DSV) enlazados simultáneamente pueden tener distintas áreas asignadas frente a no asignadas y pueden tener formatos de superficie de tamaño diferentes (lo que significa diferentes formas de mosaico).</span><span class="sxs-lookup"><span data-stu-id="06bb7-115">On all implementations, different RTVs (and DSV) bound simultaneously can have different areas mapped versus non-mapped and can have different sized surface formats (which means different tile shapes).</span></span>

<span data-ttu-id="06bb7-116">Este es el comportamiento ideal:</span><span class="sxs-lookup"><span data-stu-id="06bb7-116">Here is the ideal behavior:</span></span>

<span data-ttu-id="06bb7-117">Las lecturas de RTVs devuelven 0 en los mosaicos que faltan y las escrituras se quitan.</span><span class="sxs-lookup"><span data-stu-id="06bb7-117">Reads from RTVs return 0 in missing tiles and writes are dropped.</span></span> <span data-ttu-id="06bb7-118">Esta definición ideal para el control de escritura no es necesaria en el [nivel 2](tier-2.md); las escrituras en mosaicos no asignados pueden acabar en una memoria caché que las lecturas posteriores podrían recogerse.</span><span class="sxs-lookup"><span data-stu-id="06bb7-118">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06bb7-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="06bb7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06bb7-120">Acceso de canalización a recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="06bb7-120">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




