---
title: Para recuperar muestras comprimidas con el lector sincrónico
description: Para recuperar muestras comprimidas con el lector sincrónico
ms.assetid: 1f6da1aa-c26a-486a-bb44-cc4305c71979
keywords:
- Advanced Systems Format (ASF), recuperar muestras comprimidas
- ASF (formato de sistemas avanzados), recuperar ejemplos comprimidos
- Advanced Systems Format (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- Advanced Systems Format (ASF), ejemplos comprimidos
- ASF (formato de sistemas avanzados), ejemplos comprimidos
- lectores sincrónicos, recuperar ejemplos comprimidos
- lectores sincrónicos, ejemplos comprimidos
- ejemplos comprimidos, recuperar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f0051fc14a14500b2c6e69c5e32f7ec0c39a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149082"
---
# <a name="to-retrieve-compressed-samples-with-the-synchronous-reader"></a><span data-ttu-id="d4280-112">Para recuperar muestras comprimidas con el lector sincrónico</span><span class="sxs-lookup"><span data-stu-id="d4280-112">To Retrieve Compressed Samples with the Synchronous Reader</span></span>

<span data-ttu-id="d4280-113">Al igual que el lector asincrónico, el lector sincrónico también puede recuperar ejemplos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="d4280-113">Like the asynchronous reader, the synchronous reader can also retrieve compressed samples.</span></span> <span data-ttu-id="d4280-114">Los ejemplos comprimidos deben usarse al copiar transmisiones de un archivo a otro.</span><span class="sxs-lookup"><span data-stu-id="d4280-114">Compressed samples should be used when copying streams from one file to another.</span></span>

<span data-ttu-id="d4280-115">El SDK de Windows Media Format no proporciona ningún método para descodificar los datos una vez extraídos de un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="d4280-115">The Windows Media Format SDK does not provide any methods for decoding data after it has been extracted from an ASF file.</span></span> <span data-ttu-id="d4280-116">Si recibe ejemplos comprimidos y posteriormente desea descomprimirlos, tendrá que proporcionar su propio código para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="d4280-116">If you receive compressed samples and later want to decompress them, you will have to provide your own code to do so.</span></span> <span data-ttu-id="d4280-117">Una manera de solucionar esta limitación es escribir los ejemplos comprimidos en un nuevo archivo ASF y, a continuación, volver a leerlos en ejemplos normales y sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="d4280-117">One way to get around this limitation is to write the compressed samples to a new ASF file and then re-read them into normal, uncompressed samples.</span></span>

<span data-ttu-id="d4280-118">Para recibir muestras comprimidas con el lector sincrónico, llame a [**IWMSyncReader:: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) antes o durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="d4280-118">To receive compressed samples with the synchronous reader, call [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) before or during playback.</span></span> <span data-ttu-id="d4280-119">Pase True para *fCompressed*.</span><span class="sxs-lookup"><span data-stu-id="d4280-119">Pass true for *fCompressed*.</span></span>

> [!Note]  
> <span data-ttu-id="d4280-120">Los flujos de imagen no son válidos para la entrega de secuencias comprimidas.</span><span class="sxs-lookup"><span data-stu-id="d4280-120">Image streams are not valid for compressed stream delivery.</span></span> <span data-ttu-id="d4280-121">Si copia una secuencia de imágenes de un archivo a otro, no funcionará en el nuevo archivo.</span><span class="sxs-lookup"><span data-stu-id="d4280-121">If you copy an image stream from one file to another, it will not work in the new file.</span></span> <span data-ttu-id="d4280-122">Para copiar un flujo de imagen de archivo a archivo, recupere los ejemplos de flujo de imagen por número de salida e inclúyalo en el nuevo archivo como si se incluira una nueva secuencia de imágenes.</span><span class="sxs-lookup"><span data-stu-id="d4280-122">To copy an image stream from file to file, retrieve the image stream samples by output number and include them in the new file as if including a new image stream.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d4280-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d4280-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4280-124">**Leer archivos con el lector sincrónico**</span><span class="sxs-lookup"><span data-stu-id="d4280-124">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




