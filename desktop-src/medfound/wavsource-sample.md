---
description: Ejemplo de WavSource
ms.assetid: 905fbba5-0a04-4048-80bd-f8707c4879da
title: Ejemplo de WavSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050edb9df75032384f93c6e1f37c52e89f14a748
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908627"
---
# <a name="wavsource-sample"></a><span data-ttu-id="acfd4-103">Ejemplo de WavSource</span><span class="sxs-lookup"><span data-stu-id="acfd4-103">WavSource Sample</span></span>

<span data-ttu-id="acfd4-104">Muestra cómo crear un origen de medios personalizado en Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="acfd4-104">Shows how to create a custom media source in Microsoft Media Foundation.</span></span> <span data-ttu-id="acfd4-105">El ejemplo implementa un origen de medios que analiza los archivos de audio. wav.</span><span class="sxs-lookup"><span data-stu-id="acfd4-105">The sample implements a media source that parses .wav audio files.</span></span>

<span data-ttu-id="acfd4-106">Este ejemplo es un ejemplo relativamente sencillo de un origen multimedia:</span><span class="sxs-lookup"><span data-stu-id="acfd4-106">This sample is a relatively simple example of a media source:</span></span>

-   <span data-ttu-id="acfd4-107">Solo hay una secuencia, por lo que no hay ningún código para implementar la selección de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="acfd4-107">There is only one stream, so there is no code to implement stream selection.</span></span>
-   <span data-ttu-id="acfd4-108">El origen multimedia no implementa el control de velocidad (es decir, reproducción rápida o inversa).</span><span class="sxs-lookup"><span data-stu-id="acfd4-108">The media source does not implement rate control (that is, fast forward or reverse playback).</span></span>
-   <span data-ttu-id="acfd4-109">Todos los métodos de origen y de secuencia se implementan como métodos sincrónicos.</span><span class="sxs-lookup"><span data-stu-id="acfd4-109">All source and stream methods are implemented as synchronous methods.</span></span>
-   <span data-ttu-id="acfd4-110">Dado que la parte de datos de un archivo. wav es un único bloque de audio PCM sin comprimir, el origen multimedia no necesita leer los encabezados de paquete o analizar la secuencia durante la reproducción, aparte de leer el encabezado [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) inicial.</span><span class="sxs-lookup"><span data-stu-id="acfd4-110">Because the data portion of a .wav file is a single block of uncompressed PCM audio, the media source does not need to read packet headers or otherwise parse the stream during playback, other than reading the initial [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) header.</span></span>

<span data-ttu-id="acfd4-111">Para obtener un ejemplo más avanzado de un origen multimedia, vea el [ejemplo MPEG1Source](mpeg1source-sample.md).</span><span class="sxs-lookup"><span data-stu-id="acfd4-111">For a more advanced example of a media source, see the [MPEG1Source Sample](mpeg1source-sample.md).</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="acfd4-112">API mostradas</span><span class="sxs-lookup"><span data-stu-id="acfd4-112">APIs Demonstrated</span></span>

<span data-ttu-id="acfd4-113">Este ejemplo muestra las siguientes interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="acfd4-113">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="acfd4-114">**IMFByteStreamHandler**</span><span class="sxs-lookup"><span data-stu-id="acfd4-114">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [<span data-ttu-id="acfd4-115">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="acfd4-115">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="acfd4-116">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="acfd4-116">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

## <a name="usage"></a><span data-ttu-id="acfd4-117">Uso</span><span class="sxs-lookup"><span data-stu-id="acfd4-117">Usage</span></span>

<span data-ttu-id="acfd4-118">En el ejemplo WavSource se crea un archivo DLL que es un servidor COM para el controlador de flujo de bytes del origen multimedia y el origen del medio.</span><span class="sxs-lookup"><span data-stu-id="acfd4-118">The WavSource sample builds a DLL that is a COM server for both the media source and media source's byte-stream handler.</span></span> <span data-ttu-id="acfd4-119">Antes de usar el origen de medios, debe registrar el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="acfd4-119">Before using the media source, you must register the DLL.</span></span>

<span data-ttu-id="acfd4-120">Para usar el origen de medios, puede ejecutar [BasicPlayback](/previous-versions//bb970475(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="acfd4-120">To use the media source, you can run the [BasicPlayback](/previous-versions//bb970475(v=vs.85)).</span></span> <span data-ttu-id="acfd4-121">La resolución de origen cargará automáticamente el origen multimedia si selecciona un archivo. wav para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="acfd4-121">The source resolver will automatically load the media source if you select a .wav file for playback.</span></span> <span data-ttu-id="acfd4-122">(Si se produce un error, asegúrese de que ha registrado correctamente el archivo DLL de WavSource).</span><span class="sxs-lookup"><span data-stu-id="acfd4-122">(If an error occurs, make sure that you successfully registered the WavSource DLL.)</span></span>

<span data-ttu-id="acfd4-123">También puede usar la herramienta TopoEdit para crear una topología de reproducción que contenga el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="acfd4-123">You can also use the TopoEdit tool to build a playback topology that contains the media source.</span></span> <span data-ttu-id="acfd4-124">Para obtener más información sobre TopoEdit, consulte [TopoEdit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="acfd4-124">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="acfd4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acfd4-125">Requirements</span></span>



| <span data-ttu-id="acfd4-126">Producto</span><span class="sxs-lookup"><span data-stu-id="acfd4-126">Product</span></span>                                                        | <span data-ttu-id="acfd4-127">Versión</span><span class="sxs-lookup"><span data-stu-id="acfd4-127">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="acfd4-128">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="acfd4-128">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="acfd4-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="acfd4-129">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="acfd4-130">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="acfd4-130">Downloading the Sample</span></span>

<span data-ttu-id="acfd4-131">Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource).</span><span class="sxs-lookup"><span data-stu-id="acfd4-131">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource).</span></span>

## <a name="related-topics"></a><span data-ttu-id="acfd4-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="acfd4-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acfd4-133">Muestras de SDK de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="acfd4-133">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="acfd4-134">Orígenes multimedia</span><span class="sxs-lookup"><span data-stu-id="acfd4-134">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="acfd4-135">Ejemplo de MPEG1Source</span><span class="sxs-lookup"><span data-stu-id="acfd4-135">MPEG1Source Sample</span></span>](mpeg1source-sample.md)
</dt> <dt>

[<span data-ttu-id="acfd4-136">Controladores de esquema y controladores de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="acfd4-136">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="acfd4-137">Escritura de un origen de medios personalizado</span><span class="sxs-lookup"><span data-stu-id="acfd4-137">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)
</dt> </dl>

 

 
