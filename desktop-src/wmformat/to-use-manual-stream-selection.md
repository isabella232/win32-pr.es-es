---
title: Para usar la selección de flujo manual
description: Para usar la selección de flujo manual
ms.assetid: 49ec283f-670a-4a0e-9477-c60a80919a1e
keywords:
- Advanced Systems Format (ASF), selección de secuencias manual
- ASF (formato de sistemas avanzados), selección de flujo manual
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Advanced Systems Format (ASF), selección de secuencias
- ASF (formato de sistemas avanzados), selección de secuencias
- Advanced Systems Format (ASF), exclusión mutua
- ASF (formato de sistemas avanzados), exclusión mutua
- lectores asincrónicos, selección de secuencias manual
- lectores asincrónicos, selección de secuencias
- flujos, selección manual
- exclusión mutua, selección de secuencia manual
- flujos, lectores asincrónicos
- exclusión mutua, lectores asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87c493bc8f41bc2a03ba15832ed402939adbeff
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695554"
---
# <a name="to-use-manual-stream-selection"></a><span data-ttu-id="a9a28-117">Para usar la selección de flujo manual</span><span class="sxs-lookup"><span data-stu-id="a9a28-117">To Use Manual Stream Selection</span></span>

<span data-ttu-id="a9a28-118">Al entregar ejemplos sin comprimir con el objeto lector, solo puede entregarlos por número de salida.</span><span class="sxs-lookup"><span data-stu-id="a9a28-118">When delivering uncompressed samples with the reader object, you can deliver them only by output number.</span></span> <span data-ttu-id="a9a28-119">En el caso de las secuencias mutuamente excluyentes, esto significa que solo se pueden recibir muestras de un flujo en la exclusión mutua a la vez.</span><span class="sxs-lookup"><span data-stu-id="a9a28-119">In the case of mutually exclusive streams, this means that you can receive samples only from one stream in the mutual exclusion at a time.</span></span> <span data-ttu-id="a9a28-120">El proceso de elección de la secuencia mutuamente excluyente que se va a proporcionar se denomina selección de flujo.</span><span class="sxs-lookup"><span data-stu-id="a9a28-120">The process of choosing which mutually exclusive stream to deliver is called stream selection.</span></span>

<span data-ttu-id="a9a28-121">Para la exclusión mutua de velocidad de bits, el lector realiza las selecciones de transmisión automáticamente en función de las condiciones del equipo host en la reproducción.</span><span class="sxs-lookup"><span data-stu-id="a9a28-121">For bit-rate mutual exclusion, the reader makes stream selections automatically based on the conditions on the host machine at playback.</span></span> <span data-ttu-id="a9a28-122">Para otros tipos de exclusión mutua, el lector entregará muestras de la secuencia predeterminada a menos que seleccione manualmente otro flujo.</span><span class="sxs-lookup"><span data-stu-id="a9a28-122">For other types of mutual exclusion, the reader will deliver samples from the default stream unless you manually select a different stream yourself.</span></span> <span data-ttu-id="a9a28-123">También puede haber instancias si desea seleccionar una secuencia manualmente desde una exclusión mutua de velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="a9a28-123">There may also be instances when you want to select a stream manually from a bit-rate mutual exclusion.</span></span>

<span data-ttu-id="a9a28-124">La selección de secuencias manual está activada o desactivada para todo el archivo.</span><span class="sxs-lookup"><span data-stu-id="a9a28-124">Manual stream selection is either on or off for the entire file.</span></span> <span data-ttu-id="a9a28-125">Si un archivo contiene una exclusión mutua de velocidad de bits y algún otro tipo de exclusión mutua, debe seleccionar manualmente las secuencias basadas en la velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="a9a28-125">If a file contains bit-rate mutual exclusion and some other mutual exclusion type, you must select the bit rate based streams manually.</span></span>

<span data-ttu-id="a9a28-126">Para seleccionar manualmente una secuencia mutuamente excluyente, debe realizar los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="a9a28-126">To select a mutually exclusive stream manually, you must perform the following steps.</span></span>

1.  <span data-ttu-id="a9a28-127">Recupere un puntero a la interfaz [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) del objeto lector llamando a **IWMReader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="a9a28-127">Retrieve a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="a9a28-128">Habilite la selección de flujo manual llamando a [**IWMReaderAdvanced:: SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection).</span><span class="sxs-lookup"><span data-stu-id="a9a28-128">Enable manual stream selection by calling [**IWMReaderAdvanced::SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection).</span></span>
3.  <span data-ttu-id="a9a28-129">Para averiguar si una secuencia determinada está seleccionada, llame a [**IWMReaderAdvanced:: GetStreamSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected).</span><span class="sxs-lookup"><span data-stu-id="a9a28-129">To find out if a particular stream is selected, call [**IWMReaderAdvanced::GetStreamSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected).</span></span> <span data-ttu-id="a9a28-130">Debe pasar un puntero a una variable del tipo de enumeración de la [**\_ \_ selección de flujo WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) .</span><span class="sxs-lookup"><span data-stu-id="a9a28-130">You must pass a pointer to a variable of the [**WMT\_STREAM\_SELECTION**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) enumeration type.</span></span> <span data-ttu-id="a9a28-131">Cuando se devuelve la llamada, el valor de la variable describe el tipo de selección actual de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="a9a28-131">When the call returns, the value in the variable will describe the current selection type of the stream.</span></span>
4.  <span data-ttu-id="a9a28-132">Para seleccionar un flujo, llame a [**IWMReaderAdvanced:: SetStreamsSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected).</span><span class="sxs-lookup"><span data-stu-id="a9a28-132">To select a stream, call [**IWMReaderAdvanced::SetStreamsSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected).</span></span> <span data-ttu-id="a9a28-133">Este método permite especificar varias secuencias al mismo tiempo para la conmutación de flujos sincronizada.</span><span class="sxs-lookup"><span data-stu-id="a9a28-133">This method enables you to specify multiple streams at the same time for synchronized stream switching.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9a28-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a9a28-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9a28-135">**Leer archivos con el lector asincrónico**</span><span class="sxs-lookup"><span data-stu-id="a9a28-135">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




