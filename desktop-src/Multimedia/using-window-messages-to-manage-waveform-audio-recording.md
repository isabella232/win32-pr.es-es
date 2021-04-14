---
title: Uso de mensajes de ventana para administrar la grabación de Waveform-Audio
description: Uso de mensajes de ventana para administrar la grabación de Waveform-Audio
ms.assetid: 65637d51-9d30-48db-8681-48332442130e
keywords:
- audio de onda, administración de grabaciones con mensajes
- 'onda: interfaz de audio, administración de grabaciones con mensajes'
- grabación de audio de onda y administración de grabaciones con mensajes
- audio de una onda, mensajes
- 'onda: interfaz de audio, mensajes'
- grabar audio de onda de onda, mensajes
- Mensaje MM_WIM_CLOSE
- Mensaje MM_WIM_DATA
- Mensaje MM_WIM_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70bb1cfe1ed0f7ba6052fc1eb6af8fca8355d87d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487579"
---
# <a name="using-window-messages-to-manage-waveform-audio-recording"></a><span data-ttu-id="f61f1-112">Uso de mensajes de ventana para administrar la grabación de Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="f61f1-112">Using Window Messages to Manage Waveform-Audio Recording</span></span>

<span data-ttu-id="f61f1-113">Los siguientes mensajes se pueden enviar a una función de procedimiento de ventana para la administración de la grabación de audio de onda.</span><span class="sxs-lookup"><span data-stu-id="f61f1-113">The following messages can be sent to a window procedure function for managing waveform-audio recording.</span></span>



| <span data-ttu-id="f61f1-114">Message</span><span class="sxs-lookup"><span data-stu-id="f61f1-114">Message</span></span>                                | <span data-ttu-id="f61f1-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="f61f1-115">Description</span></span>                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f61f1-116">**MM \_ - \_ cerrar Wim**</span><span class="sxs-lookup"><span data-stu-id="f61f1-116">**MM\_WIM\_CLOSE**</span></span>](mm-wim-close.md) | <span data-ttu-id="f61f1-117">Se envía cuando el dispositivo se cierra con la función [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) .</span><span class="sxs-lookup"><span data-stu-id="f61f1-117">Sent when the device is closed by using the [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) function.</span></span>                                     |
| [<span data-ttu-id="f61f1-118">**\_datos Wim \_ mm**</span><span class="sxs-lookup"><span data-stu-id="f61f1-118">**MM\_WIM\_DATA**</span></span>](mm-wim-data.md)   | <span data-ttu-id="f61f1-119">Se envía cuando el controlador de dispositivo finaliza con un búfer enviado mediante la función [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) .</span><span class="sxs-lookup"><span data-stu-id="f61f1-119">Sent when the device driver is finished with a buffer sent by using the [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) function.</span></span> |
| [<span data-ttu-id="f61f1-120">**MM \_ Wim \_ abierto**</span><span class="sxs-lookup"><span data-stu-id="f61f1-120">**MM\_WIM\_OPEN**</span></span>](mm-wim-open.md)   | <span data-ttu-id="f61f1-121">Se envía cuando el dispositivo se abre con la función [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) .</span><span class="sxs-lookup"><span data-stu-id="f61f1-121">Sent when the device is opened by using the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function.</span></span>                                       |



 

<span data-ttu-id="f61f1-122">El parámetro *lParam* de [**\_ \_ datos Wim mm**](mm-wim-data.md) especifica un puntero a una estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica el búfer.</span><span class="sxs-lookup"><span data-stu-id="f61f1-122">The *lParam* parameter of [**MM\_WIM\_DATA**](mm-wim-data.md) specifies a pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer.</span></span> <span data-ttu-id="f61f1-123">Este búfer no se puede rellenar completamente con datos de audio de forma de onda; la grabación puede detenerse antes de que se llene el búfer.</span><span class="sxs-lookup"><span data-stu-id="f61f1-123">This buffer might not be completely filled with waveform-audio data; recording can stop before the buffer is filled.</span></span> <span data-ttu-id="f61f1-124">Use el miembro **dwBytesRecorded** de la estructura **WAVEHDR** para determinar la cantidad de datos válidos presentes en el búfer.</span><span class="sxs-lookup"><span data-stu-id="f61f1-124">Use the **dwBytesRecorded** member of the **WAVEHDR** structure to determine the amount of valid data present in the buffer.</span></span>

<span data-ttu-id="f61f1-125">El mensaje más útil es probablemente [**\_ \_ datos Wim de mm**](mm-wim-data.md).</span><span class="sxs-lookup"><span data-stu-id="f61f1-125">The most useful message is probably [**MM\_WIM\_DATA**](mm-wim-data.md).</span></span> <span data-ttu-id="f61f1-126">Cuando la aplicación termina de usar el bloque de datos enviado por el controlador de dispositivo, puede limpiar y liberar el bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="f61f1-126">When your application finishes using the data block sent by the device driver, you can clean up and free the data block.</span></span> <span data-ttu-id="f61f1-127">A menos que necesite asignar memoria o inicializar variables, es probable que no necesite usar los mensajes [**mm \_ Wim \_ Open**](mm-wim-open.md) y [**mm \_ \_ Close**](mm-wim-close.md) .</span><span class="sxs-lookup"><span data-stu-id="f61f1-127">Unless you need to allocate memory or initialize variables, you probably do not need to use the [**MM\_WIM\_OPEN**](mm-wim-open.md) and [**MM\_WIM\_CLOSE**](mm-wim-close.md) messages.</span></span>

<span data-ttu-id="f61f1-128">La aplicación proporciona la función de devolución de llamada para dispositivos de entrada de audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="f61f1-128">The callback function for waveform-audio input devices is supplied by the application.</span></span> <span data-ttu-id="f61f1-129">Para obtener información sobre esta función de devolución de llamada, vea la función [**waveInProc**](/previous-versions//dd743849(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f61f1-129">For information about this callback function, see the [**waveInProc**](/previous-versions//dd743849(v=vs.85)) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f61f1-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f61f1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f61f1-131">Grabación de audio de onda</span><span class="sxs-lookup"><span data-stu-id="f61f1-131">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 