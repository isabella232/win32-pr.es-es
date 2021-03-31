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
# <a name="using-the-source-reader-in-asynchronous-mode"></a><span data-ttu-id="aa8dc-103">Usar el lector de origen en modo asincrónico</span><span class="sxs-lookup"><span data-stu-id="aa8dc-103">Using the Source Reader in Asynchronous Mode</span></span>

<span data-ttu-id="aa8dc-104">En este tema se describe cómo usar el [lector de origen](source-reader.md) en modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-104">This topic describes how to use the [Source Reader](source-reader.md) in asynchronous mode.</span></span> <span data-ttu-id="aa8dc-105">En el modo asincrónico, la aplicación proporciona una interfaz de devolución de llamada, que se utiliza para notificar a la aplicación que los datos están disponibles.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-105">In asynchronous mode, the application provides a callback interface, which is used to notify the application that data is available.</span></span>

<span data-ttu-id="aa8dc-106">En este tema se da por supuesto que ya ha leído el tema [uso del lector de origen para procesar los datos multimedia](processing-media-data-with-the-source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="aa8dc-106">This topic assumes that you have already read the topic [Using the Source Reader to Process Media Data](processing-media-data-with-the-source-reader.md).</span></span>

## <a name="using-asynchronous-mode"></a><span data-ttu-id="aa8dc-107">Usar el modo asincrónico</span><span class="sxs-lookup"><span data-stu-id="aa8dc-107">Using Asynchronous Mode</span></span>

<span data-ttu-id="aa8dc-108">El lector de origen funciona en modo sincrónico o en modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-108">The Source Reader operates either in synchronous mode or asynchronous mode.</span></span> <span data-ttu-id="aa8dc-109">En el ejemplo de código que se muestra en la sección anterior se supone que el lector de código fuente utiliza el modo sincrónico, que es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-109">The code example shown in the previous section assumes that the Source Reader is using synchronous mode, which is the default.</span></span> <span data-ttu-id="aa8dc-110">En el modo sincrónico, el método [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) se bloquea mientras que el origen del medio genera el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-110">In synchronous mode, the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method blocks while the media source produces the next sample.</span></span> <span data-ttu-id="aa8dc-111">Normalmente, un origen multimedia adquiere datos de algún origen externo (como un archivo local o una conexión de red), por lo que el método puede bloquear el subproceso de llamada durante un período de tiempo considerable.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-111">A media source typically acquires data from some external source (such as a local file or a network connection), so the method can block the calling thread for a noticeable amount of time.</span></span>

<span data-ttu-id="aa8dc-112">En el modo asincrónico, [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) vuelve inmediatamente y el trabajo se realiza en otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-112">In asynchronous mode, the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) returns immediately and the work is performed on another thread.</span></span> <span data-ttu-id="aa8dc-113">Una vez completada la operación, el lector de origen llama a la aplicación a través de la interfaz de devolución de llamada [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) .</span><span class="sxs-lookup"><span data-stu-id="aa8dc-113">After the operation is complete, the Source Reader calls the application through the [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) callback interface.</span></span> <span data-ttu-id="aa8dc-114">Para usar el modo asincrónico, debe proporcionar un puntero de devolución de llamada cuando cree por primera vez el lector de origen, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="aa8dc-114">To use asynchronous mode, you must provide a callback pointer when you first create the Source Reader, as follows:</span></span>

1.  <span data-ttu-id="aa8dc-115">Cree un almacén de atributos mediante una llamada a la función [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .</span><span class="sxs-lookup"><span data-stu-id="aa8dc-115">Create an attribute store by calling the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function.</span></span>
2.  <span data-ttu-id="aa8dc-116">Establezca el atributo de [ \_ devolución de \_ \_ \_ llamada asincrónica lector de origen MF](mf-source-reader-async-callback.md) en el almacén de atributos.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-116">Set the [MF\_SOURCE\_READER\_ASYNC\_CALLBACK](mf-source-reader-async-callback.md) attribute on the attribute store.</span></span> <span data-ttu-id="aa8dc-117">El valor del atributo es un puntero al objeto de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-117">The attribute value is a pointer to your callback object.</span></span>
3.  <span data-ttu-id="aa8dc-118">Al crear el lector de origen, pase el almacén de atributos a la función de creación en el parámetro *pAttributes* .</span><span class="sxs-lookup"><span data-stu-id="aa8dc-118">When you create the Source Reader, pass the attribute store to the creation function in the *pAttributes* parameter.</span></span> <span data-ttu-id="aa8dc-119">Todas las funciones para crear el lector de origen tienen este parámetro.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-119">All of the functions to create the Source Reader have this parameter.</span></span>

<span data-ttu-id="aa8dc-120">En el ejemplo siguiente se muestran estos pasos.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-120">The following example shows these steps.</span></span>


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



<span data-ttu-id="aa8dc-121">Después de crear el lector de origen, no se pueden cambiar los modos entre sincrónicos y asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-121">After you create the Source Reader, you cannot switch modes between synchronous and asynchronous.</span></span>

<span data-ttu-id="aa8dc-122">Para obtener datos en modo asincrónico, llame al método [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) pero establezca los cuatro últimos parámetros en **null**, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-122">To get data in asynchronous mode, call the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method but set the last four parameters to **NULL**, as shown in the following example.</span></span>


```C++
    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
```



<span data-ttu-id="aa8dc-123">Cuando el método [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) se completa de forma asincrónica, el lector de código fuente llama al método [**IMFSourceReaderCallback:: OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) .</span><span class="sxs-lookup"><span data-stu-id="aa8dc-123">When the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method completes asynchronously, the Source Reader calls your [**IMFSourceReaderCallback::OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method.</span></span> <span data-ttu-id="aa8dc-124">Este método tiene cinco parámetros:</span><span class="sxs-lookup"><span data-stu-id="aa8dc-124">This method has five parameters:</span></span>

-   <span data-ttu-id="aa8dc-125">*hrStatus*: contiene un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aa8dc-125">*hrStatus*: Contains an **HRESULT** value.</span></span> <span data-ttu-id="aa8dc-126">Este es el mismo valor que [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) devolvería en modo sincrónico.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-126">This is the same value that [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) would return in synchronous mode.</span></span> <span data-ttu-id="aa8dc-127">Si *hrStatus* contiene un código de error, puede omitir los parámetros restantes.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-127">If *hrStatus* contains an error code, you can ignore the remaining parameters.</span></span>
-   <span data-ttu-id="aa8dc-128">*dwStreamIndex*, *dwStreamFlags*, llTimestamp y *pSample*: estos tres parámetros son equivalentes a los tres últimos parámetros en [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span><span class="sxs-lookup"><span data-stu-id="aa8dc-128">*dwStreamIndex*, *dwStreamFlags*, llTimestamp, and *pSample*: These three parameters are equivalent to the last three parameters in [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span></span> <span data-ttu-id="aa8dc-129">Contienen el número de secuencia, las marcas de estado y el puntero [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-129">They contain the stream number, status flags, and [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer, respectively.</span></span>


```C++
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);
```



<span data-ttu-id="aa8dc-130">Además, la interfaz de devolución de llamada define otros dos métodos:</span><span class="sxs-lookup"><span data-stu-id="aa8dc-130">In addition, the callback interface defines two other methods:</span></span>

-   <span data-ttu-id="aa8dc-131">[**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent).</span><span class="sxs-lookup"><span data-stu-id="aa8dc-131">[**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent).</span></span> <span data-ttu-id="aa8dc-132">Notifica a la aplicación cuando se producen determinados eventos en el origen de medios, como el almacenamiento en búfer o los eventos de conexión de red.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-132">Notifies the application when certain events occur in media source, such as buffering or network connection events.</span></span>
-   <span data-ttu-id="aa8dc-133">[**Alvaciar**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush).</span><span class="sxs-lookup"><span data-stu-id="aa8dc-133">[**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush).</span></span> <span data-ttu-id="aa8dc-134">Se le llama cuando se completa el método [**Flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) .</span><span class="sxs-lookup"><span data-stu-id="aa8dc-134">Called when the [**Flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) method completes.</span></span>

## <a name="implementing-the-callback-interface"></a><span data-ttu-id="aa8dc-135">Implementar la interfaz de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="aa8dc-135">Implementing the Callback Interface</span></span>

<span data-ttu-id="aa8dc-136">La interfaz de devolución de llamada debe ser segura para subprocesos, porque se llama a [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) y a los demás métodos de devolución de llamada desde los subprocesos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-136">The callback interface must be thread-safe, because [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) and the other callback methods are called from worker threads.</span></span>

<span data-ttu-id="aa8dc-137">Hay varios enfoques diferentes que puede realizar al implementar la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-137">There are several different approaches you can take when you implement the callback.</span></span> <span data-ttu-id="aa8dc-138">Por ejemplo, puede realizar todo el trabajo dentro de la devolución de llamada, o puede usar la devolución de llamada para notificar a la aplicación (por ejemplo, mediante la señalización de un identificador de evento) y, a continuación, realizar el trabajo desde el subproceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-138">For example, you can do all of the work inside the callback, or you can use the callback to notify the application (for example, by signaling an event handle) and then do work from the application thread.</span></span>

<span data-ttu-id="aa8dc-139">El método [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) se llamará una vez para cada llamada que realice al método [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) .</span><span class="sxs-lookup"><span data-stu-id="aa8dc-139">The [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method will be called once for every call that you make to the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method.</span></span> <span data-ttu-id="aa8dc-140">Para obtener el ejemplo siguiente, vuelva a llamar a **ReadSample** .</span><span class="sxs-lookup"><span data-stu-id="aa8dc-140">To get the next sample, call **ReadSample** again.</span></span> <span data-ttu-id="aa8dc-141">Si se produce un error, se llama a **OnReadSample** con un código de error para el parámetro *hrStatus* .</span><span class="sxs-lookup"><span data-stu-id="aa8dc-141">If an error occurs, **OnReadSample** is called with an error code for the *hrStatus* parameter.</span></span>

<span data-ttu-id="aa8dc-142">En el ejemplo siguiente se muestra una implementación mínima de la interfaz de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-142">The following example shows a minimal implementation of the callback interface.</span></span> <span data-ttu-id="aa8dc-143">En primer lugar, esta es la declaración de una clase que implementa la interfaz.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-143">First, here is the declaration of a class that implements the interface.</span></span>


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



<span data-ttu-id="aa8dc-144">En este ejemplo, no nos interesan los métodos [**onEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) y [**alflush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) , por lo que simplemente devuelven los elementos **\_ correctos**.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-144">In this example, we are not interested in the [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) and [**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) methods, so they simply return **S\_OK**.</span></span> <span data-ttu-id="aa8dc-145">La clase utiliza un identificador de evento para señalar la aplicación; Este identificador se proporciona a través del constructor.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-145">The class uses an event handle to signal the application; this handle is provided through the constructor.</span></span>

<span data-ttu-id="aa8dc-146">En este ejemplo mínimo, el método [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) simplemente imprime la marca de tiempo en la ventana de la consola.</span><span class="sxs-lookup"><span data-stu-id="aa8dc-146">In this minimal example, the [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method just prints the time stamp to the console window.</span></span> <span data-ttu-id="aa8dc-147">A continuación, almacena el código de estado y el marcador de final de secuencia y señala el identificador de evento:</span><span class="sxs-lookup"><span data-stu-id="aa8dc-147">Then it stores the status code and the end-of-stream flag, and signals the event handle:</span></span>


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



<span data-ttu-id="aa8dc-148">En el código siguiente se muestra que la aplicación usaría esta clase de devolución de llamada para leer todos los fotogramas de vídeo de un archivo multimedia:</span><span class="sxs-lookup"><span data-stu-id="aa8dc-148">The following code shows the application would use this callback class to read all of the video frames from a media file:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="aa8dc-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aa8dc-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa8dc-150">Lector de origen</span><span class="sxs-lookup"><span data-stu-id="aa8dc-150">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 



