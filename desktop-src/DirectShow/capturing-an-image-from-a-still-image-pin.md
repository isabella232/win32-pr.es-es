---
description: Captura de una imagen a partir de un pin de imagen fija
ms.assetid: cbcb4d6d-dc85-4ae2-b0a8-110f15092733
title: Captura de una imagen a partir de un pin de imagen fija
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab750fb6b847bc39d28c8906df8dcb982278f7a4447bfc3d79631ee58eb574e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158667"
---
# <a name="capturing-an-image-from-a-still-image-pin"></a>Captura de una imagen a partir de un pin de imagen fija

Algunas cámaras pueden generar una imagen fija independiente de la secuencia de captura y, a menudo, la imagen fija es de mayor calidad que las imágenes producidas por la secuencia de captura. La cámara puede tener un botón que actúa como un desencadenador de hardware o puede admitir la activación de software. Una cámara que admita imágenes fijas expondrá un pin de imagen fija, que es pin category PIN \_ CATEGORY \_ STILL.

La manera recomendada de obtener imágenes fijas del dispositivo es usar las API Windows Image Acquisition (WIA). Para más información, consulte "adquisición Windows imagen" en la documentación de Platform SDK. Sin embargo, también puede usar DirectShow para capturar una imagen.

Para desencadenar el pin, use el [**método IAMVideoControl::SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) cuando se ejecute el gráfico, como se muestra a continuación:


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



Consulte el filtro de captura [**para IAMVideoControl.**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol) Si se admite la interfaz, obtenga un puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del todavía anclado mediante una llamada al método [**ICaptureGraphBuilder2::FindPin,**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) como se muestra en el ejemplo anterior. A [**continuación, llame a IAMVideoControl::SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) con el **puntero IPin** y la marca VideoControlFlag \_ Trigger.

> [!Note]  
> Dependiendo de la cámara, es posible que tenga que representar el pin de captura (PIN CATEGORY CAPTURE) antes de que se conecte \_ \_ el pin.

 

### <a name="example-using-the-sample-grabber-filter"></a>Ejemplo: Uso del filtro de captura de ejemplo

Una manera de capturar la imagen es con el filtro [**Sample Grabber**](sample-grabber-filter.md) . Sample Grabber usa una función de devolución de llamada definida por la aplicación para procesar la imagen. Para obtener más información sobre el filtro Sample Grabber, vea [Using the Sample Grabber](using-the-sample-grabber.md).

En el ejemplo siguiente se da por supuesto que el pin sigue entregando una imagen RGB sin comprimir. En primer lugar, defina una clase que implemente la interfaz de devolución de llamada de Sample Grabber, [**ISampleGrabberCB**](isamplegrabbercb.md):


```C++
// Class to hold the callback function for the Sample Grabber filter.
class SampleGrabberCallback : public ISampleGrabberCB
{
    // Implementation is described later.
}

// Global instance of the class.
SampleGrabberCallback g_StillCapCB;
```



La implementación de la clase se describe en breve.

A continuación, conecte el pin todavía al sample grabber y conecte sample grabber al [**filtro Representador**](null-renderer-filter.md) nulo. El representador null simplemente descarta los ejemplos de medios que recibe; el trabajo real se realizará dentro de la devolución de llamada. (La única razón para que el representador null conecte el pin de salida de Sample Grabber a algo). Llame [**a CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear los filtros Sample Grabber y Null Renderer y llame a [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para agregar ambos filtros al gráfico:


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



Puede usar el método [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar los tres filtros en una llamada de método, desde el pin hasta sample grabber y desde sample grabber al representador null:


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_STILL, // Connect this pin ...
    &MEDIATYPE_Video,    // with this media type ...
    pCap,                // on this filter ...
    pSG_Filter,          // to the Sample Grabber ...
    pNull);              // ... and finally to the Null Renderer.
```



Ahora use la [**interfaz ISampleGrabber para**](isamplegrabber.md) configurar Sample Grabber para almacenar en búfer los ejemplos:


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



Establezca la interfaz de devolución de llamada con un puntero al objeto de devolución de llamada:


```C++
hr = pSG->SetCallback(&g_StillCapCB, 0); // 0 = Use the SampleCB callback method.
```



Obtenga el tipo de medio que el pin todavía usa para conectarse con sample grabber:


```C++
// Store the media type for later use.
AM_MEDIA_TYPE g_StillMediaType;

hr = pSG->GetConnectedMediaType(&g_StillMediaType);
pSG->Release();
```



Este tipo de medio contendrá la [**estructura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) que define el formato de la imagen fija. Liberar el tipo de medio antes de que se cierre la aplicación:


```C++
// On exit, remember to release the media type.
FreeMediaType(g_StillMediaType);
```



A continuación se muestra un ejemplo de la clase de devolución de llamada. Tenga en cuenta que la clase implementa **IUnknown**, que hereda a través de la [**interfaz ISampleGrabber,**](isamplegrabber.md) pero no mantiene un recuento de referencias. Esto es seguro porque la aplicación crea el objeto en la pila y el objeto permanece en el ámbito a lo largo de la duración del gráfico de filtros.

Todo el trabajo se produce en el [**método BufferCB,**](isamplegrabbercb-buffercb.md) al que llama sample Grabber cada vez que obtiene un nuevo ejemplo. En el ejemplo siguiente, el método escribe el mapa de bits en un archivo:


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas de captura de vídeo](video-capture-tasks.md)
</dt> </dl>

 

 
