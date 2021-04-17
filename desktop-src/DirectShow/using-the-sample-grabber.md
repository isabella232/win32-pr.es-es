---
description: El filtro de enganche de ejemplo es un filtro de transformación que se puede usar para obtener ejemplos de medios de un flujo a medida que pasan por el gráfico de filtro.
ms.assetid: ec0e367e-9ef9-4de6-9132-b462c233bc98
title: Usar el enganche de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4886c796691e83e02b58ddea129d60d5004c9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678080"
---
# <a name="using-the-sample-grabber"></a>Usar el enganche de ejemplo

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

El filtro de [**enganche de ejemplo**](sample-grabber-filter.md) es un filtro de transformación que se puede usar para obtener ejemplos de medios de un flujo a medida que pasan por el gráfico de filtro.

Si simplemente desea captar un mapa de bits de un archivo de vídeo, es más fácil usar el objeto de [detector de medios (MediaDet)](media-detector--mediadet.md) . Consulte [captación de un fotograma de póster](grabbing-a-poster-frame.md) para obtener más información. Sin embargo, el captador de ejemplo es más flexible porque funciona con casi cualquier tipo de medio (vea [**ISampleGrabber:: SetMediaType**](isamplegrabber-setmediatype.md) para las pocas excepciones) y ofrece más control a la aplicación.

-   [Crear el administrador de gráficos de filtro](#create-the-filter-graph-manager)
-   [Agregar el captador de ejemplo al gráfico de filtros](#add-the-sample-grabber-to-the-filter-graph)
-   [Establecer el tipo de medio](#set-the-media-type)
-   [Crear el gráfico de filtro](#build-the-filter-graph)
-   [Ejecutar el gráfico](#run-the-graph)
-   [Captar el ejemplo](#grab-the-sample)
-   [Código de ejemplo](#example-code)
-   [Temas relacionados](#related-topics)

## <a name="create-the-filter-graph-manager"></a>Crear el administrador de gráficos de filtro

Para empezar, cree el [Administrador de gráficos de filtro](filter-graph-manager.md) y consulte las interfaces [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) .


```C++
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;


    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="add-the-sample-grabber-to-the-filter-graph"></a>Agregar el captador de ejemplo al gráfico de filtros

Cree una instancia del filtro de enganche de ejemplo y addit al gráfico de filtro. Consulte el filtro de enganche de ejemplo para la interfaz [**ISampleGrabber**](isamplegrabber.md) .


```C++
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;


    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="set-the-media-type"></a>Establecer el tipo de medio

La primera vez que se crea el enganche de ejemplo, no tiene ningún tipo de medio preferido. Esto significa que puede conectarse a casi cualquier filtro del gráfico, pero no tendrá ningún control sobre el tipo de datos que recibió. Antes de compilar el resto del gráfico, por lo tanto, debe establecer un tipo de medio para el enganche de ejemplo llamando al método [**ISampleGrabber:: SetMediaType**](isamplegrabber-setmediatype.md) .

Cuando se conecte el enganche de ejemplo, comparará este tipo de medio con el tipo de medio ofrecido por el otro filtro. Los únicos campos que comprueba son el tipo principal, el subtipo y el tipo de formato. Para cualquiera de ellos, el valor \_ null GUID significa "Accept any Value". La mayoría de las veces, querrá establecer el tipo y el subtipo principales. Por ejemplo, el código siguiente especifica el vídeo RGB de 24 bits sin comprimir:


```C++
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="build-the-filter-graph"></a>Crear el gráfico de filtro

Ahora puede compilar el resto del gráfico de filtro. Dado que el enganche de ejemplo solo se conectará con el tipo de medio que ha especificado, le permite aprovechar los mecanismos de [conexión inteligente](intelligent-connect.md) del administrador de gráficos de filtro al compilar el gráfico.

Por ejemplo, si especificó vídeo sin comprimir, puede conectar un filtro de origen al enganche de ejemplo y el administrador de gráficos de filtros agregará automáticamente el analizador de archivos y el descodificador. En el ejemplo siguiente se usa la función auxiliar ConnectFilters, que se muestra en [conectar dos filtros](connect-two-filters.md):


```C++
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;


    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }
```





El enganche de ejemplo es un filtro de transformación, por lo que el PIN de salida debe estar conectado a otro filtro. A menudo, puede que simplemente desee descartar los ejemplos después de que haya terminado con ellos. En ese caso, conecte el captador de muestra al [**filtro de representador nulo**](null-renderer-filter.md), que descarta los datos que recibe.

En el ejemplo siguiente se conecta el captador de ejemplo al filtro de representador nulo:


```C++
    IBaseFilter *pNullF = NULL;


    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }
```





Tenga en cuenta que colocar el captador de ejemplo entre un descodificador de vídeo y el representador de vídeo puede perjudicar significativamente el rendimiento de la representación. El enganche de ejemplo es un filtro de transferencia en contexto, lo que significa que el búfer de salida es el mismo que el búfer de entrada. Para la representación de vídeo, es probable que el búfer de salida se encuentre en la tarjeta gráfica, donde las operaciones de lectura son mucho más lentas, en comparación con las operaciones de lectura en la memoria principal.

## <a name="run-the-graph"></a>Ejecutar el gráfico

El enganche de ejemplo funciona en uno de los dos modos siguientes:

-   El modo de almacenamiento en búfer realiza una copia de cada ejemplo antes de entregar el ejemplo de nivel inferior.
-   El modo de devolución de llamada invoca una función de devolución de llamada definida por la aplicación en cada ejemplo.

En este artículo se describe el modo de almacenamiento en búfer. (Antes de usar el modo de devolución de llamada, tenga en cuenta que la función de devolución de llamada debe estar bastante limitada. De lo contrario, puede reducir drásticamente el rendimiento o incluso causar interbloqueos. Para obtener más información, vea [**ISampleGrabber:: SetCallback**](isamplegrabber-setcallback.md)). Para activar el modo de almacenamiento en búfer, llame al método [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md) con el valor **true**.

Opcionalmente, llame al método [**ISampleGrabber:: SetOneShot**](isamplegrabber-setoneshot.md) con el valor **true**. Esto hace que el captador de ejemplo se detenga después de recibir el primer ejemplo multimedia, lo que resulta útil si desea captar un solo fotograma de la secuencia. Busque el tiempo deseado, ejecute el gráfico y espere hasta el evento de [**\_ finalización de EC**](ec-complete.md) . Tenga en cuenta que el nivel de precisión del marco depende del origen. Por ejemplo, la búsqueda de un archivo MPEG suele ser una precisión de fotogramas.

Para ejecutar el gráfico lo más rápido posible, convierta el reloj del gráfico como se describe en [establecer el reloj del gráfico](setting-the-graph-clock.md).

En el ejemplo siguiente se habilita el modo de una sola captura y el modo de almacenamiento en búfer, se ejecuta el gráfico de filtro y se espera a que finalice.


```C++
    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);
```



## <a name="grab-the-sample"></a>Captar el ejemplo

En el modo de almacenamiento en búfer, el enganche de ejemplo almacena una copia de cada ejemplo. El método [**ISampleGrabber:: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) copia el búfer en una matriz asignada por el llamador. Para determinar el tamaño de la matriz que se necesita, llame primero a **GetCurrentBuffer** con un puntero **nulo** para la dirección de la matriz. A continuación, asigne la matriz y llame a la segunda vez al método para copiar el búfer. En el ejemplo siguiente se muestran estos pasos.


```C++
    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }
```



Tendrá que conocer el formato exacto de los datos en el búfer. Para obtener esta información, llame al método [**ISampleGrabber:: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) . Este método rellena una estructura de [**\_ \_ tipo medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) con el formato.

En el caso de una secuencia de vídeo sin comprimir, la información de formato se encuentra en una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . En el ejemplo siguiente se muestra cómo obtener la información de formato de una secuencia de vídeo sin comprimir.


```C++
    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }
```



> [!Note]  
> El enganche de ejemplo no es compatible con [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).

 

## <a name="example-code"></a>Código de ejemplo

Este es el código completo de los ejemplos anteriores.

> [!Note]  
> En este ejemplo se usa la función [SafeRelease](../medfound/saferelease.md) para liberar punteros de interfaz.

 


```C++
#include <windows.h>
#include <dshow.h>
#include "qedit.h"

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}



HRESULT WriteBitmap(PCWSTR, BITMAPINFOHEADER*, size_t, BYTE*, size_t);

HRESULT GrabVideoBitmap(PCWSTR pszVideoFile, PCWSTR pszBitmapFile)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;
    IBaseFilter *pNullF = NULL;

    BYTE *pBuffer = NULL;

    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }

    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }

    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);

    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->GetConnectedMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }

    FreeMediaType(mt);

done:
    CoTaskMemFree(pBuffer);
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    SafeRelease(&pNullF);
    SafeRelease(&pSourceF);
    SafeRelease(&pGrabber);
    SafeRelease(&pGrabberF);
    SafeRelease(&pControl);
    SafeRelease(&pEvent);
    SafeRelease(&pGraph);
    return hr;
};

// Writes a bitmap file
//  pszFileName:  Output file name.
//  pBMI:         Bitmap format information (including pallete).
//  cbBMI:        Size of the BITMAPINFOHEADER, including palette, if present.
//  pData:        Pointer to the bitmap bits.
//  cbData        Size of the bitmap, in bytes.

HRESULT WriteBitmap(PCWSTR pszFileName, BITMAPINFOHEADER *pBMI, size_t cbBMI,
    BYTE *pData, size_t cbData)
{
    HANDLE hFile = CreateFile(pszFileName, GENERIC_WRITE, 0, NULL, 
        CREATE_ALWAYS, 0, NULL);
    if (hFile == NULL)
    {
        return HRESULT_FROM_WIN32(GetLastError());
    }

    BITMAPFILEHEADER bmf = { };

    bmf.bfType = &#39;MB&#39;;
    bmf.bfSize = cbBMI+ cbData + sizeof(bmf); 
    bmf.bfOffBits = sizeof(bmf) + cbBMI; 

    DWORD cbWritten = 0;
    BOOL result = WriteFile(hFile, &bmf, sizeof(bmf), &cbWritten, NULL);
    if (result)
    {
        result = WriteFile(hFile, pBMI, cbBMI, &cbWritten, NULL);
    }
    if (result)
    {
        result = WriteFile(hFile, pData, cbData, &cbWritten, NULL);
    }

    HRESULT hr = result ? S_OK : HRESULT_FROM_WIN32(GetLastError());

    CloseHandle(hFile);

    return hr;
}
```





## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar servicios de edición de DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 
