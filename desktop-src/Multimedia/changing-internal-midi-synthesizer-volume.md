---
title: Cambiar el volumen del sintetizador MIDI interno
description: Cambiar el volumen del sintetizador MIDI interno
ms.assetid: 75ab7ff5-f394-4a79-8dcc-f4eef434a36e
keywords:
- Interfaz digital de instrumentos musicales (MIDI), sintetizadores internos
- MIDI (interfaz digital de instrumentos musicales), sintetizadores internos
- reproducir archivos MIDI, sintetizadores internos
- Sintetizadores MIDI internos
- Interfaz digital de instrumentos musicales (MIDI), cambio de volumen
- MIDI (interfaz digital de instrumentos musicales), cambio de volumen
- reproducir archivos MIDI, cambiar el volumen
- cambiar el volumen MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369b13483ce6fa45d82ee177282a0de5e86538e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995225"
---
# <a name="changing-internal-midi-synthesizer-volume"></a><span data-ttu-id="748bb-111">Cambiar el volumen del sintetizador MIDI interno</span><span class="sxs-lookup"><span data-stu-id="748bb-111">Changing Internal MIDI Synthesizer Volume</span></span>

<span data-ttu-id="748bb-112">Windows proporciona las siguientes funciones para recuperar y establecer el nivel de volumen de los dispositivos de sintetizador MIDI internos:</span><span class="sxs-lookup"><span data-stu-id="748bb-112">Windows provides the following functions to retrieve and set the volume level of internal MIDI synthesizer devices:</span></span>



| <span data-ttu-id="748bb-113">Value</span><span class="sxs-lookup"><span data-stu-id="748bb-113">Value</span></span>                                        | <span data-ttu-id="748bb-114">Significado</span><span class="sxs-lookup"><span data-stu-id="748bb-114">Meaning</span></span>                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="748bb-115">**midiOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="748bb-115">**midiOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume) | <span data-ttu-id="748bb-116">Recupera el nivel de volumen del dispositivo de sintetizador MIDI interno especificado.</span><span class="sxs-lookup"><span data-stu-id="748bb-116">Retrieves the volume level of the specified internal MIDI synthesizer device.</span></span> |
| [<span data-ttu-id="748bb-117">**midiOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="748bb-117">**midiOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume) | <span data-ttu-id="748bb-118">Establece el nivel de volumen del dispositivo de sintetizador MIDI interno especificado.</span><span class="sxs-lookup"><span data-stu-id="748bb-118">Sets the volume level of the specified internal MIDI synthesizer device.</span></span>      |



 

<span data-ttu-id="748bb-119">No todos los dispositivos de salida MIDI admiten cambios de volumen.</span><span class="sxs-lookup"><span data-stu-id="748bb-119">Not all MIDI output devices support volume changes.</span></span> <span data-ttu-id="748bb-120">Algunos dispositivos pueden admitir cambios de volumen individuales en los canales izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="748bb-120">Some devices can support individual volume changes on both the left and right channels.</span></span> <span data-ttu-id="748bb-121">Para obtener información sobre cómo determinar si un dispositivo determinado admite cambios de volumen, consulte [consultar los dispositivos de salida MIDI](querying-midi-output-devices.md).</span><span class="sxs-lookup"><span data-stu-id="748bb-121">For information on how to determine if a particular device supports volume changes, see [Querying MIDI Output Devices](querying-midi-output-devices.md).</span></span>

<span data-ttu-id="748bb-122">A menos que la aplicación esté diseñada para ser una aplicación de control de volumen principal (proporciona al usuario control de volumen para todos los dispositivos de audio de un sistema), debe abrir un dispositivo de audio antes de cambiar su volumen.</span><span class="sxs-lookup"><span data-stu-id="748bb-122">Unless your application is designed to be a master volume-control application (provides the user with volume control for all audio devices in a system), you should open an audio device before changing its volume.</span></span> <span data-ttu-id="748bb-123">También debe comprobar el nivel de volumen antes de cambiarlo y restaurar el nivel de volumen a su nivel anterior lo antes posible.</span><span class="sxs-lookup"><span data-stu-id="748bb-123">You should also check the volume level before changing it and restore the volume level to its previous level as soon as possible.</span></span>

<span data-ttu-id="748bb-124">El volumen se especifica como un valor de palabra.</span><span class="sxs-lookup"><span data-stu-id="748bb-124">Volume is specified as a doubleword value.</span></span> <span data-ttu-id="748bb-125">Los 16 bits superiores especifican el volumen relativo del canal derecho y los 16 bits inferiores especifican el volumen relativo del canal izquierdo.</span><span class="sxs-lookup"><span data-stu-id="748bb-125">The upper 16 bits specify the relative volume of the right channel, and the lower 16 bits specify the relative volume of the left channel.</span></span>

<span data-ttu-id="748bb-126">En el caso de los dispositivos que no admiten cambios de volumen individuales en los canales izquierdo y derecho, los 16 bits inferiores especifican el nivel de volumen y se omiten los 16 bits superiores.</span><span class="sxs-lookup"><span data-stu-id="748bb-126">For devices that do not support individual volume changes on both the left and right channels, the lower 16 bits specify the volume level and the upper 16 bits are ignored.</span></span> <span data-ttu-id="748bb-127">Los valores para el intervalo de nivel de volumen desde 0X0 (silencio) hasta 0xFFFF (volumen máximo) y se interpretan logarítmicamente.</span><span class="sxs-lookup"><span data-stu-id="748bb-127">Values for the volume level range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="748bb-128">El aumento del volumen percibido es el mismo cuando se aumenta el nivel de volumen de 0x5000 a 0x6000, ya que es de 0x4000 a 0x5000.</span><span class="sxs-lookup"><span data-stu-id="748bb-128">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 