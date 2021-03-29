---
description: Ejemplo de MPEG1Source
ms.assetid: c9f131ff-0b79-487c-9a46-a9b1350553a1
title: Ejemplo de MPEG1Source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c71bd541a7bd01621ca7359eb9e229a08e91a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652515"
---
# <a name="mpeg1source-sample"></a><span data-ttu-id="d2023-103">Ejemplo de MPEG1Source</span><span class="sxs-lookup"><span data-stu-id="d2023-103">MPEG1Source Sample</span></span>

<span data-ttu-id="d2023-104">Muestra cómo escribir un origen multimedia personalizado en Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d2023-104">Shows how to write a custom media source in Microsoft Media Foundation.</span></span> <span data-ttu-id="d2023-105">En el ejemplo se implementa un origen multimedia que analiza los flujos de capas de sistemas MPEG-1 y genera ejemplos que contienen cargas MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="d2023-105">The sample implements a media source that parses MPEG-1 systems-layer streams and generates samples that contain MPEG-1 payloads.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="d2023-106">API mostradas</span><span class="sxs-lookup"><span data-stu-id="d2023-106">APIs Demonstrated</span></span>

<span data-ttu-id="d2023-107">Este ejemplo muestra las siguientes interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="d2023-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="d2023-108">**IMFByteStreamHandler**</span><span class="sxs-lookup"><span data-stu-id="d2023-108">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [<span data-ttu-id="d2023-109">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="d2023-109">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="d2023-110">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="d2023-110">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

<span data-ttu-id="d2023-111">Antes de examinar este ejemplo, es posible que desee revisar el [ejemplo WavSource](wavsource-sample.md), que proporciona una implementación más sencilla de un origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="d2023-111">Before examining this sample, you might want to review the [WavSource Sample](wavsource-sample.md), which provides a simpler implementation of a media source.</span></span> <span data-ttu-id="d2023-112">En el ejemplo MPEG1Source se agregan algunas características que se encuentran en la mayoría de las implementaciones reales de un origen multimedia:</span><span class="sxs-lookup"><span data-stu-id="d2023-112">The MPEG1Source sample adds some features that would be found in most real-world implementations of a media source:</span></span>

-   <span data-ttu-id="d2023-113">Varios flujos</span><span class="sxs-lookup"><span data-stu-id="d2023-113">Multiple streams</span></span>
-   <span data-ttu-id="d2023-114">Métodos asincrónicos</span><span class="sxs-lookup"><span data-stu-id="d2023-114">Asynchronous methods</span></span>
-   <span data-ttu-id="d2023-115">E/s asincrónica</span><span class="sxs-lookup"><span data-stu-id="d2023-115">Asynchronous I/O</span></span>

<span data-ttu-id="d2023-116">En el Windows SDK para Windows Server 2008, este ejemplo también incluye un descodificador de vídeo MPEG-1 de ejemplo que muestra el código de tiempo para cada fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d2023-116">In the Windows SDK for Windows Server 2008, this sample also includes a sample MPEG-1 video decoder that displays the time code for each video frame.</span></span> <span data-ttu-id="d2023-117">(En realidad, no descodifica MPEG-1 fragmentada).</span><span class="sxs-lookup"><span data-stu-id="d2023-117">(It does not actually decode the MPEG-1 bitstream.)</span></span>

<span data-ttu-id="d2023-118">A partir de la Windows SDK para Windows 7, el descodificador se ha pasado a un ejemplo independiente.</span><span class="sxs-lookup"><span data-stu-id="d2023-118">Starting in the Windows SDK for Windows 7, the decoder has been moved to a separate sample.</span></span> <span data-ttu-id="d2023-119">Consulte [ejemplo de descodificador](decoder-sample.md).</span><span class="sxs-lookup"><span data-stu-id="d2023-119">See [Decoder Sample](decoder-sample.md).</span></span>

## <a name="usage"></a><span data-ttu-id="d2023-120">Uso</span><span class="sxs-lookup"><span data-stu-id="d2023-120">Usage</span></span>

<span data-ttu-id="d2023-121">En el ejemplo MPEG1Source se crea un archivo DLL que es un servidor COM para el origen de medios, el controlador de flujo de bytes del origen multimedia y la MFT del descodificador.</span><span class="sxs-lookup"><span data-stu-id="d2023-121">The MPEG1Source sample builds a DLL that is a COM server for the media source, media source's byte-stream handler, and the decoder MFT.</span></span> <span data-ttu-id="d2023-122">Antes de usar el origen de medios, debe registrar el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="d2023-122">Before using the media source, you must register the DLL.</span></span>

<span data-ttu-id="d2023-123">Para usar el origen de medios, puede ejecutar el [ejemplo BasicPlayback](/previous-versions//bb970475(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2023-123">To use the media source, you can run the [BasicPlayback Sample](/previous-versions//bb970475(v=vs.85)).</span></span> <span data-ttu-id="d2023-124">La resolución de origen cargará automáticamente el origen multimedia si selecciona un archivo MPEG-1 para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="d2023-124">The source resolver will automatically load the media source if you select an MPEG-1 file for playback.</span></span> <span data-ttu-id="d2023-125">(Si se produce un error, asegúrese de que ha registrado correctamente el archivo DLL de MPEG1Source).</span><span class="sxs-lookup"><span data-stu-id="d2023-125">(If an error occurs, make sure that you successfully registered the MPEG1Source DLL.)</span></span>

<span data-ttu-id="d2023-126">También puede usar la herramienta TopoEdit para crear una topología de reproducción que contenga el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="d2023-126">You can also use the TopoEdit tool to build a playback topology that contains the media source.</span></span> <span data-ttu-id="d2023-127">Para obtener más información sobre TopoEdit, consulte [TopoEdit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="d2023-127">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2023-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2023-128">Requirements</span></span>



| <span data-ttu-id="d2023-129">Producto</span><span class="sxs-lookup"><span data-stu-id="d2023-129">Product</span></span>                                                        | <span data-ttu-id="d2023-130">Versión</span><span class="sxs-lookup"><span data-stu-id="d2023-130">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="d2023-131">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="d2023-131">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="d2023-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d2023-132">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="d2023-133">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2023-133">Downloading the Sample</span></span>

<span data-ttu-id="d2023-134">Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source).</span><span class="sxs-lookup"><span data-stu-id="d2023-134">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2023-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d2023-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2023-136">Muestras de SDK de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d2023-136">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="d2023-137">Orígenes multimedia</span><span class="sxs-lookup"><span data-stu-id="d2023-137">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="d2023-138">Controladores de esquema y controladores de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="d2023-138">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="d2023-139">Tutorial: escribir un origen de medios personalizado</span><span class="sxs-lookup"><span data-stu-id="d2023-139">Tutorial: Writing a Custom Media Source</span></span>](tutorial--writing-a-custom-media-source.md)
</dt> <dt>

[<span data-ttu-id="d2023-140">Ejemplo de WavSource</span><span class="sxs-lookup"><span data-stu-id="d2023-140">WavSource Sample</span></span>](wavsource-sample.md)
</dt> </dl>

 

 
