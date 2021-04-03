---
title: Media control Interface (MCI)
description: Media control Interface (MCI)
ms.assetid: e22f23b5-0fa6-4957-bbbf-b1b3a4c8bd31
keywords:
- Multimedia de Windows, interfaz de control de medios (MCI)
- multimedia, media control Interface (MCI)
- audio multimedia, interfaz de control de medios (MCI)
- audio, interfaz de control de medios (MCI)
- Interfaz digital de instrumentos musicales (MIDI), interfaz de control de medios (MCI)
- MIDI (interfaz digital de instrumentos musicales), interfaz de control de medios (MCI)
- Media control Interface (MCI), interfaz digital de instrumentos musicales (MIDI)
- MCI (media control Interface), interfaz digital de instrumentos musicales (MIDI)
- Media control Interface (MCI), MIDI Sequencer
- MCI (media control Interface), MIDI Sequencer
- Secuenciador MIDI de MCI, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aaf582f625c4411a2400ee381ec5c17d4d8ae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075647"
---
# <a name="media-control-interface-mci"></a><span data-ttu-id="67890-114">Media control Interface (MCI)</span><span class="sxs-lookup"><span data-stu-id="67890-114">Media Control Interface (MCI)</span></span>

<span data-ttu-id="67890-115">MCI MIDI Sequencer es el componente del sistema MCI que reproduce archivos MIDI.</span><span class="sxs-lookup"><span data-stu-id="67890-115">The MCI MIDI sequencer is the MCI system component that plays MIDI files.</span></span> <span data-ttu-id="67890-116">Las aplicaciones pueden reproducir archivos MIDI fácilmente mediante MCI, pero MCI impone las siguientes restricciones en las capacidades MIDI:</span><span class="sxs-lookup"><span data-stu-id="67890-116">Applications can play MIDI files easily using MCI, but MCI imposes the following restrictions on MIDI capabilities:</span></span>

-   <span data-ttu-id="67890-117">MCI solo admite la salida MIDI.</span><span class="sxs-lookup"><span data-stu-id="67890-117">MCI supports MIDI output only.</span></span>
-   <span data-ttu-id="67890-118">MCI no permite la sincronización de cierre entre eventos MIDI y otros eventos en tiempo real (por ejemplo, vídeo).</span><span class="sxs-lookup"><span data-stu-id="67890-118">MCI does not allow close synchronization between MIDI events and other real-time events (such as video).</span></span>

<span data-ttu-id="67890-119">Si necesita la sincronización de MIDI precisa, debe utilizar los búferes de secuencia o los servicios MIDI.</span><span class="sxs-lookup"><span data-stu-id="67890-119">If you need accurate MIDI synchronization, you must use the stream buffers or the MIDI services.</span></span> <span data-ttu-id="67890-120">Si necesita funciones de entrada MIDI, debe utilizar los servicios MIDI.</span><span class="sxs-lookup"><span data-stu-id="67890-120">If you need MIDI input capabilities, you must use the MIDI services.</span></span>

<span data-ttu-id="67890-121">MCI MIDI Sequencer reproduce archivos MIDI estándar y archivos MIDI de formato de archivo de intercambio de recursos (RIFF), conocidos como archivos RMID.</span><span class="sxs-lookup"><span data-stu-id="67890-121">The MCI MIDI sequencer plays standard MIDI files and resource interchange file format (RIFF) MIDI files, known as RMID files.</span></span> <span data-ttu-id="67890-122">Los archivos MIDI estándar se ajustan a la especificación [estándar de los archivos midi 1,0](creating-midi-files.md) .</span><span class="sxs-lookup"><span data-stu-id="67890-122">Standard MIDI files conform to the [Standard MIDI Files 1.0](creating-midi-files.md) specification.</span></span> <span data-ttu-id="67890-123">Dado que los archivos RMID son archivos MIDI estándar con un encabezado RIFF, la información acerca de los archivos MIDI estándar también se aplica a los archivos RMID.</span><span class="sxs-lookup"><span data-stu-id="67890-123">Because RMID files are standard MIDI files with a RIFF header, information about standard MIDI files also applies to RMID files.</span></span> <span data-ttu-id="67890-124">Para obtener más información acerca de los archivos RIFF, vea [servicios de formato de archivo de intercambio de recursos](resource-interchange-file-format-services.md).</span><span class="sxs-lookup"><span data-stu-id="67890-124">For more information about RIFF files, see [Resource Interchange File Format Services](resource-interchange-file-format-services.md).</span></span>

<span data-ttu-id="67890-125">Aunque actualmente hay tres tipos de archivos MIDI estándar, MCI Sequencer solo reproduce dos de ellos: Format 0 y Format 1 archivos MIDI.</span><span class="sxs-lookup"><span data-stu-id="67890-125">Although there are currently three kinds of standard MIDI files, the MCI sequencer plays only two of them: Format 0 and Format 1 MIDI files.</span></span>

<span data-ttu-id="67890-126">Para obtener más información sobre cómo controlar los dispositivos multimedia (incluidos los secuenciadores) mediante comandos MCI, consulte [MCI](mci.md).</span><span class="sxs-lookup"><span data-stu-id="67890-126">For more information about controlling multimedia devices (including sequencers) using MCI commands, see [MCI](mci.md).</span></span>

 

 




