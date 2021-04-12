---
title: Uso de mensajes de ventana para administrar Waveform-Audio la reproducción
description: Uso de mensajes de ventana para administrar Waveform-Audio la reproducción
ms.assetid: 217968fd-4bb3-405d-a371-c129e29637ab
keywords:
- audio de onda, administración de la reproducción con mensajes
- 'onda: interfaz de audio, administración de la reproducción con mensajes'
- reproducir archivos de audio de onda, administrar la reproducción con mensajes
- audio de una onda, mensajes
- 'onda: interfaz de audio, mensajes'
- reproducción de onda-archivos de audio, mensajes
- Mensaje MM_WOM_CLOSE
- Mensaje MM_WOM_DONE
- Mensaje MM_WOM_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce02794222274e10498e31e0f38939d930ef3745
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358880"
---
# <a name="using-window-messages-to-manage-waveform-audio-playback"></a><span data-ttu-id="b8d57-112">Uso de mensajes de ventana para administrar Waveform-Audio la reproducción</span><span class="sxs-lookup"><span data-stu-id="b8d57-112">Using Window Messages to Manage Waveform-Audio Playback</span></span>

<span data-ttu-id="b8d57-113">Los siguientes mensajes se pueden enviar a una función de procedimiento de ventana para administrar la reproducción de audio de onda.</span><span class="sxs-lookup"><span data-stu-id="b8d57-113">The following messages can be sent to a window procedure function for managing waveform-audio playback.</span></span>



| <span data-ttu-id="b8d57-114">Message</span><span class="sxs-lookup"><span data-stu-id="b8d57-114">Message</span></span>                                | <span data-ttu-id="b8d57-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8d57-115">Description</span></span>                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8d57-116">**cierre de MM \_ WOM \_**</span><span class="sxs-lookup"><span data-stu-id="b8d57-116">**MM\_WOM\_CLOSE**</span></span>](mm-wom-close.md) | <span data-ttu-id="b8d57-117">Se envía cuando el dispositivo se cierra con la función [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) .</span><span class="sxs-lookup"><span data-stu-id="b8d57-117">Sent when the device is closed by using the [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) function.</span></span>                                 |
| [<span data-ttu-id="b8d57-118">**MM \_ WOM \_ listo**</span><span class="sxs-lookup"><span data-stu-id="b8d57-118">**MM\_WOM\_DONE**</span></span>](mm-wom-done.md)   | <span data-ttu-id="b8d57-119">Se envía cuando el controlador de dispositivo finaliza con un bloque de datos enviado mediante la función [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) .</span><span class="sxs-lookup"><span data-stu-id="b8d57-119">Sent when the device driver is finished with a data block sent by using the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function.</span></span> |
| [<span data-ttu-id="b8d57-120">**MM \_ WOM \_ abierto**</span><span class="sxs-lookup"><span data-stu-id="b8d57-120">**MM\_WOM\_OPEN**</span></span>](mm-wom-open.md)   | <span data-ttu-id="b8d57-121">Se envía cuando el dispositivo se abre con la función [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .</span><span class="sxs-lookup"><span data-stu-id="b8d57-121">Sent when the device is opened by using the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span>                                   |



 

<span data-ttu-id="b8d57-122">Un parámetro *wParam* y *lParam* está asociado a cada uno de estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="b8d57-122">A *wParam* and *lParam* parameter is associated with each of these messages.</span></span> <span data-ttu-id="b8d57-123">El parámetro *wParam* siempre especifica un identificador del dispositivo de audio de onda abierto.</span><span class="sxs-lookup"><span data-stu-id="b8d57-123">The *wParam* parameter always specifies a handle of the open waveform-audio device.</span></span> <span data-ttu-id="b8d57-124">Para el mensaje [**mm \_ WOM \_ Done**](mm-wom-done.md) , *lParam* especifica un puntero a una estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica el bloque de datos completado.</span><span class="sxs-lookup"><span data-stu-id="b8d57-124">For the [**MM\_WOM\_DONE**](mm-wom-done.md) message, *lParam* specifies a pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the completed data block.</span></span> <span data-ttu-id="b8d57-125">El parámetro *lParam* no se utiliza para los mensajes de apertura de [**mm \_ WOM \_**](mm-wom-close.md) y [**\_ WOM \_**](mm-wom-open.md) .</span><span class="sxs-lookup"><span data-stu-id="b8d57-125">The *lParam* parameter is unused for the [**MM\_WOM\_CLOSE**](mm-wom-close.md) and [**MM\_WOM\_OPEN**](mm-wom-open.md) messages.</span></span>

<span data-ttu-id="b8d57-126">El mensaje más útil es probablemente MM \_ WOM \_ done.</span><span class="sxs-lookup"><span data-stu-id="b8d57-126">The most useful message is probably MM\_WOM\_DONE.</span></span> <span data-ttu-id="b8d57-127">Cuando este mensaje indica que se ha completado la reproducción de un bloque de datos, puede limpiar y liberar el bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="b8d57-127">When this message signals that playback of a data block is complete, you can clean up and free the data block.</span></span> <span data-ttu-id="b8d57-128">A menos que necesite asignar memoria o inicializar variables, es probable que no necesite procesar los \_ mensajes mm WOM \_ Open y mm \_ WOM \_ Close.</span><span class="sxs-lookup"><span data-stu-id="b8d57-128">Unless you need to allocate memory or initialize variables, you probably do not need to process the MM\_WOM\_OPEN and MM\_WOM\_CLOSE messages.</span></span>

<span data-ttu-id="b8d57-129">La aplicación proporciona la función de devolución de llamada para dispositivos de salida de onda-audio.</span><span class="sxs-lookup"><span data-stu-id="b8d57-129">The callback function for waveform-audio output devices is supplied by the application.</span></span> <span data-ttu-id="b8d57-130">Para obtener información sobre esta función de devolución de llamada, vea la función [**waveOutProc**](/previous-versions//dd743869(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b8d57-130">For information about this callback function, see the [**waveOutProc**](/previous-versions//dd743869(v=vs.85)) function.</span></span>

 

 