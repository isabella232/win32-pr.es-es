---
description: En este tutorial se usa el escritor de receptores para codificar un archivo de vídeo.
ms.assetid: 3E297366-0863-4E89-A0D5-438CD1FC5AF9
title: 'Tutorial: uso del escritor de receptores para codificar vídeo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3e6095355e18db6c8335cadcbc4afc56b35406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696870"
---
# <a name="tutorial-using-the-sink-writer-to-encode-video"></a><span data-ttu-id="50735-103">Tutorial: uso del escritor de receptores para codificar vídeo</span><span class="sxs-lookup"><span data-stu-id="50735-103">Tutorial: Using the Sink Writer to Encode Video</span></span>

<span data-ttu-id="50735-104">En este tutorial se usa el [escritor de receptores](sink-writer.md) para codificar un archivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="50735-104">This tutorial uses the [Sink Writer](sink-writer.md) to encode a video file.</span></span>

## <a name="define-the-video-format"></a><span data-ttu-id="50735-105">Definir el formato de vídeo</span><span class="sxs-lookup"><span data-stu-id="50735-105">Define the Video Format</span></span>

<span data-ttu-id="50735-106">Para simplificar, en este tutorial se usa un formato de vídeo fijo, definido por las constantes siguientes:</span><span class="sxs-lookup"><span data-stu-id="50735-106">For simplicity, this tutorial uses a fixed video format, defined by the following constants:</span></span>


```C++
// Format constants
const UINT32 VIDEO_WIDTH = 640;
const UINT32 VIDEO_HEIGHT = 480;
const UINT32 VIDEO_FPS = 30;
const UINT64 VIDEO_FRAME_DURATION = 10 * 1000 * 1000 / VIDEO_FPS;
const UINT32 VIDEO_BIT_RATE = 800000;
const GUID   VIDEO_ENCODING_FORMAT = MFVideoFormat_WMV3;
const GUID   VIDEO_INPUT_FORMAT = MFVideoFormat_RGB32;
const UINT32 VIDEO_PELS = VIDEO_WIDTH * VIDEO_HEIGHT;
const UINT32 VIDEO_FRAME_COUNT = 20 * VIDEO_FPS;
```



<span data-ttu-id="50735-107">Estas constantes especifican los siguientes parámetros del formato de vídeo:</span><span class="sxs-lookup"><span data-stu-id="50735-107">These constants specify the following parameters of the video format:</span></span>

-   <span data-ttu-id="50735-108">Tamaño de marco (ancho y alto)</span><span class="sxs-lookup"><span data-stu-id="50735-108">Frame size (width and height)</span></span>
-   <span data-ttu-id="50735-109">Fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="50735-109">Frames per second.</span></span>
-   <span data-ttu-id="50735-110">Velocidad de bits codificada.</span><span class="sxs-lookup"><span data-stu-id="50735-110">Encoded bit rate.</span></span>
-   <span data-ttu-id="50735-111">Formato de codificación, que es Windows Media Video 9 (**MFVideoFormat \_ WMV3**).</span><span class="sxs-lookup"><span data-stu-id="50735-111">Encoding format, which is Windows Media Video 9 (**MFVideoFormat\_WMV3**).</span></span>
-   <span data-ttu-id="50735-112">Formato de entrada, que es RGB de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="50735-112">Input format, which is 32-bit RGB.</span></span>
-   <span data-ttu-id="50735-113">Duración del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="50735-113">Duration of the output file.</span></span>

<span data-ttu-id="50735-114">El programa utiliza estas constantes para crear los tipos de medios que describen el formato.</span><span class="sxs-lookup"><span data-stu-id="50735-114">The program uses these constants to create the media types that describe the format.</span></span> <span data-ttu-id="50735-115">En una aplicación real, normalmente se admite un intervalo de perfiles de codificación.</span><span class="sxs-lookup"><span data-stu-id="50735-115">In a real application, you would typically support a range of encoding profiles.</span></span>

## <a name="create-an-uncompressed-video-frame"></a><span data-ttu-id="50735-116">Creación de un fotograma de vídeo sin comprimir</span><span class="sxs-lookup"><span data-stu-id="50735-116">Create an Uncompressed Video Frame</span></span>

<span data-ttu-id="50735-117">Además, para simplificar, en este tutorial se usa un fotograma de vídeo estático como entrada.</span><span class="sxs-lookup"><span data-stu-id="50735-117">Also for simplicity, this tutorial uses a static video frame as input.</span></span> <span data-ttu-id="50735-118">El fotograma de vídeo contiene un rectángulo verde sólido y se genera mediante programación.</span><span class="sxs-lookup"><span data-stu-id="50735-118">The video frame contains a solid green rectangle and is generated programmatically.</span></span> <span data-ttu-id="50735-119">El fotograma de vídeo se almacena en una variable global como una matriz de **DWORD** s:</span><span class="sxs-lookup"><span data-stu-id="50735-119">The video frame is stored in a global variable as an array of **DWORD** s:</span></span>


```C++
// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];
```



<span data-ttu-id="50735-120">En el código siguiente se establece cada píxel del marco en verde:</span><span class="sxs-lookup"><span data-stu-id="50735-120">The following code sets every pixel in the frame to green:</span></span>


```C++
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }
```



## <a name="initialize-the-sink-writer"></a><span data-ttu-id="50735-121">Inicializar el escritor del receptor</span><span class="sxs-lookup"><span data-stu-id="50735-121">Initialize the Sink Writer</span></span>

<span data-ttu-id="50735-122">Para inicializar el escritor del receptor, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="50735-122">To initialize the sink writer, perform the following steps.</span></span>

1.  <span data-ttu-id="50735-123">Llame a [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) para crear una nueva instancia del escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="50735-123">Call [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) to create a new instance of the sink writer.</span></span>
2.  <span data-ttu-id="50735-124">Cree un tipo de medio que describa el vídeo codificado.</span><span class="sxs-lookup"><span data-stu-id="50735-124">Create a media type that describes the encoded video.</span></span>
3.  <span data-ttu-id="50735-125">Pase este tipo de medio al método [**IMFSinkWriter:: AddStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream) .</span><span class="sxs-lookup"><span data-stu-id="50735-125">Pass this media type to the [**IMFSinkWriter::AddStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream) method.</span></span>
4.  <span data-ttu-id="50735-126">Cree un segundo tipo de medio que describa la entrada sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="50735-126">Create a second media type that describes the uncompressed input.</span></span>
5.  <span data-ttu-id="50735-127">Pase el tipo de medio sin comprimir al método [**IMFSinkWriter:: SetInputMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype) .</span><span class="sxs-lookup"><span data-stu-id="50735-127">Pass the uncompressed media type to the [**IMFSinkWriter::SetInputMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype) method.</span></span>
6.  <span data-ttu-id="50735-128">Llame al método [**IMFSinkWriter:: BeginWriting**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting) .</span><span class="sxs-lookup"><span data-stu-id="50735-128">Call the [**IMFSinkWriter::BeginWriting**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting) method.</span></span>
7.  <span data-ttu-id="50735-129">El escritor del receptor ya está listo para aceptar los ejemplos de entrada.</span><span class="sxs-lookup"><span data-stu-id="50735-129">The sink writer is now ready to accept input samples.</span></span>

<span data-ttu-id="50735-130">En el código siguiente se muestran estos pasos.</span><span class="sxs-lookup"><span data-stu-id="50735-130">The following code shows these steps.</span></span>


```C++
HRESULT InitializeSinkWriter(IMFSinkWriter **ppWriter, DWORD *pStreamIndex)
{
    *ppWriter = NULL;
    *pStreamIndex = NULL;

    IMFSinkWriter   *pSinkWriter = NULL;
    IMFMediaType    *pMediaTypeOut = NULL;   
    IMFMediaType    *pMediaTypeIn = NULL;   
    DWORD           streamIndex;     

    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);

    // Set the output media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeOut);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_SUBTYPE, VIDEO_ENCODING_FORMAT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_AVG_BITRATE, VIDEO_BIT_RATE);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeOut, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->AddStream(pMediaTypeOut, &streamIndex);   
    }

    // Set the input media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeIn);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_SUBTYPE, VIDEO_INPUT_FORMAT);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeIn, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->SetInputMediaType(streamIndex, pMediaTypeIn, NULL);   
    }

    // Tell the sink writer to start accepting data.
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->BeginWriting();
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppWriter = pSinkWriter;
        (*ppWriter)->AddRef();
        *pStreamIndex = streamIndex;
    }

    SafeRelease(&pSinkWriter);
    SafeRelease(&pMediaTypeOut);
    SafeRelease(&pMediaTypeIn);
    return hr;
}
```



<span data-ttu-id="50735-131">La mayoría de los pasos del ejemplo de código anterior establecen los atributos de tipo de medio para los dos tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="50735-131">Most of the steps in previous code example are setting the media type attributes for the two media types.</span></span> <span data-ttu-id="50735-132">Los detalles de los tipos de medios dependerán del contenido de origen y el perfil de codificación deseado.</span><span class="sxs-lookup"><span data-stu-id="50735-132">The details of the media types will depend on your source content and the desired encoding profile.</span></span>

## <a name="send-video-frames-to-the-sink-writer"></a><span data-ttu-id="50735-133">Enviar fotogramas de vídeo al escritor de receptor</span><span class="sxs-lookup"><span data-stu-id="50735-133">Send Video Frames to the Sink Writer</span></span>

<span data-ttu-id="50735-134">Para enviar un fotograma de vídeo al escritor del receptor, llame al método [**IMFSinkWriter:: WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) .</span><span class="sxs-lookup"><span data-stu-id="50735-134">To send a video frame to the sink writer, call the [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) method.</span></span> <span data-ttu-id="50735-135">El método **WriteSample** toma un puntero a la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , que representa un objeto de *ejemplo multimedia* .</span><span class="sxs-lookup"><span data-stu-id="50735-135">The **WriteSample** method takes a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, which represents a *media sample* object.</span></span> <span data-ttu-id="50735-136">El ejemplo multimedia contiene un objeto de *búfer multimedia* que, a su vez, contiene un puntero al fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="50735-136">The media sample contains a *media buffer* object, which in turn contains a pointer to the video frame.</span></span> <span data-ttu-id="50735-137">Para obtener más información acerca de los ejemplos de medios y el búfer, vea los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="50735-137">For more information about media samples and buffer, see the following topics.</span></span>

-   [<span data-ttu-id="50735-138">Ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="50735-138">Media Samples</span></span>](media-samples.md)
-   [<span data-ttu-id="50735-139">Búferes multimedia</span><span class="sxs-lookup"><span data-stu-id="50735-139">Media Buffers</span></span>](media-buffers.md)

<span data-ttu-id="50735-140">En función de la aplicación, puede obtener los ejemplos de medios del [lector de origen](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="50735-140">Depending on your application, you might get the media samples from the [Source Reader](source-reader.md).</span></span> <span data-ttu-id="50735-141">Como alternativa, puede crear los ejemplos de medios y manipular directamente los datos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="50735-141">Alternatively, you can create the media samples and directly manipulate the data in the buffer.</span></span> <span data-ttu-id="50735-142">En el código siguiente se muestra el segundo enfoque.</span><span class="sxs-lookup"><span data-stu-id="50735-142">The following code shows the second approach.</span></span> <span data-ttu-id="50735-143">Crea un búfer de memoria y escribe un único fotograma de vídeo en el búfer.</span><span class="sxs-lookup"><span data-stu-id="50735-143">It creates a memory buffer and writes a single video frame to the buffer.</span></span> <span data-ttu-id="50735-144">A continuación, agrega ese búfer a un ejemplo multimedia y envía el ejemplo multimedia al escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="50735-144">Then it adds that buffer to a media sample, and sends the media sample to the sink writer.</span></span>


```C++
HRESULT WriteFrame(
    IMFSinkWriter *pWriter, 
    DWORD streamIndex, 
    const LONGLONG& rtStart        // Time stamp.
    )
{
    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    const LONG cbWidth = 4 * VIDEO_WIDTH;
    const DWORD cbBuffer = cbWidth * VIDEO_HEIGHT;

    BYTE *pData = NULL;

    // Create a new memory buffer.
    HRESULT hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);

    // Lock the buffer and copy the video frame to the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFCopyImage(
            pData,                      // Destination buffer.
            cbWidth,                    // Destination stride.
            (BYTE*)videoFrameBuffer,    // First row in source image.
            cbWidth,                    // Source stride.
            cbWidth,                    // Image width in bytes.
            VIDEO_HEIGHT                // Image height in pixels.
            );
    }
    if (pBuffer)
    {
        pBuffer->Unlock();
    }

    // Set the data length of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbBuffer);
    }

    // Create a media sample and add the buffer to the sample.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSample(&pSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    // Set the time stamp and the duration.
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleTime(rtStart);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleDuration(VIDEO_FRAME_DURATION);
    }

    // Send the sample to the Sink Writer.
    if (SUCCEEDED(hr))
    {
        hr = pWriter->WriteSample(streamIndex, pSample);
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



<span data-ttu-id="50735-145">Este código realiza los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="50735-145">This code performs the following steps.</span></span>

1.  <span data-ttu-id="50735-146">Llame a [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) para crear un objeto de búfer de multimedia.</span><span class="sxs-lookup"><span data-stu-id="50735-146">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer object.</span></span> <span data-ttu-id="50735-147">Esta función asigna la memoria para el búfer.</span><span class="sxs-lookup"><span data-stu-id="50735-147">This function allocates the memory for the buffer.</span></span>
2.  <span data-ttu-id="50735-148">Llame a [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para bloquear el búfer y obtener un puntero a la memoria.</span><span class="sxs-lookup"><span data-stu-id="50735-148">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to lock the buffer and get a pointer to the memory.</span></span>
3.  <span data-ttu-id="50735-149">Llame a [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) para copiar el fotograma de vídeo en el búfer.</span><span class="sxs-lookup"><span data-stu-id="50735-149">Call [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) to copy the video frame into the buffer.</span></span>
    > [!Note]  
    > <span data-ttu-id="50735-150">En este ejemplo concreto, el uso de **memcpy** también funcionaría.</span><span class="sxs-lookup"><span data-stu-id="50735-150">In this particular example, using **memcpy** would work just as well.</span></span> <span data-ttu-id="50735-151">Sin embargo, la función [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) controla correctamente el caso en el que el paso de la imagen de origen no coincide con el búfer de destino.</span><span class="sxs-lookup"><span data-stu-id="50735-151">However, the [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) function correctly handles the case where the stride of the source image does not match the target buffer.</span></span> <span data-ttu-id="50735-152">Para obtener más información, consulte [STRIDE](image-stride.md)de la imagen.</span><span class="sxs-lookup"><span data-stu-id="50735-152">For more information, see [Image Stride](image-stride.md).</span></span>

     

4.  <span data-ttu-id="50735-153">Llame a [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) para desbloquear el búfer.</span><span class="sxs-lookup"><span data-stu-id="50735-153">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>
5.  <span data-ttu-id="50735-154">Llame a [**IMFMediaBuffer:: SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) para actualizar la longitud de los datos válidos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="50735-154">Call [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) to update the length of the valid data in the buffer.</span></span> <span data-ttu-id="50735-155">(De lo contrario, el valor predeterminado es cero).</span><span class="sxs-lookup"><span data-stu-id="50735-155">(Otherwise, this value defaults to zero.)</span></span>
6.  <span data-ttu-id="50735-156">Llame a [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) para crear un objeto de ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="50735-156">Call [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) to create a media sample object.</span></span>
7.  <span data-ttu-id="50735-157">Llame a [**IMFSample:: AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) para agregar el búfer multimedia al ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="50735-157">Call [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) to add the media buffer to the media sample.</span></span>
8.  <span data-ttu-id="50735-158">Llame a [**IMFSample:: SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) para establecer la marca de tiempo para el fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="50735-158">Call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) to set the time stamp for the video frame.</span></span>
9.  <span data-ttu-id="50735-159">Llame a [**IMFSample:: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) para establecer la duración del fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="50735-159">Call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) to set the duration of the video frame.</span></span>
10. <span data-ttu-id="50735-160">Llame a [**IMFSinkWriter:: WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) para enviar el ejemplo multimedia al escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="50735-160">Call [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) to send the media sample to the sink writer.</span></span>

## <a name="write-the-main-function"></a><span data-ttu-id="50735-161">Escribir la función Main</span><span class="sxs-lookup"><span data-stu-id="50735-161">Write the main Function</span></span>

<span data-ttu-id="50735-162">Dentro de la `main` función, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="50735-162">Inside the `main` function, perform the following steps.</span></span>

1.  <span data-ttu-id="50735-163">Llame a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar la biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="50735-163">Call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="50735-164">Llame a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) para inicializar Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="50735-164">Call [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize Microsoft Media Foundation.</span></span>
3.  <span data-ttu-id="50735-165">Cree el escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="50735-165">Create the sink writer.</span></span>
4.  <span data-ttu-id="50735-166">Enviar fotogramas de vídeo al escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="50735-166">Send video frames to the sink writer.</span></span>
5.  <span data-ttu-id="50735-167">Llame a [**IMFSinkWriter:: Finalize**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize) para finalizar el archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="50735-167">Call [**IMFSinkWriter::Finalize**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize) to finalize the output file.</span></span>
6.  <span data-ttu-id="50735-168">Libera el puntero al escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="50735-168">Release the pointer to the sink writer.</span></span>
7.  <span data-ttu-id="50735-169">Llame a [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="50735-169">Call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span>
8.  <span data-ttu-id="50735-170">Llame a [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="50735-170">Call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>


```C++
void main()
{
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            IMFSinkWriter *pSinkWriter = NULL;
            DWORD stream;

            hr = InitializeSinkWriter(&pSinkWriter, &stream);
            if (SUCCEEDED(hr))
            {
                // Send frames to the sink writer.
                LONGLONG rtStart = 0;


                for (DWORD i = 0; i < VIDEO_FRAME_COUNT; ++i)
                {
                    hr = WriteFrame(pSinkWriter, stream, rtStart);
                    if (FAILED(hr))
                    {
                        break;
                    }
                    rtStart += VIDEO_FRAME_DURATION;
                }
            }
            if (SUCCEEDED(hr))
            {
                hr = pSinkWriter->Finalize();
            }
            SafeRelease(&pSinkWriter);
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="example-code"></a><span data-ttu-id="50735-171">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="50735-171">Example Code</span></span>

<span data-ttu-id="50735-172">En el código siguiente se muestra el programa completo.</span><span class="sxs-lookup"><span data-stu-id="50735-172">The following code shows the complete program.</span></span>


```C++
#include <Windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <Mfreadwrite.h>
#include <mferror.h>

#pragma comment(lib, "mfreadwrite")
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mfuuid")

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

// Format constants
const UINT32 VIDEO_WIDTH = 640;
const UINT32 VIDEO_HEIGHT = 480;
const UINT32 VIDEO_FPS = 30;
const UINT64 VIDEO_FRAME_DURATION = 10 * 1000 * 1000 / VIDEO_FPS;
const UINT32 VIDEO_BIT_RATE = 800000;
const GUID   VIDEO_ENCODING_FORMAT = MFVideoFormat_WMV3;
const GUID   VIDEO_INPUT_FORMAT = MFVideoFormat_RGB32;
const UINT32 VIDEO_PELS = VIDEO_WIDTH * VIDEO_HEIGHT;
const UINT32 VIDEO_FRAME_COUNT = 20 * VIDEO_FPS;

// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];

HRESULT InitializeSinkWriter(IMFSinkWriter **ppWriter, DWORD *pStreamIndex)
{
    *ppWriter = NULL;
    *pStreamIndex = NULL;

    IMFSinkWriter   *pSinkWriter = NULL;
    IMFMediaType    *pMediaTypeOut = NULL;   
    IMFMediaType    *pMediaTypeIn = NULL;   
    DWORD           streamIndex;     

    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);

    // Set the output media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeOut);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_SUBTYPE, VIDEO_ENCODING_FORMAT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_AVG_BITRATE, VIDEO_BIT_RATE);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeOut, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->AddStream(pMediaTypeOut, &streamIndex);   
    }

    // Set the input media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeIn);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_SUBTYPE, VIDEO_INPUT_FORMAT);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeIn, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->SetInputMediaType(streamIndex, pMediaTypeIn, NULL);   
    }

    // Tell the sink writer to start accepting data.
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->BeginWriting();
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppWriter = pSinkWriter;
        (*ppWriter)->AddRef();
        *pStreamIndex = streamIndex;
    }

    SafeRelease(&pSinkWriter);
    SafeRelease(&pMediaTypeOut);
    SafeRelease(&pMediaTypeIn);
    return hr;
}

HRESULT WriteFrame(
    IMFSinkWriter *pWriter, 
    DWORD streamIndex, 
    const LONGLONG& rtStart        // Time stamp.
    )
{
    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    const LONG cbWidth = 4 * VIDEO_WIDTH;
    const DWORD cbBuffer = cbWidth * VIDEO_HEIGHT;

    BYTE *pData = NULL;

    // Create a new memory buffer.
    HRESULT hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);

    // Lock the buffer and copy the video frame to the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFCopyImage(
            pData,                      // Destination buffer.
            cbWidth,                    // Destination stride.
            (BYTE*)videoFrameBuffer,    // First row in source image.
            cbWidth,                    // Source stride.
            cbWidth,                    // Image width in bytes.
            VIDEO_HEIGHT                // Image height in pixels.
            );
    }
    if (pBuffer)
    {
        pBuffer->Unlock();
    }

    // Set the data length of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbBuffer);
    }

    // Create a media sample and add the buffer to the sample.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSample(&pSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    // Set the time stamp and the duration.
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleTime(rtStart);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleDuration(VIDEO_FRAME_DURATION);
    }

    // Send the sample to the Sink Writer.
    if (SUCCEEDED(hr))
    {
        hr = pWriter->WriteSample(streamIndex, pSample);
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}

void main()
{
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            IMFSinkWriter *pSinkWriter = NULL;
            DWORD stream;

            hr = InitializeSinkWriter(&pSinkWriter, &stream);
            if (SUCCEEDED(hr))
            {
                // Send frames to the sink writer.
                LONGLONG rtStart = 0;


                for (DWORD i = 0; i < VIDEO_FRAME_COUNT; ++i)
                {
                    hr = WriteFrame(pSinkWriter, stream, rtStart);
                    if (FAILED(hr))
                    {
                        break;
                    }
                    rtStart += VIDEO_FRAME_DURATION;
                }
            }
            if (SUCCEEDED(hr))
            {
                hr = pSinkWriter->Finalize();
            }
            SafeRelease(&pSinkWriter);
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="50735-173">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50735-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50735-174">Escritor de receptor</span><span class="sxs-lookup"><span data-stu-id="50735-174">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 
