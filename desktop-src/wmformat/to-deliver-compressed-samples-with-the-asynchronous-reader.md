---
title: Para proporcionar ejemplos comprimidos con el lector asincrónico
description: Para proporcionar ejemplos comprimidos con el lector asincrónico
ms.assetid: 488baa3c-8863-4afc-89b2-fe55823e5db9
keywords:
- Advanced Systems Format (ASF), entrega de muestras comprimidas
- ASF (formato de sistemas avanzados), entrega de muestras comprimidas
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Advanced Systems Format (ASF), ejemplos comprimidos
- ASF (formato de sistemas avanzados), ejemplos comprimidos
- lectores asincrónicos, entrega de muestras comprimidas
- lectores asincrónicos, ejemplos comprimidos
- ejemplos comprimidos, entrega
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ce835075f5bd760014a3b1b776ba3627adb076
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788793"
---
# <a name="to-deliver-compressed-samples-with-the-asynchronous-reader"></a><span data-ttu-id="50263-112">Para proporcionar ejemplos comprimidos con el lector asincrónico</span><span class="sxs-lookup"><span data-stu-id="50263-112">To Deliver Compressed Samples with the Asynchronous Reader</span></span>

<span data-ttu-id="50263-113">El lector asincrónico puede proporcionar ejemplos comprimidos de secuencias en archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="50263-113">The asynchronous reader can deliver compressed samples from streams in ASF files.</span></span> <span data-ttu-id="50263-114">Normalmente, las aplicaciones proporcionan ejemplos comprimidos al copiar una secuencia de un archivo a otro.</span><span class="sxs-lookup"><span data-stu-id="50263-114">Applications usually deliver compressed samples when copying a stream from one file to another.</span></span> <span data-ttu-id="50263-115">No es aconsejable volver a comprimir los datos que se han reconstruido a partir de un flujo comprimido, ya que los datos se pierden en el proceso de codificación.</span><span class="sxs-lookup"><span data-stu-id="50263-115">It is not advisable to recompress data that has been reconstructed from a compressed stream, because data is lost in the encoding process.</span></span> <span data-ttu-id="50263-116">Los medios digitales que se han comprimido más de una vez tendrán una disminución apreciable de la calidad.</span><span class="sxs-lookup"><span data-stu-id="50263-116">Digital media that has been compressed more than once will have a noticeable decrease in quality.</span></span>

<span data-ttu-id="50263-117">El SDK de Windows Media Format no proporciona ningún método para descodificar los datos una vez extraídos de un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="50263-117">The Windows Media Format SDK does not provide any methods for decoding data after it has been extracted from an ASF file.</span></span> <span data-ttu-id="50263-118">Si recibe ejemplos comprimidos y posteriormente desea descomprimirlos, tendrá que proporcionar su propio código para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="50263-118">If you receive compressed samples and later want to decompress them, you will have to provide your own code to do so.</span></span> <span data-ttu-id="50263-119">Una manera de solucionar esta limitación es escribir los ejemplos comprimidos en un nuevo archivo ASF y, a continuación, volver a leerlos en ejemplos normales y sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="50263-119">One way to get around this limitation is to write the compressed samples to a new ASF file and then re-read them into normal, uncompressed samples.</span></span>

<span data-ttu-id="50263-120">Para recibir ejemplos comprimidos con el lector asincrónico, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="50263-120">To receive compressed samples with the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="50263-121">Implemente la devolución de llamada [**IWMReaderCallbackAdvanced:: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) .</span><span class="sxs-lookup"><span data-stu-id="50263-121">Implement the [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback.</span></span> <span data-ttu-id="50263-122">Esta devolución de llamada es básicamente idéntica en función a [**IWMReaderCallback::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) en el ejemplo, salvo que proporciona muestras por número de secuencia y los ejemplos siguen estando comprimidos.</span><span class="sxs-lookup"><span data-stu-id="50263-122">This callback is basically identical in function to [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) except that it delivers samples by stream number and the samples are still compressed.</span></span>
2.  <span data-ttu-id="50263-123">Antes de iniciar la reproducción, obtenga un puntero a la interfaz [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) del objeto lector llamando a **IWMReader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="50263-123">Before starting playback, obtain a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
3.  <span data-ttu-id="50263-124">Configure el lector para proporcionar ejemplos comprimidos para el flujo deseado llamando a [**IWMReaderAdvanced:: SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples).</span><span class="sxs-lookup"><span data-stu-id="50263-124">Configure the reader to deliver compressed samples for the desired stream by calling [**IWMReaderAdvanced::SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples).</span></span>
4.  <span data-ttu-id="50263-125">Repita el paso 3 para cada flujo para el que desee la entrega de ejemplo comprimida.</span><span class="sxs-lookup"><span data-stu-id="50263-125">Repeat step 3 for each stream for which compressed sample delivery is desired.</span></span>

> [!Note]  
> <span data-ttu-id="50263-126">Los flujos de imagen no son válidos para la entrega de secuencias comprimidas.</span><span class="sxs-lookup"><span data-stu-id="50263-126">Image streams are not valid for compressed stream delivery.</span></span> <span data-ttu-id="50263-127">Si copia una secuencia de imágenes de un archivo a otro, no funcionará en el nuevo archivo.</span><span class="sxs-lookup"><span data-stu-id="50263-127">If you copy an image stream from one file to another, it will not work in the new file.</span></span> <span data-ttu-id="50263-128">Para copiar un flujo de imagen de archivo a archivo, recupere los ejemplos de flujo de imagen por número de salida e inclúyalo en el nuevo archivo como si se incluira una nueva secuencia de imágenes.</span><span class="sxs-lookup"><span data-stu-id="50263-128">To copy an image stream from file to file, retrieve the image stream samples by output number and include them in the new file as if including a new image stream.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="50263-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50263-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50263-130">**Interfaz IWMReaderCallbackAdvanced**</span><span class="sxs-lookup"><span data-stu-id="50263-130">**IWMReaderCallbackAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[<span data-ttu-id="50263-131">**Leer archivos con el lector asincrónico**</span><span class="sxs-lookup"><span data-stu-id="50263-131">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




