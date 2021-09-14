---
description: El filtro Sample Grabber es un filtro de transformación que se puede usar para obtener muestras multimedia de una secuencia a medida que pasan a través del gráfico de filtros.
ms.assetid: ec0e367e-9ef9-4de6-9132-b462c233bc98
title: Uso de Sample Grabber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4886c796691e83e02b58ddea129d60d5004c9f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127275060"
---
# <a name="using-the-sample-grabber"></a>Uso de Sample Grabber

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

El [**filtro Sample Grabber es**](sample-grabber-filter.md) un filtro de transformación que se puede usar para obtener muestras multimedia de una secuencia a medida que pasan a través del gráfico de filtros.

Si simplemente desea tomar un mapa de bits de un archivo de vídeo, es más fácil usar el objeto [Media Detector (MediaDet).](media-detector--mediadet.md) Consulte [Captura de un marco de póster](grabbing-a-poster-frame.md) para obtener más información. Sin embargo, Sample Grabber es más flexible porque funciona con casi cualquier tipo de medio (vea [**ISampleGrabber::SetMediaType para**](isamplegrabber-setmediatype.md) ver algunas excepciones) y ofrece más control a la aplicación.

-   [Crear el Administrador de Graph filtros](#create-the-filter-graph-manager)
-   [Agregue sample grabber al filtro Graph](#add-the-sample-grabber-to-the-filter-graph)
-   [Establecer el tipo de medio](#set-the-media-type)
-   [Compilar el filtro Graph](#build-the-filter-graph)
-   [Ejecute el Graph](#run-the-graph)
-   [Obtener el ejemplo](#grab-the-sample)
-   [Código de ejemplo](#example-code)
-   [Temas relacionados](#related-topics)

## <a name="create-the-filter-graph-manager"></a>Crear el Administrador de Graph filtros

Para empezar, cree el [Administrador de Graph y](filter-graph-manager.md) consulte las interfaces [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaEventEx.**](/windows/desktop/api/Control/nn-control-imediaeventex)


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





## <a name="add-the-sample-grabber-to-the-filter-graph"></a>Agregue sample grabber al filtro Graph

Cree una instancia del filtro Sample Grabber y agregue al gráfico de filtros. Consulte el filtro Sample Grabber para la [**interfaz ISampleGrabber.**](isamplegrabber.md)


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

La primera vez que se crea sample grabber, no tiene ningún tipo de medio preferido. Esto significa que puede conectarse a casi cualquier filtro del gráfico, pero no tendría control sobre el tipo de datos que recibió. Antes de compilar el resto del gráfico, por lo tanto, debe establecer un tipo de medio para Sample Grabber mediante una llamada al [**método ISampleGrabber::SetMediaType.**](isamplegrabber-setmediatype.md)

Cuando se conecta sample grabber, compara este tipo de medio con el tipo de medio que ofrece el otro filtro. Los únicos campos que comprueba son el tipo principal, el subtipo y el tipo de formato. Para cualquiera de ellos, el valor GUID \_ NULL significa "aceptar cualquier valor". La mayoría de las veces, querrá establecer el tipo principal y el subtipo. Por ejemplo, el código siguiente especifica vídeo RGB de 24 bits sin comprimir:


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



## <a name="build-the-filter-graph"></a>Compilar el filtro Graph

Ahora puede compilar el resto del gráfico de filtro. Dado que sample Grabber solo se conectará con el tipo de medio que ha especificado, esto le permite aprovechar los mecanismos intelligent [Conectar](intelligent-connect.md) de Filter Graph Manager al compilar el gráfico.

Por ejemplo, si especificó vídeo sin comprimir, puede conectar un filtro de origen al sample grabber y el Administrador de filtros Graph agregará automáticamente el analizador de archivos y el descodificador. En el ejemplo siguiente se usa la función auxiliar ConnectFilters, que se muestra [en Conectar dos filtros](connect-two-filters.md):


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





Sample Grabber es un filtro de transformación, por lo que el pin de salida debe estar conectado a otro filtro. A menudo, es posible que simplemente quiera descartar los ejemplos una vez que haya terminado con ellos. En ese caso, conecte sample grabber al filtro de representador [**null**](null-renderer-filter.md), que descarta los datos que recibe.

En el ejemplo siguiente se conecta sample grabber al filtro De representador null:


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





Tenga en cuenta que colocar sample Grabber entre un descodificador de vídeo y el representador de vídeo puede dañar significativamente el rendimiento de la representación. Sample Grabber es un filtro trans-in-place, lo que significa que el búfer de salida es el mismo que el búfer de entrada. En el caso de la representación de vídeo, es probable que el búfer de salida se encuentra en la tarjeta gráfica, donde las operaciones de lectura son mucho más lentas, en comparación con las operaciones de lectura en la memoria principal.

## <a name="run-the-graph"></a>Ejecute el Graph

Sample Grabber funciona en uno de estos dos modos:

-   El modo de almacenamiento en búfer realiza una copia de cada muestra antes de entregar el ejemplo de nivel inferior.
-   El modo de devolución de llamada invoca una función de devolución de llamada definida por la aplicación en cada ejemplo.

En este artículo se describe el modo de almacenamiento en búfer. (Antes de usar el modo de devolución de llamada, tenga en cuenta que la función de devolución de llamada debe ser bastante limitada. De lo contrario, puede reducir drásticamente el rendimiento o incluso provocar interbloqueos. Para obtener más información, [**vea ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md)). Para activar el modo de almacenamiento en búfer, llame [**al método ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) con el **valor TRUE**.

Opcionalmente, llame al [**método ISampleGrabber::SetOneShot**](isamplegrabber-setoneshot.md) con el valor **TRUE**. Esto hace que sample grabber se detenga después de recibir el primer ejemplo multimedia, lo que resulta útil si desea obtener un único fotograma de la secuencia. Busque la hora deseada, ejecute el gráfico y espere el [**evento EC \_ COMPLETE.**](ec-complete.md) Tenga en cuenta que el nivel de precisión del fotograma depende del origen. Por ejemplo, la búsqueda de un archivo MPEG a menudo no es precisa de fotogramas.

Para ejecutar el gráfico lo más rápido posible, active el reloj del gráfico tal y como se describe en [Setting the Graph Clock](setting-the-graph-clock.md).

En el ejemplo siguiente se habilita el modo de una sola toma y el modo de almacenamiento en búfer, se ejecuta el gráfico de filtros y se espera a que se complete.


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



## <a name="grab-the-sample"></a>Obtener el ejemplo

En el modo de almacenamiento en búfer, sample grabber almacena una copia de cada muestra. El [**método ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) copia el búfer en una matriz asignada por el autor de la llamada. Para determinar el tamaño de la matriz necesaria, llame primero a **GetCurrentBuffer** con un puntero **NULL** para la dirección de la matriz. A continuación, asigne la matriz y llame al método una segunda vez para copiar el búfer. En el ejemplo siguiente se muestran estos pasos.


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



Deberá conocer el formato exacto de los datos en el búfer. Para obtener esta información, llame al [**método ISampleGrabber::GetConnectedMediaType.**](isamplegrabber-getconnectedmediatype.md) Este método rellena una estructura [**\_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) con el formato .

Para una secuencia de vídeo sin comprimir, la información de formato se encuentra en una [**estructura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) En el ejemplo siguiente se muestra cómo obtener la información de formato de una secuencia de vídeo sin comprimir.


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
> Sample Grabber no admite [**VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)

 

## <a name="example-code"></a>Código de ejemplo

Este es el código completo de los ejemplos anteriores.

> [!Note]  
> En este ejemplo se usa [la función SafeRelease para](../medfound/saferelease.md) liberar punteros de interfaz.

 


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

[Uso de DirectShow Editing Services](using-directshow-editing-services.md)
</dt> </dl>

 

 
