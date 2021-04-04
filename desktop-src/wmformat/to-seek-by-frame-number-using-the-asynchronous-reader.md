---
title: Para buscar por número de marco mediante el lector asincrónico
description: Para buscar por número de marco mediante el lector asincrónico
ms.assetid: faab6344-3afc-47ff-9107-d2ce36c0a2b8
keywords:
- Advanced Systems Format (ASF), búsqueda por números de fotogramas
- ASF (formato de sistemas avanzados), búsqueda por números de fotogramas
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- lectores asincrónicos, búsqueda por números de fotogramas
- secuencias de vídeo, búsqueda por números de fotogramas
- secuencias de vídeo, lectores asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 169f5e1ac1e6034bc1db6f610e80af50dd3a0215
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077299"
---
# <a name="to-seek-by-frame-number-using-the-asynchronous-reader"></a><span data-ttu-id="10100-110">Para buscar por número de marco mediante el lector asincrónico</span><span class="sxs-lookup"><span data-stu-id="10100-110">To Seek By Frame Number Using the Asynchronous Reader</span></span>

<span data-ttu-id="10100-111">El objeto lector asincrónico se puede usar para buscar los números de fotogramas de las secuencias de vídeo en un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="10100-111">The asynchronous reader object can be used to seek to the frame numbers of video streams in an ASF file.</span></span> <span data-ttu-id="10100-112">Para usar búsquedas basadas en marcos, el archivo cargado en el lector debe estar indexado por marco.</span><span class="sxs-lookup"><span data-stu-id="10100-112">To use frame-based seeking, the file loaded in the reader must be indexed by frame.</span></span> <span data-ttu-id="10100-113">Cada flujo de vídeo individual se puede indexar.</span><span class="sxs-lookup"><span data-stu-id="10100-113">Each individual video stream can be indexed.</span></span> <span data-ttu-id="10100-114">Para determinar si un flujo se ha indizado mediante Frame, puede comprobar el \_ atributo g wszWMNumberOfFrames en el encabezado del archivo llamando a [**IWMHeaderInfo:: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span><span class="sxs-lookup"><span data-stu-id="10100-114">To determine whether a stream has been indexed by frame, you can check the g\_wszWMNumberOfFrames attribute in the header of the file by calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span>

<span data-ttu-id="10100-115">Para buscar datos en un archivo ASF por número de marco mediante el lector asincrónico, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="10100-115">To seek data in an ASF file by frame number using the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="10100-116">Obtenga un puntero a la interfaz [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) del objeto lector llamando a **IWMReader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="10100-116">Obtain a pointer to the [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="10100-117">Establezca el número de fotograma inicial y la duración mediante una llamada a [**IWMReaderAdvanced3:: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span><span class="sxs-lookup"><span data-stu-id="10100-117">Set the starting frame number and duration by calling [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span></span> <span data-ttu-id="10100-118">Debe especificar el número de secuencia de una secuencia de vídeo indexada por fotogramas.</span><span class="sxs-lookup"><span data-stu-id="10100-118">You must specify the stream number of a frame-indexed video stream.</span></span> <span data-ttu-id="10100-119">El lector sincronizará el resto de los resultados con el tiempo de presentación del marco especificado de la secuencia especificada y comenzará a entregar ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="10100-119">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
3.  <span data-ttu-id="10100-120">Controle los ejemplos como lo haría normalmente en su implementación del método **IWMReaderCallback::** .</span><span class="sxs-lookup"><span data-stu-id="10100-120">Handle the samples as you normally would in your implementation of the **IWMReaderCallback::OnSample** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10100-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="10100-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10100-122">**Leer archivos con el lector asincrónico**</span><span class="sxs-lookup"><span data-stu-id="10100-122">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="10100-123">**Leer metadatos en la reproducción**</span><span class="sxs-lookup"><span data-stu-id="10100-123">**Reading Metadata at Playback**</span></span>](reading-metadata-at-playback.md)
</dt> <dt>

[<span data-ttu-id="10100-124">**Trabajar con índices**</span><span class="sxs-lookup"><span data-stu-id="10100-124">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




