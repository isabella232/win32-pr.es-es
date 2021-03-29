---
title: Reproducción de audio simple
description: Reproducción de audio simple
ms.assetid: 51a0244d-123d-4efe-92e9-972e914cef78
keywords:
- audio multimedia, de onda
- audio, de onda
- audio de forma de onda, reproducción simple
- MessageBeep función)
- sndPlaySound función)
- Función PlaySound, reproducción simple
- audio multimedia, función PlaySound
- audio, función PlaySound
- audio de onda, función PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256feded06de4ee92ee415f14bb08adc7fb4456e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995175"
---
# <a name="simple-audio-playback"></a><span data-ttu-id="9bf1f-112">Reproducción de audio simple</span><span class="sxs-lookup"><span data-stu-id="9bf1f-112">Simple Audio Playback</span></span>

<span data-ttu-id="9bf1f-113">Puede utilizar las siguientes funciones para reproducir audio de una onda en la aplicación en una única llamada de función.</span><span class="sxs-lookup"><span data-stu-id="9bf1f-113">You can use the following functions to play waveform audio in your application in a single function call.</span></span>



| <span data-ttu-id="9bf1f-114">Función</span><span class="sxs-lookup"><span data-stu-id="9bf1f-114">Function</span></span>                                                      | <span data-ttu-id="9bf1f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="9bf1f-115">Description</span></span>                                                                                                         |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9bf1f-116">MessageBeep</span><span class="sxs-lookup"><span data-stu-id="9bf1f-116">MessageBeep</span></span>](/windows/win32/api/winuser/nf-winuser-messagebeep) | <span data-ttu-id="9bf1f-117">Reproduce el sonido que corresponde a un nivel de alerta del sistema especificado.</span><span class="sxs-lookup"><span data-stu-id="9bf1f-117">Plays the sound that corresponds to a specified system-alert level.</span></span>                                                 |
| <span data-ttu-id="9bf1f-118">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9bf1f-118">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span></span>                          | <span data-ttu-id="9bf1f-119">Reproduce el sonido que corresponde al sonido del sistema escrito en el registro o el contenido del archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="9bf1f-119">Plays the sound that corresponds to the system sound entered in the registry or the contents of the specified file.</span></span> |
| <span data-ttu-id="9bf1f-120">[**Reproducción**](/previous-versions//dd743680(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9bf1f-120">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span></span>                                | <span data-ttu-id="9bf1f-121">Proporciona toda la funcionalidad de [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) y puede acceder directamente a los recursos.</span><span class="sxs-lookup"><span data-stu-id="9bf1f-121">Provides all the functionality of [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) and can directly access resources.</span></span>           |



 

<span data-ttu-id="9bf1f-122">La función **MessageBeep** es una parte estándar de la API de Win32; Dado que sus capacidades son muy limitadas y se documentan en otro lugar, no se trata aquí.</span><span class="sxs-lookup"><span data-stu-id="9bf1f-122">The **MessageBeep** function is a standard part of the Win32 API; because its capabilities are very limited and it is documented elsewhere, it is not discussed here.</span></span>

<span data-ttu-id="9bf1f-123">Las funciones enumeradas admiten los siguientes orígenes de audio de onda:</span><span class="sxs-lookup"><span data-stu-id="9bf1f-123">The functions listed support the following sources of waveform audio:</span></span>

-   <span data-ttu-id="9bf1f-124">Archivos de audio de forma de onda asociados a los niveles de alerta del sistema</span><span class="sxs-lookup"><span data-stu-id="9bf1f-124">Waveform-audio files associated with system-alert levels</span></span>
-   <span data-ttu-id="9bf1f-125">Forma de onda: archivos de audio especificados por entradas en el registro</span><span class="sxs-lookup"><span data-stu-id="9bf1f-125">Waveform-audio files specified by entries in the registry</span></span>
-   <span data-ttu-id="9bf1f-126">Recursos de onda en memoria</span><span class="sxs-lookup"><span data-stu-id="9bf1f-126">In-memory WAVE resources</span></span>
-   <span data-ttu-id="9bf1f-127">Forma de onda-archivos de audio especificados por nombre</span><span class="sxs-lookup"><span data-stu-id="9bf1f-127">Waveform-audio files specified by name</span></span>

<span data-ttu-id="9bf1f-128">Las funciones [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) y [**PlaySound**](/previous-versions//dd743680(v=vs.85)) cargan un archivo de audio de onda completo en la memoria y, de hecho, limitan el tamaño del archivo que pueden reproducir.</span><span class="sxs-lookup"><span data-stu-id="9bf1f-128">The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) and [**PlaySound**](/previous-versions//dd743680(v=vs.85)) functions load an entire waveform-audio file into memory and, in effect, limit the size of the file they can play.</span></span> <span data-ttu-id="9bf1f-129">Use **sndPlaySound** y **PlaySound** para reproducir archivos de audio de forma de onda pequeños, de hasta 100 000.</span><span class="sxs-lookup"><span data-stu-id="9bf1f-129">Use **sndPlaySound** and **PlaySound** to play waveform-audio files that are small — up to about 100K.</span></span> <span data-ttu-id="9bf1f-130">Estas dos funciones también requieren que los datos de sonido estén en un formato que se pueda reproducir con uno de los controladores de audio de forma de onda instalados, incluido el asignador de onda.</span><span class="sxs-lookup"><span data-stu-id="9bf1f-130">These two functions also require the sound data to be in a format that is playable by one of the installed waveform-audio drivers, including the wave mapper.</span></span>

<span data-ttu-id="9bf1f-131">En el caso de archivos de sonido de mayor tamaño, utilice los servicios de media control Interface (MCI).</span><span class="sxs-lookup"><span data-stu-id="9bf1f-131">For larger sound files, use the Media Control Interface (MCI) services.</span></span> <span data-ttu-id="9bf1f-132">Para obtener más información, consulte [MCI](mci.md).</span><span class="sxs-lookup"><span data-stu-id="9bf1f-132">For more information, see [MCI](mci.md).</span></span>

 

 