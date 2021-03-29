---
title: Mapas de claves
description: Mapas de claves
ms.assetid: 5d0367b0-bbf1-4a4b-98b2-dbca6f2f8b0c
keywords:
- Interfaz digital de instrumentos musicales (MIDI), asignador MIDI
- MIDI (interfaz digital de instrumentos musicales), asignador MIDI
- Asignador de MIDI, mapas de claves
- mapas de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffafd99e6d813f12c388b633997980b7a58d62dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994079"
---
# <a name="key-maps"></a><span data-ttu-id="3f141-107">Mapas de claves</span><span class="sxs-lookup"><span data-stu-id="3f141-107">Key Maps</span></span>

<span data-ttu-id="3f141-108">Cada entrada de la tabla de traducción patch-Map puede tener asociado un mapa de claves.</span><span class="sxs-lookup"><span data-stu-id="3f141-108">Each entry in the patch-map translation table can have an associated key map.</span></span> <span data-ttu-id="3f141-109">Los mapas de claves afectan a los mensajes de Nota: on, note-off y Polyphonic-Key-aftertouch.</span><span class="sxs-lookup"><span data-stu-id="3f141-109">Key maps affect note-on, note-off, and polyphonic-key-aftertouch messages.</span></span> <span data-ttu-id="3f141-110">Un mapa de claves tiene una tabla de traducción con una entrada para cada uno de los valores de clave MIDI 128.</span><span class="sxs-lookup"><span data-stu-id="3f141-110">A key map has a translation table with an entry for each of the 128 MIDI key values.</span></span> <span data-ttu-id="3f141-111">Por ejemplo, si la entrada del valor de clave 60 es 72, el asignador de MIDI modifica los mensajes de la nota de MIDI, tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="3f141-111">For example, if the entry for key value 60 is 72, the MIDI Mapper modifies MIDI note-on messages as shown in the following illustration.</span></span>

![imagen del asignador MIDI](images/mmap-a06.gif)

<span data-ttu-id="3f141-113">Los mapas de claves son útiles con los sintetizadores que tienen instrumentos de percusión basados en claves con un sonido de percusión determinado asignado a cada clave.</span><span class="sxs-lookup"><span data-stu-id="3f141-113">Key maps are useful with synthesizers that have key-based percussion instruments with a particular percussion sound assigned to each key.</span></span> <span data-ttu-id="3f141-114">Normalmente, los mapas de claves se asignan a la primera revisión de las asignaciones de revisión en los canales de percusión (10 y 16).</span><span class="sxs-lookup"><span data-stu-id="3f141-114">Key maps are usually assigned to the first patch in the patch maps on the percussion channels (10 and 16).</span></span>

 

 




