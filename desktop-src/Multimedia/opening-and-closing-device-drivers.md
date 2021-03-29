---
title: Abrir y cerrar controladores de dispositivos
description: Abrir y cerrar controladores de dispositivos
ms.assetid: 441bc0ec-41c9-4595-92f9-4c2304b10f16
keywords:
- Interfaz digital de instrumentos musicales (MIDI), abrir dispositivos
- MIDI (interfaz digital de instrumentos musicales), abrir dispositivos
- Servicios MIDI, abrir dispositivos
- apertura de dispositivos MIDI
- Interfaz digital de instrumentos musicales (MIDI), cerrar dispositivos
- MIDI (interfaz digital de instrumentos musicales), cerrar dispositivos
- Servicios MIDI, cerrar dispositivos
- cerrar dispositivos MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d7035455baa067b81af7da980a4ae043500c7b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789958"
---
# <a name="opening-and-closing-device-drivers"></a><span data-ttu-id="7f8fc-111">Abrir y cerrar controladores de dispositivos</span><span class="sxs-lookup"><span data-stu-id="7f8fc-111">Opening and Closing Device Drivers</span></span>

<span data-ttu-id="7f8fc-112">Debe abrir un dispositivo MIDI antes de usarlo y debe cerrar el dispositivo tan pronto como termine de usarlo.</span><span class="sxs-lookup"><span data-stu-id="7f8fc-112">You must open a MIDI device before using it, and you should close the device as soon as you finish using it.</span></span> <span data-ttu-id="7f8fc-113">Windows proporciona las siguientes funciones para abrir y cerrar diferentes tipos de dispositivos MIDI.</span><span class="sxs-lookup"><span data-stu-id="7f8fc-113">Windows provides the following functions to open and close different types of MIDI devices.</span></span>



| <span data-ttu-id="7f8fc-114">Value</span><span class="sxs-lookup"><span data-stu-id="7f8fc-114">Value</span></span>                                | <span data-ttu-id="7f8fc-115">Significado</span><span class="sxs-lookup"><span data-stu-id="7f8fc-115">Meaning</span></span>                                            |
|--------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="7f8fc-116">**midiInClose**</span><span class="sxs-lookup"><span data-stu-id="7f8fc-116">**midiInClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)   | <span data-ttu-id="7f8fc-117">Cierra un dispositivo de entrada MIDI especificado.</span><span class="sxs-lookup"><span data-stu-id="7f8fc-117">Closes a specified MIDI input device.</span></span>              |
| [<span data-ttu-id="7f8fc-118">**midiInOpen**</span><span class="sxs-lookup"><span data-stu-id="7f8fc-118">**midiInOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)     | <span data-ttu-id="7f8fc-119">Abre un dispositivo de entrada MIDI especificado para grabar.</span><span class="sxs-lookup"><span data-stu-id="7f8fc-119">Opens a specified MIDI input device for recording.</span></span> |
| [<span data-ttu-id="7f8fc-120">**midiOutClose**</span><span class="sxs-lookup"><span data-stu-id="7f8fc-120">**midiOutClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) | <span data-ttu-id="7f8fc-121">Cierra un dispositivo de salida MIDI especificado.</span><span class="sxs-lookup"><span data-stu-id="7f8fc-121">Closes a specified MIDI output device.</span></span>             |
| [<span data-ttu-id="7f8fc-122">**midiOutOpen**</span><span class="sxs-lookup"><span data-stu-id="7f8fc-122">**midiOutOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)   | <span data-ttu-id="7f8fc-123">Abre un dispositivo de salida MIDI para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="7f8fc-123">Opens a MIDI output device for playback.</span></span>           |



 

<span data-ttu-id="7f8fc-124">Cada función que abre un dispositivo MIDI toma como parámetros un identificador de dispositivo, una dirección de una ubicación de memoria y algunos parámetros exclusivos de los dispositivos MIDI.</span><span class="sxs-lookup"><span data-stu-id="7f8fc-124">Each function that opens a MIDI device takes as parameters a device identifier, an address of a memory location, and some parameters unique to MIDI devices.</span></span> <span data-ttu-id="7f8fc-125">La ubicación de memoria se rellena con un identificador de dispositivo, que se usa para identificar el dispositivo de audio abierto en llamadas a otras funciones de audio.</span><span class="sxs-lookup"><span data-stu-id="7f8fc-125">The memory location is filled with a device handle, which is used to identify the open audio device in calls to other audio functions.</span></span>

<span data-ttu-id="7f8fc-126">Muchas funciones MIDI pueden aceptar un identificador de dispositivo o un identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f8fc-126">Many MIDI functions can accept either a device handle or a device identifier.</span></span> <span data-ttu-id="7f8fc-127">Aunque puede usar un identificador de dispositivo siempre que use un identificador de dispositivo, no puede usar siempre un identificador de dispositivo cuando se llama a un identificador para.</span><span class="sxs-lookup"><span data-stu-id="7f8fc-127">Although you can use a device handle wherever you would use a device identifier, you cannot always use a device identifier when a handle is called for.</span></span>

> [!Note]  
> <span data-ttu-id="7f8fc-128">Los dispositivos MIDI no se pueden compartir necesariamente, por lo que es posible que un dispositivo determinado no esté disponible cuando un usuario lo solicite.</span><span class="sxs-lookup"><span data-stu-id="7f8fc-128">MIDI devices are not necessarily sharable, so a particular device may not be available when a user requests it.</span></span> <span data-ttu-id="7f8fc-129">Si esto ocurre, la aplicación debe notificar al usuario y permitir que el usuario intente abrir el dispositivo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="7f8fc-129">If this happens, the application should notify the user and allow the user to try to open the device again.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7f8fc-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7f8fc-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f8fc-131">Servicios MIDI</span><span class="sxs-lookup"><span data-stu-id="7f8fc-131">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 