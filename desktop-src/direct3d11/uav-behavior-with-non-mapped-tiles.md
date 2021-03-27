---
title: Comportamiento UAV con iconos sin asignar
description: El comportamiento de las lecturas y escrituras de la vista de acceso desordenado (UAV) depende del nivel de compatibilidad de hardware.
ms.assetid: 26C40D1F-983B-4E5B-99F3-FD4E47BE1D7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9909f8faecd3345761ae26e60835c77aae9ab3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993981"
---
# <a name="uav-behavior-with-non-mapped-tiles"></a><span data-ttu-id="8aa6f-103">Comportamiento UAV con iconos sin asignar</span><span class="sxs-lookup"><span data-stu-id="8aa6f-103">UAV behavior with non-mapped tiles</span></span>

<span data-ttu-id="8aa6f-104">El comportamiento de las lecturas y escrituras de la vista de acceso desordenado (UAV) depende del nivel de compatibilidad de hardware.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-104">Behavior of unordered access view (UAV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="8aa6f-105">Para ver un desglose de los requisitos, consulte el comportamiento general de lectura y escritura para [los niveles de características de los recursos en mosaico](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="8aa6f-105">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span> <span data-ttu-id="8aa6f-106">En esta sección se resume el comportamiento ideal.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-106">This section summarizes the ideal behavior.</span></span>

<span data-ttu-id="8aa6f-107">Las operaciones del sombreador que leen de un mosaico no asignado en una UAV devuelven 0 en todos los componentes que no faltan del formato y el valor predeterminado para los componentes que faltan.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-107">Shader operations that read from a non-mapped tile in a UAV return 0 in all non-missing components of the format, and the default for missing components.</span></span>

<span data-ttu-id="8aa6f-108">Las operaciones del sombreador que intentan escribir en un mosaico no asignado no provocan que se escriba nada en el área no asignada (mientras se escribe en un área asignada).</span><span class="sxs-lookup"><span data-stu-id="8aa6f-108">Shader operations that attempt to write to a non-mapped tile cause nothing to be written to the non-mapped area (while writes to a mapped area proceed).</span></span> <span data-ttu-id="8aa6f-109">Esta definición ideal para el control de escritura no es necesaria en el [nivel 2](tier-2.md); las escrituras en mosaicos no asignados pueden acabar en una memoria caché que las lecturas posteriores podrían recogerse.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-109">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8aa6f-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8aa6f-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8aa6f-111">Acceso de canalización a recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="8aa6f-111">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




