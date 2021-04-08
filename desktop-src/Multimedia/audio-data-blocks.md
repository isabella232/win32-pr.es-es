---
title: Bloques de datos de audio
description: Bloques de datos de audio
ms.assetid: 9646e18c-294b-4532-bd5e-709d66ad31f4
keywords:
- audio multimedia, bloques de datos
- audio, bloques de datos
- audio de onda, bloques de datos
- bloques de datos de audio, acerca de
- Estructura WAVEHDR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a81a5a29ec9718e7c11306b6bafc1aa20369e5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995141"
---
# <a name="audio-data-blocks"></a><span data-ttu-id="50c1d-108">Bloques de datos de audio</span><span class="sxs-lookup"><span data-stu-id="50c1d-108">Audio Data Blocks</span></span>

<span data-ttu-id="50c1d-109">Las funciones [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) y [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) requieren que las aplicaciones asignen bloques de datos para pasarlos a los controladores de dispositivos con fines de grabación o reproducción.</span><span class="sxs-lookup"><span data-stu-id="50c1d-109">The [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) and [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) functions require applications to allocate data blocks to pass to the device drivers for recording or playback purposes.</span></span> <span data-ttu-id="50c1d-110">Ambas funciones usan la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para describir su bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="50c1d-110">Both of these functions use the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure to describe its data block.</span></span>

<span data-ttu-id="50c1d-111">Antes de usar una de estas funciones para pasar un bloque de datos a un controlador de dispositivo, debe asignar memoria para el bloque de datos y la estructura de encabezado que describe el bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="50c1d-111">Before using one of these functions to pass a data block to a device driver, you must allocate memory for the data block and the header structure that describes the data block.</span></span> <span data-ttu-id="50c1d-112">Los encabezados se pueden preparar y no preparar mediante las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="50c1d-112">The headers can be prepared and unprepared by using the following functions.</span></span>



| <span data-ttu-id="50c1d-113">Función</span><span class="sxs-lookup"><span data-stu-id="50c1d-113">Function</span></span>                                                 | <span data-ttu-id="50c1d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="50c1d-114">Description</span></span>                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="50c1d-115">**waveInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="50c1d-115">**waveInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)       | <span data-ttu-id="50c1d-116">Prepara un bloque de datos de entrada de onda-audio.</span><span class="sxs-lookup"><span data-stu-id="50c1d-116">Prepares a waveform-audio input data block.</span></span>                      |
| [<span data-ttu-id="50c1d-117">**waveInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="50c1d-117">**waveInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)   | <span data-ttu-id="50c1d-118">Limpia la preparación en un bloque de datos de entrada de audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="50c1d-118">Cleans up the preparation on a waveform-audio input data block.</span></span>  |
| [<span data-ttu-id="50c1d-119">**waveOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="50c1d-119">**waveOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)     | <span data-ttu-id="50c1d-120">Prepara un bloque de datos de salida de onda-audio.</span><span class="sxs-lookup"><span data-stu-id="50c1d-120">Prepares a waveform-audio output data block.</span></span>                     |
| [<span data-ttu-id="50c1d-121">**waveOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="50c1d-121">**waveOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) | <span data-ttu-id="50c1d-122">Limpia la preparación en un bloque de datos de salida de onda-audio.</span><span class="sxs-lookup"><span data-stu-id="50c1d-122">Cleans up the preparation on a waveform-audio output data block.</span></span> |



 

<span data-ttu-id="50c1d-123">Antes de pasar un bloque de datos de audio a un controlador de dispositivo, debe preparar el bloque de datos pasándolo a [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) o [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader).</span><span class="sxs-lookup"><span data-stu-id="50c1d-123">Before you pass an audio data block to a device driver, you must prepare the data block by passing it to either [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) or [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader).</span></span> <span data-ttu-id="50c1d-124">Cuando el controlador de dispositivo finaliza con el bloque de datos y lo devuelve, debe limpiar esta preparación pasando el bloque de datos a [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) o [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) antes de que se pueda liberar cualquier memoria asignada.</span><span class="sxs-lookup"><span data-stu-id="50c1d-124">When the device driver is finished with the data block and returns it, you must clean up this preparation by passing the data block to either [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) or [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) before any allocated memory can be freed.</span></span>

<span data-ttu-id="50c1d-125">A menos que los datos de entrada y salida de la forma de onda sean lo suficientemente pequeños como para que se incluyan en un único bloque de datos, las aplicaciones deben proporcionar continuamente el controlador de dispositivo con bloqueos de datos hasta que se complete la reproducción o grabación.</span><span class="sxs-lookup"><span data-stu-id="50c1d-125">Unless the waveform-audio input and output data is small enough to be contained in a single data block, applications must continually supply the device driver with data blocks until playback or recording is complete.</span></span>

<span data-ttu-id="50c1d-126">Incluso si se usa un solo bloque de datos, una aplicación debe ser capaz de determinar si un controlador de dispositivo ha terminado con el bloque de datos para que la aplicación pueda liberar la memoria asociada al bloque de datos y la estructura de encabezado.</span><span class="sxs-lookup"><span data-stu-id="50c1d-126">Even if a single data block is used, an application must be able to determine when a device driver is finished with the data block so the application can free the memory associated with the data block and header structure.</span></span> <span data-ttu-id="50c1d-127">Hay varias maneras de determinar cuándo un controlador de dispositivo ha terminado con un bloque de datos:</span><span class="sxs-lookup"><span data-stu-id="50c1d-127">There are several ways to determine when a device driver is finished with a data block:</span></span>

-   <span data-ttu-id="50c1d-128">Al especificar una función de devolución de llamada para recibir un mensaje enviado por el controlador cuando ha terminado con un bloque de datos</span><span class="sxs-lookup"><span data-stu-id="50c1d-128">By specifying a callback function to receive a message sent by the driver when it is finished with a data block</span></span>
-   <span data-ttu-id="50c1d-129">Mediante el uso de una devolución de llamada de evento</span><span class="sxs-lookup"><span data-stu-id="50c1d-129">By using an event callback</span></span>
-   <span data-ttu-id="50c1d-130">Mediante la especificación de una ventana o un subproceso para recibir un mensaje enviado por el controlador cuando ha terminado con un bloque de datos</span><span class="sxs-lookup"><span data-stu-id="50c1d-130">By specifying a window or thread to receive a message sent by the driver when it is finished with a data block</span></span>
-   <span data-ttu-id="50c1d-131">Sondeando el bit WHDR \_ done en el miembro **dwFlags** de la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) enviada con cada bloque de datos</span><span class="sxs-lookup"><span data-stu-id="50c1d-131">By polling the WHDR\_DONE bit in the **dwFlags** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure sent with each data block</span></span>

<span data-ttu-id="50c1d-132">Si una aplicación no obtiene un bloque de datos para el controlador de dispositivo cuando sea necesario, puede haber un hueco audible en la reproducción o una pérdida de la información registrada entrante.</span><span class="sxs-lookup"><span data-stu-id="50c1d-132">If an application does not get a data block to the device driver when needed, there can be an audible gap in playback or a loss of incoming recorded information.</span></span> <span data-ttu-id="50c1d-133">Esto requiere al menos un esquema de almacenamiento en búfer doble, lo que mantiene al menos un bloque de datos antes que el controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="50c1d-133">This requires at least a double-buffering scheme — staying at least one data block ahead of the device driver.</span></span>

<span data-ttu-id="50c1d-134">En los temas siguientes se describen las distintas formas de determinar cuándo un controlador de dispositivo ha terminado con un bloque de datos:</span><span class="sxs-lookup"><span data-stu-id="50c1d-134">The following topics describe ways to determine when a device driver is finished with a data block:</span></span>

<span data-ttu-id="50c1d-135">Usar una función de devolución de llamada para procesar mensajes de controlador</span><span class="sxs-lookup"><span data-stu-id="50c1d-135">Using a Callback Function to Process Driver Messages</span></span>

-   [<span data-ttu-id="50c1d-136">Usar una función de devolución de llamada para procesar mensajes de controlador</span><span class="sxs-lookup"><span data-stu-id="50c1d-136">Using a Callback Function to Process Driver Messages</span></span>](using-a-callback-function-to-process-driver-messages.md)
-   [<span data-ttu-id="50c1d-137">Usar una devolución de llamada de evento para procesar mensajes de controlador</span><span class="sxs-lookup"><span data-stu-id="50c1d-137">Using an Event Callback to Process Driver Messages</span></span>](using-an-callback-to-process-driver-messages.md)
-   [<span data-ttu-id="50c1d-138">Usar una ventana o un subproceso para procesar mensajes de controlador</span><span class="sxs-lookup"><span data-stu-id="50c1d-138">Using a Window or Thread to Process Driver Messages</span></span>](using-a-window-or-thread-to-process-driver-messages.md)
-   [<span data-ttu-id="50c1d-139">Administrar bloques de datos mediante sondeo</span><span class="sxs-lookup"><span data-stu-id="50c1d-139">Managing Data Blocks by Polling</span></span>](managing-data-blocks-by-polling.md)

 

 