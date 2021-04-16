---
title: Para indexar un archivo ASF
description: Para indexar un archivo ASF
ms.assetid: 33175444-365c-4b94-8b91-07198431062f
keywords:
- Windows Media Format SDK, indexación de archivos ASF
- Advanced Systems Format (ASF), indexación de archivos
- ASF (formato de sistemas avanzados), indexación de archivos
- índices, indexación de archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7206e1856abb9705e18e885ba06cb8253a93c84b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105685677"
---
# <a name="to-index-an-asf-file"></a><span data-ttu-id="19811-107">Para indexar un archivo ASF</span><span class="sxs-lookup"><span data-stu-id="19811-107">To Index an ASF File</span></span>

<span data-ttu-id="19811-108">El proceso de indización de un archivo ASF es muy sencillo.</span><span class="sxs-lookup"><span data-stu-id="19811-108">The process of indexing an ASF file is very simple.</span></span> <span data-ttu-id="19811-109">Realice una llamada a [**IWMIndexer:: StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) y pase el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="19811-109">Make a call to [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) and pass the file name.</span></span> <span data-ttu-id="19811-110">El indexador realiza el resto.</span><span class="sxs-lookup"><span data-stu-id="19811-110">The indexer does the rest.</span></span> <span data-ttu-id="19811-111">La llamada a **StartIndexing** es asincrónica, por lo que el estado debe supervisarse mediante la devolución de llamada de **Estado** .</span><span class="sxs-lookup"><span data-stu-id="19811-111">The call to **StartIndexing** is asynchronous, so status must be monitored using the **OnStatus** callback.</span></span>

<span data-ttu-id="19811-112">En el código siguiente se muestra cómo indizar un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="19811-112">The following code shows how to index an ASF file.</span></span> <span data-ttu-id="19811-113">Si desea configurar el indexador antes de indizar el archivo, deberá incluir el código del ejemplo incluido en [para configurar el indizador](to-configure-the-indexer.md).</span><span class="sxs-lookup"><span data-stu-id="19811-113">If you want to configure the indexer prior to indexing the file, you will need to include code from the example included in [To Configure the Indexer](to-configure-the-indexer.md).</span></span>

<span data-ttu-id="19811-114">En este ejemplo, el identificador que señala al evento debe crearse como una variable global para que sea accesible para la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="19811-114">For this example, the handle that points to the event must be created as a global variable so it will be accessible by the callback.</span></span> <span data-ttu-id="19811-115">La siguiente declaración debe aparecer en un ámbito global.</span><span class="sxs-lookup"><span data-stu-id="19811-115">The following declaration should appear in a global scope.</span></span>


```C++
HANDLE g_hEvent = NULL;

```



<span data-ttu-id="19811-116">En un escenario más realista, el identificador de evento debe ser un miembro de datos de la clase que contiene la devolución de llamada y la lógica para iniciar el indizador.</span><span class="sxs-lookup"><span data-stu-id="19811-116">In a more realistic scenario, the event handle should be a data member of the class that contains both the callback and the logic for starting the indexer.</span></span>

<span data-ttu-id="19811-117">El indexador envía varios eventos a la devolución de llamada de **Estado** después de la llamada a **IWMIndexer:: StartIndexing**.</span><span class="sxs-lookup"><span data-stu-id="19811-117">The indexer sends several events to the **OnStatus** callback after the call to **IWMIndexer::StartIndexing**.</span></span> <span data-ttu-id="19811-118">Puede interceptarlos según sea necesario para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="19811-118">You can trap them as needed for your application.</span></span> <span data-ttu-id="19811-119">Como mínimo, debe interceptar \_ el cierre de WMT, que se envía cuando se completa la indexación.</span><span class="sxs-lookup"><span data-stu-id="19811-119">At a minimum, you need to trap WMT\_CLOSED, which is sent when indexing is complete.</span></span> <span data-ttu-id="19811-120">Use la siguiente lógica en el conmutador de mensajes en la implementación de la devolución de llamada de **Estado** .</span><span class="sxs-lookup"><span data-stu-id="19811-120">Use the following logic within the message switch in your implementation of the **OnStatus** callback.</span></span>


```C++
// Inside the status switch statement.
case WMT_CLOSED:
   // You may want to deal with the HRESULT value passed with the status.
   // If you do, you should do it here.

   // Signal the event.
   SetEvent(g_hEvent);
   break;

```



<span data-ttu-id="19811-121">En este ejemplo se supone que se tiene acceso a la implementación de la devolución de llamada en **Estado** a través de un objeto denominado DoCallBack.</span><span class="sxs-lookup"><span data-stu-id="19811-121">For this example it is assumed that your implementation of the **OnStatus** callback is accessed through an object called MyCallback.</span></span> <span data-ttu-id="19811-122">Para obtener más información sobre el uso de eventos y devoluciones de llamada con este SDK, vea [usar los métodos de devolución de llamada](using-the-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="19811-122">For more information about using events and callbacks with this SDK, see [Using the Callback Methods](using-the-callback-methods.md).</span></span>


```C++
IWMIndexer* pMyIndexer     = NULL;
HRESULT     hr             = S_OK;
WCHAR       pwszFileName[] = L"C:\SomeFile.wmv";

// Initialize COM.
hr = CoInitialize(NULL);

// Create an event for asynchronous calls.
g_hEvent = CreateEvent(NULL, TRUE, FALSE, NULL);

// Create an indexer.
hr = WMCreateIndexer(&pMyIndexer);

// TODO: Configure the indexer if needed. See To Configure the Indexer.

// Start the indexer.
hr = pMyIndexer->StartIndexing(pwszFileName, &MyCallback, NULL);

// Wait for the indexer to finish.
WaitForSingleObject(g_hEvent, INFINITE);

// Clean up.
pMyIndexer->Release();
pMyIndexer = NULL

CloseHandle(g_hEvent);
g_hEvent = NULL;

```



## <a name="related-topics"></a><span data-ttu-id="19811-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="19811-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19811-124">**Interfaz IWMIndexer**</span><span class="sxs-lookup"><span data-stu-id="19811-124">**IWMIndexer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[<span data-ttu-id="19811-125">**Para configurar el indexador**</span><span class="sxs-lookup"><span data-stu-id="19811-125">**To Configure the Indexer**</span></span>](to-configure-the-indexer.md)
</dt> <dt>

[<span data-ttu-id="19811-126">**WMCreateIndexer**</span><span class="sxs-lookup"><span data-stu-id="19811-126">**WMCreateIndexer**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[<span data-ttu-id="19811-127">**Trabajar con índices**</span><span class="sxs-lookup"><span data-stu-id="19811-127">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




