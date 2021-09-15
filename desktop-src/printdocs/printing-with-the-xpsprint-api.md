---
description: En este tema se describe cómo usar XPS Print API para imprimir desde una Windows aplicación.
ms.assetid: 3d7ab169-412c-434f-a865-4da4af370eaf
title: 'Cómo: Imprimir con XPS Print API'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4be5f083fb31eccaf2dc4b555435bd15a7fb45
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359707"
---
# <a name="how-to-print-with-the-xps-print-api"></a>Cómo: Imprimir con XPS Print API

En este tema se describe cómo usar [XPS Print API](xpsprint-api.md) para imprimir desde una Windows aplicación.

XpS [Print API permite](xpsprint-api.md) que las aplicaciones Windows nativas impriman documentos XPS. Una aplicación puede crear un documento XPS mediante [la API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)). En [el tema de ayuda Tareas comunes de programación](/previous-versions/windows/desktop/dd316968(v=vs.85)) de documentos XPS se describe cómo hacerlo. Una vez creado un documento XPS, la aplicación puede usar xpS Print API para imprimirlo.

El uso [de XPS Print API](xpsprint-api.md) para imprimir un documento desde una aplicación implica los pasos siguientes.

-   [Inicialización de la interfaz COM](#initialize-com-interface)
-   [Crear un evento de finalización](#create-a-completion-event)
-   [Iniciar un trabajo de impresión XPS](#start-an-xps-print-job)
-   [Crear una interfaz IXpsOMPackageWriter](#create-an-ixpsompackagewriter-interface)
-   [Cierre la interfaz IXpsOMPackageWriter](#close-the-ixpsompackagewriter-interface)
-   [Cierre de la secuencia de trabajos de impresión](#close-the-print-job-stream)
-   [Esperar al evento de finalización](#wait-for-the-completion-event)
-   [Liberación de recursos](#release-resources)

XpS [Print API requiere](xpsprint-api.md) que se imprima un documento XPS. En el ejemplo siguiente, el documento XPS se crea a medida que se envía a la impresora mediante xpS Print API. También es posible crear un documento XPS sin enviarlo a una impresora mediante la API de documentos [XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) y mantenerlo como XPS OM o guardando xpS OM como un documento XPS. Para más información sobre el uso de XPS OM, consulte LA API de documentos XPS.

### <a name="initialize-com-interface"></a>Inicialización de la interfaz COM

Inicialice la interfaz COM, si la aplicación aún no lo ha hecho.


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



### <a name="create-a-completion-event"></a>Crear un evento de finalización

Cree un evento de finalización, que la API de impresión [XPS](xpsprint-api.md) usa para notificar a la aplicación cuando el colador de impresión ha recibido todo el documento de la aplicación. XpS Print API también admite un evento de progreso para que una aplicación pueda conocer otra actividad de cola.


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



### <a name="start-an-xps-print-job"></a>Iniciar un trabajo de impresión XPS

Inicie un trabajo de impresión XPS mediante una [**llamada a StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob). **StartXpsPrintJob** devuelve una secuencia en la que la aplicación enviará el documento que se va a imprimir.


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



### <a name="create-an-ixpsompackagewriter-interface"></a>Crear una interfaz IXpsOMPackageWriter

Cree una [**interfaz IXpsOMPackageWriter**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) llamando a [**IXpsOMObjectFactory::CreatePackageWriterOnStream**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream) en la secuencia devuelta por [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).


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



Para cada documento de este trabajo de impresión, inicie un nuevo documento y agregue páginas a ese documento.

### <a name="start-a-new-document"></a>Iniciar un nuevo documento

Inicie un nuevo documento en el escritor de paquetes mediante una [**llamada a IXpsOMPackageWriter::StartNewDocument**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument). Si un documento está abierto cuando se llama a este método, se cierra y se abre un nuevo documento.


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



### <a name="add-a-page"></a>Agregar una página

Llame [**a IXpsOMPackageWriter::AddPage**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) para escribir cada una de las páginas del documento de la aplicación en el nuevo documento del escritor de paquetes.

> [!Note]  
> Se supone que la aplicación ha creado la página antes de este paso. Para obtener más información sobre cómo crear páginas de documento y agregarles contenido, vea [Tareas comunes de programación de documentos XPS](/previous-versions/windows/desktop/dd316968(v=vs.85)).

 


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



### <a name="close-the-ixpsompackagewriter-interface"></a>Cierre la interfaz IXpsOMPackageWriter

Una vez que se hayan escrito todos los documentos para este trabajo de impresión, llame a [**IXpsOMPackageWriter::Close**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close) para cerrar el paquete.


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



### <a name="close-the-print-job-stream"></a>Cierre de la secuencia de trabajos de impresión

Cierre la secuencia del trabajo de impresión mediante una llamada a [**Cerrar**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjobstream-close), que indica al cola de impresión que la aplicación ha enviado todo el trabajo de impresión.


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



### <a name="wait-for-the-completion-event"></a>Esperar al evento de finalización

Espere el evento de finalización del trabajo de impresión.


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



Después de que se señale el evento de finalización, llame [**a GetJobStatus**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjob-getjobstatus) para obtener el estado del trabajo.


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



### <a name="release-resources"></a>Liberación de recursos

Una vez que el estado de un trabajo indique la finalización, libere las interfaces y los recursos que se usan para este trabajo de impresión.


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



 

 
