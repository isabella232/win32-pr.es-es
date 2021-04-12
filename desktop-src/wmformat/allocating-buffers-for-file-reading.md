---
title: Asignar búferes para la lectura de archivos
description: Asignar búferes para la lectura de archivos
ms.assetid: da66ef5b-ec92-445c-90ba-5ee89e0def36
keywords:
- SDK de Windows Media Format, leer archivos ASF
- Advanced Systems Format (ASF), leer archivos
- ASF (formato de sistemas avanzados), lectura de archivos
- Windows Media Format SDK, asignar búferes
- Advanced Systems Format (ASF), asignar búferes
- ASF (formato de sistemas avanzados), asignar búferes
- Advanced Systems Format (ASF), asignación de búfer
- ASF (formato de sistemas avanzados), asignación de búfer
- asignación de búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecdf9ba0a333bbe25c94ec087911237b68f38f74
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420225"
---
# <a name="allocating-buffers-for-file-reading"></a><span data-ttu-id="202f9-112">Asignar búferes para la lectura de archivos</span><span class="sxs-lookup"><span data-stu-id="202f9-112">Allocating Buffers for File Reading</span></span>

<span data-ttu-id="202f9-113">En el escenario de lectura de archivos más básico, los búferes que se usan para proporcionar ejemplos se asignan mediante el objeto de lectura (el objeto lector o el objeto lector sincrónico).</span><span class="sxs-lookup"><span data-stu-id="202f9-113">In the most basic file-reading scenario, the buffers used to deliver samples are allocated by the reading object (the reader object or the synchronous reader object).</span></span> <span data-ttu-id="202f9-114">Sin embargo, puede asignar búferes personalmente.</span><span class="sxs-lookup"><span data-stu-id="202f9-114">You can, however, allocate buffers yourself.</span></span> <span data-ttu-id="202f9-115">Para obtener más información sobre las ventajas de la asignación de sus propios búferes, consulte [compatibilidad con el ejemplo](user-allocated-sample-support.md)de asignación de usuarios.</span><span class="sxs-lookup"><span data-stu-id="202f9-115">For more information about the benefits of allocating your own buffers, see [User Allocated Sample Support](user-allocated-sample-support.md).</span></span>

<span data-ttu-id="202f9-116">Para usar sus propios búferes para la lectura de archivos, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="202f9-116">To use your own buffers for file reading, perform the following steps.</span></span>

1.  <span data-ttu-id="202f9-117">Implemente una devolución de llamada o devoluciones de llamada para que el lector llame cuando necesite un búfer.</span><span class="sxs-lookup"><span data-stu-id="202f9-117">Implement a callback or callbacks for the reader to call when it needs a buffer.</span></span> <span data-ttu-id="202f9-118">Si está leyendo ejemplos de salida, use [**IWMReaderAllocatorEx:: AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex).</span><span class="sxs-lookup"><span data-stu-id="202f9-118">If you are reading output samples, use [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex).</span></span> <span data-ttu-id="202f9-119">Si está leyendo ejemplos de secuencias, use [**IWMReaderAllocatorEx:: AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span><span class="sxs-lookup"><span data-stu-id="202f9-119">If you are reading stream samples, use [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span></span> <span data-ttu-id="202f9-120">Incluya la lógica para administrar los búferes que mejor se adapte a su aplicación.</span><span class="sxs-lookup"><span data-stu-id="202f9-120">Include whatever logic for managing buffers that suits your application.</span></span>
2.  <span data-ttu-id="202f9-121">Asigne un grupo de búferes que usará para la lectura de archivos.</span><span class="sxs-lookup"><span data-stu-id="202f9-121">Allocate a pool of buffers that you will use for file reading.</span></span>
    -   <span data-ttu-id="202f9-122">Busque el tamaño necesario para los búferes mediante una llamada a [**IWMReaderAdvanced:: GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) o [**IWMReaderAdvanced:: GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) para cada salida o secuencia para la que se usa el búfer.</span><span class="sxs-lookup"><span data-stu-id="202f9-122">Find the size required for your buffers by calling [**IWMReaderAdvanced::GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) or [**IWMReaderAdvanced::GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) for each output and/or stream for which the buffer is used.</span></span> <span data-ttu-id="202f9-123">Si usa el lector sincrónico, use [**IWMSyncReader:: GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) o [**IWMSyncReader:: GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="202f9-123">If using the synchronous reader, use [**IWMSyncReader::GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) or [**IWMSyncReader::GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) instead.</span></span>
    -   <span data-ttu-id="202f9-124">Cree cada búfer para el grupo.</span><span class="sxs-lookup"><span data-stu-id="202f9-124">Create each buffer for the pool.</span></span>
3.  <span data-ttu-id="202f9-125">Configure el lector o el lector sincrónico para lectura.</span><span class="sxs-lookup"><span data-stu-id="202f9-125">Set up the reader or synchronous reader for reading.</span></span> <span data-ttu-id="202f9-126">Para obtener más información, vea [leer archivos con el lector asincrónico](reading-files-with-the-asynchronous-reader.md) o [leer archivos con el lector sincrónico](reading-files-with-the-synchronous-reader.md).</span><span class="sxs-lookup"><span data-stu-id="202f9-126">For more information see [Reading Files with the Asynchronous Reader](reading-files-with-the-asynchronous-reader.md) or [Reading Files with the Synchronous Reader](reading-files-with-the-synchronous-reader.md).</span></span>
4.  <span data-ttu-id="202f9-127">Antes de empezar a escribir, llame a [**IWMReaderAdvanced:: SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) o [**IWMReaderAdvanced:: SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) para cada salida y flujo para los que va a asignar búferes mediante el objeto de lector.</span><span class="sxs-lookup"><span data-stu-id="202f9-127">Before beginning writing, call [**IWMReaderAdvanced::SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) or [**IWMReaderAdvanced::SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) for each output and stream for which you are allocating buffers using the reader object.</span></span> <span data-ttu-id="202f9-128">En el caso del lector sincrónico, llame a [**IWMSyncReader2:: SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) o [**IWMSyncReader2:: SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="202f9-128">For the synchronous reader, call [**IWMSyncReader2::SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) or [**IWMSyncReader2::SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) instead.</span></span>
5.  <span data-ttu-id="202f9-129">Empiece a leer el archivo.</span><span class="sxs-lookup"><span data-stu-id="202f9-129">Begin reading the file.</span></span>

<span data-ttu-id="202f9-130">El objeto de lectura realizará las llamadas a la devolución de llamada de asignador adecuada y obtendrá ejemplos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="202f9-130">The reading object will make calls to the appropriate allocator callback and get samples from your application.</span></span> <span data-ttu-id="202f9-131">La lógica de administración de búfer debe incluir una manera de indicar que un búfer puede volver a usarse.</span><span class="sxs-lookup"><span data-stu-id="202f9-131">Your buffer management logic must include a way to signal that a buffer is free to be used again.</span></span> <span data-ttu-id="202f9-132">Normalmente, un búfer se vuelve a colocar en el grupo cuando se representa su contenido.</span><span class="sxs-lookup"><span data-stu-id="202f9-132">Typically, a buffer is put back into the pool when its contents are rendered.</span></span> <span data-ttu-id="202f9-133">Dependiendo de la aplicación, es posible que necesite unos pocos búferes en el grupo o muchos.</span><span class="sxs-lookup"><span data-stu-id="202f9-133">Depending upon your application, you may need just a few buffers in the pool or many.</span></span>

## <a name="related-topics"></a><span data-ttu-id="202f9-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="202f9-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="202f9-135">**Leer archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="202f9-135">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




