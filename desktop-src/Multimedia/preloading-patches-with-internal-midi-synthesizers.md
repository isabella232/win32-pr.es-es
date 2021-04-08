---
title: Carga previa de revisiones con sintetizadores MIDI internos
description: Carga previa de revisiones con sintetizadores MIDI internos
ms.assetid: c200aa91-ab91-48e8-b3b5-8e7f36e511be
keywords:
- Interfaz digital de instrumentos musicales (MIDI), sintetizadores internos
- MIDI (interfaz digital de instrumentos musicales), sintetizadores internos
- reproducir archivos MIDI, sintetizadores internos
- Sintetizadores MIDI internos
- Interfaz digital de instrumentos musicales (MIDI), precarga de revisiones
- MIDI (interfaz digital de instrumentos musicales), precarga de revisiones
- reproducir archivos MIDI, carga previa de revisiones
- carga previa de revisiones MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc54eccdaa0a0c9aa16f206e7e036f322b615d96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995165"
---
# <a name="preloading-patches-with-internal-midi-synthesizers"></a><span data-ttu-id="75bd0-111">Carga previa de revisiones con sintetizadores MIDI internos</span><span class="sxs-lookup"><span data-stu-id="75bd0-111">Preloading Patches with Internal MIDI Synthesizers</span></span>

<span data-ttu-id="75bd0-112">Algunos dispositivos de sintetizador MIDI internos no pueden mantener todas las revisiones cargadas simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="75bd0-112">Some internal MIDI synthesizer devices cannot keep all of their patches loaded simultaneously.</span></span> <span data-ttu-id="75bd0-113">Estos dispositivos deben cargar previamente los datos de revisión.</span><span class="sxs-lookup"><span data-stu-id="75bd0-113">These devices must preload their patch data.</span></span>

<span data-ttu-id="75bd0-114">Windows proporciona las siguientes funciones para solicitar que un sintetizador precargue y almacene en caché las revisiones especificadas.</span><span class="sxs-lookup"><span data-stu-id="75bd0-114">Windows provides the following functions to request that a synthesizer preload and cache specified patches.</span></span>



| <span data-ttu-id="75bd0-115">Value</span><span class="sxs-lookup"><span data-stu-id="75bd0-115">Value</span></span>                                                      | <span data-ttu-id="75bd0-116">Significado</span><span class="sxs-lookup"><span data-stu-id="75bd0-116">Meaning</span></span>                                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75bd0-117">**midiOutCachePatches**</span><span class="sxs-lookup"><span data-stu-id="75bd0-117">**midiOutCachePatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)         | <span data-ttu-id="75bd0-118">Solicita que un dispositivo de sintetizador MIDI interno precargue y almacene en caché las revisiones de melodic especificadas.</span><span class="sxs-lookup"><span data-stu-id="75bd0-118">Requests that an internal MIDI synthesizer device preload and cache specified melodic patches.</span></span>              |
| [<span data-ttu-id="75bd0-119">**midiOutCacheDrumPatches**</span><span class="sxs-lookup"><span data-stu-id="75bd0-119">**midiOutCacheDrumPatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches) | <span data-ttu-id="75bd0-120">Solicita que un dispositivo de sintetizador MIDI interno precargue y almacene en caché las revisiones de percusión basadas en clave especificadas.</span><span class="sxs-lookup"><span data-stu-id="75bd0-120">Requests that an internal MIDI synthesizer device preload and cache specified key-based percussion patches.</span></span> |



 

<span data-ttu-id="75bd0-121">Para obtener información sobre cómo determinar si un dispositivo determinado admite revisiones de carga previa, consulte [consultar los dispositivos de salida MIDI](querying-midi-output-devices.md).</span><span class="sxs-lookup"><span data-stu-id="75bd0-121">For information on how to determine if a particular device supports preloading patches, see [Querying MIDI Output Devices](querying-midi-output-devices.md).</span></span>

 

 