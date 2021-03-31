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
# <a name="case-study-mpeg-1-media-source"></a><span data-ttu-id="f2523-103">Caso práctico: origen de medios MPEG-1</span><span class="sxs-lookup"><span data-stu-id="f2523-103">Case Study: MPEG-1 Media Source</span></span>

<span data-ttu-id="f2523-104">En Microsoft Media Foundation, el objeto que presenta los datos multimedia en la canalización de datos se denomina *origen de medios*.</span><span class="sxs-lookup"><span data-stu-id="f2523-104">In Microsoft Media Foundation, the object that introduces media data into the data pipeline is called a *media source*.</span></span> <span data-ttu-id="f2523-105">En este tema se analiza en profundidad el ejemplo de SDK de [origen de medios MPEG-1](mpeg1source-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="f2523-105">This topic takes an in-depth look at the [MPEG-1 Media Source](mpeg1source-sample.md) SDK Sample.</span></span>

-   [<span data-ttu-id="f2523-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f2523-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="f2523-107">Clases de C++ utilizadas en el origen MPEG-1</span><span class="sxs-lookup"><span data-stu-id="f2523-107">C++ Classes Used in the MPEG-1 Source</span></span>](#c-classes-used-in-the-mpeg-1-source)
-   [<span data-ttu-id="f2523-108">Controlador de flujo de bytes</span><span class="sxs-lookup"><span data-stu-id="f2523-108">Byte-Stream Handler</span></span>](#byte-stream-handler)
-   [<span data-ttu-id="f2523-109">Descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="f2523-109">Presentation Descriptor</span></span>](#presentation-descriptor)
-   [<span data-ttu-id="f2523-110">Estados de streaming</span><span class="sxs-lookup"><span data-stu-id="f2523-110">Streaming States</span></span>](#streaming-states)
    -   [<span data-ttu-id="f2523-111">Iniciar</span><span class="sxs-lookup"><span data-stu-id="f2523-111">Start</span></span>](#start)
    -   [<span data-ttu-id="f2523-112">Pausar</span><span class="sxs-lookup"><span data-stu-id="f2523-112">Pause</span></span>](#pause)
    -   [<span data-ttu-id="f2523-113">Detención</span><span class="sxs-lookup"><span data-stu-id="f2523-113">Stop</span></span>](#stop)
-   [<span data-ttu-id="f2523-114">Solicitudes de ejemplo</span><span class="sxs-lookup"><span data-stu-id="f2523-114">Sample Requests</span></span>](#sample-requests)
-   [<span data-ttu-id="f2523-115">Final de la secuencia</span><span class="sxs-lookup"><span data-stu-id="f2523-115">End of Stream</span></span>](#end-of-stream)
-   [<span data-ttu-id="f2523-116">Operaciones asincrónicas</span><span class="sxs-lookup"><span data-stu-id="f2523-116">Asynchronous Operations</span></span>](#asynchronous-operations)
    -   [<span data-ttu-id="f2523-117">Cola de operaciones</span><span class="sxs-lookup"><span data-stu-id="f2523-117">Operation Queue</span></span>](#operation-queue)
-   [<span data-ttu-id="f2523-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f2523-118">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="f2523-119">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f2523-119">Prerequisites</span></span>

<span data-ttu-id="f2523-120">Antes de leer este tema, debe comprender los siguientes conceptos de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="f2523-120">Before reading this topic you should understand the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="f2523-121">Modelo de objetos de origen de medios</span><span class="sxs-lookup"><span data-stu-id="f2523-121">Media Source Object Model</span></span>](media-source-object-model.md)
-   <span data-ttu-id="f2523-122">[Métodos de devolución de llamada asincrónica](asynchronous-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="f2523-122">[Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>
-   [<span data-ttu-id="f2523-123">Colas de trabajo</span><span class="sxs-lookup"><span data-stu-id="f2523-123">Work Queues</span></span>](work-queues.md)
-   [<span data-ttu-id="f2523-124">Generadores de eventos multimedia</span><span class="sxs-lookup"><span data-stu-id="f2523-124">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="f2523-125">Búferes multimedia</span><span class="sxs-lookup"><span data-stu-id="f2523-125">Media Buffers</span></span>](media-buffers.md)
-   [<span data-ttu-id="f2523-126">Ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="f2523-126">Media Samples</span></span>](media-samples.md)
-   [<span data-ttu-id="f2523-127">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="f2523-127">Media Types</span></span>](media-types.md)

<span data-ttu-id="f2523-128">También debe tener un conocimiento básico de la arquitectura de Media Foundation, especialmente del papel de los orígenes multimedia en la canalización.</span><span class="sxs-lookup"><span data-stu-id="f2523-128">You should also have a basic understanding of the Media Foundation architecture, particularly the role of media sources in the pipeline.</span></span> <span data-ttu-id="f2523-129">(Para obtener más información, vea [orígenes multimedia](media-sources.md)).</span><span class="sxs-lookup"><span data-stu-id="f2523-129">(For more information, see [Media Sources](media-sources.md).)</span></span>

<span data-ttu-id="f2523-130">Además, es posible que quiera leer el tema [Writing a Custom Media Source](writing-a-custom-media-source.md), que ofrece una introducción más general de los pasos que se describen aquí.</span><span class="sxs-lookup"><span data-stu-id="f2523-130">In addition, you may want to read the topic [Writing a Custom Media Source](writing-a-custom-media-source.md), which gives a more general overview of the steps described here.</span></span>

<span data-ttu-id="f2523-131">En este tema no se reproduce todo el código del ejemplo de SDK, porque el ejemplo es bastante grande.</span><span class="sxs-lookup"><span data-stu-id="f2523-131">This topic does not reproduce all of the code from the SDK sample, because the sample is fairly large.</span></span>

## <a name="c-classes-used-in-the-mpeg-1-source"></a><span data-ttu-id="f2523-132">Clases de C++ utilizadas en el origen MPEG-1</span><span class="sxs-lookup"><span data-stu-id="f2523-132">C++ Classes Used in the MPEG-1 Source</span></span>

<span data-ttu-id="f2523-133">El origen MPEG-1 de ejemplo se implementa con las siguientes clases de C++:</span><span class="sxs-lookup"><span data-stu-id="f2523-133">The sample MPEG-1 source is implemented with the following C++ classes:</span></span>

-   <span data-ttu-id="f2523-134">`MPEG1ByteStreamHandler`.</span><span class="sxs-lookup"><span data-stu-id="f2523-134">`MPEG1ByteStreamHandler`.</span></span> <span data-ttu-id="f2523-135">Implementa el controlador de flujo de bytes para el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="f2523-135">Implements the byte-stream handler for the media source.</span></span> <span data-ttu-id="f2523-136">Dado un flujo de bytes, el controlador de flujo de bytes crea una instancia del origen.</span><span class="sxs-lookup"><span data-stu-id="f2523-136">Given a byte stream, the byte-stream handler creates an instance of the source.</span></span>
-   <span data-ttu-id="f2523-137">`MPEG1Source`.</span><span class="sxs-lookup"><span data-stu-id="f2523-137">`MPEG1Source`.</span></span> <span data-ttu-id="f2523-138">Implementa el origen de los medios.</span><span class="sxs-lookup"><span data-stu-id="f2523-138">Implements the media source.</span></span>
-   <span data-ttu-id="f2523-139">`MPEG1Stream`.</span><span class="sxs-lookup"><span data-stu-id="f2523-139">`MPEG1Stream`.</span></span> <span data-ttu-id="f2523-140">Implementa los objetos de flujo multimedia.</span><span class="sxs-lookup"><span data-stu-id="f2523-140">Implements the media stream objects.</span></span> <span data-ttu-id="f2523-141">El origen de medios crea un `MPEG1Stream` objeto para cada secuencia de audio o vídeo en el fragmentada MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="f2523-141">The media source creates one `MPEG1Stream` object for every audio or video stream in the MPEG-1 bitstream.</span></span>
-   <span data-ttu-id="f2523-142">`Parser`.</span><span class="sxs-lookup"><span data-stu-id="f2523-142">`Parser`.</span></span> <span data-ttu-id="f2523-143">Analiza el fragmentada MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="f2523-143">Parses the MPEG-1 bitstream.</span></span> <span data-ttu-id="f2523-144">En su mayor parte, los detalles de esta clase no son relevantes para las API de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f2523-144">For the most part, the details of this class are not relevant to the Media Foundation APIs.</span></span>
-   <span data-ttu-id="f2523-145">SourceOp, OpQueue: estas dos clases administran las operaciones asincrónicas en el origen de los medios.</span><span class="sxs-lookup"><span data-stu-id="f2523-145">SourceOp, OpQueue: These two classes manage asynchronous operations in the media source.</span></span> <span data-ttu-id="f2523-146">(Consulte [operaciones asincrónicas](#asynchronous-operations)).</span><span class="sxs-lookup"><span data-stu-id="f2523-146">(See [Asynchronous Operations](#asynchronous-operations)).</span></span>

<span data-ttu-id="f2523-147">Más adelante en el tema se describen otras clases auxiliares.</span><span class="sxs-lookup"><span data-stu-id="f2523-147">Other miscellaneous helper classes are described later in the topic.</span></span>

## <a name="byte-stream-handler"></a><span data-ttu-id="f2523-148">Controlador de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="f2523-148">Byte-Stream Handler</span></span>

<span data-ttu-id="f2523-149">El controlador *de flujo de bytes* es el objeto que crea el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="f2523-149">The *byte-stream* handler is the object that creates the media source.</span></span> <span data-ttu-id="f2523-150">La resolución de origen crea el controlador de flujo de bytes. las aplicaciones no interactúan directamente con el controlador de flujo de bytes.</span><span class="sxs-lookup"><span data-stu-id="f2523-150">The byte-stream handler is created by the source resolver; applications do not interact directly with the byte-stream handler.</span></span> <span data-ttu-id="f2523-151">La resolución de origen detecta el controlador de flujo de bytes mediante la búsqueda en el registro.</span><span class="sxs-lookup"><span data-stu-id="f2523-151">The source resolver discovers the byte-stream handler by looking in the registry.</span></span> <span data-ttu-id="f2523-152">Los controladores se registran por extensión de nombre de archivo o tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="f2523-152">Handler are registered by file name extension or MIME type.</span></span> <span data-ttu-id="f2523-153">Para el origen MPEG-1, el controlador de flujo de bytes se registra para la extensión de nombre de archivo ". mpg".</span><span class="sxs-lookup"><span data-stu-id="f2523-153">For the MPEG-1 source, the byte-stream handler is registered for the ".mpg" file name extension.</span></span>

> [!Note]  
> <span data-ttu-id="f2523-154">Si desea admitir esquemas de dirección URL personalizados, también puede escribir un *controlador de esquema*.</span><span class="sxs-lookup"><span data-stu-id="f2523-154">If you want to support custom URL schemes, you can also write a *scheme handler*.</span></span> <span data-ttu-id="f2523-155">El origen MPEG-1 está diseñado para archivos locales y Media Foundation ya proporciona un controlador de esquema para las direcciones URL "file://".</span><span class="sxs-lookup"><span data-stu-id="f2523-155">The MPEG-1 source is designed for local files, and Media Foundation already provides a scheme handler for "file://" URLs.</span></span>

 

<span data-ttu-id="f2523-156">El controlador de flujo de bytes implementa la interfaz [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) .</span><span class="sxs-lookup"><span data-stu-id="f2523-156">The byte-stream handler implements the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span> <span data-ttu-id="f2523-157">Esta interfaz tiene dos métodos más importantes que se deben implementar:</span><span class="sxs-lookup"><span data-stu-id="f2523-157">This interface has two most important methods that must be implemented:</span></span>

-   <span data-ttu-id="f2523-158">[**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span><span class="sxs-lookup"><span data-stu-id="f2523-158">[**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span></span> <span data-ttu-id="f2523-159">Inicia una operación asincrónica para crear el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="f2523-159">Starts an asynchronous operation to create the media source.</span></span>
-   <span data-ttu-id="f2523-160">[**EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span><span class="sxs-lookup"><span data-stu-id="f2523-160">[**EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span></span> <span data-ttu-id="f2523-161">Completa la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f2523-161">Completes the asynchronous call.</span></span>

<span data-ttu-id="f2523-162">Otros dos métodos son opcionales y no se implementan en el ejemplo de SDK:</span><span class="sxs-lookup"><span data-stu-id="f2523-162">Two other methods are optional and not implemented in the SDK sample:</span></span>

-   <span data-ttu-id="f2523-163">[**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation).</span><span class="sxs-lookup"><span data-stu-id="f2523-163">[**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation).</span></span> <span data-ttu-id="f2523-164">Cancela el método [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) .</span><span class="sxs-lookup"><span data-stu-id="f2523-164">Cancels the [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) method.</span></span> <span data-ttu-id="f2523-165">Este método es útil para un origen de red que podría tener una latencia alta en el inicio.</span><span class="sxs-lookup"><span data-stu-id="f2523-165">This method is useful for a network source that might have a high latency at startup.</span></span>
-   <span data-ttu-id="f2523-166">[**GetMaxNumberOfBytesRequiredForResolution**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution).</span><span class="sxs-lookup"><span data-stu-id="f2523-166">[**GetMaxNumberOfBytesRequiredForResolution**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution).</span></span> <span data-ttu-id="f2523-167">Obtiene el número máximo de bytes que el controlador leerá de la secuencia de origen.</span><span class="sxs-lookup"><span data-stu-id="f2523-167">Gets the maximum number of bytes that the handler will read from the source stream.</span></span> <span data-ttu-id="f2523-168">Implemente este método si sabe cuántos datos el controlador de secuencias de bytes tiene antes de poder crear el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="f2523-168">Implement this method if you know how much data the byte-stream handler before it can create the media source.</span></span> <span data-ttu-id="f2523-169">De lo contrario, simplemente devuelva **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="f2523-169">Otherwise, simply return **E\_NOTIMPL**.</span></span>

<span data-ttu-id="f2523-170">Esta es la implementación del método [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) :</span><span class="sxs-lookup"><span data-stu-id="f2523-170">Here is the implementation of the [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) method:</span></span>


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



<span data-ttu-id="f2523-171">El método realiza los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f2523-171">The method performs the following steps:</span></span>

1.  <span data-ttu-id="f2523-172">Crea una nueva instancia del objeto `MPEG1Source`.</span><span class="sxs-lookup"><span data-stu-id="f2523-172">Creates a new instance of the `MPEG1Source` object.</span></span>
2.  <span data-ttu-id="f2523-173">Cree un objeto de resultado asincrónico.</span><span class="sxs-lookup"><span data-stu-id="f2523-173">Create an asynchronous result object.</span></span> <span data-ttu-id="f2523-174">Este objeto se usa más adelante para invocar el método de devolución de llamada del solucionador de origen.</span><span class="sxs-lookup"><span data-stu-id="f2523-174">This object is used later to invoke the source resolver's callback method.</span></span>
3.  <span data-ttu-id="f2523-175">Llama a `MPEG1Source::BeginOpen` , un método asincrónico definido en la `MPEG1Source` clase.</span><span class="sxs-lookup"><span data-stu-id="f2523-175">Calls `MPEG1Source::BeginOpen`, an asynchronous method defined in the `MPEG1Source` class.</span></span>
4.  <span data-ttu-id="f2523-176">Establece *ppIUnknownCancelCookie* en **null**, que informa al llamador de que [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) no se admite.</span><span class="sxs-lookup"><span data-stu-id="f2523-176">Sets *ppIUnknownCancelCookie* to **NULL**, which informs the caller that [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) is not supported.</span></span>

<span data-ttu-id="f2523-177">El `MPEG1Source::BeginOpen` método realiza el trabajo real de leer la secuencia de bytes e inicializar el `MPEG1Source` objeto.</span><span class="sxs-lookup"><span data-stu-id="f2523-177">The `MPEG1Source::BeginOpen` method does the actual work of reading the byte stream and initializing the `MPEG1Source` object.</span></span> <span data-ttu-id="f2523-178">Este método no forma parte de la API pública.</span><span class="sxs-lookup"><span data-stu-id="f2523-178">This method is not part of the public API.</span></span> <span data-ttu-id="f2523-179">Puede definir cualquier mecanismo entre el controlador y el origen multimedia que se ajuste a sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="f2523-179">You can define any mechanism between the handler and the media source that suits your needs.</span></span> <span data-ttu-id="f2523-180">Poner la mayor parte de la lógica en el origen de medios mantiene el controlador de flujo de bytes relativamente sencillo.</span><span class="sxs-lookup"><span data-stu-id="f2523-180">Putting most of the logic into the media source keeps the byte-stream handler relatively simple.</span></span>

<span data-ttu-id="f2523-181">Brevemente, `BeginOpen` hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f2523-181">Briefly, `BeginOpen` does the following:</span></span>

1.  <span data-ttu-id="f2523-182">Llama a [**IMFByteStream:: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) para comprobar que la secuencia de bytes de origen es legible y se puede buscar.</span><span class="sxs-lookup"><span data-stu-id="f2523-182">Calls [**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) to verify that the source byte stream is both readable and seekable.</span></span>
2.  <span data-ttu-id="f2523-183">Llama a [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) para iniciar una solicitud de e/s asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f2523-183">Calls [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) to start an asynchronous I/O request.</span></span>

<span data-ttu-id="f2523-184">El resto de la inicialización se produce de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f2523-184">The rest of the initialization occurs asynchronously.</span></span> <span data-ttu-id="f2523-185">El origen de medios Lee suficientes datos de la secuencia para analizar los encabezados de secuencia MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="f2523-185">The media source reads enough data from the stream to parse the MPEG-1 sequence headers.</span></span> <span data-ttu-id="f2523-186">A continuación, crea un *descriptor de presentación*, que es el objeto que se usa para describir las secuencias de audio y vídeo del archivo.</span><span class="sxs-lookup"><span data-stu-id="f2523-186">Then it creates a *presentation descriptor*, which is the object used to describe the audio and video streams in the file.</span></span> <span data-ttu-id="f2523-187">(Para obtener más información, vea [descriptor de presentación](#presentation-descriptor)). Cuando se `BeginOpen` completa la operación, el controlador de flujo de bytes invoca el método de devolución de llamada del solucionador de origen.</span><span class="sxs-lookup"><span data-stu-id="f2523-187">(For more information, see [Presentation Descriptor](#presentation-descriptor).) When the `BeginOpen` operation completes, the byte-stream handler invokes the source resolver's callback method.</span></span> <span data-ttu-id="f2523-188">En ese momento, el solucionador de origen llama a [**IMFByteStreamHandler:: EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span><span class="sxs-lookup"><span data-stu-id="f2523-188">At that point, the source resolver calls [**IMFByteStreamHandler::EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span></span> <span data-ttu-id="f2523-189">El método **EndCreateObject** devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="f2523-189">The **EndCreateObject** method returns the status of the operation.</span></span>


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



<span data-ttu-id="f2523-190">Si se produce un error en cualquier momento durante este proceso, la devolución de llamada se invoca con un código de estado de error.</span><span class="sxs-lookup"><span data-stu-id="f2523-190">If an error occurs at any time during this process, the callback is invoked with an error status code.</span></span>

## <a name="presentation-descriptor"></a><span data-ttu-id="f2523-191">Descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="f2523-191">Presentation Descriptor</span></span>

<span data-ttu-id="f2523-192">El descriptor de presentación describe el contenido del archivo MPEG-1, incluida la información siguiente:</span><span class="sxs-lookup"><span data-stu-id="f2523-192">The presentation descriptor describes the contents of the MPEG-1 file, including the following information:</span></span>

-   <span data-ttu-id="f2523-193">El número de secuencias.</span><span class="sxs-lookup"><span data-stu-id="f2523-193">The number of the streams.</span></span>
-   <span data-ttu-id="f2523-194">El formato de cada flujo.</span><span class="sxs-lookup"><span data-stu-id="f2523-194">The format of each stream.</span></span>
-   <span data-ttu-id="f2523-195">Identificadores de secuencia.</span><span class="sxs-lookup"><span data-stu-id="f2523-195">Stream identifiers.</span></span>
-   <span data-ttu-id="f2523-196">El estado de selección de cada secuencia (seleccionada o anulada).</span><span class="sxs-lookup"><span data-stu-id="f2523-196">The selection status of each stream (selected or deselected).</span></span>

<span data-ttu-id="f2523-197">En cuanto a la arquitectura de Media Foundation, el descriptor de presentación contiene uno o más *descriptores de flujo*.</span><span class="sxs-lookup"><span data-stu-id="f2523-197">In terms of the Media Foundation architecture, the presentation descriptor contains one or more *stream descriptors*.</span></span> <span data-ttu-id="f2523-198">Cada descriptor de flujo contiene un *controlador de tipo de medio*, que se usa para obtener o establecer los tipos de medios en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f2523-198">Each stream descriptor contains a *media type handler*, which is used to get or set media types on the stream.</span></span> <span data-ttu-id="f2523-199">Media Foundation proporciona implementaciones de existencias para el descriptor de presentación y el descriptor de flujo; son adecuados para la mayoría de los orígenes de medios.</span><span class="sxs-lookup"><span data-stu-id="f2523-199">Media Foundation provides stock implementations for the presentation descriptor and stream descriptor; these are suitable for most media sources.</span></span>

<span data-ttu-id="f2523-200">Para crear un descriptor de presentación, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f2523-200">To create a presentation descriptor, perform the following steps:</span></span>

1.  <span data-ttu-id="f2523-201">Para cada flujo:</span><span class="sxs-lookup"><span data-stu-id="f2523-201">For each stream:</span></span>
    1.  <span data-ttu-id="f2523-202">Proporcione un identificador de flujo y una matriz de posibles tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="f2523-202">Provide a stream ID and an array of possible media types.</span></span> <span data-ttu-id="f2523-203">Si la secuencia admite más de un tipo de medio, ordene la lista de tipos de medios por preferencia, si existe.</span><span class="sxs-lookup"><span data-stu-id="f2523-203">If the stream supports more than one media type, order the list of media types by preference, if any.</span></span> <span data-ttu-id="f2523-204">(Ponga primero el tipo óptimo y el último tipo óptimo).</span><span class="sxs-lookup"><span data-stu-id="f2523-204">(Put the optimal type first, and the least optimal type last.)</span></span>
    2.  <span data-ttu-id="f2523-205">Llame a [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) para crear el descriptor de flujo.</span><span class="sxs-lookup"><span data-stu-id="f2523-205">Call [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) to create the stream descriptor.</span></span>
    3.  <span data-ttu-id="f2523-206">Llame a [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) en el descriptor de la secuencia recién creado.</span><span class="sxs-lookup"><span data-stu-id="f2523-206">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the newly created stream descriptor.</span></span>
    4.  <span data-ttu-id="f2523-207">Llame a [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) para establecer el formato predeterminado de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f2523-207">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) to set the default format for the stream.</span></span> <span data-ttu-id="f2523-208">Si hay más de un tipo de medio, normalmente debe establecer el primer tipo en la lista.</span><span class="sxs-lookup"><span data-stu-id="f2523-208">If there is more than one media type, you should generally set the first type in the list.</span></span>
2.  <span data-ttu-id="f2523-209">Llame a [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) y pase la matriz de punteros del descriptor de flujo.</span><span class="sxs-lookup"><span data-stu-id="f2523-209">Call [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) and pass in the array of stream descriptor pointers.</span></span>
3.  <span data-ttu-id="f2523-210">Para cada flujo, llame a [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) o [**DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) para establecer el estado de selección predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f2523-210">For each stream, call [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) or [**DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) to set the default selection state.</span></span> <span data-ttu-id="f2523-211">Si hay más de un flujo del mismo tipo (audio o vídeo), solo debe seleccionarse uno de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f2523-211">If there is more than one stream of the same type (audio or video), only one should be selected by default.</span></span>

<span data-ttu-id="f2523-212">El `MPEG1Source` objeto crea el descriptor de presentación en su `InitPresentationDescriptor` método:</span><span class="sxs-lookup"><span data-stu-id="f2523-212">The `MPEG1Source` object creates the presentation descriptor in its `InitPresentationDescriptor` method:</span></span>


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



<span data-ttu-id="f2523-213">La aplicación obtiene el descriptor de presentación mediante una llamada a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="f2523-213">The application gets the presentation descriptor by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="f2523-214">Este método crea una copia superficial del descriptor de presentación mediante una llamada a [**IMFPresentationDescriptor:: Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone).</span><span class="sxs-lookup"><span data-stu-id="f2523-214">This method creates a shallow copy of the presentation descriptor by calling [**IMFPresentationDescriptor::Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone).</span></span> <span data-ttu-id="f2523-215">(La copia contiene punteros a los descriptores de secuencia originales). La aplicación puede usar el descriptor de presentación para establecer el tipo de medio, seleccionar una secuencia o anular la selección de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="f2523-215">(The copy contains pointers to the original stream descriptors.) The application can use the presentation descriptor to set the media type, select a stream, or deselect a stream.</span></span>

<span data-ttu-id="f2523-216">Opcionalmente, los descriptores de presentación y los descriptores de flujo pueden contener atributos que proporcionan información adicional sobre el origen.</span><span class="sxs-lookup"><span data-stu-id="f2523-216">Optionally, presentation descriptors and stream descriptors can contain attributes that give additional information about the source.</span></span> <span data-ttu-id="f2523-217">Para obtener una lista de estos atributos, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="f2523-217">For a list such attributes, see the following topics:</span></span>

-   [<span data-ttu-id="f2523-218">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="f2523-218">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
-   [<span data-ttu-id="f2523-219">Atributos de descriptor de secuencia</span><span class="sxs-lookup"><span data-stu-id="f2523-219">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)

<span data-ttu-id="f2523-220">Un atributo merece mención especial: el atributo de [**\_ \_ duración MF PD**](mf-pd-duration-attribute.md) contiene la duración total del origen.</span><span class="sxs-lookup"><span data-stu-id="f2523-220">One attribute deserves special mention: The [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute contains the total duration of the source.</span></span> <span data-ttu-id="f2523-221">Establezca este atributo si conoce la duración por adelantado; por ejemplo, la duración podría especificarse en los encabezados de archivo, dependiendo del formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="f2523-221">Set this attribute if you know the duration up front; for example, the duration might be specified in the file headers, depending on the file format.</span></span> <span data-ttu-id="f2523-222">La aplicación puede mostrar este valor o usarlo para establecer una barra de progreso o una barra de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f2523-222">The application might display this value, or use it to set a progress bar or seek bar.</span></span>

## <a name="streaming-states"></a><span data-ttu-id="f2523-223">Estados de streaming</span><span class="sxs-lookup"><span data-stu-id="f2523-223">Streaming States</span></span>

<span data-ttu-id="f2523-224">Un origen multimedia define los siguientes Estados:</span><span class="sxs-lookup"><span data-stu-id="f2523-224">A media source defines the following states:</span></span>



| <span data-ttu-id="f2523-225">Estado</span><span class="sxs-lookup"><span data-stu-id="f2523-225">State</span></span>    | <span data-ttu-id="f2523-226">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2523-226">Description</span></span>                                                                                                     |
|----------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2523-227">Iniciado</span><span class="sxs-lookup"><span data-stu-id="f2523-227">Started</span></span>  | <span data-ttu-id="f2523-228">El origen acepta y procesa solicitudes de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f2523-228">The source accepts and processes sample requests.</span></span>                                                               |
| <span data-ttu-id="f2523-229">En pausa</span><span class="sxs-lookup"><span data-stu-id="f2523-229">Paused</span></span>   | <span data-ttu-id="f2523-230">El origen acepta solicitudes de ejemplo, pero no las procesa.</span><span class="sxs-lookup"><span data-stu-id="f2523-230">The source accepts sample requests, but does not process them.</span></span> <span data-ttu-id="f2523-231">Las solicitudes se ponen en cola hasta que se inicia el origen.</span><span class="sxs-lookup"><span data-stu-id="f2523-231">Requests are queued until the source is started.</span></span> |
| <span data-ttu-id="f2523-232">Detenido.</span><span class="sxs-lookup"><span data-stu-id="f2523-232">Stopped.</span></span> | <span data-ttu-id="f2523-233">El origen rechaza las solicitudes de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f2523-233">The source rejects sample requests.</span></span>                                                                             |



 

### <a name="start"></a><span data-ttu-id="f2523-234">Start</span><span class="sxs-lookup"><span data-stu-id="f2523-234">Start</span></span>

<span data-ttu-id="f2523-235">El método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) inicia el origen del medio.</span><span class="sxs-lookup"><span data-stu-id="f2523-235">The [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method starts the media source.</span></span> <span data-ttu-id="f2523-236">Toma los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="f2523-236">It takes the following parameters:</span></span>

-   <span data-ttu-id="f2523-237">Descriptor de presentación.</span><span class="sxs-lookup"><span data-stu-id="f2523-237">A presentation descriptor.</span></span>
-   <span data-ttu-id="f2523-238">Un GUID con formato de hora.</span><span class="sxs-lookup"><span data-stu-id="f2523-238">A time-format GUID.</span></span>
-   <span data-ttu-id="f2523-239">Posición inicial.</span><span class="sxs-lookup"><span data-stu-id="f2523-239">A start position.</span></span>

<span data-ttu-id="f2523-240">La aplicación debe obtener el descriptor de presentación llamando a [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) en el origen.</span><span class="sxs-lookup"><span data-stu-id="f2523-240">The application must obtain the presentation descriptor by calling [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) on the source.</span></span> <span data-ttu-id="f2523-241">No hay ningún mecanismo definido para validar un descriptor de presentación.</span><span class="sxs-lookup"><span data-stu-id="f2523-241">There is no defined mechanism for validating a presentation descriptor.</span></span> <span data-ttu-id="f2523-242">Si la aplicación especifica un descriptor de presentación incorrecto, los resultados son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="f2523-242">If the application specifies the wrong presentation descriptor, the results are undefined.</span></span>

<span data-ttu-id="f2523-243">El GUID de formato de hora especifica cómo interpretar la posición inicial.</span><span class="sxs-lookup"><span data-stu-id="f2523-243">The time-format GUID specifies how to interpret the starting position.</span></span> <span data-ttu-id="f2523-244">El formato estándar es unidades 100-nanosegundos (NS), indicado por GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="f2523-244">The standard format is 100-nanosecond (ns) units, indicated by GUID\_NULL.</span></span> <span data-ttu-id="f2523-245">Cada origen multimedia debe admitir 100 unidades NS.</span><span class="sxs-lookup"><span data-stu-id="f2523-245">Every media source must support 100-ns units.</span></span> <span data-ttu-id="f2523-246">Opcionalmente, un origen puede admitir otras unidades de tiempo, como el número de marco o el código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f2523-246">Optionally, a source can support other units of time, such as frame number or time code.</span></span> <span data-ttu-id="f2523-247">Sin embargo, no hay ninguna manera estándar de consultar un origen de medios para obtener la lista de formatos de hora que admite.</span><span class="sxs-lookup"><span data-stu-id="f2523-247">However, there is no standard way to query a media source for the list of time formats it supports.</span></span>

<span data-ttu-id="f2523-248">La posición inicial se proporciona como **PROPVARIANT**, lo que permite tipos de datos diferentes en función del formato de hora.</span><span class="sxs-lookup"><span data-stu-id="f2523-248">The start position is given as a **PROPVARIANT**, allowing for different data types depending on the time format.</span></span> <span data-ttu-id="f2523-249">Para 100-NS, el tipo **PROPVARIANT** es **VT \_ i8** o **VT \_ vacío**.</span><span class="sxs-lookup"><span data-stu-id="f2523-249">For 100-ns, the **PROPVARIANT** type is either **VT\_I8** or **VT\_EMPTY**.</span></span> <span data-ttu-id="f2523-250">Si **VT \_ i8**, **PROPVARIANT** contiene la posición inicial en 100-unidades NS.</span><span class="sxs-lookup"><span data-stu-id="f2523-250">If **VT\_I8**, the **PROPVARIANT** contains the start position in 100-ns units.</span></span> <span data-ttu-id="f2523-251">El valor **VT \_ vacío** tiene el significado especial "comenzar en la posición actual".</span><span class="sxs-lookup"><span data-stu-id="f2523-251">The value **VT\_EMPTY** has the special meaning "start at the current position."</span></span>

<span data-ttu-id="f2523-252">Implemente el método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="f2523-252">Implement the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method as follows:</span></span>

1.  <span data-ttu-id="f2523-253">Validar parámetros y estado:</span><span class="sxs-lookup"><span data-stu-id="f2523-253">Validate parameters and state:</span></span>
    -   <span data-ttu-id="f2523-254">Compruebe si hay parámetros **null** .</span><span class="sxs-lookup"><span data-stu-id="f2523-254">Check for **NULL** parameters.</span></span>
    -   <span data-ttu-id="f2523-255">Compruebe el GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="f2523-255">Check the time-format GUID.</span></span> <span data-ttu-id="f2523-256">Si el valor no es válido, se devuelve el **\_ formato de \_ \_ hora \_ no compatible con MF E**.</span><span class="sxs-lookup"><span data-stu-id="f2523-256">If the value is invalid, return **MF\_E\_UNSUPPORTED\_TIME\_FORMAT**.</span></span>
    -   <span data-ttu-id="f2523-257">Compruebe el tipo de datos de **PROPVARIANT** que contiene la posición de inicio.</span><span class="sxs-lookup"><span data-stu-id="f2523-257">Check the data type of the **PROPVARIANT** that holds the start position.</span></span>
    -   <span data-ttu-id="f2523-258">Valida la posición inicial.</span><span class="sxs-lookup"><span data-stu-id="f2523-258">Validate the start position.</span></span> <span data-ttu-id="f2523-259">Si no es válido, se devuelve **MF \_ E \_ INVALIDREQUEST**.</span><span class="sxs-lookup"><span data-stu-id="f2523-259">If invalid, return **MF\_E\_INVALIDREQUEST**.</span></span>
    -   <span data-ttu-id="f2523-260">Si el origen se ha cerrado, devuelva **el \_ \_ cierre MF E**.</span><span class="sxs-lookup"><span data-stu-id="f2523-260">If the source has been shut down, return **MF\_E\_SHUTDOWN**.</span></span>
2.  <span data-ttu-id="f2523-261">Si no se produce ningún error en el paso 1, poner en cola una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f2523-261">If no error occurs in step 1, queue an asynchronous operation.</span></span> <span data-ttu-id="f2523-262">Todo después de este paso se produce en un subproceso de cola de trabajo.</span><span class="sxs-lookup"><span data-stu-id="f2523-262">Everything after this step occurs on a work-queue thread.</span></span>
3.  <span data-ttu-id="f2523-263">Para cada flujo:</span><span class="sxs-lookup"><span data-stu-id="f2523-263">For each stream:</span></span>
    1.  <span data-ttu-id="f2523-264">Compruebe si la secuencia ya está activa desde una solicitud de [**Inicio**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) anterior.</span><span class="sxs-lookup"><span data-stu-id="f2523-264">Check if the stream is already active from a previous [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) request.</span></span>
    2.  <span data-ttu-id="f2523-265">Llame a [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) para comprobar si la aplicación seleccionó o anula la selección de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f2523-265">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to check whether the application selected or deselected the stream.</span></span>
    3.  <span data-ttu-id="f2523-266">Si ahora se anula la selección de una secuencia seleccionada anteriormente, vacíe cualquier ejemplo no entregado de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f2523-266">If a previously selected stream is now deselected, flush any undelivered samples for that stream.</span></span>
    4.  <span data-ttu-id="f2523-267">Si la secuencia está activa, el origen multimedia (no la secuencia) envía uno de los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="f2523-267">If the stream is active, the media source (not the stream) sends one of the following events:</span></span>
        -   <span data-ttu-id="f2523-268">Envía [MEUpdatedStream](meupdatedstream.md) si la secuencia estaba activa previamente.</span><span class="sxs-lookup"><span data-stu-id="f2523-268">It sends [MEUpdatedStream](meupdatedstream.md) if the stream was previously active.</span></span>
        -   <span data-ttu-id="f2523-269">De lo contrario, envía [MENewStream](menewstream.md).</span><span class="sxs-lookup"><span data-stu-id="f2523-269">Otherwise, it sends [MENewStream](menewstream.md).</span></span>

        <span data-ttu-id="f2523-270">En ambos eventos, los datos del evento son el puntero [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f2523-270">For both events, the event data is the [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) pointer for the stream.</span></span>
    5.  <span data-ttu-id="f2523-271">Si el origen se reinicia a partir del estado en pausa, puede que haya solicitudes de ejemplo pendientes.</span><span class="sxs-lookup"><span data-stu-id="f2523-271">If the source is restarting from the paused state, there might be pending sample requests.</span></span> <span data-ttu-id="f2523-272">Si es así, envíelos ahora.</span><span class="sxs-lookup"><span data-stu-id="f2523-272">If so, deliver these now.</span></span>
    6.  <span data-ttu-id="f2523-273">Si el origen está buscando una nueva posición, cada objeto de secuencia envía un evento [MEStreamSeeked](mestreamseeked.md) .</span><span class="sxs-lookup"><span data-stu-id="f2523-273">If the source is seeking to a new position, each stream object sends an [MEStreamSeeked](mestreamseeked.md) event.</span></span> <span data-ttu-id="f2523-274">De lo contrario, cada secuencia envía un evento [MEStreamStarted](mestreamstarted.md) .</span><span class="sxs-lookup"><span data-stu-id="f2523-274">Otherwise, each stream sends an [MEStreamStarted](mestreamstarted.md) event.</span></span>
4.  <span data-ttu-id="f2523-275">Si el origen está buscando una nueva posición, el origen multimedia envía un evento [MESourceSeeked](mesourceseeked.md) .</span><span class="sxs-lookup"><span data-stu-id="f2523-275">If the source is seeking to a new position, the media source sends an [MESourceSeeked](mesourceseeked.md) event.</span></span> <span data-ttu-id="f2523-276">De lo contrario, envía un evento [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="f2523-276">Otherwise, it sends an [MESourceStarted](mesourcestarted.md) event.</span></span>

<span data-ttu-id="f2523-277">Si se produce un error en cualquier momento después del paso 2, el origen envía un evento [MESourceStarted](mesourcestarted.md) con un código de error.</span><span class="sxs-lookup"><span data-stu-id="f2523-277">If an error occurs at any time after step 2, the source sends an [MESourceStarted](mesourcestarted.md) event with an error code.</span></span> <span data-ttu-id="f2523-278">Esto alerta a la aplicación de que el método de [**Inicio**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) produjo un error de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f2523-278">This alerts the application that the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method failed asynchronously.</span></span>

<span data-ttu-id="f2523-279">En el código siguiente se muestran los pasos 1 a 2:</span><span class="sxs-lookup"><span data-stu-id="f2523-279">The following code shows steps 1–2:</span></span>


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



<span data-ttu-id="f2523-280">En el ejemplo siguiente se muestran los pasos restantes:</span><span class="sxs-lookup"><span data-stu-id="f2523-280">The remaining steps are shown in the next example:</span></span>


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



### <a name="pause"></a><span data-ttu-id="f2523-281">Pausar</span><span class="sxs-lookup"><span data-stu-id="f2523-281">Pause</span></span>

<span data-ttu-id="f2523-282">El método [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) pone en pausa el origen del medio.</span><span class="sxs-lookup"><span data-stu-id="f2523-282">The [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method pauses the media source.</span></span> <span data-ttu-id="f2523-283">Implemente este método como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="f2523-283">Implement this method as follows:</span></span>

1.  <span data-ttu-id="f2523-284">Poner en cola una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f2523-284">Queue an asynchronous operation.</span></span>
2.  <span data-ttu-id="f2523-285">Cada flujo activo envía un evento [MEStreamPaused](mestreampaused.md) .</span><span class="sxs-lookup"><span data-stu-id="f2523-285">Each active stream sends an [MEStreamPaused](mestreampaused.md) event.</span></span>
3.  <span data-ttu-id="f2523-286">El origen de medios envía un evento [MESourcePaused](mesourcepaused.md) .</span><span class="sxs-lookup"><span data-stu-id="f2523-286">The media source sends an [MESourcePaused](mesourcepaused.md) event.</span></span>

<span data-ttu-id="f2523-287">Mientras está en pausa, el origen pone en cola las solicitudes de ejemplo sin procesarlas.</span><span class="sxs-lookup"><span data-stu-id="f2523-287">While paused, the source queues sample requests without processing them.</span></span> <span data-ttu-id="f2523-288">(Consulte [solicitudes de ejemplo](#sample-requests)).</span><span class="sxs-lookup"><span data-stu-id="f2523-288">(See [Sample Requests](#sample-requests).)</span></span>

### <a name="stop"></a><span data-ttu-id="f2523-289">Stop</span><span class="sxs-lookup"><span data-stu-id="f2523-289">Stop</span></span>

<span data-ttu-id="f2523-290">El método [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) detiene el origen del medio.</span><span class="sxs-lookup"><span data-stu-id="f2523-290">The [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method stops the media source.</span></span> <span data-ttu-id="f2523-291">Implemente este método como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="f2523-291">Implement this method as follows:</span></span>

1.  <span data-ttu-id="f2523-292">Poner en cola una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f2523-292">Queue an asynchronous operation.</span></span>
2.  <span data-ttu-id="f2523-293">Cada flujo activo envía un evento [MEStreamStopped](mestreamstopped.md) .</span><span class="sxs-lookup"><span data-stu-id="f2523-293">Each active stream sends an [MEStreamStopped](mestreamstopped.md) event.</span></span>
3.  <span data-ttu-id="f2523-294">Borre todos los ejemplos en cola y las solicitudes de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f2523-294">Clear all queued samples and sample requests.</span></span>
4.  <span data-ttu-id="f2523-295">El origen de medios envía un evento [MESourceStopped](mesourcestopped.md) .</span><span class="sxs-lookup"><span data-stu-id="f2523-295">The media source sends an [MESourceStopped](mesourcestopped.md) event.</span></span>

<span data-ttu-id="f2523-296">Mientras se detiene, el origen rechaza todas las solicitudes de ejemplos.</span><span class="sxs-lookup"><span data-stu-id="f2523-296">While stopped, the source rejects all requests for samples.</span></span>

<span data-ttu-id="f2523-297">Si el origen se detiene mientras una solicitud de e/s está en curso, la solicitud de e/s puede completarse después de que el origen entre en el estado de detención.</span><span class="sxs-lookup"><span data-stu-id="f2523-297">If the source is stopped while an I/O request is in progress, the I/O request might complete after the source enters the stopped state.</span></span> <span data-ttu-id="f2523-298">En ese caso, el origen debe descartar el resultado de la solicitud de e/s.</span><span class="sxs-lookup"><span data-stu-id="f2523-298">In that case, the source should discard the result of that I/O request.</span></span>

## <a name="sample-requests"></a><span data-ttu-id="f2523-299">Solicitudes de ejemplo</span><span class="sxs-lookup"><span data-stu-id="f2523-299">Sample Requests</span></span>

<span data-ttu-id="f2523-300">Media Foundation usar un modelo de *extracción* , en el que la canalización solicita muestras del origen de los medios.</span><span class="sxs-lookup"><span data-stu-id="f2523-300">Media Foundation use a *pull* model, in which the pipeline requests samples from the media source.</span></span> <span data-ttu-id="f2523-301">Esto difiere del modelo usado por DirectShow, en el que los orígenes "inserciones" son ejemplos.</span><span class="sxs-lookup"><span data-stu-id="f2523-301">This differs from the model used by DirectShow, in which the sources "pushes" samples.</span></span>

<span data-ttu-id="f2523-302">Para solicitar un nuevo ejemplo, la canalización Media Foundation llama a [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span><span class="sxs-lookup"><span data-stu-id="f2523-302">To request a new sample, the Media Foundation pipeline calls [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span></span> <span data-ttu-id="f2523-303">Este método toma un puntero **IUnknown** que representa un objeto de *token* .</span><span class="sxs-lookup"><span data-stu-id="f2523-303">This method takes an **IUnknown** pointer that represents a *token* object.</span></span> <span data-ttu-id="f2523-304">La implementación del objeto de token es hasta el autor de la llamada; simplemente proporciona una manera para que el llamador realice un seguimiento de las solicitudes de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f2523-304">The implementation of the token object is up to the caller; it simply provides a way for the caller to track sample requests.</span></span> <span data-ttu-id="f2523-305">El parámetro token también puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="f2523-305">The token parameter can also be **NULL**.</span></span>

<span data-ttu-id="f2523-306">Suponiendo que el origen usa solicitudes de e/s asincrónicas para leer los datos, la generación de la muestra no se sincronizará con las solicitudes de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f2523-306">Assuming the source uses asynchronous I/O requests to read data, sample generation will not be synchronized with sample requests.</span></span> <span data-ttu-id="f2523-307">Para sincronizar las solicitudes de ejemplo con la generación de ejemplo, un origen multimedia hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f2523-307">To synchronize sample requests with sample generation, a media source does the following:</span></span>

1.  <span data-ttu-id="f2523-308">Los tokens de solicitud se colocan en una cola.</span><span class="sxs-lookup"><span data-stu-id="f2523-308">Request tokens are placed on a queue.</span></span>
2.  <span data-ttu-id="f2523-309">A medida que se generan ejemplos, se colocan en una segunda cola.</span><span class="sxs-lookup"><span data-stu-id="f2523-309">As samples are generated, they are placed on a second queue.</span></span>
3.  <span data-ttu-id="f2523-310">El origen multimedia completa una solicitud de ejemplo mediante la extracción de un token de solicitud de la primera cola y un ejemplo de la segunda cola.</span><span class="sxs-lookup"><span data-stu-id="f2523-310">The media source completes a sample request by pulling a request token from the first queue and a sample from the second queue.</span></span>
4.  <span data-ttu-id="f2523-311">El origen de medios envía un evento MEMediaSample.</span><span class="sxs-lookup"><span data-stu-id="f2523-311">The media source sends an MEMediaSample event.</span></span> <span data-ttu-id="f2523-312">El evento contiene un puntero al ejemplo y el ejemplo contiene un puntero al token.</span><span class="sxs-lookup"><span data-stu-id="f2523-312">The event contains a pointer to the sample, and the sample contains a pointer to the token.</span></span>

<span data-ttu-id="f2523-313">En el diagrama siguiente se muestra la relación entre el evento [MEMediaSample](memediasample.md) , el ejemplo y el token de solicitud.</span><span class="sxs-lookup"><span data-stu-id="f2523-313">The following diagram shows the relationship between the [MEMediaSample](memediasample.md) event, the sample, and the request token.</span></span>

![diagrama que muestra memediasample y una cola de ejemplo que apunta a imfsample; imfsample y el punto de cola de solicitudes a IUnknown](images/mediasourceimpl01.png)

<span data-ttu-id="f2523-315">El origen MPEG-1 de ejemplo implementa este proceso como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="f2523-315">The example MPEG-1 source implements this process as follows:</span></span>

1.  <span data-ttu-id="f2523-316">El método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) coloca la solicitud en una cola FIFO.</span><span class="sxs-lookup"><span data-stu-id="f2523-316">The [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method puts the request on a FIFO queue.</span></span>
2.  <span data-ttu-id="f2523-317">A medida que se completan las solicitudes de e/s, el origen multimedia crea nuevos ejemplos y los coloca en una segunda cola FIFO.</span><span class="sxs-lookup"><span data-stu-id="f2523-317">As I/O requests are completed, the media source creates new samples and puts them on a second FIFO queue.</span></span> <span data-ttu-id="f2523-318">(Esta cola tiene un tamaño máximo, para evitar que el origen se lea demasiado lejos).</span><span class="sxs-lookup"><span data-stu-id="f2523-318">(This queue has a maximum size, to prevent the source from reading too far ahead.)</span></span>
3.  <span data-ttu-id="f2523-319">Siempre que ambas colas tengan al menos un elemento (una solicitud y una muestra), el origen multimedia completa la primera solicitud de la cola de solicitudes mediante el envío de la primera muestra de la cola de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f2523-319">Whenever both of these queues have at least one item (one request and one sample), the media source completes the first request from the request queue by sending out the first sample from the sample queue.</span></span>
4.  <span data-ttu-id="f2523-320">Para ofrecer un ejemplo, el objeto de secuencia (no el objeto de origen) envía un evento [MEMediaSample](memediasample.md) .</span><span class="sxs-lookup"><span data-stu-id="f2523-320">To deliver a sample, the stream object (not the source object) sends an [MEMediaSample](memediasample.md) event.</span></span>
    -   <span data-ttu-id="f2523-321">Los datos de evento son un puntero a la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f2523-321">The event data is a pointer to the sample's [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span>
    -   <span data-ttu-id="f2523-322">Si la solicitud incluye un token, adjunte el token al ejemplo estableciendo el atributo [**de \_ token MFSampleExtension**](mfsampleextension-token-attribute.md) en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f2523-322">If the request included a token, attach the token to the sample by setting the [**MFSampleExtension\_Token**](mfsampleextension-token-attribute.md) attribute on the sample.</span></span>

<span data-ttu-id="f2523-323">En este momento, hay tres posibilidades:</span><span class="sxs-lookup"><span data-stu-id="f2523-323">At this point, there are three possibilities:</span></span>

-   <span data-ttu-id="f2523-324">Hay otro ejemplo en la cola de ejemplo, pero no hay ninguna solicitud coincidente.</span><span class="sxs-lookup"><span data-stu-id="f2523-324">There is another sample in the sample queue, but no matching request.</span></span>
-   <span data-ttu-id="f2523-325">Hay una solicitud, pero no muestra ningún ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f2523-325">There is a request, but no sample.</span></span>
-   <span data-ttu-id="f2523-326">Ambas colas están vacías; no hay ningún ejemplo y ninguna solicitud.</span><span class="sxs-lookup"><span data-stu-id="f2523-326">Both queues are empty; there are no samples and no requests.</span></span>

<span data-ttu-id="f2523-327">Si la cola de ejemplo está vacía, el origen comprueba el final de la secuencia (vea [final de la secuencia](#end-of-stream)).</span><span class="sxs-lookup"><span data-stu-id="f2523-327">If the sample queue is empty, the source checks for the end of the stream (see [End of Stream](#end-of-stream)).</span></span> <span data-ttu-id="f2523-328">De lo contrario, inicia otra solicitud de e/s para los datos.</span><span class="sxs-lookup"><span data-stu-id="f2523-328">Otherwise, it starts another I/O request for data.</span></span> <span data-ttu-id="f2523-329">Si se produce algún error durante este proceso, el flujo envía un evento [MEError](meerror.md) .</span><span class="sxs-lookup"><span data-stu-id="f2523-329">If any error occurs during this process, the stream sends an [MEError](meerror.md) event.</span></span>

<span data-ttu-id="f2523-330">El código siguiente implementa el método [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) :</span><span class="sxs-lookup"><span data-stu-id="f2523-330">The following code implements the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method:</span></span>


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



<span data-ttu-id="f2523-331">El `DispatchSamples` método extrae ejemplos de la cola de ejemplo, los hace coincidir con solicitudes de ejemplo pendientes y pone en cola eventos [MEMediaSample](memediasample.md) :</span><span class="sxs-lookup"><span data-stu-id="f2523-331">The `DispatchSamples` method pulls samples from the sample queue, matches them with pending sample requests, and queues [MEMediaSample](memediasample.md) events:</span></span>


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



<span data-ttu-id="f2523-332">`DispatchSamples`Se llama al método en las siguientes circunstancias:</span><span class="sxs-lookup"><span data-stu-id="f2523-332">The `DispatchSamples` method is called in the following circumstances:</span></span>

-   <span data-ttu-id="f2523-333">Dentro del método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="f2523-333">Inside the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>
-   <span data-ttu-id="f2523-334">Cuando el origen de medios se reinicia a partir del estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="f2523-334">When the media source restarts from the paused state.</span></span>
-   <span data-ttu-id="f2523-335">Cuando se completa una solicitud de e/s.</span><span class="sxs-lookup"><span data-stu-id="f2523-335">When an I/O request completes.</span></span>

## <a name="end-of-stream"></a><span data-ttu-id="f2523-336">Final de la secuencia</span><span class="sxs-lookup"><span data-stu-id="f2523-336">End of Stream</span></span>

<span data-ttu-id="f2523-337">Cuando un flujo no tiene más datos y se han entregado todos los ejemplos de ese flujo, los objetos de secuencia envían un evento [MEEndOfStream](meendofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="f2523-337">When a stream has no more data, and all of the samples for that stream have been delivered, the stream objects sends an [MEEndOfStream](meendofstream.md) event.</span></span>

<span data-ttu-id="f2523-338">Cuando se realizan todas las secuencias activas, el origen de medios envía un evento [MEEndOfPresentation](meendofpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="f2523-338">When all of the active streams are done, the media source sends an [MEEndOfPresentation](meendofpresentation.md) event.</span></span>

## <a name="asynchronous-operations"></a><span data-ttu-id="f2523-339">Operaciones asincrónicas</span><span class="sxs-lookup"><span data-stu-id="f2523-339">Asynchronous Operations</span></span>

<span data-ttu-id="f2523-340">Quizás la parte más difícil de escribir un origen multimedia es comprender el Media Foundation modelo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="f2523-340">Perhaps the hardest part of writing a media source is understanding the Media Foundation asynchronous model.</span></span>

<span data-ttu-id="f2523-341">Todos los métodos de un origen de medios que controlan el streaming son asíncronos.</span><span class="sxs-lookup"><span data-stu-id="f2523-341">All of the methods on a media source that control streaming are asynchronous.</span></span> <span data-ttu-id="f2523-342">En cada caso, el método realiza algunas validaciones iniciales, como comprobar los parámetros.</span><span class="sxs-lookup"><span data-stu-id="f2523-342">In each case, the method does some initial validation, such as checking parameters.</span></span> <span data-ttu-id="f2523-343">Después, el origen envía el resto del trabajo a una cola de trabajo.</span><span class="sxs-lookup"><span data-stu-id="f2523-343">The source then dispatches the rest of the work to a work queue.</span></span> <span data-ttu-id="f2523-344">Una vez finalizada la operación, el origen del medio envía un evento de vuelta al llamador, a través de la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) del origen del medio.</span><span class="sxs-lookup"><span data-stu-id="f2523-344">After the operation completes, the media source sends an event back to the caller, through the media source's [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="f2523-345">Por lo tanto, es importante entender las colas de trabajos.</span><span class="sxs-lookup"><span data-stu-id="f2523-345">It is therefore important to understand work queues.</span></span>

<span data-ttu-id="f2523-346">Para colocar un elemento en una cola de trabajo, puede llamar a [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) o [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex).</span><span class="sxs-lookup"><span data-stu-id="f2523-346">To put an item on a work queue, you can call either [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) or [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex).</span></span> <span data-ttu-id="f2523-347">El origen MPEG-1 tiene lugar para usar **MFPutWorkItem**, pero las dos funciones hacen lo mismo.</span><span class="sxs-lookup"><span data-stu-id="f2523-347">The MPEG-1 source happens to use **MFPutWorkItem**, but the two functions do the same thing.</span></span> <span data-ttu-id="f2523-348">La función **MFPutWorkItem** toma los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="f2523-348">The **MFPutWorkItem** function takes the following parameters:</span></span>

-   <span data-ttu-id="f2523-349">Valor **DWORD** que identifica la cola de trabajo.</span><span class="sxs-lookup"><span data-stu-id="f2523-349">A **DWORD** value that identifies the work queue.</span></span> <span data-ttu-id="f2523-350">Puede crear una cola de trabajo privada o usar **el \_ \_ \_ estándar de cola de devolución de llamada MFASYNC**.</span><span class="sxs-lookup"><span data-stu-id="f2523-350">You can create a private work queue or use **MFASYNC\_CALLBACK\_QUEUE\_STANDARD**.</span></span>
-   <span data-ttu-id="f2523-351">Puntero a la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="f2523-351">A pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="f2523-352">Esta interfaz de devolución de llamada se invoca para realizar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f2523-352">This callback interface is invoked to perform the work.</span></span>
-   <span data-ttu-id="f2523-353">Un objeto de estado opcional, que debe implementar **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="f2523-353">An optional state object, which must implement **IUnknown**.</span></span>

<span data-ttu-id="f2523-354">Una o más subprocesos de trabajo que reenvían continuamente el siguiente elemento de trabajo de la cola prestan servicio a la cola de trabajo e invocan el método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) de la interfaz de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f2523-354">The work queue is serviced by one or more worker threads that continuously pull the next work item from the queue and invoke the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of the callback interface.</span></span>

<span data-ttu-id="f2523-355">No se garantiza que los elementos de trabajo se ejecuten en el mismo orden en que se colocan en la cola.</span><span class="sxs-lookup"><span data-stu-id="f2523-355">Work items are not guaranteed to execute in the same order that you put them on the queue.</span></span> <span data-ttu-id="f2523-356">Recuerde que más de un subproceso puede dar servicio a la misma cola de trabajo, por lo que [**invocar**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) llamadas puede superponerse o producirse sin orden.</span><span class="sxs-lookup"><span data-stu-id="f2523-356">Remember that more than one thread can service the same work queue, so [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) calls can overlap or occur out of order.</span></span> <span data-ttu-id="f2523-357">Por lo tanto, depende del origen de los medios mantener el estado interno correcto, enviando los elementos de la cola de trabajo en el orden correcto.</span><span class="sxs-lookup"><span data-stu-id="f2523-357">Therefore, it is up to the media source to maintain the correct internal state, by submitting work queue items in the right order.</span></span> <span data-ttu-id="f2523-358">Solo cuando se completa la operación anterior, el origen inicia la siguiente operación.</span><span class="sxs-lookup"><span data-stu-id="f2523-358">Only when the previous operation is complete does the source start the next operation.</span></span>

<span data-ttu-id="f2523-359">Para representar las operaciones pendientes, el origen MPEG-1 define una clase denominada `SourceOp` :</span><span class="sxs-lookup"><span data-stu-id="f2523-359">To represent pending operations, the MPEG-1 source defines a class named `SourceOp`:</span></span>


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



<span data-ttu-id="f2523-360">La `Operation` enumeración identifica qué operación está pendiente.</span><span class="sxs-lookup"><span data-stu-id="f2523-360">The `Operation` enumeration identifies which operation is pending.</span></span> <span data-ttu-id="f2523-361">La clase también contiene un **PROPVARIANT** para transmitir los datos adicionales para la operación.</span><span class="sxs-lookup"><span data-stu-id="f2523-361">The class also contains a **PROPVARIANT** to convey any additional data for the operation.</span></span>

### <a name="operation-queue"></a><span data-ttu-id="f2523-362">Cola de operaciones</span><span class="sxs-lookup"><span data-stu-id="f2523-362">Operation Queue</span></span>

<span data-ttu-id="f2523-363">Para serializar las operaciones, el origen de medios mantiene una cola de `SourceOp` objetos.</span><span class="sxs-lookup"><span data-stu-id="f2523-363">To serialize operations, the media source maintains a queue of `SourceOp` objects.</span></span> <span data-ttu-id="f2523-364">Usa una clase auxiliar para administrar la cola:</span><span class="sxs-lookup"><span data-stu-id="f2523-364">It uses a helper class to manage the queue:</span></span>


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



<span data-ttu-id="f2523-365">La `OpQueue` clase está diseñada para ser heredada por el componente que realiza los elementos de trabajo asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="f2523-365">The `OpQueue` class is designed to be inherited by the component that performs asynchronous work items.</span></span> <span data-ttu-id="f2523-366">El parámetro de plantilla *\_ tipo de operación* es el tipo de objeto que se usa para representar los elementos de trabajo en la cola; en este caso, el *\_ tipo de operación* será `SourceOp` .</span><span class="sxs-lookup"><span data-stu-id="f2523-366">The *OP\_TYPE* template parameter is the object type used to represent work items in the queue—in this case, *OP\_TYPE* will be `SourceOp`.</span></span> <span data-ttu-id="f2523-367">La `OpQueue` clase implementa los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f2523-367">The `OpQueue` class implements the following methods:</span></span>

-   <span data-ttu-id="f2523-368">`QueueOperation` coloca un nuevo elemento en la cola.</span><span class="sxs-lookup"><span data-stu-id="f2523-368">`QueueOperation` puts a new item on the queue.</span></span>
-   <span data-ttu-id="f2523-369">`ProcessQueue` envía la siguiente operación desde la cola.</span><span class="sxs-lookup"><span data-stu-id="f2523-369">`ProcessQueue` dispatches the next operation from the queue.</span></span> <span data-ttu-id="f2523-370">Este método es asincrónico.</span><span class="sxs-lookup"><span data-stu-id="f2523-370">This method is asynchronous.</span></span>
-   <span data-ttu-id="f2523-371">`ProcessQueueAsync` completa el `ProcessQueue` método asincrónico.</span><span class="sxs-lookup"><span data-stu-id="f2523-371">`ProcessQueueAsync` completes the asynchronous `ProcessQueue` method.</span></span>

<span data-ttu-id="f2523-372">La clase derivada debe implementar otros dos métodos:</span><span class="sxs-lookup"><span data-stu-id="f2523-372">Another two methods must be implemented by the derived class:</span></span>

-   <span data-ttu-id="f2523-373">`ValidateOperation` comprueba si es válido realizar una operación especificada, dado el estado actual del origen de los medios.</span><span class="sxs-lookup"><span data-stu-id="f2523-373">`ValidateOperation` checks whether it is valid to perform a specified operation, given the current state of the media source.</span></span>
-   <span data-ttu-id="f2523-374">`DispatchOperation` lleva a cabo el elemento de trabajo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="f2523-374">`DispatchOperation` carries out the asynchronous work item.</span></span>

<span data-ttu-id="f2523-375">La cola de operaciones se utiliza como sigue:</span><span class="sxs-lookup"><span data-stu-id="f2523-375">The operation queue is used as follows:</span></span>

1.  <span data-ttu-id="f2523-376">La canalización Media Foundation llama a un método asincrónico en el origen multimedia, como [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="f2523-376">The Media Foundation pipeline calls an asynchronous method on the media source, such as [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>
2.  <span data-ttu-id="f2523-377">El método asincrónico llama a `QueueOperation` , que coloca la operación de [**Inicio**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) en la cola y llama a `ProcessQueue` (en el formulario de un `SourceOp` objeto).</span><span class="sxs-lookup"><span data-stu-id="f2523-377">The asynchronous method calls `QueueOperation`, which puts the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) operation on the queue and calls `ProcessQueue` (in the form of a `SourceOp` object).</span></span>
3.  <span data-ttu-id="f2523-378">`ProcessQueue` llama a [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span><span class="sxs-lookup"><span data-stu-id="f2523-378">`ProcessQueue` calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span></span>
4.  <span data-ttu-id="f2523-379">El subproceso de cola de trabajo llama a `ProcessQueueAsync` .</span><span class="sxs-lookup"><span data-stu-id="f2523-379">The work-queue thread calls `ProcessQueueAsync`.</span></span>
5.  <span data-ttu-id="f2523-380">El `ProcessQueueAsync` método llama a `ValidateOperation` y a `DispatchOperation` .</span><span class="sxs-lookup"><span data-stu-id="f2523-380">The `ProcessQueueAsync` method calls `ValidateOperation` and `DispatchOperation`.</span></span>

<span data-ttu-id="f2523-381">El código siguiente pone en cola una nueva operación en el origen MPEG-1:</span><span class="sxs-lookup"><span data-stu-id="f2523-381">The following code queues a new operation on the MPEG-1 source:</span></span>


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



<span data-ttu-id="f2523-382">El código siguiente procesa la cola:</span><span class="sxs-lookup"><span data-stu-id="f2523-382">The following code processes the queue:</span></span>


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



<span data-ttu-id="f2523-383">El `ValidateOperation` método comprueba si el origen MPEG-1 puede enviar la siguiente operación en la cola.</span><span class="sxs-lookup"><span data-stu-id="f2523-383">The `ValidateOperation` method checks whether the MPEG-1 source can dispatch the next operation in the queue.</span></span> <span data-ttu-id="f2523-384">Si hay otra operación en curso, `ValidateOperation` devuelve **MF \_ E \_ NOTACCEPTING**.</span><span class="sxs-lookup"><span data-stu-id="f2523-384">If another operation is in progress, `ValidateOperation` returns **MF\_E\_NOTACCEPTING**.</span></span> <span data-ttu-id="f2523-385">Esto garantiza que `DispatchOperation` no se llama mientras haya otra operación pendiente.</span><span class="sxs-lookup"><span data-stu-id="f2523-385">This ensures that `DispatchOperation` is not called while there is another operation pending.</span></span>


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



<span data-ttu-id="f2523-386">El método DispatchOperation cambia en el tipo de operación:</span><span class="sxs-lookup"><span data-stu-id="f2523-386">The DispatchOperation method switches on the operation type:</span></span>


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



<span data-ttu-id="f2523-387">En resumen:</span><span class="sxs-lookup"><span data-stu-id="f2523-387">To summarize:</span></span>

1.  <span data-ttu-id="f2523-388">La canalización llama a un método asincrónico, como [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="f2523-388">The pipeline calls an asynchronous method, such as [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>
2.  <span data-ttu-id="f2523-389">El método asincrónico llama a `OpQueue::QueueOperation` , pasando un puntero a un `SourceOp` objeto.</span><span class="sxs-lookup"><span data-stu-id="f2523-389">The asynchronous method calls `OpQueue::QueueOperation`, passing in a pointer to a `SourceOp` object.</span></span>
3.  <span data-ttu-id="f2523-390">El `QueueOperation` método coloca la operación en la cola *m \_ OpQueue* y llama a `OpQueue::ProcessQueue` .</span><span class="sxs-lookup"><span data-stu-id="f2523-390">The `QueueOperation` method puts the operation on the *m\_OpQueue* queue and calls `OpQueue::ProcessQueue`.</span></span>
4.  <span data-ttu-id="f2523-391">El `ProcessQueue` método llama a [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span><span class="sxs-lookup"><span data-stu-id="f2523-391">The `ProcessQueue` method calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span></span> <span data-ttu-id="f2523-392">Desde este punto, todo sucede en un subproceso de cola de trabajo Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f2523-392">From this point, everything happens on a Media Foundation work-queue thread.</span></span> <span data-ttu-id="f2523-393">El método asincrónico vuelve al llamador.</span><span class="sxs-lookup"><span data-stu-id="f2523-393">The asynchronous method returns to the caller.</span></span>
5.  <span data-ttu-id="f2523-394">El subproceso de cola de trabajo llama al `OpQueue::ProcessQueueAsync` método.</span><span class="sxs-lookup"><span data-stu-id="f2523-394">The work-queue thread calls the `OpQueue::ProcessQueueAsync` method.</span></span>
6.  <span data-ttu-id="f2523-395">El `ProcessQueueAsync` método llama `MPEG1Source:ValidateOperation` a para validar la operación.</span><span class="sxs-lookup"><span data-stu-id="f2523-395">The `ProcessQueueAsync` method calls `MPEG1Source:ValidateOperation` to validate the operation.</span></span>
7.  <span data-ttu-id="f2523-396">El `ProcessQueueAsync` método llama `MPEG1Source::DispatchOperation` a para procesar la operación.</span><span class="sxs-lookup"><span data-stu-id="f2523-396">The `ProcessQueueAsync` method calls `MPEG1Source::DispatchOperation` to process the operation.</span></span>

<span data-ttu-id="f2523-397">Este diseño tiene varias ventajas:</span><span class="sxs-lookup"><span data-stu-id="f2523-397">There are several benefits to this design:</span></span>

-   <span data-ttu-id="f2523-398">Los métodos son asincrónicos, por lo que no bloquean el subproceso de la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="f2523-398">Methods are asynchronous, so they do not block the calling application's thread.</span></span>
-   <span data-ttu-id="f2523-399">Las operaciones se envían en un subproceso de cola de trabajo Media Foundation, que se comparte entre los componentes de canalización.</span><span class="sxs-lookup"><span data-stu-id="f2523-399">Operations are dispatched on a Media Foundation work-queue thread, which is shared among pipeline components.</span></span> <span data-ttu-id="f2523-400">Por consiguiente, el origen de medios no crea su propio subproceso, lo que reduce el número total de subprocesos que se crean.</span><span class="sxs-lookup"><span data-stu-id="f2523-400">Therefore, the media source does not create its own thread, reducing the total number of threads that are created.</span></span>
-   <span data-ttu-id="f2523-401">El origen multimedia no se bloquea mientras se espera a que se completen las operaciones.</span><span class="sxs-lookup"><span data-stu-id="f2523-401">The media source does not block while waiting for operations to complete.</span></span> <span data-ttu-id="f2523-402">Esto reduce la posibilidad de que un origen multimedia cause accidentalmente un interbloqueo y ayuda a reducir el cambio de contexto.</span><span class="sxs-lookup"><span data-stu-id="f2523-402">This reduces the chance that a media source will accidentally cause a deadlock, and helps to reduce context switching.</span></span>
-   <span data-ttu-id="f2523-403">El origen multimedia puede usar la e/s asincrónica para leer el archivo de código fuente (llamando a [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)).</span><span class="sxs-lookup"><span data-stu-id="f2523-403">The media source can use asynchronous I/O to read the source file (by calling [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)).</span></span> <span data-ttu-id="f2523-404">No es necesario que el origen de medios se bloquee mientras se espera la rutina de e/s.</span><span class="sxs-lookup"><span data-stu-id="f2523-404">The media source does not need to block while waiting for I/O routine complete.</span></span>

<span data-ttu-id="f2523-405">Si sigue el patrón que se muestra en el ejemplo de SDK, puede centrarse en los detalles concretos de su origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="f2523-405">If you follow the pattern shown in the SDK sample, you can focus on the particular details of your media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2523-406">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f2523-406">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2523-407">Orígenes multimedia</span><span class="sxs-lookup"><span data-stu-id="f2523-407">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="f2523-408">Escritura de un origen de medios personalizado</span><span class="sxs-lookup"><span data-stu-id="f2523-408">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)
</dt> </dl>

 

 



