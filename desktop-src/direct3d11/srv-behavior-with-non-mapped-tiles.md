---
title: Comportamiento SRV con iconos sin asignar
description: El comportamiento de las lecturas de vista de recursos del sombreador (SRV) que impliquen mosaicos no asignados depende del nivel de compatibilidad de hardware.
ms.assetid: 9B720BEE-AB0C-4B75-92AD-3F382A107D48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e086a4db869c3204fc560e64002ba04e8bd8ba9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268244"
---
# <a name="srv-behavior-with-non-mapped-tiles"></a><span data-ttu-id="146a5-103">Comportamiento SRV con iconos sin asignar</span><span class="sxs-lookup"><span data-stu-id="146a5-103">SRV behavior with non-mapped tiles</span></span>

<span data-ttu-id="146a5-104">El comportamiento de las lecturas de vista de recursos del sombreador (SRV) que impliquen mosaicos no asignados depende del nivel de compatibilidad de hardware.</span><span class="sxs-lookup"><span data-stu-id="146a5-104">Behavior of shader resource view (SRV) reads that involve non-mapped tiles depends on the level of hardware support.</span></span> <span data-ttu-id="146a5-105">Para ver un desglose de los requisitos, consulte el comportamiento de lectura de [los recursos en mosaico características de las capas](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="146a5-105">For a breakdown of requirements, see read behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span> <span data-ttu-id="146a5-106">En esta sección se resume el comportamiento ideal, que requiere el [nivel 2](tier-2.md) .</span><span class="sxs-lookup"><span data-stu-id="146a5-106">This section summarizes the ideal behavior, which [Tier 2](tier-2.md) requires.</span></span>

<span data-ttu-id="146a5-107">Considere una operación de filtro de textura que lee de un conjunto de textura en un SRV.</span><span class="sxs-lookup"><span data-stu-id="146a5-107">Consider a texture filter operation that reads from a set of texels in an SRV.</span></span> <span data-ttu-id="146a5-108">Los textura que se encuentran en mosaicos no asignados contribuyen a 0 en todos los componentes que no faltan del formato (y el valor predeterminado para los componentes que faltan) en la operación de filtro general junto con las contribuciones de textura asignados.</span><span class="sxs-lookup"><span data-stu-id="146a5-108">Texels that fall on non-mapped tiles contribute 0 in all non-missing components of the format (and the default for missing components) into the overall filter operation alongside contributions from mapped texels.</span></span> <span data-ttu-id="146a5-109">Los textura están todos ponderados y combinados juntos, independientemente de si los datos proceden de mosaicos asignados o no asignados.</span><span class="sxs-lookup"><span data-stu-id="146a5-109">The texels are all weighted and combined together independent of whether the data came from mapped or non-mapped tiles.</span></span>

<span data-ttu-id="146a5-110">Parte del hardware de nivel [2](tier-2.md) de primera generación no cumple este requisito de especificación y devuelve 0 con los valores predeterminados descritos anteriormente como resultado de filtro general si cualquier textura (con un peso distinto de cero) se encuentra en mosaicos no asignados.</span><span class="sxs-lookup"><span data-stu-id="146a5-110">Some first generation [Tier 2](tier-2.md) level hardware does not meet this spec requirement and returns the 0 with defaults described preceding as the overall filter result if any texels (with nonzero weight) fall on non-mapped tiles.</span></span> <span data-ttu-id="146a5-111">No se permitirá que ningún otro hardware pierda el requisito de incluir todos los textura (sin peso) en el filtro.</span><span class="sxs-lookup"><span data-stu-id="146a5-111">No other hardware will be allowed to miss the requirement to include all (nonzero weight) texels in the filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="146a5-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="146a5-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="146a5-113">Acceso de canalización a recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="146a5-113">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




