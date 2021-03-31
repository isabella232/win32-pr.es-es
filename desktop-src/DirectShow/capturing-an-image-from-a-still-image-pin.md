---
description: Captura de una imagen a partir de un PIN de imagen fija
ms.assetid: cbcb4d6d-dc85-4ae2-b0a8-110f15092733
title: Captura de una imagen a partir de un PIN de imagen fija
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3510f318f3107dd698dc753704d6c09d70ddd308
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805714"
---
# <a name="capturing-an-image-from-a-still-image-pin"></a><span data-ttu-id="022dd-103">Captura de una imagen a partir de un PIN de imagen fija</span><span class="sxs-lookup"><span data-stu-id="022dd-103">Capturing an Image From a Still Image Pin</span></span>

<span data-ttu-id="022dd-104">Algunas cámaras pueden producir una imagen fija independiente de la secuencia de captura y, a menudo, la imagen sigue siendo de mayor calidad que las imágenes generadas por la secuencia de captura.</span><span class="sxs-lookup"><span data-stu-id="022dd-104">Some cameras can produce a still image separate from the capture stream, and often the still image is of higher quality than the images produced by the capture stream.</span></span> <span data-ttu-id="022dd-105">Es posible que la cámara tenga un botón que actúe como un desencadenador de hardware o que admita la activación de software.</span><span class="sxs-lookup"><span data-stu-id="022dd-105">The camera may have a button that acts as a hardware trigger, or it may support software triggering.</span></span> <span data-ttu-id="022dd-106">Una cámara que admita imágenes fijas expondrá un PIN de imagen fija, que sigue siendo la categoría PIN de la categoría PIN \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="022dd-106">A camera that supports still images will expose a still image pin, which is pin category PIN\_CATEGORY\_STILL.</span></span>

<span data-ttu-id="022dd-107">La manera recomendada de obtener imágenes estáticas del dispositivo es usar las API de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="022dd-107">The recommended way to get still images from the device is to use the Windows Image Acquisition (WIA) APIs.</span></span> <span data-ttu-id="022dd-108">Para obtener más información, vea "adquisición de imagen de Windows" en la documentación de Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="022dd-108">For more information, see "Windows Image Acquisition" in the Platform SDK documentation.</span></span> <span data-ttu-id="022dd-109">Sin embargo, también puede usar DirectShow para capturar una imagen.</span><span class="sxs-lookup"><span data-stu-id="022dd-109">However, you can also use DirectShow to capture an image.</span></span>

<span data-ttu-id="022dd-110">Para desencadenar el PIN fijo, use el método [**IAMVideoControl:: SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) cuando el gráfico se esté ejecutando, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="022dd-110">To trigger the still pin, use the [**IAMVideoControl::SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) method when the graph is running, as follows:</span></span>


```C++
IAMVideoControl *pAMVidControl = NULL;

hr = pControl->Run(); // Run the graph.
if (FAILED(hr))
{
    // Handle error.
}

hr = pCap->QueryInterface(IID_IAMVideoControl, (void**)&pAMVidControl);

if (SUCCEEDED(hr))
{
    // Find the still pin.
    IPin *pPin = NULL;

    // pBuild is an ICaptureGraphBuilder2 pointer.

    hr = pBuild->FindPin(
        pCap,                  // Filter.
        PINDIR_OUTPUT,         // Look for an output pin.
        &PIN_CATEGORY_STILL,   // Pin category.
        NULL,                  // Media type (don't care).
        FALSE,                 // Pin must be unconnected.
        0,                     // Get the 0'th pin.
        &pPin                  // Receives a pointer to thepin.
        );

    if (SUCCEEDED(hr))
    {
        hr = pAMVidControl->SetMode(pPin, VideoControlFlag_Trigger);
        pPin->Release();
    }
    pAMVidControl->Release();
}
```



<span data-ttu-id="022dd-111">Consulte el filtro de captura para [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol).</span><span class="sxs-lookup"><span data-stu-id="022dd-111">Query the capture filter for [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol).</span></span> <span data-ttu-id="022dd-112">Si se admite la interfaz, obtenga un puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN fijo llamando al método [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) , como se muestra en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="022dd-112">If the interface is supported, get a pointer to the still pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface by calling the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method, as shown in the previous example.</span></span> <span data-ttu-id="022dd-113">Después, llame a [**IAMVideoControl:: SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) con el puntero **IPin** y la \_ marca de desencadenador VideoControlFlag.</span><span class="sxs-lookup"><span data-stu-id="022dd-113">Then call [**IAMVideoControl::SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) with the **IPin** pointer and the VideoControlFlag\_Trigger flag.</span></span>

> [!Note]  
> <span data-ttu-id="022dd-114">En función de la cámara, es posible que deba representar el PIN de captura ( \_ captura de categoría de PIN \_ ) antes de que se conecte el PIN fijo.</span><span class="sxs-lookup"><span data-stu-id="022dd-114">Depending on the camera, you might need to render the capture pin (PIN\_CATEGORY\_CAPTURE) before the still pin will connect.</span></span>

 

### <a name="example-using-the-sample-grabber-filter"></a><span data-ttu-id="022dd-115">Ejemplo: uso del filtro de enganche de ejemplo</span><span class="sxs-lookup"><span data-stu-id="022dd-115">Example: Using the Sample Grabber Filter</span></span>

<span data-ttu-id="022dd-116">Una manera de capturar la imagen es con el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="022dd-116">One way to capture the image is with the [**Sample Grabber**](sample-grabber-filter.md) filter.</span></span> <span data-ttu-id="022dd-117">El enganche de ejemplo utiliza una función de devolución de llamada definida por la aplicación para procesar la imagen.</span><span class="sxs-lookup"><span data-stu-id="022dd-117">The Sample Grabber uses an application-defined callback function to process the image.</span></span> <span data-ttu-id="022dd-118">Para obtener más información sobre el filtro de enganche de ejemplo, vea [usar el enganche de ejemplo](using-the-sample-grabber.md).</span><span class="sxs-lookup"><span data-stu-id="022dd-118">For more information about the Sample Grabber filter, see [Using the Sample Grabber](using-the-sample-grabber.md).</span></span>

<span data-ttu-id="022dd-119">En el siguiente ejemplo se da por supuesto que el PIN sigue entrega una imagen RGB sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="022dd-119">The following example assumes that the still pin delivers an uncompressed RGB image.</span></span> <span data-ttu-id="022dd-120">En primer lugar, defina una clase que implemente la interfaz de devolución de llamada del enganche de ejemplo, [**ISampleGrabberCB**](isamplegrabbercb.md):</span><span class="sxs-lookup"><span data-stu-id="022dd-120">First, define a class that will implement the Sample Grabber's callback interface, [**ISampleGrabberCB**](isamplegrabbercb.md):</span></span>


```C++
// Class to hold the callback function for the Sample Grabber filter.
class SampleGrabberCallback : public ISampleGrabberCB
{
    // Implementation is described later.
}

// Global instance of the class.
SampleGrabberCallback g_StillCapCB;
```



<span data-ttu-id="022dd-121">La implementación de la clase se describe en breve.</span><span class="sxs-lookup"><span data-stu-id="022dd-121">The implementation of the class is described shortly.</span></span>

<span data-ttu-id="022dd-122">A continuación, conecte el anclado todavía al enganche de ejemplo y conecte el captador de ejemplo al filtro de [**representador nulo**](null-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="022dd-122">Next, connect the still pin to the Sample Grabber, and connect the Sample Grabber to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span> <span data-ttu-id="022dd-123">El representador null simplemente descarta los ejemplos multimedia que recibe; el trabajo real se realizará dentro de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="022dd-123">The Null Renderer simply discards media samples that it receives; the actual work will be done within the callback.</span></span> <span data-ttu-id="022dd-124">(La única razón para el representador nulo es conectar el PIN de salida del enganche de ejemplo a algo). Llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el enganche de ejemplo y los filtros de representador nulos, y llame a [**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para agregar ambos filtros al gráfico:</span><span class="sxs-lookup"><span data-stu-id="022dd-124">(The only reason for the Null Renderer is to connect the Sample Grabber's output pin to something.) Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Sample Grabber and Null Renderer filters, and call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add both filters to the graph:</span></span>


```C++
// Add the Sample Grabber filter to the graph.
IBaseFilter *pSG_Filter;
hr = CoCreateInstance(
    CLSID_SampleGrabber, 
    NULL, 
    CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, 
    (void**)&pSG_Filter
    );

hr = pGraph->AddFilter(pSG_Filter, L"SampleGrab");

// Add the Null Renderer filter to the graph.
IBaseFilter *pNull;

hr = CoCreateInstance(
    CLSID_NullRenderer, 
    NULL, 
    CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, 
    (void**)&pNull
    );

hr = pGraph->AddFilter(pNull, L"NullRender");
```



<span data-ttu-id="022dd-125">Puede usar el método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar los tres filtros en una llamada al método, desde el PIN fijo hasta el enganche de ejemplo y desde el enganche de ejemplo al representador NULL:</span><span class="sxs-lookup"><span data-stu-id="022dd-125">You can use the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to connect all three filters in one method call, going from the still pin to the Sample Grabber, and from the Sample Grabber to the Null Renderer:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_STILL, // Connect this pin ...
    &MEDIATYPE_Video,    // with this media type ...
    pCap,                // on this filter ...
    pSG_Filter,          // to the Sample Grabber ...
    pNull);              // ... and finally to the Null Renderer.
```



<span data-ttu-id="022dd-126">Ahora use la interfaz [**ISampleGrabber**](isamplegrabber.md) para configurar el captador de ejemplo de modo que almacene en búfer ejemplos:</span><span class="sxs-lookup"><span data-stu-id="022dd-126">Now use the [**ISampleGrabber**](isamplegrabber.md) interface to configure the Sample Grabber so that it buffers samples:</span></span>


```C++
// Configure the Sample Grabber.
ISampleGrabber *pSG = NULL;

hr = pSG_Filter->QueryInterface(IID_ISampleGrabber, (void**)&pSG);
if (SUCCEEDED(hr))
{
    hr = pSG->SetOneShot(FALSE);
    hr = pSG->SetBufferSamples(TRUE);

    ...
```



<span data-ttu-id="022dd-127">Establezca la interfaz de devolución de llamada con un puntero al objeto de devolución de llamada:</span><span class="sxs-lookup"><span data-stu-id="022dd-127">Set the callback interface with a pointer to your callback object:</span></span>


```C++
hr = pSG->SetCallback(&g_StillCapCB, 0); // 0 = Use the SampleCB callback method.
```



<span data-ttu-id="022dd-128">Obtiene el tipo de medio que el PIN sigue usando para conectarse con el enganche de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="022dd-128">Get the media type that the still pin used to connect with the Sample Grabber:</span></span>


```C++
// Store the media type for later use.
AM_MEDIA_TYPE g_StillMediaType;

hr = pSG->GetConnectedMediaType(&g_StillMediaType);
pSG->Release();
```



<span data-ttu-id="022dd-129">Este tipo de medio contendrá la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) que define el formato de la imagen fija.</span><span class="sxs-lookup"><span data-stu-id="022dd-129">This media type will contain the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure that defines the format of the still image.</span></span> <span data-ttu-id="022dd-130">Libere el tipo de medio antes de salir de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="022dd-130">Free the media type before the application exits:</span></span>


```C++
// On exit, remember to release the media type.
FreeMediaType(g_StillMediaType);
```



<span data-ttu-id="022dd-131">A continuación se muestra un ejemplo de la clase de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="022dd-131">What follows is an example of the callback class.</span></span> <span data-ttu-id="022dd-132">Tenga en cuenta que la clase implementa **IUnknown**, que hereda a través de la interfaz [**ISampleGrabber**](isamplegrabber.md) , pero no mantiene un recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="022dd-132">Note that the class implements **IUnknown**, which it inherits through the [**ISampleGrabber**](isamplegrabber.md) interface, but it does not keep a reference count.</span></span> <span data-ttu-id="022dd-133">Esto es seguro porque la aplicación crea el objeto en la pila y el objeto permanece en el ámbito a lo largo de la duración del gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="022dd-133">This is safe because the application creates the object on the stack, and the object remains in scope throughout the lifetime of the filter graph.</span></span>

<span data-ttu-id="022dd-134">Todo el trabajo se produce en el método [**BufferCB**](isamplegrabbercb-buffercb.md) , al que llama el enganche de ejemplo cada vez que obtiene un nuevo ejemplo.</span><span class="sxs-lookup"><span data-stu-id="022dd-134">All of the work happens in the [**BufferCB**](isamplegrabbercb-buffercb.md) method, which is called by the Sample Grabber whenever it gets a new sample.</span></span> <span data-ttu-id="022dd-135">En el ejemplo siguiente, el método escribe el mapa de bits en un archivo:</span><span class="sxs-lookup"><span data-stu-id="022dd-135">In the following example, the method writes the bitmap to a file:</span></span>


```C++
class SampleGrabberCallback : public ISampleGrabberCB
{
public:
    // Fake referance counting.
    STDMETHODIMP_(ULONG) AddRef() { return 1; }
    STDMETHODIMP_(ULONG) Release() { return 2; }

    STDMETHODIMP QueryInterface(REFIID riid, void **ppvObject)
    {
        if (NULL == ppvObject) return E_POINTER;
        if (riid == __uuidof(IUnknown))
        {
            *ppvObject = static_cast<IUnknown*>(this);
             return S_OK;
        }
        if (riid == __uuidof(ISampleGrabberCB))
        {
            *ppvObject = static_cast<ISampleGrabberCB*>(this);
             return S_OK;
        }
        return E_NOTIMPL;
    }

    STDMETHODIMP SampleCB(double Time, IMediaSample *pSample)
    {
        return E_NOTIMPL;
    }

    STDMETHODIMP BufferCB(double Time, BYTE *pBuffer, long BufferLen)
    {
        if ((g_StillMediaType.majortype != MEDIATYPE_Video) ||
            (g_StillMediaType.formattype != FORMAT_VideoInfo) ||
            (g_StillMediaType.cbFormat < sizeof(VIDEOINFOHEADER)) ||
            (g_StillMediaType.pbFormat == NULL))
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
        HANDLE hf = CreateFile("C:\\Example.bmp", GENERIC_WRITE, 
        FILE_SHARE_WRITE, NULL, CREATE_ALWAYS, 0, NULL);
        if (hf == INVALID_HANDLE_VALUE)
        {
            return E_FAIL;
        }
        long cbBitmapInfoSize = g_StillMediaType.cbFormat - SIZE_PREHEADER;
        VIDEOINFOHEADER *pVideoHeader =
           (VIDEOINFOHEADER*)g_StillMediaType.pbFormat;

        BITMAPFILEHEADER bfh;
        ZeroMemory(&bfh, sizeof(bfh));
        bfh.bfType = 'MB';  // Little-endian for "BM".
        bfh.bfSize = sizeof( bfh ) + BufferLen + cbBitmapInfoSize;
        bfh.bfOffBits = sizeof( BITMAPFILEHEADER ) + cbBitmapInfoSize;
        
        // Write the file header.
        DWORD dwWritten = 0;
        WriteFile( hf, &bfh, sizeof( bfh ), &dwWritten, NULL );
        WriteFile(hf, HEADER(pVideoHeader), cbBitmapInfoSize, &dwWritten, NULL);        
        WriteFile( hf, pBuffer, BufferLen, &dwWritten, NULL );
        CloseHandle( hf );
        return S_OK;

    }
};
```



## <a name="related-topics"></a><span data-ttu-id="022dd-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="022dd-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="022dd-137">Tareas de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="022dd-137">Video Capture Tasks</span></span>](video-capture-tasks.md)
</dt> </dl>

 

 
