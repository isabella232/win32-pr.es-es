---
description: En este tema se describe cómo usar el lector de origen en modo asincrónico.
ms.assetid: 9D3C2780-D7DB-4151-8474-9A19EC94F6BE
title: Usar el lector de origen en modo asincrónico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357d0405cb3e594d059b7c93e793250e0be88562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082289"
---
# <a name="using-the-source-reader-in-asynchronous-mode"></a>Usar el lector de origen en modo asincrónico

En este tema se describe cómo usar el [lector de origen](source-reader.md) en modo asincrónico. En el modo asincrónico, la aplicación proporciona una interfaz de devolución de llamada, que se utiliza para notificar a la aplicación que los datos están disponibles.

En este tema se da por supuesto que ya ha leído el tema [uso del lector de origen para procesar los datos multimedia](processing-media-data-with-the-source-reader.md).

## <a name="using-asynchronous-mode"></a>Usar el modo asincrónico

El lector de origen funciona en modo sincrónico o en modo asincrónico. En el ejemplo de código que se muestra en la sección anterior se supone que el lector de código fuente utiliza el modo sincrónico, que es el valor predeterminado. En el modo sincrónico, el método [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) se bloquea mientras que el origen del medio genera el ejemplo siguiente. Normalmente, un origen multimedia adquiere datos de algún origen externo (como un archivo local o una conexión de red), por lo que el método puede bloquear el subproceso de llamada durante un período de tiempo considerable.

En el modo asincrónico, [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) vuelve inmediatamente y el trabajo se realiza en otro subproceso. Una vez completada la operación, el lector de origen llama a la aplicación a través de la interfaz de devolución de llamada [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) . Para usar el modo asincrónico, debe proporcionar un puntero de devolución de llamada cuando cree por primera vez el lector de origen, como se indica a continuación:

1.  Cree un almacén de atributos mediante una llamada a la función [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .
2.  Establezca el atributo de [ \_ devolución de \_ \_ \_ llamada asincrónica lector de origen MF](mf-source-reader-async-callback.md) en el almacén de atributos. El valor del atributo es un puntero al objeto de devolución de llamada.
3.  Al crear el lector de origen, pase el almacén de atributos a la función de creación en el parámetro *pAttributes* . Todas las funciones para crear el lector de origen tienen este parámetro.

En el ejemplo siguiente se muestran estos pasos.


```C++
HRESULT CreateSourceReaderAsync(
    PCWSTR pszURL, 
    IMFSourceReaderCallback *pCallback, 
    IMFSourceReader **ppReader)
{
    HRESULT hr = S_OK;
    IMFAttributes *pAttributes = NULL;

    hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAttributes->SetUnknown(MF_SOURCE_READER_ASYNC_CALLBACK, pCallback);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateSourceReaderFromURL(pszURL, pAttributes, ppReader);

done:
    SafeRelease(&pAttributes);
    return hr;
}
```



Después de crear el lector de origen, no se pueden cambiar los modos entre sincrónicos y asincrónicos.

Para obtener datos en modo asincrónico, llame al método [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) pero establezca los cuatro últimos parámetros en **null**, como se muestra en el ejemplo siguiente.


```C++
    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
```



Cuando el método [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) se completa de forma asincrónica, el lector de código fuente llama al método [**IMFSourceReaderCallback:: OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) . Este método tiene cinco parámetros:

-   *hrStatus*: contiene un valor **HRESULT** . Este es el mismo valor que [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) devolvería en modo sincrónico. Si *hrStatus* contiene un código de error, puede omitir los parámetros restantes.
-   *dwStreamIndex*, *dwStreamFlags*, llTimestamp y *pSample*: estos tres parámetros son equivalentes a los tres últimos parámetros en [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample). Contienen el número de secuencia, las marcas de estado y el puntero [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , respectivamente.


```C++
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);
```



Además, la interfaz de devolución de llamada define otros dos métodos:

-   [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent). Notifica a la aplicación cuando se producen determinados eventos en el origen de medios, como el almacenamiento en búfer o los eventos de conexión de red.
-   [**Alvaciar**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush). Se le llama cuando se completa el método [**Flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) .

## <a name="implementing-the-callback-interface"></a>Implementar la interfaz de devolución de llamada

La interfaz de devolución de llamada debe ser segura para subprocesos, porque se llama a [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) y a los demás métodos de devolución de llamada desde los subprocesos de trabajo.

Hay varios enfoques diferentes que puede realizar al implementar la devolución de llamada. Por ejemplo, puede realizar todo el trabajo dentro de la devolución de llamada, o puede usar la devolución de llamada para notificar a la aplicación (por ejemplo, mediante la señalización de un identificador de evento) y, a continuación, realizar el trabajo desde el subproceso de la aplicación.

El método [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) se llamará una vez para cada llamada que realice al método [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) . Para obtener el ejemplo siguiente, vuelva a llamar a **ReadSample** . Si se produce un error, se llama a **OnReadSample** con un código de error para el parámetro *hrStatus* .

En el ejemplo siguiente se muestra una implementación mínima de la interfaz de devolución de llamada. En primer lugar, esta es la declaración de una clase que implementa la interfaz.


```C++
#include <shlwapi.h>

class SourceReaderCB : public IMFSourceReaderCallback
{
public:
    SourceReaderCB(HANDLE hEvent) : 
      m_nRefCount(1), m_hEvent(hEvent), m_bEOS(FALSE), m_hrStatus(S_OK)
    {
        InitializeCriticalSection(&m_critsec);
    }

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(SourceReaderCB, IMFSourceReaderCallback),
            { 0 },
        };
        return QISearch(this, qit, iid, ppv);
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_nRefCount);
    }
    STDMETHODIMP_(ULONG) Release()
    {
        ULONG uCount = InterlockedDecrement(&m_nRefCount);
        if (uCount == 0)
        {
            delete this;
        }
        return uCount;
    }

    // IMFSourceReaderCallback methods
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);

    STDMETHODIMP OnEvent(DWORD, IMFMediaEvent *)
    {
        return S_OK;
    }

    STDMETHODIMP OnFlush(DWORD)
    {
        return S_OK;
    }

public:
    HRESULT Wait(DWORD dwMilliseconds, BOOL *pbEOS)
    {
        *pbEOS = FALSE;

        DWORD dwResult = WaitForSingleObject(m_hEvent, dwMilliseconds);
        if (dwResult == WAIT_TIMEOUT)
        {
            return E_PENDING;
        }
        else if (dwResult != WAIT_OBJECT_0)
        {
            return HRESULT_FROM_WIN32(GetLastError());
        }

        *pbEOS = m_bEOS;
        return m_hrStatus;
    }
    
private:
    
    // Destructor is private. Caller should call Release.
    virtual ~SourceReaderCB() 
    {
    }

    void NotifyError(HRESULT hr)
    {
        wprintf(L"Source Reader error: 0x%X\n", hr);
    }

private:
    long                m_nRefCount;        // Reference count.
    CRITICAL_SECTION    m_critsec;
    HANDLE              m_hEvent;
    BOOL                m_bEOS;
    HRESULT             m_hrStatus;

};
```



En este ejemplo, no nos interesan los métodos [**onEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) y [**alflush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) , por lo que simplemente devuelven los elementos **\_ correctos**. La clase utiliza un identificador de evento para señalar la aplicación; Este identificador se proporciona a través del constructor.

En este ejemplo mínimo, el método [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) simplemente imprime la marca de tiempo en la ventana de la consola. A continuación, almacena el código de estado y el marcador de final de secuencia y señala el identificador de evento:


```C++
HRESULT SourceReaderCB::OnReadSample(
    HRESULT hrStatus,
    DWORD /* dwStreamIndex */,
    DWORD dwStreamFlags,
    LONGLONG llTimestamp,
    IMFSample *pSample      // Can be NULL
    )
{
    EnterCriticalSection(&m_critsec);

    if (SUCCEEDED(hrStatus))
    {
        if (pSample)
        {
            // Do something with the sample.
            wprintf(L"Frame @ %I64d\n", llTimestamp);
        }
    }
    else
    {
        // Streaming error.
        NotifyError(hrStatus);
    }

    if (MF_SOURCE_READERF_ENDOFSTREAM & dwStreamFlags)
    {
        // Reached the end of the stream.
        m_bEOS = TRUE;
    }
    m_hrStatus = hrStatus;

    LeaveCriticalSection(&m_critsec);
    SetEvent(m_hEvent);
    return S_OK;
}
```



En el código siguiente se muestra que la aplicación usaría esta clase de devolución de llamada para leer todos los fotogramas de vídeo de un archivo multimedia:


```C++
HRESULT ReadMediaFile(PCWSTR pszURL)
{
    HRESULT hr = S_OK;

    IMFSourceReader *pReader = NULL;
    SourceReaderCB *pCallback = NULL;

    HANDLE hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto done;
    }

    // Create an instance of the callback object.
    pCallback = new (std::nothrow) SourceReaderCB(hEvent);
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    // Create the Source Reader.
    hr = CreateSourceReaderAsync(pszURL, pCallback, &pReader);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConfigureDecoder(pReader, MF_SOURCE_READER_FIRST_VIDEO_STREAM);
    if (FAILED(hr))
    {
        goto done;
    }

    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    while (SUCCEEDED(hr))
    {
        BOOL bEOS;
        hr = pCallback->Wait(INFINITE, &bEOS);
        if (FAILED(hr) || bEOS)
        {
            break;
        }
        hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM,
            0, NULL, NULL, NULL, NULL);
    }

done:
    SafeRelease(&pReader);
    SafeRelease(&pCallback);
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lector de origen](source-reader.md)
</dt> </dl>

 

 



