---
description: En este tema se describe cómo usar el lector de origen para procesar datos multimedia.
ms.assetid: 583f5736-f767-47c5-8fdc-b3645aed59f6
title: Usar el lector de origen para procesar los datos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b19bce4d83298693825037aef92a220d78ed7c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361835"
---
# <a name="using-the-source-reader-to-process-media-data"></a><span data-ttu-id="73c32-103">Usar el lector de origen para procesar los datos multimedia</span><span class="sxs-lookup"><span data-stu-id="73c32-103">Using the Source Reader to Process Media Data</span></span>

<span data-ttu-id="73c32-104">En este tema se describe cómo usar el [lector de origen](source-reader.md) para procesar datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="73c32-104">This topic describes how to use the [Source Reader](source-reader.md) to process media data.</span></span>

<span data-ttu-id="73c32-105">Para usar el lector de origen, siga estos pasos básicos:</span><span class="sxs-lookup"><span data-stu-id="73c32-105">To use the Source Reader, follow these basic steps:</span></span>

1.  <span data-ttu-id="73c32-106">Cree una instancia del lector de origen.</span><span class="sxs-lookup"><span data-stu-id="73c32-106">Create an instance of the Source Reader.</span></span>
2.  <span data-ttu-id="73c32-107">Enumerar los posibles formatos de salida.</span><span class="sxs-lookup"><span data-stu-id="73c32-107">Enumerate the possible output formats.</span></span>
3.  <span data-ttu-id="73c32-108">Establezca el formato de salida real para cada flujo.</span><span class="sxs-lookup"><span data-stu-id="73c32-108">Set the actual output format for each stream.</span></span>
4.  <span data-ttu-id="73c32-109">Procesa los datos del origen.</span><span class="sxs-lookup"><span data-stu-id="73c32-109">Process data from the source.</span></span>

<span data-ttu-id="73c32-110">En el resto de este tema se describen estos pasos con detalle.</span><span class="sxs-lookup"><span data-stu-id="73c32-110">The remainder of this topic describes these steps in detail.</span></span>

-   [<span data-ttu-id="73c32-111">Crear el lector de origen</span><span class="sxs-lookup"><span data-stu-id="73c32-111">Creating the Source Reader</span></span>](#creating-the-source-reader)
-   [<span data-ttu-id="73c32-112">Enumerar formatos de salida</span><span class="sxs-lookup"><span data-stu-id="73c32-112">Enumerating Output Formats</span></span>](#enumerating-output-formats)
-   [<span data-ttu-id="73c32-113">Establecer formatos de salida</span><span class="sxs-lookup"><span data-stu-id="73c32-113">Setting Output Formats</span></span>](#setting-output-formats)
-   [<span data-ttu-id="73c32-114">Procesar datos multimedia</span><span class="sxs-lookup"><span data-stu-id="73c32-114">Processing Media Data</span></span>](#using-the-source-reader-to-process-media-data)
-   [<span data-ttu-id="73c32-115">Purga de la canalización de datos</span><span class="sxs-lookup"><span data-stu-id="73c32-115">Draining the Data Pipeline</span></span>](#draining-the-data-pipeline)
-   [<span data-ttu-id="73c32-116">Obtención de la duración del archivo</span><span class="sxs-lookup"><span data-stu-id="73c32-116">Getting the File Duration</span></span>](#getting-the-file-duration)
-   [<span data-ttu-id="73c32-117">Invoca</span><span class="sxs-lookup"><span data-stu-id="73c32-117">Seeking</span></span>](#seeking)
-   [<span data-ttu-id="73c32-118">Velocidad de reproducción</span><span class="sxs-lookup"><span data-stu-id="73c32-118">Playback Rate</span></span>](#playback-rate)
-   [<span data-ttu-id="73c32-119">Aceleración de hardware</span><span class="sxs-lookup"><span data-stu-id="73c32-119">Hardware Acceleration</span></span>](#hardware-acceleration)
-   [<span data-ttu-id="73c32-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="73c32-120">Related topics</span></span>](#related-topics)

## <a name="creating-the-source-reader"></a><span data-ttu-id="73c32-121">Crear el lector de origen</span><span class="sxs-lookup"><span data-stu-id="73c32-121">Creating the Source Reader</span></span>

<span data-ttu-id="73c32-122">Para crear una instancia del lector de origen, llame a una de las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="73c32-122">To create an instance of the Source Reader, call one of the following functions:</span></span>



| <span data-ttu-id="73c32-123">Función</span><span class="sxs-lookup"><span data-stu-id="73c32-123">Function</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="73c32-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="73c32-124">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73c32-125"><span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)</span><span class="sxs-lookup"><span data-stu-id="73c32-125"><span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)</span></span><br/>                                         | <span data-ttu-id="73c32-126">Toma una dirección URL como entrada.</span><span class="sxs-lookup"><span data-stu-id="73c32-126">Takes a URL as input.</span></span> <span data-ttu-id="73c32-127">Esta función usa la [resolución de origen](source-resolver.md) para crear un origen multimedia a partir de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="73c32-127">This function uses the [Source Resolver](source-resolver.md) to create a media source from the URL.</span></span><br/>                                                                       |
| <span data-ttu-id="73c32-128"><span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)</span><span class="sxs-lookup"><span data-stu-id="73c32-128"><span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)</span></span><br/>      | <span data-ttu-id="73c32-129">Toma un puntero a una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="73c32-129">Takes a pointer to a byte stream.</span></span> <span data-ttu-id="73c32-130">Esta función también utiliza la resolución de origen para crear el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="73c32-130">This function also uses the Source Resolver to create the media source.</span></span><br/>                                                                                        |
| <span data-ttu-id="73c32-131"><span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)</span><span class="sxs-lookup"><span data-stu-id="73c32-131"><span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)</span></span><br/> | <span data-ttu-id="73c32-132">Toma un puntero a un origen de medios que ya se ha creado.</span><span class="sxs-lookup"><span data-stu-id="73c32-132">Takes a pointer to a media source that has already been created.</span></span> <span data-ttu-id="73c32-133">Esta función es útil para los orígenes multimedia que la resolución de origen no puede crear, tales como los dispositivos de captura o los orígenes de medios personalizados.</span><span class="sxs-lookup"><span data-stu-id="73c32-133">This function is useful for media sources that the Source Resolver cannot create, such capture devices or custom media sources.</span></span><br/> |



 

<span data-ttu-id="73c32-134">Normalmente, para los archivos multimedia, use [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl).</span><span class="sxs-lookup"><span data-stu-id="73c32-134">Typically, for media files, use [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl).</span></span> <span data-ttu-id="73c32-135">En el caso de los dispositivos, como las cámaras Web, use [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource).</span><span class="sxs-lookup"><span data-stu-id="73c32-135">For devices, such as webcams, use [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource).</span></span> <span data-ttu-id="73c32-136">(Para obtener más información acerca de la captura de dispositivos en Microsoft Media Foundation, consulte [captura de audio y vídeo](audio-video-capture.md)).</span><span class="sxs-lookup"><span data-stu-id="73c32-136">(For more information about capture devices in Microsoft Media Foundation, see [Audio/Video Capture](audio-video-capture.md).)</span></span>

<span data-ttu-id="73c32-137">Cada una de estas funciones toma un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) opcional, que se usa para establecer varias opciones en el lector de origen, tal y como se describe en los temas de referencia de estas funciones.</span><span class="sxs-lookup"><span data-stu-id="73c32-137">Each of these functions takes an optional [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer, which is used to set various options on the Source Reader, as described in the reference topics for these functions.</span></span> <span data-ttu-id="73c32-138">Para obtener el comportamiento predeterminado, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="73c32-138">To get the default behavior, set this parameter to **NULL**.</span></span> <span data-ttu-id="73c32-139">Cada función devuelve un puntero [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="73c32-139">Each function returns an [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) pointer as an output parameter.</span></span> <span data-ttu-id="73c32-140">Debe llamar a la función **CoInitialize (ex)** y [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) antes de llamar a cualquiera de estas funciones.</span><span class="sxs-lookup"><span data-stu-id="73c32-140">You must call **CoInitialize(Ex)** and [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function before calling any of these functions.</span></span>

<span data-ttu-id="73c32-141">En el código siguiente se crea el lector de origen a partir de una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="73c32-141">The following code creates the Source Reader from a URL.</span></span>


```C++
int __cdecl wmain(int argc, __in_ecount(argc) PCWSTR* argv)
{
    if (argc < 2)
    {
        return 1;
    }

    const WCHAR *pszURL = argv[1];

    // Initialize the COM runtime.
    HRESULT hr = CoInitializeEx(0, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        // Initialize the Media Foundation platform.
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            // Create the source reader.
            IMFSourceReader *pReader;
            hr = MFCreateSourceReaderFromURL(pszURL, NULL, &pReader);
            if (SUCCEEDED(hr))
            {
                ReadMediaFile(pReader);
                pReader->Release();
            }
            // Shut down Media Foundation.
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="enumerating-output-formats"></a><span data-ttu-id="73c32-142">Enumerar formatos de salida</span><span class="sxs-lookup"><span data-stu-id="73c32-142">Enumerating Output Formats</span></span>

<span data-ttu-id="73c32-143">Cada origen multimedia tiene al menos un flujo.</span><span class="sxs-lookup"><span data-stu-id="73c32-143">Every media source has at least one stream.</span></span> <span data-ttu-id="73c32-144">Por ejemplo, un archivo de vídeo puede contener una secuencia de vídeo y una secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="73c32-144">For example, a video file might contain a video stream and an audio stream.</span></span> <span data-ttu-id="73c32-145">El formato de cada flujo se describe mediante un tipo de medio, representado por la interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="73c32-145">The format of each stream is described using a media type, represented by the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface.</span></span> <span data-ttu-id="73c32-146">Para obtener más información sobre los tipos de medios, consulte [tipos de medios](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="73c32-146">For more information about media types, see [Media Types](media-types.md).</span></span> <span data-ttu-id="73c32-147">Debe examinar el tipo de medio para comprender el formato de los datos que obtiene del lector de origen.</span><span class="sxs-lookup"><span data-stu-id="73c32-147">You must examine the media type to understand the format of the data that you get from the Source Reader.</span></span>

<span data-ttu-id="73c32-148">Inicialmente, cada flujo tiene un formato predeterminado, que se puede encontrar mediante una llamada al método [**IMFSourceReader:: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) :</span><span class="sxs-lookup"><span data-stu-id="73c32-148">Initially, every stream has a default format, which you can find by calling the [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) method:</span></span>

<span data-ttu-id="73c32-149">Para cada flujo, el origen multimedia ofrece una lista de los posibles tipos de medios para esa secuencia.</span><span class="sxs-lookup"><span data-stu-id="73c32-149">For each stream, the media source offers a list of possible media types for that stream.</span></span> <span data-ttu-id="73c32-150">El número de tipos depende del origen.</span><span class="sxs-lookup"><span data-stu-id="73c32-150">The number of types depends on the source.</span></span> <span data-ttu-id="73c32-151">Si el origen representa un archivo multimedia, normalmente solo hay un tipo por secuencia.</span><span class="sxs-lookup"><span data-stu-id="73c32-151">If the source represents a media file, there is typically only one type per stream.</span></span> <span data-ttu-id="73c32-152">Por otro lado, una cámara web podría transmitir vídeo en varios formatos distintos.</span><span class="sxs-lookup"><span data-stu-id="73c32-152">A webcam, on the other hand, might be able to stream video in several different formats.</span></span> <span data-ttu-id="73c32-153">En ese caso, la aplicación puede seleccionar el formato que se va a usar en la lista de tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="73c32-153">In that case, the application can select which format to use from the list of media types.</span></span>

<span data-ttu-id="73c32-154">Para obtener uno de los tipos de medios de un flujo, llame al método [**IMFSourceReader:: GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) .</span><span class="sxs-lookup"><span data-stu-id="73c32-154">To get one of the media types for a stream, call the [**IMFSourceReader::GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) method.</span></span> <span data-ttu-id="73c32-155">Este método toma dos parámetros de índice: el índice de la secuencia y un índice en la lista de tipos de medios para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="73c32-155">This method takes two index parameters: The index of the stream, and an index into the list of media types for the stream.</span></span> <span data-ttu-id="73c32-156">Para enumerar todos los tipos de una secuencia, aumente el índice de la lista manteniendo la constante de índice de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="73c32-156">To enumerate all the types for a stream, increment the list index while keeping the stream index constant.</span></span> <span data-ttu-id="73c32-157">Cuando el índice de la lista sale de los límites, **GetNativeMediaType** devuelve **MF \_ E \_ no hay \_ más \_ tipos**.</span><span class="sxs-lookup"><span data-stu-id="73c32-157">When the list index goes out of bounds, **GetNativeMediaType** returns **MF\_E\_NO\_MORE\_TYPES**.</span></span>


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



<span data-ttu-id="73c32-158">Para enumerar los tipos de medios de cada flujo, aumente el índice de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="73c32-158">To enumerate the media types for every stream, increment the stream index.</span></span> <span data-ttu-id="73c32-159">Cuando el índice de la secuencia sale de los límites, [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) devuelve **MF \_ E \_ INVALIDSTREAMNUMBER**.</span><span class="sxs-lookup"><span data-stu-id="73c32-159">When the stream index goes out of bounds, [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) returns **MF\_E\_INVALIDSTREAMNUMBER**.</span></span>


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



## <a name="setting-output-formats"></a><span data-ttu-id="73c32-160">Establecer formatos de salida</span><span class="sxs-lookup"><span data-stu-id="73c32-160">Setting Output Formats</span></span>

<span data-ttu-id="73c32-161">Para cambiar el formato de salida, llame al método [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) .</span><span class="sxs-lookup"><span data-stu-id="73c32-161">To change the output format, call the [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) method.</span></span> <span data-ttu-id="73c32-162">Este método toma el índice de la secuencia y un tipo de medio:</span><span class="sxs-lookup"><span data-stu-id="73c32-162">This method takes the stream index and a media type:</span></span>

``` syntax
hr = pReader->SetCurrentMediaType(dwStreamIndex, pMediaType);
```

<span data-ttu-id="73c32-163">En el caso del tipo de medio, depende de si desea insertar un descodificador.</span><span class="sxs-lookup"><span data-stu-id="73c32-163">For the media type, it depends on whether you want to insert a decoder.</span></span>

-   <span data-ttu-id="73c32-164">Para obtener datos directamente del origen sin descodificarlos, use uno de los tipos devueltos por [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype).</span><span class="sxs-lookup"><span data-stu-id="73c32-164">To get data directly from the source without decoding it, use one of the types returned by [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype).</span></span>
-   <span data-ttu-id="73c32-165">Para descodificar la secuencia, cree un nuevo tipo de medio que describa el formato no comprimido deseado.</span><span class="sxs-lookup"><span data-stu-id="73c32-165">To decode the stream, create a new media type that describes the desired uncompressed format.</span></span>

<span data-ttu-id="73c32-166">En el caso del descodificador, cree el tipo de medio de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="73c32-166">In the case of the decoder, create the media type as follows:</span></span>

1.  <span data-ttu-id="73c32-167">Llame a [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) para crear un nuevo tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="73c32-167">Call [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) to create a new media type.</span></span>
2.  <span data-ttu-id="73c32-168">Establezca el atributo de [**\_ \_ \_ tipo principal MF MT**](mf-mt-major-type-attribute.md) para especificar audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="73c32-168">Set the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute to specify audio or video.</span></span>
3.  <span data-ttu-id="73c32-169">Establezca el atributo [**MF \_ MT \_ SubType**](mf-mt-subtype-attribute.md) para especificar el subtipo del formato de descodificación.</span><span class="sxs-lookup"><span data-stu-id="73c32-169">Set the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute to specify the subtype of the decoding format.</span></span> <span data-ttu-id="73c32-170">(Consulte GUID de [subtipo de audio](audio-subtype-guids.md) y [GUID de subtipo de vídeo](video-subtype-guids.md)).</span><span class="sxs-lookup"><span data-stu-id="73c32-170">(See [Audio Subtype GUIDs](audio-subtype-guids.md) and [Video Subtype GUIDs](video-subtype-guids.md).)</span></span>
4.  <span data-ttu-id="73c32-171">Llame a [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="73c32-171">Call [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span></span>

<span data-ttu-id="73c32-172">El lector de origen cargará automáticamente el descodificador.</span><span class="sxs-lookup"><span data-stu-id="73c32-172">The Source Reader will automatically load the decoder.</span></span> <span data-ttu-id="73c32-173">Para obtener los detalles completos del formato descodificado, llame a [**IMFSourceReader:: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) después de la llamada a [**SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)</span><span class="sxs-lookup"><span data-stu-id="73c32-173">To get the complete details of the decoded format, call [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) after the call to [**SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)</span></span>

<span data-ttu-id="73c32-174">El código siguiente configura el flujo de vídeo para RGB-32 y la secuencia de audio para audio PCM.</span><span class="sxs-lookup"><span data-stu-id="73c32-174">The following code configures the video stream for RGB-32 and the audio stream for PCM audio.</span></span>


```C++
HRESULT ConfigureDecoder(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    IMFMediaType *pNativeType = NULL;
    IMFMediaType *pType = NULL;

    // Find the native format of the stream.
    HRESULT hr = pReader->GetNativeMediaType(dwStreamIndex, 0, &pNativeType);
    if (FAILED(hr))
    {
        return hr;
    }

    GUID majorType, subtype;

    // Find the major type.
    hr = pNativeType->GetGUID(MF_MT_MAJOR_TYPE, &majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Define the output type.
    hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Select a subtype.
    if (majorType == MFMediaType_Video)
    {
        subtype= MFVideoFormat_RGB32;
    }
    else if (majorType == MFMediaType_Audio)
    {
        subtype = MFAudioFormat_PCM;
    }
    else
    {
        // Unrecognized type. Skip.
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the uncompressed format.
    hr = pReader->SetCurrentMediaType(dwStreamIndex, NULL, pType);
    if (FAILED(hr))
    {
        goto done;
    }

done:
    SafeRelease(&pNativeType);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="processing-media-data"></a><span data-ttu-id="73c32-175">Procesar datos multimedia</span><span class="sxs-lookup"><span data-stu-id="73c32-175">Processing Media Data</span></span>

<span data-ttu-id="73c32-176">Para obtener datos multimedia del origen, llame al método [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) , como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="73c32-176">To get media data from the source, call the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method, as shown in the following code.</span></span>


```C++
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );
```



<span data-ttu-id="73c32-177">El primer parámetro es el índice de la secuencia para la que desea obtener los datos.</span><span class="sxs-lookup"><span data-stu-id="73c32-177">The first parameter is the index of the stream for which you want to get data.</span></span> <span data-ttu-id="73c32-178">También puede especificar el **lector de origen MF en \_ \_ \_ cualquier \_ flujo** para obtener los siguientes datos disponibles de cualquier secuencia.</span><span class="sxs-lookup"><span data-stu-id="73c32-178">You can also specify **MF\_SOURCE\_READER\_ANY\_STREAM** to get the next available data from any stream.</span></span> <span data-ttu-id="73c32-179">El segundo parámetro contiene marcas opcionales; vea [**la \_ \_ marca de \_ control \_ del lector de código fuente MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) para obtener una lista de ellos.</span><span class="sxs-lookup"><span data-stu-id="73c32-179">The second parameter contains optional flags; see [**MF\_SOURCE\_READER\_CONTROL\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) for a list of these.</span></span> <span data-ttu-id="73c32-180">El tercer parámetro recibe el índice de la secuencia que realmente genera los datos.</span><span class="sxs-lookup"><span data-stu-id="73c32-180">The third parameter receives the index of the stream that actually produces the data.</span></span> <span data-ttu-id="73c32-181">Necesitará esta información si establece el primer parámetro en el **lector de \_ origen MF en \_ \_ cualquier \_ flujo**.</span><span class="sxs-lookup"><span data-stu-id="73c32-181">You will need this information if you set the first parameter to **MF\_SOURCE\_READER\_ANY\_STREAM**.</span></span> <span data-ttu-id="73c32-182">El cuarto parámetro recibe marcas de estado, que indican varios eventos que se pueden producir al leer los datos, como los cambios de formato en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="73c32-182">The fourth parameter receives status flags, indicating various events that can occur while reading the data, such as format changes in the stream.</span></span> <span data-ttu-id="73c32-183">Para obtener una lista de las marcas de estado, consulte [**MF \_ source \_ Reader \_ Flag**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).</span><span class="sxs-lookup"><span data-stu-id="73c32-183">For a list of status flags, see [**MF\_SOURCE\_READER\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).</span></span>

<span data-ttu-id="73c32-184">Si el origen multimedia es capaz de generar datos para la secuencia solicitada, el último parámetro de [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) recibe un puntero a la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) de un objeto de ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="73c32-184">If the media source is able to produce data for the requested stream, the last parameter of [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) receives a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface of a media sample object.</span></span> <span data-ttu-id="73c32-185">Use el ejemplo multimedia para:</span><span class="sxs-lookup"><span data-stu-id="73c32-185">Use the media sample to:</span></span>

-   <span data-ttu-id="73c32-186">Obtiene un puntero a los datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="73c32-186">Get a pointer to the media data.</span></span>
-   <span data-ttu-id="73c32-187">Obtiene el tiempo de presentación y la duración de la muestra.</span><span class="sxs-lookup"><span data-stu-id="73c32-187">Get the presentation time and sample duration.</span></span>
-   <span data-ttu-id="73c32-188">Obtiene los atributos que describen el entrelazado, el dominio de campo y otros aspectos del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="73c32-188">Get attributes that describe interlacing, field dominance, and other aspects of the sample.</span></span>

<span data-ttu-id="73c32-189">El contenido de los datos multimedia depende del formato del flujo.</span><span class="sxs-lookup"><span data-stu-id="73c32-189">The contents of the media data depend on the format of the stream.</span></span> <span data-ttu-id="73c32-190">En el caso de una secuencia de vídeo sin comprimir, cada ejemplo multimedia contiene un solo fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="73c32-190">For an uncompressed video stream, each media sample contains a single video frame.</span></span> <span data-ttu-id="73c32-191">En el caso de una secuencia de audio sin comprimir, cada ejemplo multimedia contiene una secuencia de fotogramas de audio.</span><span class="sxs-lookup"><span data-stu-id="73c32-191">For an uncompressed audio stream, each media sample contains a sequence of audio frames.</span></span>

<span data-ttu-id="73c32-192">El método [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) puede devolver **S \_ OK** y no devolver un ejemplo multimedia en el parámetro *pSample* .</span><span class="sxs-lookup"><span data-stu-id="73c32-192">The [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method can return **S\_OK** and yet not return a media sample in the *pSample* parameter.</span></span> <span data-ttu-id="73c32-193">Por ejemplo, cuando se alcanza el final del archivo, **ReadSample** establece la marca **MF \_ source \_ READERF \_ ENDOFSTREAM** en *dwFlags* y establece *pSample* en **null**.</span><span class="sxs-lookup"><span data-stu-id="73c32-193">For example, when you reach the end of the file, **ReadSample** sets the **MF\_SOURCE\_READERF\_ENDOFSTREAM** flag in *dwFlags* and sets *pSample* to **NULL**.</span></span> <span data-ttu-id="73c32-194">En este caso, el método **ReadSample** devuelve **S \_ OK** porque no se ha producido ningún error, aunque el parámetro *pSample* está establecido en **null**.</span><span class="sxs-lookup"><span data-stu-id="73c32-194">In this case, the **ReadSample** method returns **S\_OK** because no error has occurred, even though the *pSample* parameter is set to **NULL**.</span></span> <span data-ttu-id="73c32-195">Por consiguiente, compruebe siempre el valor de *pSample* antes de desreferenciarlo.</span><span class="sxs-lookup"><span data-stu-id="73c32-195">Therefore, always check the value of *pSample* before you dereference it.</span></span>

<span data-ttu-id="73c32-196">En el código siguiente se muestra cómo llamar a [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) en un bucle y comprobar la información devuelta por el método hasta que se alcanza el final del archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="73c32-196">The following code shows how to call [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) in a loop and check the information returned by the method, until the end of the media file is reached.</span></span>


```C++
HRESULT ProcessSamples(IMFSourceReader *pReader)
{
    HRESULT hr = S_OK;
    IMFSample *pSample = NULL;
    size_t  cSamples = 0;

    bool quit = false;
    while (!quit)
    {
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );

        if (FAILED(hr))
        {
            break;
        }

        wprintf(L"Stream %d (%I64d)\n", streamIndex, llTimeStamp);
        if (flags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            wprintf(L"\tEnd of stream\n");
            quit = true;
        }
        if (flags & MF_SOURCE_READERF_NEWSTREAM)
        {
            wprintf(L"\tNew stream\n");
        }
        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            wprintf(L"\tNative type changed\n");
        }
        if (flags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            wprintf(L"\tCurrent type changed\n");
        }
        if (flags & MF_SOURCE_READERF_STREAMTICK)
        {
            wprintf(L"\tStream tick\n");
        }

        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            // The format changed. Reconfigure the decoder.
            hr = ConfigureDecoder(pReader, streamIndex);
            if (FAILED(hr))
            {
                break;
            }
        }

        if (pSample)
        {
            ++cSamples;
        }

        SafeRelease(&pSample);
    }

    if (FAILED(hr))
    {
        wprintf(L"ProcessSamples FAILED, hr = 0x%x\n", hr);
    }
    else
    {
        wprintf(L"Processed %d samples\n", cSamples);
    }
    SafeRelease(&pSample);
    return hr;
}
```



## <a name="draining-the-data-pipeline"></a><span data-ttu-id="73c32-197">Purga de la canalización de datos</span><span class="sxs-lookup"><span data-stu-id="73c32-197">Draining the Data Pipeline</span></span>

<span data-ttu-id="73c32-198">Durante el procesamiento de datos, un descodificador u otra transformación podría almacenar en búfer ejemplos de entrada.</span><span class="sxs-lookup"><span data-stu-id="73c32-198">During data processing, a decoder or other transform might buffer input samples.</span></span> <span data-ttu-id="73c32-199">En el diagrama siguiente, la aplicación llama a [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) y recibe un ejemplo con un tiempo de presentación igual a *T1*.</span><span class="sxs-lookup"><span data-stu-id="73c32-199">In the following diagram, the application calls [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) and receives a sample with a presentation time equal to *t1*.</span></span> <span data-ttu-id="73c32-200">El descodificador contiene ejemplos de *T2* y *T3*.</span><span class="sxs-lookup"><span data-stu-id="73c32-200">The decoder is holding samples for *t2* and *t3*.</span></span>

![Ilustración que muestra el almacenamiento en búfer en un descodificador.](images/sourcereader02.png)

<span data-ttu-id="73c32-202">En la siguiente llamada a [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample), el lector de código fuente puede proporcionar *T4* al descodificador y devolver *T2* a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="73c32-202">On the next call to [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample), the Source Reader might give *t4* to the decoder and return *t2* to the application.</span></span>

<span data-ttu-id="73c32-203">Si desea descodificar todos los ejemplos que están almacenados actualmente en el búfer en el descodificador, sin pasar los nuevos ejemplos al descodificador, establezca la marca **de \_ purga del lector de origen MF \_ \_ CONTROLF \_** en el parámetro *dwControlFlags* de [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span><span class="sxs-lookup"><span data-stu-id="73c32-203">If you want to decode all of the samples that are currently buffered in the decoder, without passing any new samples to the decoder, set the **MF\_SOURCE\_READER\_CONTROLF\_DRAIN** flag in the *dwControlFlags* parameter of [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span></span> <span data-ttu-id="73c32-204">Siga haciendo esto en un bucle hasta que **ReadSample** devuelva un puntero de muestra **nulo** .</span><span class="sxs-lookup"><span data-stu-id="73c32-204">Continue to do this in a loop until **ReadSample** returns a **NULL** sample pointer.</span></span> <span data-ttu-id="73c32-205">En función de cómo los ejemplos de búferes del descodificador, pueden producirse inmediatamente o después de varias llamadas a **ReadSample**.</span><span class="sxs-lookup"><span data-stu-id="73c32-205">Depending on how the decoder buffers samples, that might happen immediately or after several calls to **ReadSample**.</span></span>

## <a name="getting-the-file-duration"></a><span data-ttu-id="73c32-206">Obtención de la duración del archivo</span><span class="sxs-lookup"><span data-stu-id="73c32-206">Getting the File Duration</span></span>

<span data-ttu-id="73c32-207">Para obtener la duración de un archivo multimedia, llame al método [**IMFSourceReader:: GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) y solicite el atributo de [**\_ \_ duración MF PD**](mf-pd-duration-attribute.md) , tal como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="73c32-207">To get the duration of a media file, call the [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) method and request the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute, as shown in the following code.</span></span>


```C++
HRESULT GetDuration(IMFSourceReader *pReader, LONGLONG *phnsDuration)
{
    PROPVARIANT var;
    HRESULT hr = pReader->GetPresentationAttribute(MF_SOURCE_READER_MEDIASOURCE, 
        MF_PD_DURATION, &var);
    if (SUCCEEDED(hr))
    {
        hr = PropVariantToInt64(var, phnsDuration);
        PropVariantClear(&var);
    }
    return hr;
}
```



<span data-ttu-id="73c32-208">La función mostrada aquí obtiene la duración en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="73c32-208">The function shown here gets the duration in 100-nanosecond units.</span></span> <span data-ttu-id="73c32-209">Divida por 10 millones para obtener la duración en segundos.</span><span class="sxs-lookup"><span data-stu-id="73c32-209">Divide by 10,000,000 to get the duration in seconds.</span></span>

## <a name="seeking"></a><span data-ttu-id="73c32-210">Invoca</span><span class="sxs-lookup"><span data-stu-id="73c32-210">Seeking</span></span>

<span data-ttu-id="73c32-211">Un origen multimedia que obtiene datos de un archivo local normalmente puede buscar posiciones arbitrarias en el archivo.</span><span class="sxs-lookup"><span data-stu-id="73c32-211">A media source that gets data from a local file can usually seek to arbitrary positions in the file.</span></span> <span data-ttu-id="73c32-212">Normalmente, los dispositivos de captura, como las cámaras Web, no pueden buscar, ya que los datos están activos.</span><span class="sxs-lookup"><span data-stu-id="73c32-212">Capture devices such as webcams generally cannot seek, because the data is live.</span></span> <span data-ttu-id="73c32-213">Un origen que transmite datos a través de una red podría ser capaz de buscar, dependiendo del Protocolo de transmisión por secuencias de red.</span><span class="sxs-lookup"><span data-stu-id="73c32-213">A source that streams data over a network might be able to seek, depending on the network streaming protocol.</span></span>

<span data-ttu-id="73c32-214">Para averiguar si un origen multimedia puede buscar, llame a [**IMFSourceReader:: GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) y solicite el atributo de la instancia de [ \_ MEDIASOURCE del lector de origen \_ \_ \_ MF](mf-source-reader-mediasource-characteristics.md) , tal como se muestra en el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="73c32-214">To find out whether a media source can seek, call [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) and request the [MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS](mf-source-reader-mediasource-characteristics.md) attribute, as shown in the following code:</span></span>


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



<span data-ttu-id="73c32-215">Esta función obtiene un conjunto de marcas de funcionalidades del origen.</span><span class="sxs-lookup"><span data-stu-id="73c32-215">This function gets a set of capabilities flags from the source.</span></span> <span data-ttu-id="73c32-216">Estas marcas se definen en la enumeración de [**\_ características de MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="73c32-216">These flags are defined in the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span> <span data-ttu-id="73c32-217">Dos marcas están relacionadas con la búsqueda:</span><span class="sxs-lookup"><span data-stu-id="73c32-217">Two flags relate to seeking:</span></span>



| <span data-ttu-id="73c32-218">Marca</span><span class="sxs-lookup"><span data-stu-id="73c32-218">Flag</span></span>                                                                                                                                      | <span data-ttu-id="73c32-219">Descripción</span><span class="sxs-lookup"><span data-stu-id="73c32-219">Description</span></span>                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73c32-220"><span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**MFMEDIASOURCE \_ puede \_ Buscar**</span><span class="sxs-lookup"><span data-stu-id="73c32-220"><span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**MFMEDIASOURCE\_CAN\_SEEK**</span></span><br/>                 | <span data-ttu-id="73c32-221">El origen puede buscar.</span><span class="sxs-lookup"><span data-stu-id="73c32-221">The source can seek.</span></span><br/>                                                                                                                                                                            |
| <span data-ttu-id="73c32-222"><span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**MFMEDIASOURCE \_ tiene \_ una \_ búsqueda lenta**</span><span class="sxs-lookup"><span data-stu-id="73c32-222"><span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**MFMEDIASOURCE\_HAS\_SLOW\_SEEK**</span></span><br/> | <span data-ttu-id="73c32-223">La búsqueda puede tardar mucho tiempo en completarse.</span><span class="sxs-lookup"><span data-stu-id="73c32-223">Seeking might take a long time to complete.</span></span> <span data-ttu-id="73c32-224">Por ejemplo, es posible que el origen tenga que descargar todo el archivo antes de que pueda buscar.</span><span class="sxs-lookup"><span data-stu-id="73c32-224">For example, the source might need to download the entire file before it can seek.</span></span> <span data-ttu-id="73c32-225">(No hay ningún criterio estricto para que un origen devuelva esta marca).</span><span class="sxs-lookup"><span data-stu-id="73c32-225">(There are no strict criteria for a source to return this flag.)</span></span><br/> |



 

<span data-ttu-id="73c32-226">Las siguientes pruebas de código para **MFMEDIASOURCE \_ pueden \_ Buscar** la marca.</span><span class="sxs-lookup"><span data-stu-id="73c32-226">The following code tests for the **MFMEDIASOURCE\_CAN\_SEEK** flag.</span></span>


```C++
BOOL SourceCanSeek(IMFSourceReader *pReader)
{
    BOOL bCanSeek = FALSE;
    ULONG flags;
    if (SUCCEEDED(GetSourceFlags(pReader, &flags)))
    {
        bCanSeek = ((flags & MFMEDIASOURCE_CAN_SEEK) == MFMEDIASOURCE_CAN_SEEK);
    }
    return bCanSeek;
}
```



<span data-ttu-id="73c32-227">Para buscar, llame al método [**IMFSourceReader:: SetCurrentPosition**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) , tal y como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="73c32-227">To seek, call the [**IMFSourceReader::SetCurrentPosition**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) method, as shown in the following code.</span></span>


```C++
HRESULT SetPosition(IMFSourceReader *pReader, const LONGLONG& hnsPosition)
{
    PROPVARIANT var;
    HRESULT hr = InitPropVariantFromInt64(hnsPosition, &var);
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentPosition(GUID_NULL, var);
        PropVariantClear(&var);
    }
    return hr;
}
```



<span data-ttu-id="73c32-228">El primer parámetro proporciona el formato de hora que se usa para especificar la posición de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="73c32-228">The first parameter gives the time format that you are using to specify the seek position.</span></span> <span data-ttu-id="73c32-229">Todos los orígenes multimedia en Media Foundation son necesarios para admitir unidades 100-nanosegundos, indicado por el valor **\_ null GUID**.</span><span class="sxs-lookup"><span data-stu-id="73c32-229">All media sources in Media Foundation are required to support 100-nanosecond units, indicated by the value **GUID\_NULL**.</span></span> <span data-ttu-id="73c32-230">El segundo parámetro es un **PROPVARIANT** que contiene la posición de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="73c32-230">The second parameter is a **PROPVARIANT** that contains the seek position.</span></span> <span data-ttu-id="73c32-231">En las unidades de tiempo de 100-nanosegundos, el tipo de datos es **LONGLONG**.</span><span class="sxs-lookup"><span data-stu-id="73c32-231">For 100-nanosecond time units, the data type is **LONGLONG**.</span></span>

<span data-ttu-id="73c32-232">Tenga en cuenta que no todos los orígenes multimedia proporcionan búsquedas precisas de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="73c32-232">Be aware that not every media source provides frame-accurate seeking.</span></span> <span data-ttu-id="73c32-233">La precisión de la búsqueda depende de varios factores, como el intervalo de fotogramas clave, si el archivo multimedia contiene un índice y si los datos tienen una velocidad de bits constante o variable.</span><span class="sxs-lookup"><span data-stu-id="73c32-233">The accuracy of seeking depends on several factors, such as the key frame interval, whether the media file contains an index, and whether the data has a constant or variable bit rate.</span></span> <span data-ttu-id="73c32-234">Por lo tanto, después de buscar una posición en un archivo, no hay ninguna garantía de que la marca de tiempo en el siguiente ejemplo coincida exactamente con la posición solicitada.</span><span class="sxs-lookup"><span data-stu-id="73c32-234">Therefore, after you seek to a position in a file, there is no guarantee that the time stamp on the next sample will exactly match the requested position.</span></span> <span data-ttu-id="73c32-235">Por lo general, la posición real no será posterior a la posición solicitada, por lo que puede descartar muestras hasta alcanzar el punto deseado en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="73c32-235">Generally, the actual position will not be later than the requested position, so you can discard samples until you reach the desired point in the stream.</span></span>

## <a name="playback-rate"></a><span data-ttu-id="73c32-236">Velocidad de reproducción</span><span class="sxs-lookup"><span data-stu-id="73c32-236">Playback Rate</span></span>

<span data-ttu-id="73c32-237">Aunque puede establecer la velocidad de reproducción mediante el lector de origen, no suele ser muy útil, por las razones siguientes:</span><span class="sxs-lookup"><span data-stu-id="73c32-237">Although you can set the playback rate using the Source Reader, doing is typically not very useful, for the following reasons:</span></span>

-   <span data-ttu-id="73c32-238">El lector de origen no admite la reproducción inversa, incluso si el origen multimedia sí lo hace.</span><span class="sxs-lookup"><span data-stu-id="73c32-238">The Source Reader does not support reverse playback, even if the media source does.</span></span>
-   <span data-ttu-id="73c32-239">La aplicación controla los tiempos de presentación, por lo que la aplicación puede implementar la reproducción rápida o lenta sin establecer la tasa en el origen.</span><span class="sxs-lookup"><span data-stu-id="73c32-239">The application controls the presentation times, so the application can implement fast or slow play without setting the rate on the source.</span></span>
-   <span data-ttu-id="73c32-240">Algunos orígenes multimedia admiten el modo *delgado* , donde el origen ofrece menos muestras, normalmente solo los fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="73c32-240">Some media sources support *thinning* mode, where the source delivers fewer samples—typically just the key frames.</span></span> <span data-ttu-id="73c32-241">Sin embargo, si desea quitar fotogramas no clave, puede comprobar cada ejemplo del atributo [ \_ CleanPoint de MFSampleExtension](mfsampleextension-cleanpoint-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="73c32-241">However, if you want to drop non-key frames, you can check each sample for the [MFSampleExtension\_CleanPoint](mfsampleextension-cleanpoint-attribute.md) attribute.</span></span>

<span data-ttu-id="73c32-242">Para establecer la velocidad de reproducción mediante el lector de origen, llame al método [**IMFSourceReader:: GetServiceForStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) para obtener las interfaces [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) y [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) del origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="73c32-242">To set the playback rate using the Source Reader, call the [**IMFSourceReader::GetServiceForStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) method to get the [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) and [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interfaces from the media source.</span></span>

## <a name="hardware-acceleration"></a><span data-ttu-id="73c32-243">Aceleración de hardware</span><span class="sxs-lookup"><span data-stu-id="73c32-243">Hardware Acceleration</span></span>

<span data-ttu-id="73c32-244">El lector de origen es compatible con la aceleración de vídeo de Microsoft DirectX (DXVA) 2,0 para la descodificación de vídeo acelerada de hardware.</span><span class="sxs-lookup"><span data-stu-id="73c32-244">The Source Reader is compatible with Microsoft DirectX Video Acceleration (DXVA) 2.0 for hardware accelerated video decoding.</span></span> <span data-ttu-id="73c32-245">Para usar DXVA con el lector de origen, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="73c32-245">To use DXVA with the Source Reader, perform the following steps.</span></span>

1.  <span data-ttu-id="73c32-246">Cree un dispositivo de Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="73c32-246">Create a Microsoft Direct3D device.</span></span>
2.  <span data-ttu-id="73c32-247">Llame a la función [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) para crear el administrador de dispositivos de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="73c32-247">Call the [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) function to create the Direct3D device manager.</span></span> <span data-ttu-id="73c32-248">Esta función obtiene un puntero a la interfaz [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .</span><span class="sxs-lookup"><span data-stu-id="73c32-248">This function gets a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span>
3.  <span data-ttu-id="73c32-249">Llame al método [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) con un puntero al dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="73c32-249">Call the [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) method with a pointer to the Direct3D device.</span></span>
4.  <span data-ttu-id="73c32-250">Cree un almacén de atributos mediante una llamada a la función [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .</span><span class="sxs-lookup"><span data-stu-id="73c32-250">Create an attribute store by calling the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function.</span></span>
5.  <span data-ttu-id="73c32-251">Cree el lector de origen.</span><span class="sxs-lookup"><span data-stu-id="73c32-251">Create the Source Reader.</span></span> <span data-ttu-id="73c32-252">Pase el almacén de atributos en el parámetro *pAttributes* de la función de creación.</span><span class="sxs-lookup"><span data-stu-id="73c32-252">Pass the attribute store in the *pAttributes* parameter of the creation function.</span></span>

<span data-ttu-id="73c32-253">Cuando se proporciona un dispositivo Direct3D, el lector de código fuente asigna muestras de vídeo que son compatibles con la API del procesador de vídeo de DXVA.</span><span class="sxs-lookup"><span data-stu-id="73c32-253">When you provide a Direct3D device, the Source Reader allocates video samples that are compatible with the DXVA video processor API.</span></span> <span data-ttu-id="73c32-254">Puede usar el procesamiento de vídeo de DXVA para realizar el desentrelazado de hardware o la combinación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="73c32-254">You can use DXVA video processing to perform hardware deinterlacing or video mixing.</span></span> <span data-ttu-id="73c32-255">Para obtener más información, vea [procesamiento de vídeo de DXVA](dxva-video-processing.md).</span><span class="sxs-lookup"><span data-stu-id="73c32-255">For more information, see [DXVA Video Processing](dxva-video-processing.md).</span></span> <span data-ttu-id="73c32-256">Además, si el descodificador admite DXVA 2,0, usará el dispositivo Direct3D para realizar la descodificación acelerada por hardware.</span><span class="sxs-lookup"><span data-stu-id="73c32-256">Also, if the decoder supports DXVA 2.0, it will use the Direct3D device to perform hardware-accelerated decoding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="73c32-257">A partir de Windows 8, se puede usar [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) en lugar de [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9).</span><span class="sxs-lookup"><span data-stu-id="73c32-257">Beginning in Windows 8, [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) can be used instead of the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9).</span></span> <span data-ttu-id="73c32-258">En el caso de las aplicaciones de la tienda Windows, debe usar **IMFDXGIDeviceManager**.</span><span class="sxs-lookup"><span data-stu-id="73c32-258">For Windows Store apps, you must use **IMFDXGIDeviceManager**.</span></span> <span data-ttu-id="73c32-259">Para obtener más información, consulte las [API de vídeo de Direct3D 11](direct3d-11-video-apis.md).</span><span class="sxs-lookup"><span data-stu-id="73c32-259">For more info, see the [Direct3D 11 Video APIs](direct3d-11-video-apis.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="73c32-260">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="73c32-260">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73c32-261">Lector de origen</span><span class="sxs-lookup"><span data-stu-id="73c32-261">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




