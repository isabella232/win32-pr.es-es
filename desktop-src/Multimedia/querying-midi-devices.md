---
title: Consulta de dispositivos MIDI
description: Consulta de dispositivos MIDI
ms.assetid: 0c9882a7-b5cb-41d1-a52e-003112225035
keywords:
- Interfaz digital de instrumentos musicales (MIDI), consultar dispositivos
- MIDI (interfaz digital de instrumentos musicales), consultar dispositivos
- Servicios MIDI, consultar dispositivos
- consulta de dispositivos MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066648d6e9ce89e03b26940cb27f3b62b6a03c07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420580"
---
# <a name="querying-midi-devices"></a><span data-ttu-id="fec61-107">Consulta de dispositivos MIDI</span><span class="sxs-lookup"><span data-stu-id="fec61-107">Querying MIDI Devices</span></span>

<span data-ttu-id="fec61-108">Antes de reproducir o grabar datos MIDI, debe determinar las capacidades del hardware de MIDI presente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="fec61-108">Before playing or recording MIDI data, you must determine the capabilities of the MIDI hardware present in the system.</span></span> <span data-ttu-id="fec61-109">La capacidad MIDI puede variar de un equipo multimedia a otro; las aplicaciones no deben hacer suposiciones sobre el hardware presente en un sistema determinado.</span><span class="sxs-lookup"><span data-stu-id="fec61-109">MIDI capability can vary from one multimedia computer to the next; applications should not make assumptions about the hardware present in a given system.</span></span>

<span data-ttu-id="fec61-110">Windows proporciona las siguientes funciones para determinar el número de dispositivos MIDI que están disponibles para la entrada o la salida en un sistema determinado.</span><span class="sxs-lookup"><span data-stu-id="fec61-110">Windows provides the following functions to determine how many MIDI devices are available for input or output in a given system.</span></span>



| <span data-ttu-id="fec61-111">Value</span><span class="sxs-lookup"><span data-stu-id="fec61-111">Value</span></span>                                          | <span data-ttu-id="fec61-112">Significado</span><span class="sxs-lookup"><span data-stu-id="fec61-112">Meaning</span></span>                                                            |
|------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="fec61-113">**midiInGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="fec61-113">**midiInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)   | <span data-ttu-id="fec61-114">Recupera el número de dispositivos de entrada MIDI presentes en el sistema.</span><span class="sxs-lookup"><span data-stu-id="fec61-114">Retrieves the number of MIDI input devices present in the system.</span></span>  |
| [<span data-ttu-id="fec61-115">**midiOutGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="fec61-115">**midiOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) | <span data-ttu-id="fec61-116">Recupera el número de dispositivos de salida MIDI presentes en el sistema.</span><span class="sxs-lookup"><span data-stu-id="fec61-116">Retrieves the number of MIDI output devices present in the system.</span></span> |



 

<span data-ttu-id="fec61-117">Al igual que otros dispositivos de audio, los dispositivos MIDI se identifican mediante un identificador de dispositivo, que se determina implícitamente a partir del número de dispositivos presentes en un sistema determinado.</span><span class="sxs-lookup"><span data-stu-id="fec61-117">Like other audio devices, MIDI devices are identified by a device identifier, which is determined implicitly from the number of devices present in a given system.</span></span> <span data-ttu-id="fec61-118">Los identificadores de dispositivo van desde cero hasta el número de dispositivos presentes, menos uno.</span><span class="sxs-lookup"><span data-stu-id="fec61-118">Device identifiers range from zero to the number of devices present, minus one.</span></span> <span data-ttu-id="fec61-119">Por ejemplo, si hay dos dispositivos de salida MIDI en un sistema, los identificadores de dispositivo válidos son 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="fec61-119">For example, if there are two MIDI output devices in a system, valid device identifiers are 0 and 1.</span></span>

<span data-ttu-id="fec61-120">Después de determinar el número de dispositivos de entrada o salida MIDI presentes en un sistema, puede consultar las capacidades de cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fec61-120">After you determine how many MIDI input or output devices are present in a system, you can inquire about the capabilities of each device.</span></span> <span data-ttu-id="fec61-121">Windows proporciona las siguientes funciones para determinar las capacidades de los dispositivos de audio.</span><span class="sxs-lookup"><span data-stu-id="fec61-121">Windows provides the following functions to determine the capabilities of audio devices.</span></span>



| <span data-ttu-id="fec61-122">Value</span><span class="sxs-lookup"><span data-stu-id="fec61-122">Value</span></span>                                          | <span data-ttu-id="fec61-123">Significado</span><span class="sxs-lookup"><span data-stu-id="fec61-123">Meaning</span></span>                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fec61-124">**midiInGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="fec61-124">**midiInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)   | <span data-ttu-id="fec61-125">Recupera las capacidades de un dispositivo de entrada MIDI determinado y coloca esta información en la estructura [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) .</span><span class="sxs-lookup"><span data-stu-id="fec61-125">Retrieves the capabilities of a given MIDI input device and places this information in the [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) structure.</span></span>    |
| [<span data-ttu-id="fec61-126">**midiOutGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="fec61-126">**midiOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) | <span data-ttu-id="fec61-127">Recupera las capacidades de un dispositivo de salida MIDI determinado y coloca esta información en la estructura [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) .</span><span class="sxs-lookup"><span data-stu-id="fec61-127">Retrieves the capabilities of a given MIDI output device and places this information in the [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) structure.</span></span> |



 

<span data-ttu-id="fec61-128">Cada una de estas funciones tiene un parámetro que especifica la dirección de una estructura que la función rellena con información sobre las capacidades de un dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="fec61-128">Each of these functions has a parameter specifying the address of a structure that the function fills with information about the capabilities of a specified device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fec61-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fec61-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fec61-130">Servicios MIDI</span><span class="sxs-lookup"><span data-stu-id="fec61-130">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 