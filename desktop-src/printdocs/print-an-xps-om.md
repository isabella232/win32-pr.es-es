---
description: Describe cómo enviar un XPS OM a una impresora como un documento XPS.
ms.assetid: eb1068c4-6a6a-4ef2-8ed6-033a6a2c273b
title: Imprimir una OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f1386352cff1556a5ce2403f34ebe4258c4110d4c3bf455990f3f1eb226d17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470908"
---
# <a name="print-an-xps-om"></a>Imprimir una OM XPS

Describe cómo enviar un XPS OM a una impresora como un documento XPS.

Para obtener instrucciones sobre cómo imprimir un XPS OM que contiene un documento XPS completo, vea [Imprimir un XPS OM completo.](#print-a-complete-xps-om) Para contener un documento XPS, un OM XPS debe incluir los elementos enumerados en Crear una OM [XPS en blanco.](create-a-blank-xps-om.md)

Para obtener instrucciones sobre cómo imprimir una OM XPS que se crea o procesa una página a la vez, vea Impresión incremental de una [om XPS](#incrementally-print-an-xps-om).

Antes de usar estos ejemplos de código en el programa, lea la declinación de responsabilidades en [Tareas comunes de programación de documentos XPS](common-xps-document-tasks.md).

En este tema, aprenderá a realizar las siguientes tareas:

-   [Imprimir una OM XPS completa](#print-a-complete-xps-om)
-   [Impresión incremental de una om xps](#incrementally-print-an-xps-om)
-   [Temas relacionados](#related-topics)

## <a name="print-a-complete-xps-om"></a>Imprimir una OM XPS completa

Cuando un XPS OM contiene un documento XPS completo, el método [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) de la interfaz [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) puede enviar el contenido de XPS OM a una impresora o una cola de impresión.

Para detectar cuándo se ha completado el trabajo de impresión, cree un identificador de eventos como se muestra en el ejemplo siguiente.


```C++
    HANDLE completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



Para imprimir un XPS OM completo:

1.  Cree una nueva secuencia de trabajo de impresión mediante [**una llamada a StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).
2.  Envíe el contenido de XPS OM a la secuencia mediante una llamada al [**método WriteToStream del**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) paquete.
3.  Cierre la secuencia del trabajo de impresión mediante una llamada al **método Close de la** secuencia.
4.  Espere a que el trabajo de impresión señale que se ha completado.
5.  Compruebe el estado de finalización.
6.  Cierre y libere los recursos.


```C++
    IXpsPrintJob *job = NULL;
    IXpsPrintJobStream *jobStream = NULL;
    hr = StartXpsPrintJob(
                printerName,
                NULL,
                NULL,
                NULL,
                completionEvent,
                NULL,
                0,
                &job,
                &jobStream,
                NULL);

    // Write package to print job stream
    hr = package->WriteToStream (jobStream, FALSE);

    // Close the stream to tell the print job
    // that the entire document has been sent.
    hr = jobStream->Close();

    // Wait for the print job to finish spooling...
    if (NULL != completionEvent) {
        if (WaitForSingleObject(completionEvent, INFINITE) == WAIT_OBJECT_0)
        {
            // Get the print job status to see why the wait completed.
            //  Note that without waiting for a completion event, 
            //  the print job may not be complete when the status is queried.
            XPS_JOB_STATUS jobStatus;
            hr = job->GetJobStatus(&jobStatus);

            // Evaluate the job status returned.
            switch (jobStatus.completion)
            {
                case XPS_JOB_COMPLETED:
                    // The job completed as expected.
                    hr = S_OK;
                    break;
                case XPS_JOB_CANCELLED:
                    // The job was canceled.
                    hr = E_FAIL;
                    break;
                case XPS_JOB_FAILED:
                    // The job failed, 
                    // jobStatus.jobStatus has the reason.
                    hr = E_FAIL;
                    break;
                default:
                    // An unexpected value was returned.
                    hr = E_UNEXPECTED;
                    break;
            }
                
            // Release completion event handle
            CloseHandle(completionEvent);
        }
        else
        {    // there was a problem, set hr to error status
            hr  = HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // hr contains the result of the print operation

    CoUninitialize(); // if COM is no longer needed in this thread
```



## <a name="incrementally-print-an-xps-om"></a>Impresión incremental de una om xps

Puede enviar los componentes de documento de una om xps a un trabajo de impresora de forma incremental mediante la creación de un flujo de trabajo de impresión XPS y, a continuación, pasar los componentes de documento individuales al flujo de trabajos de impresión, de uno en uno. La secuencia en la que se envían los componentes del documento determina cómo aparecerán en el documento finalizado. Por lo tanto, antes de que un programa pueda llamar al código de este ejemplo, debe organizar correctamente los componentes del documento.

Antes de usar interfaces XPS OM, inicialice COM en el subproceso como se muestra en el código de ejemplo siguiente.


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



Para supervisar la finalización del trabajo de impresión, cree un identificador de eventos como se muestra en el código de ejemplo siguiente.


```C++
    HANDLE completionEvent = NULL;
    completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



Cree un nuevo flujo de trabajo de impresión y un nuevo escritor de paquetes. Pase cada uno de los componentes del documento a los métodos de escritor de paquetes correspondientes en la misma secuencia que aparecerán en el documento finalizado.

Inicie cada documento nuevo y, a continuación, agrégréle páginas. Después de pasar todos los componentes del documento al flujo de trabajo de impresión, cierre la secuencia, espere a que se complete el trabajo de impresión y, a continuación, cierre y libere los recursos abiertos.

1.  Cree una nueva secuencia de trabajo de impresión mediante [**una llamada a StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).
2.  Cree un URI de elemento para el elemento FixedDocumentSequence.
3.  Cree un nuevo escritor de paquetes en la secuencia de trabajos de impresión.
4.  Para cada documento que se va a escribir:
    1.  Cree un nuevo URI de elemento para el elemento FixedDocument.
    2.  Inicie un nuevo documento en el escritor de paquetes.
    3.  Para cada página del documento actual, cree un URI de elemento para el elemento FixedPage y agregue la página al escritor de paquetes.
5.  Una vez que se hayan agregado todas las páginas al escritor de paquetes, cándalo.
6.  Cierre la secuencia del trabajo de impresión.
7.  Espere a que se complete el trabajo de impresión.
8.  Compruebe el estado de finalización.
9.  Cierre y libere los recursos abiertos.


```C++
    IXpsPrintJob* job = NULL;
    IXpsPrintJobStream* jobStream = NULL;
    hr = StartXpsPrintJob(
                argv[1],
                NULL,
                NULL,
                NULL,
                completionEvent,
                NULL,
                0,
                &job,
                &jobStream,
                NULL);

    // Note the implicit requirement that CoInitializeEx 
    //  has previously been called from this thread.
    IXpsOMObjectFactory *xpsFactory = NULL;
    hr = CoCreateInstance(
                __uuidof(XpsOMObjectFactory),
                NULL,
                CLSCTX_INPROC_SERVER,
                __uuidof(IXpsOMObjectFactory),
                reinterpret_cast<void**>(&xpsFactory)
                );
    // Create part URI for FixedDocumentSequence part
    //  This can use a static string because there is only one
    //  FixedDocumentSequence part in the print job.
    IOpcPartUri *partUri = NULL;
    hr = xpsFactory->CreatePartUri(L"/FixedDocumentSequence.fdseq", &partUri);

    // Create the package writer on the print job stream
    //  Note that the interleaving parameter set to 
    //  XPS_INTERLEAVING_ON, the package writer will create
    //  empty print ticket parts when a NULL pointer is
    //  passed in the print ticket argument of this method,
    //  the StartNewDocument method, and the AddPage method.
    //  For more information, see the help for these methods.
    IXpsOMPackageWriter *packageWriter = NULL;
    hr = xpsFactory->CreatePackageWriterOnStream(
            jobStream,
            TRUE,
            XPS_INTERLEAVING_ON, // to create blank print ticket objects
            partUri,
            NULL,
            NULL,
            NULL,
            NULL,
            &packageWriter);
    // release partUri after it's been used to create new doc. seq.
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }

    // Add document content to the print job stream.
    int docNumber = 1;
    int docsInPackage = 1; // Change this value as required.
    while (docNumber <= docsInPackage) {

        // Create a unique part URI for the current document.
        WCHAR DocPartUri[MAX_PATH];
        hr = MakeDocumentPartUri (docNumber, MAX_PATH, DocPartUri);
        hr = xpsFactory->CreatePartUri(DocPartUri, &partUri);
        
        // Initialize the new document in the package writer.
        hr = packageWriter->StartNewDocument(partUri, NULL, NULL, NULL, NULL);

        // release part URI after it's been used to create new doc.
        if (partUri)
        {
            partUri->Release();
            partUri = NULL;
        }

        // Add the pages
        int pageNumber = 1;
        int pagesInDocument = 1; // Change this value as required.
        while (pageNumber <= pagesInDocument) {

            // Create a unique part URI for the current page
            WCHAR PagePartUri[MAX_PATH];
            hr = MakePagePartUri (
                docNumber, 
                pageNumber, 
                MAX_PATH, 
                PagePartUri);
            hr = xpsFactory->CreatePartUri(PagePartUri, &partUri);

            // create page in OM
            XPS_SIZE pageSize = {816, 1056};
            IXpsOMPage *xpsPage = NULL;
            hr = xpsFactory->CreatePage(
                &pageSize, 
                L"en-US", 
                partUri, 
                &xpsPage);

            // release pagePartUri after it's been used to create the page
            if (partUri)
            {
                partUri->Release();
                partUri = NULL;
            }

            // add content to the page or retrieve 
            //  the page from the XPS OM.
            //  (not shown in this example)

            // add page to document
            hr = packageWriter->AddPage(
                        xpsPage,
                        &pageSize,
                        NULL,
                        NULL,
                        NULL,
                        NULL);

             if (xpsPage)
              {
                 xpsPage->Release();
                 xpsPage = NULL;
             }

            // go to the next page
            pageNumber++;
        }
        // the fixed document does not need to be closed.
        // it will be closed when a new fixed doc is opened
        // or the package is closed.

        // go to the next document
        docNumber++;
    }

    // Close the package writer when finished
    hr = packageWriter->Close();

    if (SUCCEEDED(hr))
    {
        // Close the print stream to tell the print
        //  job that the all document contents have
        //  been sent
        hr = jobStream->Close();
        // Wait for the print job to finish spooling...
        if (NULL != completionEvent) {
            if (WaitForSingleObject(completionEvent, INFINITE) == WAIT_OBJECT_0)
            {
                // Get the print job status to see why the wait completed.
                //  Note that without waiting for a completion event, 
                //  the print job may not be complete when the status is queried.
                XPS_JOB_STATUS jobStatus;
                hr = job->GetJobStatus(&jobStatus);

                // Evaluate the job status returned.
                switch (jobStatus.completion)
                {
                    case XPS_JOB_COMPLETED:
                        // The job completed as expected.
                        hr = S_OK;
                        break;
                    case XPS_JOB_CANCELLED:
                        // The job was canceled.
                        hr = E_FAIL;
                        break;
                    case XPS_JOB_FAILED:
                        // The job failed, 
                        // jobStatus.jobStatus has the reason.
                        hr = E_FAIL;
                        break;
                    default:
                        // An unexpected value was returned.
                        hr = E_UNEXPECTED;
                        break;
                }
                    
                // Release completion event handle
                CloseHandle(completionEvent);
            }
            else
            {    // there was a problem, set hr to error status
                hr  = HRESULT_FROM_WIN32(GetLastError());
            }
        }
    } 
    else
    {
        // cancel the job, if one exists, because
        //  the close call returned an error
        if (job) job->Cancel();
    }
    // hr contains the result of the print operation

    // free/release pointers and handles used.

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

    CoUninitialize(); // If done with COM in this thread.
```



Cuando el programa escribe los componentes del documento de forma incremental, como se muestra en este ejemplo, debe generar los nombres de los elementos para cada elemento del documento que envía al flujo de trabajo de impresión. En el ejemplo anterior, el URI de la parte FixedDocumentSequence se crea a partir de una cadena estática porque hay uno y solo uno de estos elementos en el documento XPS. El URI de cada elemento FixedPage y FixedDocument debe ser único dentro del documento XPS. La creación del URI de la parte mediante el índice de estos componentes puede ayudar a garantizar que la cadena de URI resultante sea única en el documento XPS.


```C++
HRESULT MakeDocumentPartUri (
                              __in int docNumber,
                              __in DWORD partUriStringLength,
                              __inout LPWSTR partUriStringBuffer
                              )
{
    // create a Part URI string using the document number
    //  that was passed as an argument
    // for example, "/Documents/1/FixedDocument.fdoc"
    //  where "1" specifies the document number, which would
    //  change with each document printed
    return S_OK;
}
 
HRESULT MakePagePartUri (
                              __in int docNumber,
                              __in int pageNumber,
                              __in DWORD partUriStringLength,
                              __inout LPWSTR partUriStringBuffer
                              )
{
    // create a Part URI string using the document number
    //   and page number that were passed as an argument
    // for example: "/Documents/1/Pages/1.fpage"
    //  where the first "1" between Documents and Pages 
    //  specifies the document number, which would change with
    //  each document. The second "1" specifies the page number,
    //  which would change with each page in the document.
    return S_OK;
}
```



Para obtener más información sobre la estructura de un documento XPS, vea [el XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Pasos siguientes**
</dt> <dt>

[Escribir una om xps en un documento XPS](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

**Se usa en esta sección**
</dt> <dt>

[**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
</dt> <dt>

[**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[**IXpsPrintJob**](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjob)
</dt> <dt>

[**IXpsPrintJobStream**](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjobstream)
</dt> <dt>

[**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)
</dt> <dt>

[**Waitforsingleobject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)
</dt> <dt>

**Para obtener más información**
</dt> <dt>

[Inicialización de una instancia de XPS OM](xps-object-model-initialization.md)
</dt> <dt>

[Referencia de LA API del documento XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
