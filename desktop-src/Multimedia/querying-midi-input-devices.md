---
title: Consulta de dispositivos de entrada MIDI
description: Consulta de dispositivos de entrada MIDI
ms.assetid: 2da88418-f9cf-49da-b17f-8a26d357b5ab
keywords:
- Interfaz digital de instrumentos musicales (MIDI), dispositivos de entrada
- MIDI (interfaz digital de instrumentos musicales), dispositivos de entrada
- grabación de audio MIDI, dispositivos de entrada
- Dispositivos de entrada MIDI
- Interfaz digital de instrumentos musicales (MIDI), consultando dispositivos de entrada
- MIDI (interfaz digital de instrumentos musicales), consulta de dispositivos de entrada
- grabación de audio MIDI, consulta de dispositivos de entrada
- consulta de dispositivos de entrada MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a92bec8733887e20c25f37d1de3dd493e555c8a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665799"
---
# <a name="querying-midi-input-devices"></a><span data-ttu-id="c628e-111">Consulta de dispositivos de entrada MIDI</span><span class="sxs-lookup"><span data-stu-id="c628e-111">Querying MIDI Input Devices</span></span>

<span data-ttu-id="c628e-112">Antes de grabar audio MIDI, debe usar la función [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps) para determinar las capacidades del dispositivo de entrada MIDI que está presente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="c628e-112">Before recording MIDI audio, you should use the [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps) function to determine the capabilities of the MIDI input device that is present in the system.</span></span> <span data-ttu-id="c628e-113">Esta función toma una dirección de una estructura [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) , que rellena con información sobre las capacidades del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="c628e-113">This function takes an address of a [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) structure, which it fills with information about the capabilities of the given device.</span></span> <span data-ttu-id="c628e-114">Esta información incluye los identificadores de fabricante y de producto, un nombre de producto para el dispositivo y el número de versión del controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c628e-114">This information includes the manufacturer and product identifiers, a product name for the device, and the version number of the device driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c628e-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c628e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c628e-116">Grabación de audio MIDI</span><span class="sxs-lookup"><span data-stu-id="c628e-116">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 