---
description: En este tema se describe cómo usar la API de impresión XPS para imprimir desde una aplicación de Windows.
ms.assetid: 3d7ab169-412c-434f-a865-4da4af370eaf
title: 'Cómo: imprimir con la API de impresión XPS'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4be5f083fb31eccaf2dc4b555435bd15a7fb45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912154"
---
# <a name="how-to-print-with-the-xps-print-api"></a><span data-ttu-id="b4606-103">Cómo: imprimir con la API de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="b4606-103">How To: Print with the XPS Print API</span></span>

<span data-ttu-id="b4606-104">En este tema se describe cómo usar la [API de impresión XPS](xpsprint-api.md) para imprimir desde una aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="b4606-104">This topic describes how to use the [XPS Print API](xpsprint-api.md) to print from a Windows application.</span></span>

<span data-ttu-id="b4606-105">La [API de impresión XPS](xpsprint-api.md) permite a las aplicaciones Windows nativas imprimir documentos XPS.</span><span class="sxs-lookup"><span data-stu-id="b4606-105">The [XPS Print API](xpsprint-api.md) enables native Windows applications to print XPS documents.</span></span> <span data-ttu-id="b4606-106">Una aplicación puede crear un documento XPS mediante la [API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b4606-106">An application can create an XPS document by using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span></span> <span data-ttu-id="b4606-107">El tema de ayuda [tareas comunes de programación de documentos XPS](/previous-versions/windows/desktop/dd316968(v=vs.85)) describe cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="b4606-107">The [Common XPS Document Programming Tasks](/previous-versions/windows/desktop/dd316968(v=vs.85)) help topic describes how to do this.</span></span> <span data-ttu-id="b4606-108">Una vez creado un documento XPS, la aplicación puede usar la API de impresión XPS para imprimirlo.</span><span class="sxs-lookup"><span data-stu-id="b4606-108">Once an XPS document has been created, the application can use the XPS Print API to print it.</span></span>

<span data-ttu-id="b4606-109">El uso de la [API de impresión XPS](xpsprint-api.md) para imprimir un documento desde una aplicación conlleva los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="b4606-109">Using the [XPS Print API](xpsprint-api.md) to print a document from an application involves the following steps.</span></span>

-   [<span data-ttu-id="b4606-110">Inicializar interfaz COM</span><span class="sxs-lookup"><span data-stu-id="b4606-110">Initialize COM Interface</span></span>](#initialize-com-interface)
-   [<span data-ttu-id="b4606-111">Crear un evento de finalización</span><span class="sxs-lookup"><span data-stu-id="b4606-111">Create a Completion Event</span></span>](#create-a-completion-event)
-   [<span data-ttu-id="b4606-112">Iniciar un trabajo de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="b4606-112">Start an XPS Print Job</span></span>](#start-an-xps-print-job)
-   [<span data-ttu-id="b4606-113">Creación de una interfaz IXpsOMPackageWriter</span><span class="sxs-lookup"><span data-stu-id="b4606-113">Create an IXpsOMPackageWriter Interface</span></span>](#create-an-ixpsompackagewriter-interface)
-   [<span data-ttu-id="b4606-114">Cierre la interfaz IXpsOMPackageWriter</span><span class="sxs-lookup"><span data-stu-id="b4606-114">Close the IXpsOMPackageWriter Interface</span></span>](#close-the-ixpsompackagewriter-interface)
-   [<span data-ttu-id="b4606-115">Cerrar la secuencia de trabajo de impresión</span><span class="sxs-lookup"><span data-stu-id="b4606-115">Close the Print Job Stream</span></span>](#close-the-print-job-stream)
-   [<span data-ttu-id="b4606-116">Esperar al evento de finalización</span><span class="sxs-lookup"><span data-stu-id="b4606-116">Wait for the Completion Event</span></span>](#wait-for-the-completion-event)
-   [<span data-ttu-id="b4606-117">Liberación de recursos</span><span class="sxs-lookup"><span data-stu-id="b4606-117">Release Resources</span></span>](#release-resources)

<span data-ttu-id="b4606-118">La [API de impresión XPS](xpsprint-api.md) requiere un documento XPS para imprimir.</span><span class="sxs-lookup"><span data-stu-id="b4606-118">The [XPS Print API](xpsprint-api.md) requires an XPS document to print.</span></span> <span data-ttu-id="b4606-119">En el ejemplo siguiente, el documento XPS se crea cuando se envía a la impresora mediante la API de impresión XPS.</span><span class="sxs-lookup"><span data-stu-id="b4606-119">In the following example, the XPS document is created as it is sent to the printer by the XPS Print API.</span></span> <span data-ttu-id="b4606-120">También es posible crear un documento XPS sin enviarlo a una impresora mediante la [API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) y mantenerlo como un OM XPS o guardando el OM XPS como un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="b4606-120">It is also possible to create an XPS document without sending it to a printer by using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) and maintaining it as an XPS OM or by saving the XPS OM as an XPS document.</span></span> <span data-ttu-id="b4606-121">Para obtener más información sobre el uso de un OM XPS, consulte la API de documentos XPS.</span><span class="sxs-lookup"><span data-stu-id="b4606-121">For more information about using an XPS OM, see the XPS Document API.</span></span>

### <a name="initialize-com-interface"></a><span data-ttu-id="b4606-122">Inicializar interfaz COM</span><span class="sxs-lookup"><span data-stu-id="b4606-122">Initialize COM Interface</span></span>

<span data-ttu-id="b4606-123">Inicialice la interfaz COM, si la aplicación aún no lo ha hecho.</span><span class="sxs-lookup"><span data-stu-id="b4606-123">Initialize the COM interface, if the application has not already done so.</span></span>


```C++
    // Initialize the COM interface, if the application has not 
    //  already done so.
    if (FAILED(hr = CoInitializeEx(0, COINIT_MULTITHREADED)))
    {
        fwprintf(stderr, 
            L"ERROR: CoInitializeEx failed with HRESULT 0x%X\n", hr);
        return 1;
    }
```



### <a name="create-a-completion-event"></a><span data-ttu-id="b4606-124">Crear un evento de finalización</span><span class="sxs-lookup"><span data-stu-id="b4606-124">Create a Completion Event</span></span>

<span data-ttu-id="b4606-125">Crear un evento de finalización, que la [API de impresión XPS](xpsprint-api.md) usa para notificar a la aplicación cuando el administrador de trabajos de impresión ha recibido todo el documento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b4606-125">Create a completion event, which the [XPS Print API](xpsprint-api.md) uses to notify the application when the print spooler has received the entire document from the application.</span></span> <span data-ttu-id="b4606-126">La API de impresión XPS también admite un evento de progreso para que una aplicación pueda conocer la actividad de la cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="b4606-126">The XPS Print API also supports a progress event so an application can know about other spooling activity.</span></span>


```C++
        // Create the completion event
        completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
        if (!completionEvent)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            fwprintf(stderr, 
                L"ERROR: Could not create completion event: %08X\n", hr);
        }
```



### <a name="start-an-xps-print-job"></a><span data-ttu-id="b4606-127">Iniciar un trabajo de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="b4606-127">Start an XPS Print Job</span></span>

<span data-ttu-id="b4606-128">Inicie un trabajo de impresión XPS llamando a [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).</span><span class="sxs-lookup"><span data-stu-id="b4606-128">Start an XPS print job by calling [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).</span></span> <span data-ttu-id="b4606-129">**StartXpsPrintJob** devuelve un flujo en el que la aplicación enviará el documento que se va a imprimir.</span><span class="sxs-lookup"><span data-stu-id="b4606-129">**StartXpsPrintJob** returns a stream into which the application will send the document to be printed.</span></span>


```C++
        // Start an XPS Print Job
        if (FAILED(hr = StartXpsPrintJob(
                    printerName,
                    NULL,
                    NULL,
                    NULL,
                    completionEvent,
                    NULL,
                    0,
                    &job,
                    &jobStream,
                    NULL
                    )))
        {
            fwprintf(stderr, 
                L"ERROR: Could not start XPS print job: %08X\n", hr);
        }
```



### <a name="create-an-ixpsompackagewriter-interface"></a><span data-ttu-id="b4606-130">Creación de una interfaz IXpsOMPackageWriter</span><span class="sxs-lookup"><span data-stu-id="b4606-130">Create an IXpsOMPackageWriter Interface</span></span>

<span data-ttu-id="b4606-131">Cree una interfaz [**IXpsOMPackageWriter**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) llamando a [**IXpsOMObjectFactory:: CreatePackageWriterOnStream**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream) en la secuencia devuelta por [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).</span><span class="sxs-lookup"><span data-stu-id="b4606-131">Create an [**IXpsOMPackageWriter**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface by calling [**IXpsOMObjectFactory::CreatePackageWriterOnStream**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream) on the stream returned by [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).</span></span>


```C++
    // Create an XPS OM Object Factory. If one has already been 
    //  created by the application, a new one is not necessary.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = CoCreateInstance(
                __uuidof(XpsOMObjectFactory), 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&xpsFactory))))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create XPS OM Object Factory: %08X\n", 
                hr);
        }
    }
    // Create the Part URI for the Fixed Document Sequence. The
    //  Fixed Document Sequence is the top-level element in the
    //  package hierarchy of objects. There is one Fixed Document
    //  Sequence in an XPS document.
    //
    // The part name is not specified by the XML Paper Specification,
    //  however, the name used in this example is the part name
    //  used by convention.
    //
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePartUri(
                    L"/FixedDocumentSequence.fdseq", 
                    &partUri)))
        {
            fwprintf(stderr, 
                L"ERROR: Could not create part URI: %08X\n", hr);
        }
    }

    // Create the package writer on the print job stream.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePackageWriterOnStream(
                    jobStream,
                    TRUE,
                    XPS_INTERLEAVING_ON,
                    partUri,
                    NULL,
                    NULL,
                    NULL,
                    NULL,
                    &packageWriter
                    )
                )
           )
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create package writer: 0x%X\n", 
                hr);
        }
    }

    // Release the part URI interface.
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }
```



<span data-ttu-id="b4606-132">Para cada documento de este trabajo de impresión, inicie un nuevo documento y, a continuación, agregue páginas a ese documento.</span><span class="sxs-lookup"><span data-stu-id="b4606-132">For each document in this print job, start a new document and then add pages to that document.</span></span>

### <a name="start-a-new-document"></a><span data-ttu-id="b4606-133">Iniciar un nuevo documento</span><span class="sxs-lookup"><span data-stu-id="b4606-133">Start a New Document</span></span>

<span data-ttu-id="b4606-134">Inicie un nuevo documento en el escritor de paquetes mediante una llamada a [**IXpsOMPackageWriter:: StartNewDocument**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).</span><span class="sxs-lookup"><span data-stu-id="b4606-134">Start a new document in the package writer by calling [**IXpsOMPackageWriter::StartNewDocument**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).</span></span> <span data-ttu-id="b4606-135">Si un documento está abierto cuando se llama a este método, se cierra y se abre un nuevo documento.</span><span class="sxs-lookup"><span data-stu-id="b4606-135">If a document is open when this method is called, it is closed and a new document is opened.</span></span>


```C++
    // Create the Part URI for the Fixed Document. The
    //  Fixed Document part contains the pages of the document. 
    //  There can be one or more Fixed Documents in an XPS document.
    //
    // The part name is not specified by the XML Paper Specification,
    //  however, the name format used in this example is the format 
    //  used by convention. The number "1" in this example must be 
    //  changed for each document in the package. For example, 1 
    //  for the first document, 2 for the second, and so on.
    //

    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePartUri(
                    L"/Documents/1/FixedDocument.fdoc", 
                    &partUri)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create part URI: %08X\n", 
                hr);
        }
    }

    // Start the new document.
    //
    //  If there was already a document started in this page,
    //  this call will close it and start a new one.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = packageWriter->StartNewDocument(
                    partUri, 
                    NULL, 
                    NULL, 
                    NULL,
                    NULL)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not start new document: 0x%X\n", 
                hr);
        }
    }
    
    // Release the part URI interface
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }
```



### <a name="add-a-page"></a><span data-ttu-id="b4606-136">Agregar una página</span><span class="sxs-lookup"><span data-stu-id="b4606-136">Add a Page</span></span>

<span data-ttu-id="b4606-137">Llame a [**IXpsOMPackageWriter:: AddPage**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) para escribir cada una de las páginas del documento de la aplicación en el nuevo documento del escritor de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b4606-137">Call [**IXpsOMPackageWriter::AddPage**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) to write each of the document's pages from the application to the new document in the package writer.</span></span>

> [!Note]  
> <span data-ttu-id="b4606-138">Se supone que la aplicación ha creado la página antes de este paso.</span><span class="sxs-lookup"><span data-stu-id="b4606-138">The application is assumed to have created the page prior to this step.</span></span> <span data-ttu-id="b4606-139">Para obtener más información sobre cómo crear páginas de documento y agregar contenido a ellas, vea las [tareas comunes de programación de documentos XPS](/previous-versions/windows/desktop/dd316968(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b4606-139">For more information about creating document pages and adding content to them, see the [Common XPS Document Programming Tasks](/previous-versions/windows/desktop/dd316968(v=vs.85)).</span></span>

 


```C++
    if (SUCCEEDED(hr))
    {
        // Add the current page to the document.
        if (FAILED(hr = packageWriter->AddPage(
                    xpsPage,
                    &pageSize,
                    NULL,
                    NULL,
                    NULL,
                    NULL
                    )))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not add page to document: %08X\n", 
                hr);
        }
    }
```



### <a name="close-the-ixpsompackagewriter-interface"></a><span data-ttu-id="b4606-140">Cierre la interfaz IXpsOMPackageWriter</span><span class="sxs-lookup"><span data-stu-id="b4606-140">Close the IXpsOMPackageWriter Interface</span></span>

<span data-ttu-id="b4606-141">Una vez escritos todos los documentos para este trabajo de impresión, llame a [**IXpsOMPackageWriter:: Close**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close) para cerrar el paquete.</span><span class="sxs-lookup"><span data-stu-id="b4606-141">After all the documents have been written for this print job, call [**IXpsOMPackageWriter::Close**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close) to close the package.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = packageWriter->Close()))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not close package writer: %08X\n", 
                hr);
        }
    }
```



### <a name="close-the-print-job-stream"></a><span data-ttu-id="b4606-142">Cerrar la secuencia de trabajo de impresión</span><span class="sxs-lookup"><span data-stu-id="b4606-142">Close the Print Job Stream</span></span>

<span data-ttu-id="b4606-143">Cierre la secuencia de trabajo de impresión mediante una llamada a [**Close**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjobstream-close), que indica al administrador de trabajos de impresión que la aplicación ha enviado todo el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="b4606-143">Close the print job stream by calling [**Close**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjobstream-close), which tells the print spooler that the entire print job has been sent by the application.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = jobStream->Close()))
        {
            fwprintf(
                stderr,
                L"ERROR: Could not close job stream: %08X\n",
                hr);
        }
    }
    else
    {
        // Only cancel the job if we succeeded in creating a job.
        if (job)
        {
            // Tell the XPS Print API that we're giving up.  
            //  Don't overwrite hr with the return from this function.
            job->Cancel();
        }
    }
```



### <a name="wait-for-the-completion-event"></a><span data-ttu-id="b4606-144">Esperar al evento de finalización</span><span class="sxs-lookup"><span data-stu-id="b4606-144">Wait for the Completion Event</span></span>

<span data-ttu-id="b4606-145">Espere a que se complete el evento de finalización del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="b4606-145">Wait for the print job's completion event.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        wprintf(L"Waiting for job completion...\n");

        if (WaitForSingleObject(completionEvent, INFINITE) != 
                                                    WAIT_OBJECT_0)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            fwprintf(
                stderr, 
                L"ERROR: Wait for completion event failed: %08X\n", 
                hr);
        }
    }
```



<span data-ttu-id="b4606-146">Una vez señalado el evento de finalización, llame a [**GetJobStatus**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjob-getjobstatus) para obtener el estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="b4606-146">After the completion event is signaled, call [**GetJobStatus**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjob-getjobstatus) to get the job status.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = job->GetJobStatus(&jobStatus)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not get job status: %08X\n", 
                hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        switch (jobStatus.completion)
        {
            case XPS_JOB_COMPLETED:
                break;
            case XPS_JOB_CANCELLED:
                fwprintf(stderr, L"ERROR: job was cancelled\n");
                hr = E_FAIL;
                break;
            case XPS_JOB_FAILED:
                fwprintf(
                    stderr, 
                    L"ERROR: Print job failed: %08X\n", 
                    jobStatus.jobStatus);
                hr = E_FAIL;
                break;
            default:
                fwprintf(stderr, L"ERROR: unexpected failure\n");
                hr = E_UNEXPECTED;
                break;
        }
    }
```



### <a name="release-resources"></a><span data-ttu-id="b4606-147">Liberación de recursos</span><span class="sxs-lookup"><span data-stu-id="b4606-147">Release Resources</span></span>

<span data-ttu-id="b4606-148">Una vez que el estado del trabajo indica finalización, libere las interfaces y los recursos usados para este trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="b4606-148">After a job status indicates completion, release the interfaces and resources used for this print job.</span></span>


```C++
    if (packageWriter)
    {
        packageWriter->Release();
        packageWriter = NULL;
    }

    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }

    if (xpsFactory)
    {
        xpsFactory->Release();
        xpsFactory = NULL;
    }

    if (jobStream)
    {
        jobStream->Release();
        jobStream = NULL;
    }

    if (job)
    {
        job->Release();
        job = NULL;
    }

    if (completionEvent)
    {
        CloseHandle(completionEvent);
        completionEvent = NULL;
    }
```



 

 
