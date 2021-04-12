---
title: Arquitectura del asignador MIDI
description: Arquitectura del asignador MIDI
ms.assetid: d08d1442-bf9f-46bb-bd44-f512ff4b6bd5
keywords:
- Interfaz digital de instrumentos musicales (MIDI), asignador MIDI
- MIDI (interfaz digital de instrumentos musicales), asignador MIDI
- Asignador de MIDI, arquitectura
- Asignador de MIDI, mapa de configuración
- Mapa de configuración de MIDI
- Asignador de MIDI, mapa de canales
- Asignador de MIDI, mapas de revisiones
- Asignador de MIDI, mapas de claves
- mapa de canal
- mapas de revisiones
- mapas de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba337b05fcff1bd0bb0e948e36e7d290eacb9604
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357495"
---
# <a name="the-midi-mapper-architecture"></a><span data-ttu-id="8413e-114">Arquitectura del asignador MIDI</span><span class="sxs-lookup"><span data-stu-id="8413e-114">The MIDI Mapper Architecture</span></span>

<span data-ttu-id="8413e-115">El asignador MIDI utiliza un mapa de configuración de MIDI para determinar cómo trasladar y redirigir los mensajes que recibe.</span><span class="sxs-lookup"><span data-stu-id="8413e-115">The MIDI Mapper uses a MIDI setup map to determine how to translate and redirect the messages it receives.</span></span> <span data-ttu-id="8413e-116">Un mapa de configuración de MIDI consta de los siguientes tipos de mapas.</span><span class="sxs-lookup"><span data-stu-id="8413e-116">A MIDI setup map consists of the following types of maps.</span></span>

-   [<span data-ttu-id="8413e-117">Asignación de canal</span><span class="sxs-lookup"><span data-stu-id="8413e-117">The Channel Map</span></span>](the-channel-map.md)
-   [<span data-ttu-id="8413e-118">Mapas de revisiones</span><span class="sxs-lookup"><span data-stu-id="8413e-118">Patch Maps</span></span>](patch-maps.md)
-   [<span data-ttu-id="8413e-119">Mapas de claves</span><span class="sxs-lookup"><span data-stu-id="8413e-119">Key Maps</span></span>](key-maps.md)

<span data-ttu-id="8413e-120">En la ilustración siguiente se muestran los roles de canal, revisión y mapas de claves en un mapa de configuración de MIDI.</span><span class="sxs-lookup"><span data-stu-id="8413e-120">The following illustration shows the roles of channel, patch, and key maps in a MIDI setup map.</span></span>

![los roles de canal, revisión y mapas de claves en una imagen de mapa de configuración de MIDI](images/mmap-a02.gif)

 

 




