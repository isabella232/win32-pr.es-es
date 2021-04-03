---
description: Describe cómo enviar un OM XPS a una impresora como un documento XPS.
ms.assetid: eb1068c4-6a6a-4ef2-8ed6-033a6a2c273b
title: Imprimir un OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01ae1081c4f0c58c66efedc30406e310dd8dd9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082828"
---
# <a name="print-an-xps-om"></a><span data-ttu-id="a3b07-103">Imprimir un OM XPS</span><span class="sxs-lookup"><span data-stu-id="a3b07-103">Print an XPS OM</span></span>

<span data-ttu-id="a3b07-104">Describe cómo enviar un OM XPS a una impresora como un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="a3b07-104">Describes how to send an XPS OM to a printer as an XPS document.</span></span>

<span data-ttu-id="a3b07-105">Para obtener instrucciones sobre cómo imprimir un OM XPS que contenga un documento XPS completo, consulte [imprimir un OM de XPS completo](#print-a-complete-xps-om).</span><span class="sxs-lookup"><span data-stu-id="a3b07-105">For instructions on how to print an XPS OM that contains a complete XPS document, see [Print a complete XPS OM](#print-a-complete-xps-om).</span></span> <span data-ttu-id="a3b07-106">Para contener un documento XPS, un OM XPS debe incluir los elementos enumerados en [crear un OM XPS en blanco](create-a-blank-xps-om.md).</span><span class="sxs-lookup"><span data-stu-id="a3b07-106">To contain an XPS document, an XPS OM must include the items listed in [Create a Blank XPS OM](create-a-blank-xps-om.md).</span></span>

<span data-ttu-id="a3b07-107">Para obtener instrucciones sobre cómo imprimir un OM XPS que se está creando o procesando una página a la vez, consulte [impresión incremental de un OM XPS](#incrementally-print-an-xps-om).</span><span class="sxs-lookup"><span data-stu-id="a3b07-107">For instructions on how to print an XPS OM that is being created or processed one page at a time, see [Incrementally print an XPS OM](#incrementally-print-an-xps-om).</span></span>

<span data-ttu-id="a3b07-108">Antes de usar estos ejemplos de código en el programa, lea la declinación de responsabilidades en [las tareas comunes de programación de documentos XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="a3b07-108">Before using these code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

<span data-ttu-id="a3b07-109">En este tema, aprenderá a realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="a3b07-109">In this topic, you will learn how to perform the following tasks:</span></span>

-   [<span data-ttu-id="a3b07-110">Imprimir un OM XPS completo</span><span class="sxs-lookup"><span data-stu-id="a3b07-110">Print a complete XPS OM</span></span>](#print-a-complete-xps-om)
-   [<span data-ttu-id="a3b07-111">Impresión incremental de un OM XPS</span><span class="sxs-lookup"><span data-stu-id="a3b07-111">Incrementally print an XPS OM</span></span>](#incrementally-print-an-xps-om)
-   [<span data-ttu-id="a3b07-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3b07-112">Related topics</span></span>](#related-topics)

## <a name="print-a-complete-xps-om"></a><span data-ttu-id="a3b07-113">Imprimir un OM XPS completo</span><span class="sxs-lookup"><span data-stu-id="a3b07-113">Print a complete XPS OM</span></span>

<span data-ttu-id="a3b07-114">Cuando un OM XPS contiene un documento XPS completo, el método [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) de la interfaz [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) puede enviar el contenido del OM XPS a una impresora o una cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="a3b07-114">When an XPS OM contains a complete XPS document, the [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface can send the contents of the XPS OM to a printer or a print queue.</span></span>

<span data-ttu-id="a3b07-115">Para detectar cuándo se ha completado el trabajo de impresión, cree un identificador de evento como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="a3b07-115">To detect when the print job has completed, create an event handle as shown in the following example.</span></span>


```C++
    HANDLE completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



<span data-ttu-id="a3b07-116">Para imprimir un OM XPS completo:</span><span class="sxs-lookup"><span data-stu-id="a3b07-116">To print a complete XPS OM:</span></span>

1.  <span data-ttu-id="a3b07-117">Cree un nuevo flujo de trabajo de impresión mediante una llamada a [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span><span class="sxs-lookup"><span data-stu-id="a3b07-117">Create a new print job stream by calling [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span></span>
2.  <span data-ttu-id="a3b07-118">Envíe el contenido del OM XPS a la secuencia llamando al método [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) del paquete.</span><span class="sxs-lookup"><span data-stu-id="a3b07-118">Send the contents of the XPS OM to the stream by calling the package's [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) method.</span></span>
3.  <span data-ttu-id="a3b07-119">Cierre el flujo de trabajo de impresión llamando al método **Close** de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="a3b07-119">Close the print job stream by calling the stream's **Close** method.</span></span>
4.  <span data-ttu-id="a3b07-120">Espere a que el trabajo de impresión señale que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="a3b07-120">Wait for the print job to signal that it has completed.</span></span>
5.  <span data-ttu-id="a3b07-121">Compruebe el estado de finalización.</span><span class="sxs-lookup"><span data-stu-id="a3b07-121">Check the completion status.</span></span>
6.  <span data-ttu-id="a3b07-122">Cierre y libere recursos.</span><span class="sxs-lookup"><span data-stu-id="a3b07-122">Close and release resources.</span></span>


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



## <a name="incrementally-print-an-xps-om"></a><span data-ttu-id="a3b07-123">Impresión incremental de un OM XPS</span><span class="sxs-lookup"><span data-stu-id="a3b07-123">Incrementally print an XPS OM</span></span>

<span data-ttu-id="a3b07-124">Puede enviar los componentes de documento de un OM XPS a un trabajo de impresora de forma incremental; para ello, cree una secuencia de trabajo de impresión XPS y, a continuación, pase los componentes de documento individuales al flujo de trabajo de impresión, de uno en uno.</span><span class="sxs-lookup"><span data-stu-id="a3b07-124">You can send the document components of an XPS OM to a printer job incrementally, by creating an XPS print job stream and then passing the individual document components to the print job stream, one at a time.</span></span> <span data-ttu-id="a3b07-125">La secuencia en la que se envían los componentes de documento determina cómo aparecerán en el documento terminado.</span><span class="sxs-lookup"><span data-stu-id="a3b07-125">The sequence in which the document components are sent determines how they will appear in the finished document.</span></span> <span data-ttu-id="a3b07-126">Por lo tanto, antes de que un programa pueda llamar al código de este ejemplo, debe organizar correctamente los componentes del documento.</span><span class="sxs-lookup"><span data-stu-id="a3b07-126">Thus, before a program can call the code in this example, it must correctly organize the document components.</span></span>

<span data-ttu-id="a3b07-127">Antes de utilizar las interfaces de XPS OM, inicialice COM en el subproceso, tal y como se muestra en el código de ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="a3b07-127">Before using XPS OM interfaces, initialize COM in the thread as shown in the following example code.</span></span>


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



<span data-ttu-id="a3b07-128">Para supervisar la finalización del trabajo de impresión, cree un identificador de evento, tal como se muestra en el código de ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="a3b07-128">To monitor the print job completion, create an event handle as shown in the following example code.</span></span>


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



<span data-ttu-id="a3b07-129">Cree un nuevo flujo de trabajo de impresión y un nuevo escritor de paquetes.</span><span class="sxs-lookup"><span data-stu-id="a3b07-129">Create a new print job stream and a new package writer.</span></span> <span data-ttu-id="a3b07-130">Pase cada uno de los componentes del documento a los métodos del escritor de paquetes correspondientes en la misma secuencia en que aparecerán en el documento terminado.</span><span class="sxs-lookup"><span data-stu-id="a3b07-130">Pass each of the document components to the corresponding package writer methods in the same sequence as they will appear in the finished document.</span></span>

<span data-ttu-id="a3b07-131">Inicie cada documento nuevo y agréguele páginas.</span><span class="sxs-lookup"><span data-stu-id="a3b07-131">Start each document new, then add pages to it.</span></span> <span data-ttu-id="a3b07-132">Después de pasar todos los componentes de documento al flujo de trabajo de impresión, cierre el flujo, espere a que finalice el trabajo de impresión y, a continuación, cierre y libere los recursos abiertos.</span><span class="sxs-lookup"><span data-stu-id="a3b07-132">After passing all document components to the print job stream, close the stream, wait for the print job to complete, and then close and release open resources.</span></span>

1.  <span data-ttu-id="a3b07-133">Cree un nuevo flujo de trabajo de impresión mediante una llamada a [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span><span class="sxs-lookup"><span data-stu-id="a3b07-133">Create a new print job stream by calling [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span></span>
2.  <span data-ttu-id="a3b07-134">Cree un URI de elemento para la parte FixedDocumentSequence.</span><span class="sxs-lookup"><span data-stu-id="a3b07-134">Create a part URI for the FixedDocumentSequence part.</span></span>
3.  <span data-ttu-id="a3b07-135">Cree un nuevo escritor de paquetes en el flujo de trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="a3b07-135">Create a new package writer on the print job stream.</span></span>
4.  <span data-ttu-id="a3b07-136">Para cada documento que se va a escribir:</span><span class="sxs-lookup"><span data-stu-id="a3b07-136">For each document to be written:</span></span>
    1.  <span data-ttu-id="a3b07-137">Cree un nuevo URI de elemento para la parte FixedDocument.</span><span class="sxs-lookup"><span data-stu-id="a3b07-137">Create a new part URI for the FixedDocument part.</span></span>
    2.  <span data-ttu-id="a3b07-138">Inicie un nuevo documento en el escritor de paquetes.</span><span class="sxs-lookup"><span data-stu-id="a3b07-138">Start a new document in the package writer.</span></span>
    3.  <span data-ttu-id="a3b07-139">Para cada página del documento actual, cree un URI de elemento para la parte FixedPage y agregue la página al escritor de paquetes.</span><span class="sxs-lookup"><span data-stu-id="a3b07-139">For each page in the current document, create a part URI for the FixedPage part and add the page to the package writer.</span></span>
5.  <span data-ttu-id="a3b07-140">Después de agregar todas las páginas al escritor de paquetes, ciérrela.</span><span class="sxs-lookup"><span data-stu-id="a3b07-140">After all pages have been added to the package writer, close it.</span></span>
6.  <span data-ttu-id="a3b07-141">Cierre el flujo de trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="a3b07-141">Close the print job stream.</span></span>
7.  <span data-ttu-id="a3b07-142">Espere a que se complete el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="a3b07-142">Wait for the print job to complete.</span></span>
8.  <span data-ttu-id="a3b07-143">Compruebe el estado de finalización.</span><span class="sxs-lookup"><span data-stu-id="a3b07-143">Check the completion status.</span></span>
9.  <span data-ttu-id="a3b07-144">Cierre y libere recursos abiertos.</span><span class="sxs-lookup"><span data-stu-id="a3b07-144">Close and release open resources.</span></span>


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



<span data-ttu-id="a3b07-145">Cuando el programa está escribiendo los componentes de documento incrementalmente, tal como se muestra en este ejemplo, debe generar los nombres de las partes de cada elemento de documento que envía al flujo de trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="a3b07-145">When the program is writing the document components incrementally, as shown in this example, it must generate the part names for each document part that it sends to the print job stream.</span></span> <span data-ttu-id="a3b07-146">En el ejemplo anterior, el URI de la parte FixedDocumentSequence se crea a partir de una cadena estática porque solo hay una parte de este tipo en el documento XPS.</span><span class="sxs-lookup"><span data-stu-id="a3b07-146">In the preceding example, the FixedDocumentSequence part URI is created from a static string because there is one and only one such part in the XPS document.</span></span> <span data-ttu-id="a3b07-147">El URI de cada elemento FixedPage y FixedDocument debe ser único en el documento XPS.</span><span class="sxs-lookup"><span data-stu-id="a3b07-147">The URI of each FixedPage and FixedDocument part must be unique within the XPS document.</span></span> <span data-ttu-id="a3b07-148">La creación del URI del elemento mediante el índice de estos componentes puede ayudar a garantizar que la cadena de URI resultante sea única en el documento XPS.</span><span class="sxs-lookup"><span data-stu-id="a3b07-148">Building the part URI by using the index of these components can help ensure that the resulting URI string is unique within the XPS document.</span></span>


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



<span data-ttu-id="a3b07-149">Para obtener más información sobre la estructura de un documento XPS, consulte [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span><span class="sxs-lookup"><span data-stu-id="a3b07-149">For more information on the structure of an XPS document, see the [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3b07-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3b07-150">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a3b07-151">**Pasos siguientes**</span><span class="sxs-lookup"><span data-stu-id="a3b07-151">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="a3b07-152">Escribir un OM XPS en un documento XPS</span><span class="sxs-lookup"><span data-stu-id="a3b07-152">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

<span data-ttu-id="a3b07-153">**Se usa en esta sección**</span><span class="sxs-lookup"><span data-stu-id="a3b07-153">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="a3b07-154">**Fall**</span><span class="sxs-lookup"><span data-stu-id="a3b07-154">**CoInitializeEx**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
</dt> <dt>

[<span data-ttu-id="a3b07-155">**CreateEvent**</span><span class="sxs-lookup"><span data-stu-id="a3b07-155">**CreateEvent**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="a3b07-156">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="a3b07-156">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="a3b07-157">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="a3b07-157">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="a3b07-158">**IXpsOMPackageWriter**</span><span class="sxs-lookup"><span data-stu-id="a3b07-158">**IXpsOMPackageWriter**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[<span data-ttu-id="a3b07-159">**IXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="a3b07-159">**IXpsPrintJob**</span></span>](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjob)
</dt> <dt>

[<span data-ttu-id="a3b07-160">**IXpsPrintJobStream**</span><span class="sxs-lookup"><span data-stu-id="a3b07-160">**IXpsPrintJobStream**</span></span>](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjobstream)
</dt> <dt>

[<span data-ttu-id="a3b07-161">**StartXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="a3b07-161">**StartXpsPrintJob**</span></span>](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)
</dt> <dt>

[<span data-ttu-id="a3b07-162">**WaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="a3b07-162">**WaitForSingleObject**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)
</dt> <dt>

<span data-ttu-id="a3b07-163">**Para obtener más información**</span><span class="sxs-lookup"><span data-stu-id="a3b07-163">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="a3b07-164">Inicializar un OM XPS</span><span class="sxs-lookup"><span data-stu-id="a3b07-164">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="a3b07-165">Referencia de la API de documentos XPS</span><span class="sxs-lookup"><span data-stu-id="a3b07-165">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="a3b07-166">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="a3b07-166">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
