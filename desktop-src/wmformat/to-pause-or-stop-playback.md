---
title: Para pausar o detener la reproducción
description: Para pausar o detener la reproducción
ms.assetid: 8e43ea80-36c7-4530-8ed3-dfdb64a3a2e3
keywords:
- Advanced Systems Format (ASF), pausar la reproducción
- ASF (formato de sistemas avanzados), pausar la reproducción
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Advanced Systems Format (ASF), detener la reproducción
- ASF (formato de sistemas avanzados), detener la reproducción
- Advanced Systems Format (ASF), reproducción en pausa o detención
- ASF (formato de sistemas avanzados), reproducción en pausa o detención
- lectores asincrónicos, pausar la reproducción
- lectores asincrónicos, detener la reproducción
- lectores asincrónicos, reproducción en pausa o detención
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728ce4c58f9198f605764d0f19d0d5f55c7f6c6b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104532980"
---
# <a name="to-pause-or-stop-playback"></a><span data-ttu-id="aa7be-114">Para pausar o detener la reproducción</span><span class="sxs-lookup"><span data-stu-id="aa7be-114">To Pause or Stop Playback</span></span>

<span data-ttu-id="aa7be-115">Al llamar a [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) para empezar a reproducir un archivo, el lector asincrónico continuará el procesamiento en sus propios subprocesos independientes hasta que se alcance el final del archivo.</span><span class="sxs-lookup"><span data-stu-id="aa7be-115">When you call [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) to begin playing a file, the asynchronous reader will continue processing in its own separate threads until the end of the file is reached.</span></span> <span data-ttu-id="aa7be-116">Puede pausar o detener la entrega de muestras mediante los métodos [**IWMReader::P ause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) o [**IWMReader:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="aa7be-116">You can pause or stop the delivery of samples using the [**IWMReader::Pause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) or [**IWMReader::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) methods respectively.</span></span>

## <a name="pausing"></a><span data-ttu-id="aa7be-117">Pausando</span><span class="sxs-lookup"><span data-stu-id="aa7be-117">Pausing</span></span>

<span data-ttu-id="aa7be-118">Cuando se llama a **IWMReader::P ause** para pausar la reproducción de un archivo, el lector realiza un seguimiento de la posición actual en el archivo.</span><span class="sxs-lookup"><span data-stu-id="aa7be-118">When you call **IWMReader::Pause** to pause playback of a file, the reader keeps track of the current position in the file.</span></span> <span data-ttu-id="aa7be-119">Para reanudar la reproducción después de la pausa, llame a [**IWMReader:: resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume).</span><span class="sxs-lookup"><span data-stu-id="aa7be-119">To resume playing after pausing, call [**IWMReader::Resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume).</span></span> <span data-ttu-id="aa7be-120">La reproducción se reanudará desde el punto en el que se ha pausado.</span><span class="sxs-lookup"><span data-stu-id="aa7be-120">Playback will resume from the point at which it paused.</span></span>

## <a name="stopping"></a><span data-ttu-id="aa7be-121">Deteniéndose</span><span class="sxs-lookup"><span data-stu-id="aa7be-121">Stopping</span></span>

<span data-ttu-id="aa7be-122">Cuando se llama a **IWMReader:: Stop** para detener la reproducción de un archivo, el lector no realiza un seguimiento de la información sobre el progreso de la reproducción.</span><span class="sxs-lookup"><span data-stu-id="aa7be-122">When you call **IWMReader::Stop** to halt playback of a file, the reader does not keep track of any information about the progress of playback.</span></span> <span data-ttu-id="aa7be-123">Para usar **detener** y volver al punto de detención, debe guardar el tiempo de presentación del último ejemplo entregado y usarlo en la llamada a **IWMReader:: Start**.</span><span class="sxs-lookup"><span data-stu-id="aa7be-123">To use **Stop** and later return to the stopping point you must save the presentation time of the last sample delivered and use it in your call to **IWMReader::Start**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa7be-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aa7be-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa7be-125">**Interfaz IWMReader**</span><span class="sxs-lookup"><span data-stu-id="aa7be-125">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="aa7be-126">**Leer archivos con el lector asincrónico**</span><span class="sxs-lookup"><span data-stu-id="aa7be-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




