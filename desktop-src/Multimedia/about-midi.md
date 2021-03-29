---
title: Acerca de MIDI
description: Acerca de MIDI
ms.assetid: 32030c98-e513-4ee3-bbd0-ba41fceadd57
keywords:
- Windows multimedia, interfaz digital de instrumentos musicales (MIDI)
- multimedia, interfaz digital de instrumentos musicales (MIDI)
- audio multimedia, interfaz digital de instrumentos musicales (MIDI)
- audio, interfaz digital de instrumentos musicales (MIDI)
- Interfaz digital de instrumentos musicales (MIDI), acerca de
- MIDI (interfaz digital de instrumentos musicales), acerca de
- Interfaz digital de instrumentos musicales (MIDI), interfaz de control de medios (MCI)
- MIDI (interfaz digital de instrumentos musicales), interfaz de control de medios (MCI)
- Interfaz digital de instrumentos musicales (MIDI), búferes de secuencia
- MIDI (interfaz digital de instrumentos musicales), búferes de secuencia
- Interfaz digital de instrumentos musicales (MIDI), servicios MIDI
- MIDI (interfaz digital de instrumentos musicales), servicios MIDI
- Media control Interface (MCI), interfaz digital de instrumentos musicales (MIDI)
- MCI (media control Interface), interfaz digital de instrumentos musicales (MIDI)
- búferes de secuencia, acerca de
- Servicios MIDI, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c476807f750f9e90788377588f6c9af96561aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774461"
---
# <a name="about-midi"></a><span data-ttu-id="d865b-119">Acerca de MIDI</span><span class="sxs-lookup"><span data-stu-id="d865b-119">About MIDI</span></span>

<span data-ttu-id="d865b-120">La interfaz de programación de aplicaciones (API) de Microsoft Win32 proporciona los siguientes métodos para que las aplicaciones funcionen con datos MIDI:</span><span class="sxs-lookup"><span data-stu-id="d865b-120">The Microsoft Win32 application programming interface (API) provides the following methods for applications to work with MIDI data:</span></span>

-   <span data-ttu-id="d865b-121">La interfaz de control de medios (MCI).</span><span class="sxs-lookup"><span data-stu-id="d865b-121">The Media Control Interface (MCI).</span></span> <span data-ttu-id="d865b-122">Aunque la manera más sencilla de reproducir un archivo MIDI es usar la clase de ventana MCIWnd, también puede usar comandos MCI para crear una interfaz personalizada para un dispositivo MIDI.</span><span class="sxs-lookup"><span data-stu-id="d865b-122">Although the simplest way to play a MIDI file is to use the MCIWnd window class, you can also use MCI commands to create a customized interface to a MIDI device.</span></span> <span data-ttu-id="d865b-123">Para obtener más información sobre la clase de ventana MCIWnd, consulte [clase de ventana MCIWnd](mciwnd-window-class.md).</span><span class="sxs-lookup"><span data-stu-id="d865b-123">For more information about the MCIWnd window class, see [MCIWnd Window Class](mciwnd-window-class.md).</span></span> <span data-ttu-id="d865b-124">Para obtener más información acerca de MCI, consulte [MCI](mci.md)o [media control Interface (MCI)](media-control-interface--mci.md).</span><span class="sxs-lookup"><span data-stu-id="d865b-124">For more information about MCI, see [MCI](mci.md), or [Media Control Interface (MCI)](media-control-interface--mci.md).</span></span>
-   <span data-ttu-id="d865b-125">[Búferes de secuencia](stream-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="d865b-125">[Stream Buffers](stream-buffers.md).</span></span> <span data-ttu-id="d865b-126">Este formato permite a una aplicación manipular los búferes de datos MIDI con marca de tiempo para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="d865b-126">This format allows an application to manipulate buffers of time-stamped MIDI data for playback.</span></span> <span data-ttu-id="d865b-127">Los búferes de secuencia son útiles para las aplicaciones que requieren un control más preciso de la salida que las ofertas de MCI.</span><span class="sxs-lookup"><span data-stu-id="d865b-127">Stream buffers are useful to applications that require more precise control over output than MCI offers.</span></span>
-   <span data-ttu-id="d865b-128">[Servicios MIDI](midi-services.md).</span><span class="sxs-lookup"><span data-stu-id="d865b-128">[MIDI Services](midi-services.md).</span></span> <span data-ttu-id="d865b-129">Las aplicaciones que necesitan el control más preciso de los datos MIDI suelen usar estos servicios de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="d865b-129">Applications that need the most precise control of MIDI data typically use these low-level services.</span></span>

<span data-ttu-id="d865b-130">En los temas siguientes se describe cada uno de estos métodos y se proporciona información general sobre el asignador MIDI.</span><span class="sxs-lookup"><span data-stu-id="d865b-130">The following topics discuss each of these methods and provides an overview of the MIDI Mapper.</span></span>

-   [<span data-ttu-id="d865b-131">El asignador MIDI</span><span class="sxs-lookup"><span data-stu-id="d865b-131">The MIDI Mapper</span></span>](the-midi-mapper.md)
-   [<span data-ttu-id="d865b-132">Media control Interface (MCI)</span><span class="sxs-lookup"><span data-stu-id="d865b-132">Media Control Interface (MCI)</span></span>](media-control-interface--mci.md)
-   [<span data-ttu-id="d865b-133">Búferes de secuencia</span><span class="sxs-lookup"><span data-stu-id="d865b-133">Stream Buffers</span></span>](stream-buffers.md)
-   [<span data-ttu-id="d865b-134">Servicios MIDI</span><span class="sxs-lookup"><span data-stu-id="d865b-134">MIDI Services</span></span>](midi-services.md)
-   [<span data-ttu-id="d865b-135">Reproducir archivos MIDI</span><span class="sxs-lookup"><span data-stu-id="d865b-135">Playing MIDI Files</span></span>](playing-midi-files.md)
-   [<span data-ttu-id="d865b-136">Grabación de audio MIDI</span><span class="sxs-lookup"><span data-stu-id="d865b-136">Recording MIDI Audio</span></span>](recording-midi-audio.md)
-   [<span data-ttu-id="d865b-137">Procesamiento de datos MIDI de dos orígenes MIDI</span><span class="sxs-lookup"><span data-stu-id="d865b-137">Processing MIDI Data from Two MIDI Sources</span></span>](processing-midi-data-from-two-midi-sources.md)
-   [<span data-ttu-id="d865b-138">Crear archivos MIDI</span><span class="sxs-lookup"><span data-stu-id="d865b-138">Creating MIDI Files</span></span>](creating-midi-files.md)

 

 




