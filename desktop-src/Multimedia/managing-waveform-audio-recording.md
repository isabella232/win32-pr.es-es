---
title: Administración de la grabación de Waveform-Audio
description: Administración de la grabación de Waveform-Audio
ms.assetid: a44f7c33-54d6-4ba7-bc57-b63c8b205392
keywords:
- audio de onda, grabación
- 'onda: interfaz de audio, grabación'
- grabar audio de onda de onda, acerca de
- Estructura WAVEHDR
- waveInAddBuffer función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539f722a705d489064d38eccdf6d89e80ccb1518
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358853"
---
# <a name="managing-waveform-audio-recording"></a><span data-ttu-id="8a7f7-108">Administración de la grabación de Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="8a7f7-108">Managing Waveform-Audio Recording</span></span>

<span data-ttu-id="8a7f7-109">Después de abrir un dispositivo de entrada de onda-audio, puede empezar a grabar datos de audio de onda.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-109">After you open a waveform-audio input device, you can begin recording waveform-audio data.</span></span> <span data-ttu-id="8a7f7-110">La forma de onda: los datos de audio se registran en los búferes proporcionados por la aplicación especificados por una estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) .</span><span class="sxs-lookup"><span data-stu-id="8a7f7-110">Waveform-audio data is recorded into application-supplied buffers specified by a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure.</span></span> <span data-ttu-id="8a7f7-111">Estos bloques de datos se deben preparar antes de usarse; para obtener más información, consulte [bloques de datos de audio](audio-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="8a7f7-111">These data blocks must be prepared before they are used; for more information, see [Audio Data Blocks](audio-data-blocks.md).</span></span>

<span data-ttu-id="8a7f7-112">Windows proporciona las siguientes funciones para administrar la grabación de audio de onda.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-112">Windows provides the following functions to manage waveform-audio recording.</span></span>



| <span data-ttu-id="8a7f7-113">Función</span><span class="sxs-lookup"><span data-stu-id="8a7f7-113">Function</span></span>                                   | <span data-ttu-id="8a7f7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a7f7-114">Description</span></span>                                                                                |
|--------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a7f7-115">**waveInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="8a7f7-115">**waveInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) | <span data-ttu-id="8a7f7-116">Envía un búfer al controlador de dispositivo para que se pueda rellenar con datos de audio de forma de onda grabados.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-116">Sends a buffer to the device driver so it can be filled with recorded waveform-audio data.</span></span> |
| [<span data-ttu-id="8a7f7-117">**waveInReset**</span><span class="sxs-lookup"><span data-stu-id="8a7f7-117">**waveInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)         | <span data-ttu-id="8a7f7-118">Detiene la grabación de la forma de onda y marca todos los búferes pendientes como terminados.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-118">Stops waveform-audio recording and marks all pending buffers as done.</span></span>                      |
| [<span data-ttu-id="8a7f7-119">**waveInStart**</span><span class="sxs-lookup"><span data-stu-id="8a7f7-119">**waveInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)         | <span data-ttu-id="8a7f7-120">Inicia la grabación de onda y de audio.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-120">Starts waveform-audio recording.</span></span>                                                           |
| [<span data-ttu-id="8a7f7-121">**waveInStop**</span><span class="sxs-lookup"><span data-stu-id="8a7f7-121">**waveInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)           | <span data-ttu-id="8a7f7-122">Detiene la grabación de audio de onda.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-122">Stops waveform-audio recording.</span></span>                                                            |



 

<span data-ttu-id="8a7f7-123">Utilice la función [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) para enviar búferes al controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-123">Use the [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) function to send buffers to the device driver.</span></span> <span data-ttu-id="8a7f7-124">A medida que los búferes se rellenan con datos de audio de forma de onda grabados, se notifica a la aplicación con un mensaje de ventana, un mensaje de devolución de llamada, un mensaje de subproceso o un evento, en función de la marca especificada al abrir el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-124">As the buffers are filled with recorded waveform-audio data, the application is notified with a window message, callback message, thread message, or event, depending on the flag specified when the device was opened.</span></span>

<span data-ttu-id="8a7f7-125">Antes de empezar a grabar mediante [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart), debe enviar al menos un búfer al controlador o se pueden perder los datos entrantes.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-125">Before you begin recording by using [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart), you should send at least one buffer to the driver, or incoming data could be lost.</span></span>

<span data-ttu-id="8a7f7-126">Antes de cerrar el dispositivo con [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose), llame a [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) para marcar los bloques de datos pendientes como realizados.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-126">Before closing the device using [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose), call [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) to mark any pending data blocks as being done.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a7f7-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8a7f7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a7f7-128">Grabación de audio de onda</span><span class="sxs-lookup"><span data-stu-id="8a7f7-128">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 