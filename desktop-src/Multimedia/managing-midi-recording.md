---
title: Administración de la grabación de MIDI
description: Administración de la grabación de MIDI
ms.assetid: 48b2d815-72cf-4c96-8d93-247d2426b8f2
keywords:
- Interfaz digital de instrumentos musicales (MIDI), grabación
- MIDI (interfaz digital de instrumentos musicales), grabar
- grabar audio MIDI, administrar
- Grabación MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edfb81976e1f5333798c9705640e7676281968a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487550"
---
# <a name="managing-midi-recording"></a><span data-ttu-id="c50e5-107">Administración de la grabación de MIDI</span><span class="sxs-lookup"><span data-stu-id="c50e5-107">Managing MIDI Recording</span></span>

<span data-ttu-id="c50e5-108">Después de abrir un dispositivo MIDI, puede empezar a grabar datos MIDI.</span><span class="sxs-lookup"><span data-stu-id="c50e5-108">After you open a MIDI device, you can begin recording MIDI data.</span></span> <span data-ttu-id="c50e5-109">Windows proporciona las siguientes funciones para la administración de la grabación de MIDI.</span><span class="sxs-lookup"><span data-stu-id="c50e5-109">Windows provides the following functions for managing MIDI recording.</span></span>



| <span data-ttu-id="c50e5-110">Value</span><span class="sxs-lookup"><span data-stu-id="c50e5-110">Value</span></span>                                      | <span data-ttu-id="c50e5-111">Significado</span><span class="sxs-lookup"><span data-stu-id="c50e5-111">Meaning</span></span>                                                                                           |
|--------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c50e5-112">**midiInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="c50e5-112">**midiInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) | <span data-ttu-id="c50e5-113">Envía un búfer al controlador de dispositivo para que se pueda rellenar con datos MIDI exclusivos del sistema grabados.</span><span class="sxs-lookup"><span data-stu-id="c50e5-113">Sends a buffer to the device driver so it can be filled with recorded system-exclusive MIDI data.</span></span> |
| [<span data-ttu-id="c50e5-114">**midiInReset**</span><span class="sxs-lookup"><span data-stu-id="c50e5-114">**midiInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)         | <span data-ttu-id="c50e5-115">Detiene la grabación de MIDI y marca todos los búferes pendientes como terminados.</span><span class="sxs-lookup"><span data-stu-id="c50e5-115">Stops MIDI recording and marks all pending buffers as done.</span></span>                                       |
| [<span data-ttu-id="c50e5-116">**midiInStart**</span><span class="sxs-lookup"><span data-stu-id="c50e5-116">**midiInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)         | <span data-ttu-id="c50e5-117">Inicia la grabación MIDI y restablece la marca de tiempo en cero.</span><span class="sxs-lookup"><span data-stu-id="c50e5-117">Starts MIDI recording and resets the time stamp to zero.</span></span>                                          |
| [<span data-ttu-id="c50e5-118">**midiInStop**</span><span class="sxs-lookup"><span data-stu-id="c50e5-118">**midiInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)           | <span data-ttu-id="c50e5-119">Detiene la grabación de MIDI.</span><span class="sxs-lookup"><span data-stu-id="c50e5-119">Stops MIDI recording.</span></span>                                                                             |



 

<span data-ttu-id="c50e5-120">Para enviar búferes al controlador de dispositivo para grabar mensajes exclusivos del sistema, use [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer).</span><span class="sxs-lookup"><span data-stu-id="c50e5-120">To send buffers to the device driver for recording system-exclusive messages, use [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer).</span></span> <span data-ttu-id="c50e5-121">La aplicación recibe una notificación, ya que los búferes se rellenan con datos registrados exclusivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="c50e5-121">The application is notified as the buffers are filled with system-exclusive recorded data.</span></span> <span data-ttu-id="c50e5-122">Para obtener más información acerca de las técnicas de notificación, consulte [administrar bloques de datos MIDI](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="c50e5-122">For more information about the notification techniques, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

<span data-ttu-id="c50e5-123">La función [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) inicia el proceso de grabación.</span><span class="sxs-lookup"><span data-stu-id="c50e5-123">The [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function begins the recording process.</span></span> <span data-ttu-id="c50e5-124">Al grabar mensajes exclusivos del sistema, envíe al menos un búfer al controlador antes de iniciar la grabación.</span><span class="sxs-lookup"><span data-stu-id="c50e5-124">When recording system-exclusive messages, send at least one buffer to the driver before starting recording.</span></span> <span data-ttu-id="c50e5-125">Para detener la grabación, use [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop).</span><span class="sxs-lookup"><span data-stu-id="c50e5-125">To stop recording, use [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop).</span></span> <span data-ttu-id="c50e5-126">Antes de cerrar el dispositivo mediante la función [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) , marque los bloques de datos pendientes como si se realizara llamando a [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).</span><span class="sxs-lookup"><span data-stu-id="c50e5-126">Before closing the device by using the [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) function, mark any pending data blocks as being done by calling [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).</span></span>

<span data-ttu-id="c50e5-127">Las aplicaciones que requieren datos con marca de tiempo usan una función de devolución de llamada para recibir datos MIDI.</span><span class="sxs-lookup"><span data-stu-id="c50e5-127">Applications that require time-stamped data use a callback function to receive MIDI data.</span></span> <span data-ttu-id="c50e5-128">Si los requisitos de control de tiempo no son estrictos, puede utilizar una devolución de llamada de ventana o de subproceso.</span><span class="sxs-lookup"><span data-stu-id="c50e5-128">If your timing requirements are not strict, you can use a window or thread callback.</span></span> <span data-ttu-id="c50e5-129">Sin embargo, no puede usar una devolución de llamada de evento para recibir datos MIDI.</span><span class="sxs-lookup"><span data-stu-id="c50e5-129">However, you cannot use an event callback to receive MIDI data.</span></span>

<span data-ttu-id="c50e5-130">Para registrar mensajes exclusivos del sistema con aplicaciones que no utilizan búferes de secuencia, debe proporcionar el controlador de dispositivo con búferes.</span><span class="sxs-lookup"><span data-stu-id="c50e5-130">To record system-exclusive messages with applications that do not use stream buffers, you must supply the device driver with buffers.</span></span> <span data-ttu-id="c50e5-131">Estos búferes se especifican mediante una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .</span><span class="sxs-lookup"><span data-stu-id="c50e5-131">These buffers are specified by using a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c50e5-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c50e5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c50e5-133">Grabación de audio MIDI</span><span class="sxs-lookup"><span data-stu-id="c50e5-133">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 