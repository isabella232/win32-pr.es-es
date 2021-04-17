---
title: Para buscar marcadores
description: Para buscar marcadores
ms.assetid: 2d5efebf-dcbd-4fb8-933e-cc6d3a99adf8
keywords:
- Advanced Systems Format (ASF), buscar marcadores
- ASF (formato de sistemas avanzados), buscar marcadores
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Advanced Systems Format (ASF), marcadores
- ASF (formato de sistemas avanzados), marcadores
- lectores asincrónicos, buscar marcadores
- lectores asincrónicos, marcadores
- marcadores, buscar
- marcadores, lectores asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16cb4fef99a5c735a12f03f8d2e962d6caf9c2a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "105704923"
---
# <a name="to-seek-to-markers"></a><span data-ttu-id="bae9b-113">Para buscar marcadores</span><span class="sxs-lookup"><span data-stu-id="bae9b-113">To Seek to Markers</span></span>

<span data-ttu-id="bae9b-114">Un marcador es una ubicación con nombre en un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="bae9b-114">A marker is a named location in an ASF file.</span></span> <span data-ttu-id="bae9b-115">Solo se puede iniciar la reproducción desde la ubicación de un marcador mediante el lector asincrónico.</span><span class="sxs-lookup"><span data-stu-id="bae9b-115">You can only start playback from the location of a marker by using the asynchronous reader.</span></span> <span data-ttu-id="bae9b-116">Puede comenzar la reproducción en un marcador siguiendo estos pasos.</span><span class="sxs-lookup"><span data-stu-id="bae9b-116">You can begin playback at a marker by following these steps.</span></span>

1.  <span data-ttu-id="bae9b-117">Llame a **IWMReader:: QueryInterface** para obtener un puntero a la interfaz [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) .</span><span class="sxs-lookup"><span data-stu-id="bae9b-117">Call **IWMReader::QueryInterface** to obtain a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface.</span></span>
2.  <span data-ttu-id="bae9b-118">Recupere el número total de marcadores del archivo mediante una llamada a [**IWMHeaderInfo:: GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount).</span><span class="sxs-lookup"><span data-stu-id="bae9b-118">Retrieve the total number of markers in the file by calling [**IWMHeaderInfo::GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount).</span></span>
3.  <span data-ttu-id="bae9b-119">Recorra los marcadores con el recuento de marcadores recuperado en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="bae9b-119">Loop through the markers, using the marker count retrieved in step 2.</span></span> <span data-ttu-id="bae9b-120">Recupere el nombre y la hora de cada marcador mediante una llamada a [**IWMHeaderInfo:: GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) para cada uno.</span><span class="sxs-lookup"><span data-stu-id="bae9b-120">Retrieve the name and time of each marker by calling [**IWMHeaderInfo::GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) for each.</span></span> <span data-ttu-id="bae9b-121">Guarde el índice del marcador deseado.</span><span class="sxs-lookup"><span data-stu-id="bae9b-121">Save the index of the desired marker.</span></span>
4.  <span data-ttu-id="bae9b-122">Llame a **IWMReader:: QueryInterface** para obtener un puntero a la interfaz [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) .</span><span class="sxs-lookup"><span data-stu-id="bae9b-122">Call **IWMReader::QueryInterface** to obtain a pointer to the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface.</span></span>
5.  <span data-ttu-id="bae9b-123">Especifique el marcador en el que se va a iniciar la reproducción llamando a [**IWMReaderAdvanced2:: StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker).</span><span class="sxs-lookup"><span data-stu-id="bae9b-123">Specify the marker at which to start playback by calling [**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker).</span></span> <span data-ttu-id="bae9b-124">Debe pasar el índice del marcador deseado, que guardó en el paso 3.</span><span class="sxs-lookup"><span data-stu-id="bae9b-124">You must pass the index of the desired marker, which you saved in step 3.</span></span>
6.  <span data-ttu-id="bae9b-125">Controle los ejemplos como lo haría normalmente en su implementación del método [**IWMReaderCallback::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) .</span><span class="sxs-lookup"><span data-stu-id="bae9b-125">Handle the samples as you normally would in your implementation of the [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bae9b-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bae9b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bae9b-127">**Marcadores**</span><span class="sxs-lookup"><span data-stu-id="bae9b-127">**Markers**</span></span>](markers.md)
</dt> <dt>

[<span data-ttu-id="bae9b-128">**Leer archivos con el lector asincrónico**</span><span class="sxs-lookup"><span data-stu-id="bae9b-128">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="bae9b-129">**Trabajar con índices**</span><span class="sxs-lookup"><span data-stu-id="bae9b-129">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




