---
description: En este tema se analiza en profundidad el ejemplo de SDK de origen de medios MPEG-1.
ms.assetid: d392f30c-c963-4eb3-add2-1bb986919c0b
title: 'Caso práctico: origen de medios MPEG-1'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e1f72cc6ae6df119439bdae1942732bf8d2fa2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104083548"
---
# <a name="case-study-mpeg-1-media-source"></a>Caso práctico: origen de medios MPEG-1

En Microsoft Media Foundation, el objeto que presenta los datos multimedia en la canalización de datos se denomina *origen de medios*. En este tema se analiza en profundidad el ejemplo de SDK de [origen de medios MPEG-1](mpeg1source-sample.md) .

-   [Requisitos previos](#prerequisites)
-   [Clases de C++ utilizadas en el origen MPEG-1](#c-classes-used-in-the-mpeg-1-source)
-   [Controlador de flujo de bytes](#byte-stream-handler)
-   [Descriptor de presentación](#presentation-descriptor)
-   [Estados de streaming](#streaming-states)
    -   [Iniciar](#start)
    -   [Pausar](#pause)
    -   [Detención](#stop)
-   [Solicitudes de ejemplo](#sample-requests)
-   [Final de la secuencia](#end-of-stream)
-   [Operaciones asincrónicas](#asynchronous-operations)
    -   [Cola de operaciones](#operation-queue)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Requisitos previos

Antes de leer este tema, debe comprender los siguientes conceptos de Media Foundation:

-   [Modelo de objetos de origen de medios](media-source-object-model.md)
-   [Métodos de devolución de llamada asincrónica](asynchronous-callback-methods.md).
-   [Colas de trabajo](work-queues.md)
-   [Generadores de eventos multimedia](media-event-generators.md)
-   [Búferes multimedia](media-buffers.md)
-   [Ejemplos de medios](media-samples.md)
-   [Tipos de medios](media-types.md)

También debe tener un conocimiento básico de la arquitectura de Media Foundation, especialmente del papel de los orígenes multimedia en la canalización. (Para obtener más información, vea [orígenes multimedia](media-sources.md)).

Además, es posible que quiera leer el tema [Writing a Custom Media Source](writing-a-custom-media-source.md), que ofrece una introducción más general de los pasos que se describen aquí.

En este tema no se reproduce todo el código del ejemplo de SDK, porque el ejemplo es bastante grande.

## <a name="c-classes-used-in-the-mpeg-1-source"></a>Clases de C++ utilizadas en el origen MPEG-1

El origen MPEG-1 de ejemplo se implementa con las siguientes clases de C++:

-   `MPEG1ByteStreamHandler`. Implementa el controlador de flujo de bytes para el origen de medios. Dado un flujo de bytes, el controlador de flujo de bytes crea una instancia del origen.
-   `MPEG1Source`. Implementa el origen de los medios.
-   `MPEG1Stream`. Implementa los objetos de flujo multimedia. El origen de medios crea un `MPEG1Stream` objeto para cada secuencia de audio o vídeo en el fragmentada MPEG-1.
-   `Parser`. Analiza el fragmentada MPEG-1. En su mayor parte, los detalles de esta clase no son relevantes para las API de Media Foundation.
-   SourceOp, OpQueue: estas dos clases administran las operaciones asincrónicas en el origen de los medios. (Consulte [operaciones asincrónicas](#asynchronous-operations)).

Más adelante en el tema se describen otras clases auxiliares.

## <a name="byte-stream-handler"></a>Controlador de Byte-Stream

El controlador *de flujo de bytes* es el objeto que crea el origen de medios. La resolución de origen crea el controlador de flujo de bytes. las aplicaciones no interactúan directamente con el controlador de flujo de bytes. La resolución de origen detecta el controlador de flujo de bytes mediante la búsqueda en el registro. Los controladores se registran por extensión de nombre de archivo o tipo MIME. Para el origen MPEG-1, el controlador de flujo de bytes se registra para la extensión de nombre de archivo ". mpg".

> [!Note]  
> Si desea admitir esquemas de dirección URL personalizados, también puede escribir un *controlador de esquema*. El origen MPEG-1 está diseñado para archivos locales y Media Foundation ya proporciona un controlador de esquema para las direcciones URL "file://".

 

El controlador de flujo de bytes implementa la interfaz [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) . Esta interfaz tiene dos métodos más importantes que se deben implementar:

-   [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject). Inicia una operación asincrónica para crear el origen de medios.
-   [**EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject). Completa la llamada asincrónica.

Otros dos métodos son opcionales y no se implementan en el ejemplo de SDK:

-   [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation). Cancela el método [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) . Este método es útil para un origen de red que podría tener una latencia alta en el inicio.
-   [**GetMaxNumberOfBytesRequiredForResolution**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution). Obtiene el número máximo de bytes que el controlador leerá de la secuencia de origen. Implemente este método si sabe cuántos datos el controlador de secuencias de bytes tiene antes de poder crear el origen de medios. De lo contrario, simplemente devuelva **E \_ NOTIMPL**.

Esta es la implementación del método [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) :


```C++
HRESULT MPEG1ByteStreamHandler::BeginCreateObject(
        /* [in] */ IMFByteStream *pByteStream,
        /* [in] */ LPCWSTR pwszURL,
        /* [in] */ DWORD dwFlags,
        /* [in] */ IPropertyStore *pProps,
        /* [out] */ IUnknown **ppIUnknownCancelCookie,  // Can be NULL
        /* [in] */ IMFAsyncCallback *pCallback,
        /* [in] */ IUnknown *punkState                  // Can be NULL
        )
{
    if (pByteStream == NULL)
    {
        return E_POINTER;
    }

    if (pCallback == NULL)
    {
        return E_POINTER;
    }

    if ((dwFlags & MF_RESOLUTION_MEDIASOURCE) == 0)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFAsyncResult *pResult = NULL;
    MPEG1Source    *pSource = NULL;

    // Create an instance of the media source.
    hr = MPEG1Source::CreateInstance(&pSource);

    // Create a result object for the caller's async callback.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);
    }

    // Start opening the source. This is an async operation.
    // When it completes, the source will invoke our callback
    // and then we will invoke the caller's callback.
    if (SUCCEEDED(hr))
    {
        hr = pSource->BeginOpen(pByteStream, this, NULL);
    }

    if (SUCCEEDED(hr))
    {
        if (ppIUnknownCancelCookie)
        {
            *ppIUnknownCancelCookie = NULL;
        }

        m_pSource = pSource;
        m_pSource->AddRef();

        m_pResult = pResult;
        m_pResult->AddRef();
    }

// cleanup
    SafeRelease(&pSource);
    SafeRelease(&pResult);
    return hr;
}
```



El método realiza los pasos siguientes:

1.  Crea una nueva instancia del objeto `MPEG1Source`.
2.  Cree un objeto de resultado asincrónico. Este objeto se usa más adelante para invocar el método de devolución de llamada del solucionador de origen.
3.  Llama a `MPEG1Source::BeginOpen` , un método asincrónico definido en la `MPEG1Source` clase.
4.  Establece *ppIUnknownCancelCookie* en **null**, que informa al llamador de que [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) no se admite.

El `MPEG1Source::BeginOpen` método realiza el trabajo real de leer la secuencia de bytes e inicializar el `MPEG1Source` objeto. Este método no forma parte de la API pública. Puede definir cualquier mecanismo entre el controlador y el origen multimedia que se ajuste a sus necesidades. Poner la mayor parte de la lógica en el origen de medios mantiene el controlador de flujo de bytes relativamente sencillo.

Brevemente, `BeginOpen` hace lo siguiente:

1.  Llama a [**IMFByteStream:: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) para comprobar que la secuencia de bytes de origen es legible y se puede buscar.
2.  Llama a [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) para iniciar una solicitud de e/s asincrónica.

El resto de la inicialización se produce de forma asincrónica. El origen de medios Lee suficientes datos de la secuencia para analizar los encabezados de secuencia MPEG-1. A continuación, crea un *descriptor de presentación*, que es el objeto que se usa para describir las secuencias de audio y vídeo del archivo. (Para obtener más información, vea [descriptor de presentación](#presentation-descriptor)). Cuando se `BeginOpen` completa la operación, el controlador de flujo de bytes invoca el método de devolución de llamada del solucionador de origen. En ese momento, el solucionador de origen llama a [**IMFByteStreamHandler:: EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject). El método **EndCreateObject** devuelve el estado de la operación.


```C++
HRESULT MPEG1ByteStreamHandler::EndCreateObject(
        /* [in] */ IMFAsyncResult *pResult,
        /* [out] */ MF_OBJECT_TYPE *pObjectType,
        /* [out] */ IUnknown **ppObject)
{
    if (pResult == NULL || pObjectType == NULL || ppObject == NULL)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    *pObjectType = MF_OBJECT_INVALID;
    *ppObject = NULL;

    hr = pResult->GetStatus();

    if (SUCCEEDED(hr))
    {
        *pObjectType = MF_OBJECT_MEDIASOURCE;

        assert(m_pSource != NULL);

        hr = m_pSource->QueryInterface(IID_PPV_ARGS(ppObject));
    }

    SafeRelease(&m_pSource);
    SafeRelease(&m_pResult);
    return hr;
}
```



Si se produce un error en cualquier momento durante este proceso, la devolución de llamada se invoca con un código de estado de error.

## <a name="presentation-descriptor"></a>Descriptor de presentación

El descriptor de presentación describe el contenido del archivo MPEG-1, incluida la información siguiente:

-   El número de secuencias.
-   El formato de cada flujo.
-   Identificadores de secuencia.
-   El estado de selección de cada secuencia (seleccionada o anulada).

En cuanto a la arquitectura de Media Foundation, el descriptor de presentación contiene uno o más *descriptores de flujo*. Cada descriptor de flujo contiene un *controlador de tipo de medio*, que se usa para obtener o establecer los tipos de medios en la secuencia. Media Foundation proporciona implementaciones de existencias para el descriptor de presentación y el descriptor de flujo; son adecuados para la mayoría de los orígenes de medios.

Para crear un descriptor de presentación, realice los pasos siguientes:

1.  Para cada flujo:
    1.  Proporcione un identificador de flujo y una matriz de posibles tipos de medios. Si la secuencia admite más de un tipo de medio, ordene la lista de tipos de medios por preferencia, si existe. (Ponga primero el tipo óptimo y el último tipo óptimo).
    2.  Llame a [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) para crear el descriptor de flujo.
    3.  Llame a [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) en el descriptor de la secuencia recién creado.
    4.  Llame a [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) para establecer el formato predeterminado de la secuencia. Si hay más de un tipo de medio, normalmente debe establecer el primer tipo en la lista.
2.  Llame a [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) y pase la matriz de punteros del descriptor de flujo.
3.  Para cada flujo, llame a [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) o [**DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) para establecer el estado de selección predeterminado. Si hay más de un flujo del mismo tipo (audio o vídeo), solo debe seleccionarse uno de forma predeterminada.

El `MPEG1Source` objeto crea el descriptor de presentación en su `InitPresentationDescriptor` método:


```C++
HRESULT MPEG1Source::InitPresentationDescriptor()
{
    HRESULT hr = S_OK;
    DWORD cStreams = 0;

    assert(m_pPresentationDescriptor == NULL);
    assert(m_state == STATE_OPENING);

    if (m_pHeader == NULL)
    {
        return E_FAIL;
    }

    // Get the number of streams, as declared in the MPEG-1 header, skipping
    // any streams with an unsupported format.
    for (DWORD i = 0; i < m_pHeader->cStreams; i++)
    {
        if (IsStreamTypeSupported(m_pHeader->streams[i].type))
        {
            cStreams++;
        }
    }

    // How many streams do we actually have?
    if (cStreams > m_streams.GetCount())
    {
        // Keep reading data until we have seen a packet for each stream.
        return S_OK;
    }

    // We should never create a stream we don't support.
    assert(cStreams == m_streams.GetCount());

    // Ready to create the presentation descriptor.

    // Create an array of IMFStreamDescriptor pointers.
    IMFStreamDescriptor **ppSD =
            new (std::nothrow) IMFStreamDescriptor*[cStreams];

    if (ppSD == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    ZeroMemory(ppSD, cStreams * sizeof(IMFStreamDescriptor*));

    // Fill the array by getting the stream descriptors from the streams.
    for (DWORD i = 0; i < cStreams; i++)
    {
        hr = m_streams[i]->GetStreamDescriptor(&ppSD[i]);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Create the presentation descriptor.
    hr = MFCreatePresentationDescriptor(cStreams, ppSD,
        &m_pPresentationDescriptor);

    if (FAILED(hr))
    {
        goto done;
    }

    // Select the first video stream (if any).
    for (DWORD i = 0; i < cStreams; i++)
    {
        GUID majorType = GUID_NULL;

        hr = GetStreamMajorType(ppSD[i], &majorType);
        if (FAILED(hr))
        {
            goto done;
        }

        if (majorType == MFMediaType_Video)
        {
            hr = m_pPresentationDescriptor->SelectStream(i);
            if (FAILED(hr))
            {
                goto done;
            }
            break;
        }
    }

    // Switch state from "opening" to stopped.
    m_state = STATE_STOPPED;

    // Invoke the async callback to complete the BeginOpen operation.
    hr = CompleteOpen(S_OK);

done:
    // clean up:
    if (ppSD)
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            SafeRelease(&ppSD[i]);
        }
        delete [] ppSD;
    }
    return hr;
}
```



La aplicación obtiene el descriptor de presentación mediante una llamada a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). Este método crea una copia superficial del descriptor de presentación mediante una llamada a [**IMFPresentationDescriptor:: Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone). (La copia contiene punteros a los descriptores de secuencia originales). La aplicación puede usar el descriptor de presentación para establecer el tipo de medio, seleccionar una secuencia o anular la selección de una secuencia.

Opcionalmente, los descriptores de presentación y los descriptores de flujo pueden contener atributos que proporcionan información adicional sobre el origen. Para obtener una lista de estos atributos, vea los temas siguientes:

-   [Atributos de descriptor de presentación](presentation-descriptor-attributes.md)
-   [Atributos de descriptor de secuencia](stream-descriptor-attributes.md)

Un atributo merece mención especial: el atributo de [**\_ \_ duración MF PD**](mf-pd-duration-attribute.md) contiene la duración total del origen. Establezca este atributo si conoce la duración por adelantado; por ejemplo, la duración podría especificarse en los encabezados de archivo, dependiendo del formato de archivo. La aplicación puede mostrar este valor o usarlo para establecer una barra de progreso o una barra de búsqueda.

## <a name="streaming-states"></a>Estados de streaming

Un origen multimedia define los siguientes Estados:



| Estado    | Descripción                                                                                                     |
|----------|-----------------------------------------------------------------------------------------------------------------|
| Iniciado  | El origen acepta y procesa solicitudes de ejemplo.                                                               |
| En pausa   | El origen acepta solicitudes de ejemplo, pero no las procesa. Las solicitudes se ponen en cola hasta que se inicia el origen. |
| Detenido. | El origen rechaza las solicitudes de ejemplo.                                                                             |



 

### <a name="start"></a>Start

El método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) inicia el origen del medio. Toma los parámetros siguientes:

-   Descriptor de presentación.
-   Un GUID con formato de hora.
-   Posición inicial.

La aplicación debe obtener el descriptor de presentación llamando a [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) en el origen. No hay ningún mecanismo definido para validar un descriptor de presentación. Si la aplicación especifica un descriptor de presentación incorrecto, los resultados son indefinidos.

El GUID de formato de hora especifica cómo interpretar la posición inicial. El formato estándar es unidades 100-nanosegundos (NS), indicado por GUID \_ null. Cada origen multimedia debe admitir 100 unidades NS. Opcionalmente, un origen puede admitir otras unidades de tiempo, como el número de marco o el código de tiempo. Sin embargo, no hay ninguna manera estándar de consultar un origen de medios para obtener la lista de formatos de hora que admite.

La posición inicial se proporciona como **PROPVARIANT**, lo que permite tipos de datos diferentes en función del formato de hora. Para 100-NS, el tipo **PROPVARIANT** es **VT \_ i8** o **VT \_ vacío**. Si **VT \_ i8**, **PROPVARIANT** contiene la posición inicial en 100-unidades NS. El valor **VT \_ vacío** tiene el significado especial "comenzar en la posición actual".

Implemente el método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) de la manera siguiente:

1.  Validar parámetros y estado:
    -   Compruebe si hay parámetros **null** .
    -   Compruebe el GUID de formato de hora. Si el valor no es válido, se devuelve el **\_ formato de \_ \_ hora \_ no compatible con MF E**.
    -   Compruebe el tipo de datos de **PROPVARIANT** que contiene la posición de inicio.
    -   Valida la posición inicial. Si no es válido, se devuelve **MF \_ E \_ INVALIDREQUEST**.
    -   Si el origen se ha cerrado, devuelva **el \_ \_ cierre MF E**.
2.  Si no se produce ningún error en el paso 1, poner en cola una operación asincrónica. Todo después de este paso se produce en un subproceso de cola de trabajo.
3.  Para cada flujo:
    1.  Compruebe si la secuencia ya está activa desde una solicitud de [**Inicio**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) anterior.
    2.  Llame a [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) para comprobar si la aplicación seleccionó o anula la selección de la secuencia.
    3.  Si ahora se anula la selección de una secuencia seleccionada anteriormente, vacíe cualquier ejemplo no entregado de la secuencia.
    4.  Si la secuencia está activa, el origen multimedia (no la secuencia) envía uno de los siguientes eventos:
        -   Envía [MEUpdatedStream](meupdatedstream.md) si la secuencia estaba activa previamente.
        -   De lo contrario, envía [MENewStream](menewstream.md).

        En ambos eventos, los datos del evento son el puntero [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) para la secuencia.
    5.  Si el origen se reinicia a partir del estado en pausa, puede que haya solicitudes de ejemplo pendientes. Si es así, envíelos ahora.
    6.  Si el origen está buscando una nueva posición, cada objeto de secuencia envía un evento [MEStreamSeeked](mestreamseeked.md) . De lo contrario, cada secuencia envía un evento [MEStreamStarted](mestreamstarted.md) .
4.  Si el origen está buscando una nueva posición, el origen multimedia envía un evento [MESourceSeeked](mesourceseeked.md) . De lo contrario, envía un evento [MESourceStarted](mesourcestarted.md) .

Si se produce un error en cualquier momento después del paso 2, el origen envía un evento [MESourceStarted](mesourcestarted.md) con un código de error. Esto alerta a la aplicación de que el método de [**Inicio**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) produjo un error de forma asincrónica.

En el código siguiente se muestran los pasos 1 a 2:


```C++
HRESULT MPEG1Source::Start(
        IMFPresentationDescriptor* pPresentationDescriptor,
        const GUID* pguidTimeFormat,
        const PROPVARIANT* pvarStartPos
    )
{

    HRESULT hr = S_OK;
    SourceOp *pAsyncOp = NULL;

    // Check parameters.

    // Start position and presentation descriptor cannot be NULL.
    if (pvarStartPos == NULL || pPresentationDescriptor == NULL)
    {
        return E_INVALIDARG;
    }

    // Check the time format.
    if ((pguidTimeFormat != NULL) && (*pguidTimeFormat != GUID_NULL))
    {
        // Unrecognized time format GUID.
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    // Check the data type of the start position.
    if ((pvarStartPos->vt != VT_I8) && (pvarStartPos->vt != VT_EMPTY))
    {
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    EnterCriticalSection(&m_critSec);

    // Check if this is a seek request. This sample does not support seeking.

    if (pvarStartPos->vt == VT_I8)
    {
        // If the current state is STOPPED, then position 0 is valid.
        // Otherwise, the start position must be VT_EMPTY (current position).

        if ((m_state != STATE_STOPPED) || (pvarStartPos->hVal.QuadPart != 0))
        {
            hr = MF_E_INVALIDREQUEST;
            goto done;
        }
    }

    // Fail if the source is shut down.
    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Fail if the source was not initialized yet.
    hr = IsInitialized();
    if (FAILED(hr))
    {
        goto done;
    }

    // Perform a basic check on the caller's presentation descriptor.
    hr = ValidatePresentationDescriptor(pPresentationDescriptor);
    if (FAILED(hr))
    {
        goto done;
    }

    // The operation looks OK. Complete the operation asynchronously.
    hr = SourceOp::CreateStartOp(pPresentationDescriptor, &pAsyncOp);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAsyncOp->SetData(*pvarStartPos);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = QueueOperation(pAsyncOp);

done:
    SafeRelease(&pAsyncOp);
    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



En el ejemplo siguiente se muestran los pasos restantes:


```C++
HRESULT MPEG1Source::DoStart(StartOp *pOp)
{
    assert(pOp->Op() == SourceOp::OP_START);

    IMFPresentationDescriptor *pPD = NULL;
    IMFMediaEvent  *pEvent = NULL;

    HRESULT     hr = S_OK;
    LONGLONG    llStartOffset = 0;
    BOOL        bRestartFromCurrentPosition = FALSE;
    BOOL        bSentEvents = FALSE;

    hr = BeginAsyncOp(pOp);

    // Get the presentation descriptor from the SourceOp object.
    // This is the PD that the caller passed into the Start() method.
    // The PD has already been validated.
    if (SUCCEEDED(hr))
    {
        hr = pOp->GetPresentationDescriptor(&pPD);
    }

    // Because this sample does not support seeking, the start
    // position must be 0 (from stopped) or "current position."

    // If the sample supported seeking, we would need to get the
    // start position from the PROPVARIANT data contained in pOp.

    if (SUCCEEDED(hr))
    {
        // Select/deselect streams, based on what the caller set in the PD.
        // This method also sends the MENewStream/MEUpdatedStream events.
        hr = SelectStreams(pPD, pOp->Data());
    }

    if (SUCCEEDED(hr))
    {
        m_state = STATE_STARTED;

        // Queue the "started" event. The event data is the start position.
        hr = m_pEventQueue->QueueEventParamVar(
            MESourceStarted,
            GUID_NULL,
            S_OK,
            &pOp->Data()
            );
    }

    if (FAILED(hr))
    {
        // Failure. Send the error code to the application.

        // Note: It's possible that QueueEvent itself failed, in which case it
        // is likely to fail again. But there is no good way to recover in
        // that case.

        (void)m_pEventQueue->QueueEventParamVar(
            MESourceStarted, GUID_NULL, hr, NULL);
    }

    CompleteAsyncOp(pOp);

    SafeRelease(&pEvent);
    SafeRelease(&pPD);
    return hr;
}
```



### <a name="pause"></a>Pausar

El método [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) pone en pausa el origen del medio. Implemente este método como se indica a continuación:

1.  Poner en cola una operación asincrónica.
2.  Cada flujo activo envía un evento [MEStreamPaused](mestreampaused.md) .
3.  El origen de medios envía un evento [MESourcePaused](mesourcepaused.md) .

Mientras está en pausa, el origen pone en cola las solicitudes de ejemplo sin procesarlas. (Consulte [solicitudes de ejemplo](#sample-requests)).

### <a name="stop"></a>Stop

El método [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) detiene el origen del medio. Implemente este método como se indica a continuación:

1.  Poner en cola una operación asincrónica.
2.  Cada flujo activo envía un evento [MEStreamStopped](mestreamstopped.md) .
3.  Borre todos los ejemplos en cola y las solicitudes de ejemplo.
4.  El origen de medios envía un evento [MESourceStopped](mesourcestopped.md) .

Mientras se detiene, el origen rechaza todas las solicitudes de ejemplos.

Si el origen se detiene mientras una solicitud de e/s está en curso, la solicitud de e/s puede completarse después de que el origen entre en el estado de detención. En ese caso, el origen debe descartar el resultado de la solicitud de e/s.

## <a name="sample-requests"></a>Solicitudes de ejemplo

Media Foundation usar un modelo de *extracción* , en el que la canalización solicita muestras del origen de los medios. Esto difiere del modelo usado por DirectShow, en el que los orígenes "inserciones" son ejemplos.

Para solicitar un nuevo ejemplo, la canalización Media Foundation llama a [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample). Este método toma un puntero **IUnknown** que representa un objeto de *token* . La implementación del objeto de token es hasta el autor de la llamada; simplemente proporciona una manera para que el llamador realice un seguimiento de las solicitudes de ejemplo. El parámetro token también puede ser **null**.

Suponiendo que el origen usa solicitudes de e/s asincrónicas para leer los datos, la generación de la muestra no se sincronizará con las solicitudes de ejemplo. Para sincronizar las solicitudes de ejemplo con la generación de ejemplo, un origen multimedia hace lo siguiente:

1.  Los tokens de solicitud se colocan en una cola.
2.  A medida que se generan ejemplos, se colocan en una segunda cola.
3.  El origen multimedia completa una solicitud de ejemplo mediante la extracción de un token de solicitud de la primera cola y un ejemplo de la segunda cola.
4.  El origen de medios envía un evento MEMediaSample. El evento contiene un puntero al ejemplo y el ejemplo contiene un puntero al token.

En el diagrama siguiente se muestra la relación entre el evento [MEMediaSample](memediasample.md) , el ejemplo y el token de solicitud.

![diagrama que muestra memediasample y una cola de ejemplo que apunta a imfsample; imfsample y el punto de cola de solicitudes a IUnknown](images/mediasourceimpl01.png)

El origen MPEG-1 de ejemplo implementa este proceso como se indica a continuación:

1.  El método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) coloca la solicitud en una cola FIFO.
2.  A medida que se completan las solicitudes de e/s, el origen multimedia crea nuevos ejemplos y los coloca en una segunda cola FIFO. (Esta cola tiene un tamaño máximo, para evitar que el origen se lea demasiado lejos).
3.  Siempre que ambas colas tengan al menos un elemento (una solicitud y una muestra), el origen multimedia completa la primera solicitud de la cola de solicitudes mediante el envío de la primera muestra de la cola de ejemplo.
4.  Para ofrecer un ejemplo, el objeto de secuencia (no el objeto de origen) envía un evento [MEMediaSample](memediasample.md) .
    -   Los datos de evento son un puntero a la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) del ejemplo.
    -   Si la solicitud incluye un token, adjunte el token al ejemplo estableciendo el atributo [**de \_ token MFSampleExtension**](mfsampleextension-token-attribute.md) en el ejemplo.

En este momento, hay tres posibilidades:

-   Hay otro ejemplo en la cola de ejemplo, pero no hay ninguna solicitud coincidente.
-   Hay una solicitud, pero no muestra ningún ejemplo.
-   Ambas colas están vacías; no hay ningún ejemplo y ninguna solicitud.

Si la cola de ejemplo está vacía, el origen comprueba el final de la secuencia (vea [final de la secuencia](#end-of-stream)). De lo contrario, inicia otra solicitud de e/s para los datos. Si se produce algún error durante este proceso, el flujo envía un evento [MEError](meerror.md) .

El código siguiente implementa el método [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) :


```C++
HRESULT MPEG1Stream::RequestSample(IUnknown* pToken)
{
    HRESULT hr = S_OK;
    IMFMediaSource *pSource = NULL;

    // Hold the media source object's critical section.
    SourceLock lock(m_pSource);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_state == STATE_STOPPED)
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (!m_bActive)
    {
        // If the stream is not active, it should not get sample requests.
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (m_bEOS && m_Samples.IsEmpty())
    {
        // This stream has already reached the end of the stream, and the
        // sample queue is empty.
        hr = MF_E_END_OF_STREAM;
        goto done;
    }

    hr = m_Requests.InsertBack(pToken);
    if (FAILED(hr))
    {
        goto done;
    }

    // Dispatch the request.
    hr = DispatchSamples();
    if (FAILED(hr))
    {
        goto done;
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        hr = m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }
    return hr;
}
```



El `DispatchSamples` método extrae ejemplos de la cola de ejemplo, los hace coincidir con solicitudes de ejemplo pendientes y pone en cola eventos [MEMediaSample](memediasample.md) :


```C++
HRESULT MPEG1Stream::DispatchSamples()
{
    HRESULT hr = S_OK;
    BOOL bNeedData = FALSE;
    BOOL bEOS = FALSE;

    SourceLock lock(m_pSource);

    // An I/O request can complete after the source is paused, stopped, or
    // shut down. Do not deliver samples unless the source is running.
    if (m_state != STATE_STARTED)
    {
        return S_OK;
    }

    IMFSample *pSample = NULL;
    IUnknown  *pToken = NULL;

    // Deliver as many samples as we can.
    while (!m_Samples.IsEmpty() && !m_Requests.IsEmpty())
    {
        // Pull the next sample from the queue.
        hr = m_Samples.RemoveFront(&pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Pull the next request token from the queue. Tokens can be NULL.
        hr = m_Requests.RemoveFront(&pToken);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pToken)
        {
            // Set the token on the sample.
            hr = pSample->SetUnknown(MFSampleExtension_Token, pToken);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Send an MEMediaSample event with the sample.
        hr = m_pEventQueue->QueueEventParamUnk(
            MEMediaSample, GUID_NULL, S_OK, pSample);

        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pSample);
        SafeRelease(&pToken);
    }

    if (m_Samples.IsEmpty() && m_bEOS)
    {
        // The sample queue is empty AND we have reached the end of the source
        // stream. Notify the pipeline by sending the end-of-stream event.

        hr = m_pEventQueue->QueueEventParamVar(
            MEEndOfStream, GUID_NULL, S_OK, NULL);

        if (FAILED(hr))
        {
            goto done;
        }

        // Notify the source. It will send the end-of-presentation event.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_END_OF_STREAM);
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (NeedsData())
    {
        // The sample queue is empty; the request queue is not empty; and we
        // have not reached the end of the stream. Ask for more data.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_REQUEST_DATA);
        if (FAILED(hr))
        {
            goto done;
        }
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }

    SafeRelease(&pSample);
    SafeRelease(&pToken);
    return S_OK;
}
```



`DispatchSamples`Se llama al método en las siguientes circunstancias:

-   Dentro del método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .
-   Cuando el origen de medios se reinicia a partir del estado de pausa.
-   Cuando se completa una solicitud de e/s.

## <a name="end-of-stream"></a>Final de la secuencia

Cuando un flujo no tiene más datos y se han entregado todos los ejemplos de ese flujo, los objetos de secuencia envían un evento [MEEndOfStream](meendofstream.md) .

Cuando se realizan todas las secuencias activas, el origen de medios envía un evento [MEEndOfPresentation](meendofpresentation.md) .

## <a name="asynchronous-operations"></a>Operaciones asincrónicas

Quizás la parte más difícil de escribir un origen multimedia es comprender el Media Foundation modelo asincrónico.

Todos los métodos de un origen de medios que controlan el streaming son asíncronos. En cada caso, el método realiza algunas validaciones iniciales, como comprobar los parámetros. Después, el origen envía el resto del trabajo a una cola de trabajo. Una vez finalizada la operación, el origen del medio envía un evento de vuelta al llamador, a través de la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) del origen del medio. Por lo tanto, es importante entender las colas de trabajos.

Para colocar un elemento en una cola de trabajo, puede llamar a [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) o [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex). El origen MPEG-1 tiene lugar para usar **MFPutWorkItem**, pero las dos funciones hacen lo mismo. La función **MFPutWorkItem** toma los siguientes parámetros:

-   Valor **DWORD** que identifica la cola de trabajo. Puede crear una cola de trabajo privada o usar **el \_ \_ \_ estándar de cola de devolución de llamada MFASYNC**.
-   Puntero a la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . Esta interfaz de devolución de llamada se invoca para realizar el trabajo.
-   Un objeto de estado opcional, que debe implementar **IUnknown**.

Una o más subprocesos de trabajo que reenvían continuamente el siguiente elemento de trabajo de la cola prestan servicio a la cola de trabajo e invocan el método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) de la interfaz de devolución de llamada.

No se garantiza que los elementos de trabajo se ejecuten en el mismo orden en que se colocan en la cola. Recuerde que más de un subproceso puede dar servicio a la misma cola de trabajo, por lo que [**invocar**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) llamadas puede superponerse o producirse sin orden. Por lo tanto, depende del origen de los medios mantener el estado interno correcto, enviando los elementos de la cola de trabajo en el orden correcto. Solo cuando se completa la operación anterior, el origen inicia la siguiente operación.

Para representar las operaciones pendientes, el origen MPEG-1 define una clase denominada `SourceOp` :


```C++
// Represents a request for an asynchronous operation.

class SourceOp : public IUnknown
{
public:

    enum Operation
    {
        OP_START,
        OP_PAUSE,
        OP_STOP,
        OP_REQUEST_DATA,
        OP_END_OF_STREAM
    };

    static HRESULT CreateOp(Operation op, SourceOp **ppOp);
    static HRESULT CreateStartOp(IMFPresentationDescriptor *pPD, SourceOp **ppOp);

    // IUnknown
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    SourceOp(Operation op);
    virtual ~SourceOp();

    HRESULT SetData(const PROPVARIANT& var);

    Operation Op() const { return m_op; }
    const PROPVARIANT& Data() { return m_data;}

protected:
    long        m_cRef;     // Reference count.
    Operation   m_op;
    PROPVARIANT m_data;     // Data for the operation.
};
```



La `Operation` enumeración identifica qué operación está pendiente. La clase también contiene un **PROPVARIANT** para transmitir los datos adicionales para la operación.

### <a name="operation-queue"></a>Cola de operaciones

Para serializar las operaciones, el origen de medios mantiene una cola de `SourceOp` objetos. Usa una clase auxiliar para administrar la cola:


```C++
template <class OP_TYPE>
class OpQueue : public IUnknown
{
public:

    typedef ComPtrList<OP_TYPE>   OpList;

    HRESULT QueueOperation(OP_TYPE *pOp);

protected:

    HRESULT ProcessQueue();
    HRESULT ProcessQueueAsync(IMFAsyncResult *pResult);

    virtual HRESULT DispatchOperation(OP_TYPE *pOp) = 0;
    virtual HRESULT ValidateOperation(OP_TYPE *pOp) = 0;

    OpQueue(CRITICAL_SECTION& critsec)
        : m_OnProcessQueue(this, &OpQueue::ProcessQueueAsync),
          m_critsec(critsec)
    {
    }

    virtual ~OpQueue()
    {
    }

protected:
    OpList                  m_OpQueue;         // Queue of operations.
    CRITICAL_SECTION&       m_critsec;         // Protects the queue state.
    AsyncCallback<OpQueue>  m_OnProcessQueue;  // ProcessQueueAsync callback.
};
```



La `OpQueue` clase está diseñada para ser heredada por el componente que realiza los elementos de trabajo asincrónicos. El parámetro de plantilla *\_ tipo de operación* es el tipo de objeto que se usa para representar los elementos de trabajo en la cola; en este caso, el *\_ tipo de operación* será `SourceOp` . La `OpQueue` clase implementa los métodos siguientes:

-   `QueueOperation` coloca un nuevo elemento en la cola.
-   `ProcessQueue` envía la siguiente operación desde la cola. Este método es asincrónico.
-   `ProcessQueueAsync` completa el `ProcessQueue` método asincrónico.

La clase derivada debe implementar otros dos métodos:

-   `ValidateOperation` comprueba si es válido realizar una operación especificada, dado el estado actual del origen de los medios.
-   `DispatchOperation` lleva a cabo el elemento de trabajo asincrónico.

La cola de operaciones se utiliza como sigue:

1.  La canalización Media Foundation llama a un método asincrónico en el origen multimedia, como [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).
2.  El método asincrónico llama a `QueueOperation` , que coloca la operación de [**Inicio**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) en la cola y llama a `ProcessQueue` (en el formulario de un `SourceOp` objeto).
3.  `ProcessQueue` llama a [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).
4.  El subproceso de cola de trabajo llama a `ProcessQueueAsync` .
5.  El `ProcessQueueAsync` método llama a `ValidateOperation` y a `DispatchOperation` .

El código siguiente pone en cola una nueva operación en el origen MPEG-1:


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::QueueOperation(OP_TYPE *pOp)
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_critsec);

    hr = m_OpQueue.InsertBack(pOp);
    if (SUCCEEDED(hr))
    {
        hr = ProcessQueue();
    }

    LeaveCriticalSection(&m_critsec);
    return hr;
}
```



El código siguiente procesa la cola:


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::ProcessQueue()
{
    HRESULT hr = S_OK;
    if (m_OpQueue.GetCount() > 0)
    {
        hr = MFPutWorkItem(
            MFASYNC_CALLBACK_QUEUE_STANDARD,    // Use the standard work queue.
            &m_OnProcessQueue,                  // Callback method.
            NULL                                // State object.
            );
    }
    return hr;
}
```



El `ValidateOperation` método comprueba si el origen MPEG-1 puede enviar la siguiente operación en la cola. Si hay otra operación en curso, `ValidateOperation` devuelve **MF \_ E \_ NOTACCEPTING**. Esto garantiza que `DispatchOperation` no se llama mientras haya otra operación pendiente.


```C++
HRESULT MPEG1Source::ValidateOperation(SourceOp *pOp)
{
    if (m_pCurrentOp != NULL)
    {
        return MF_E_NOTACCEPTING;
    }
    return S_OK;
}
```



El método DispatchOperation cambia en el tipo de operación:


```C++
//-------------------------------------------------------------------
// DispatchOperation
//
// Performs the asynchronous operation indicated by pOp.
//
// NOTE:
// This method implements the pure-virtual OpQueue::DispatchOperation
// method. It is always called from a work-queue thread.
//-------------------------------------------------------------------

HRESULT MPEG1Source::DispatchOperation(SourceOp *pOp)
{
    EnterCriticalSection(&m_critSec);

    HRESULT hr = S_OK;

    if (m_state == STATE_SHUTDOWN)
    {
        LeaveCriticalSection(&m_critSec);

        return S_OK; // Already shut down, ignore the request.
    }

    switch (pOp->Op())
    {

    // IMFMediaSource methods:

    case SourceOp::OP_START:
        hr = DoStart((StartOp*)pOp);
        break;

    case SourceOp::OP_STOP:
        hr = DoStop(pOp);
        break;

    case SourceOp::OP_PAUSE:
        hr = DoPause(pOp);
        break;

    // Operations requested by the streams:

    case SourceOp::OP_REQUEST_DATA:
        hr = OnStreamRequestSample(pOp);
        break;

    case SourceOp::OP_END_OF_STREAM:
        hr = OnEndOfStream(pOp);
        break;

    default:
        hr = E_UNEXPECTED;
    }

    if (FAILED(hr))
    {
        StreamingError(hr);
    }

    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



En resumen:

1.  La canalización llama a un método asincrónico, como [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).
2.  El método asincrónico llama a `OpQueue::QueueOperation` , pasando un puntero a un `SourceOp` objeto.
3.  El `QueueOperation` método coloca la operación en la cola *m \_ OpQueue* y llama a `OpQueue::ProcessQueue` .
4.  El `ProcessQueue` método llama a [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem). Desde este punto, todo sucede en un subproceso de cola de trabajo Media Foundation. El método asincrónico vuelve al llamador.
5.  El subproceso de cola de trabajo llama al `OpQueue::ProcessQueueAsync` método.
6.  El `ProcessQueueAsync` método llama `MPEG1Source:ValidateOperation` a para validar la operación.
7.  El `ProcessQueueAsync` método llama `MPEG1Source::DispatchOperation` a para procesar la operación.

Este diseño tiene varias ventajas:

-   Los métodos son asincrónicos, por lo que no bloquean el subproceso de la aplicación que realiza la llamada.
-   Las operaciones se envían en un subproceso de cola de trabajo Media Foundation, que se comparte entre los componentes de canalización. Por consiguiente, el origen de medios no crea su propio subproceso, lo que reduce el número total de subprocesos que se crean.
-   El origen multimedia no se bloquea mientras se espera a que se completen las operaciones. Esto reduce la posibilidad de que un origen multimedia cause accidentalmente un interbloqueo y ayuda a reducir el cambio de contexto.
-   El origen multimedia puede usar la e/s asincrónica para leer el archivo de código fuente (llamando a [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)). No es necesario que el origen de medios se bloquee mientras se espera la rutina de e/s.

Si sigue el patrón que se muestra en el ejemplo de SDK, puede centrarse en los detalles concretos de su origen multimedia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Orígenes multimedia](media-sources.md)
</dt> <dt>

[Escritura de un origen de medios personalizado](writing-a-custom-media-source.md)
</dt> </dl>

 

 



