---
description: Cómo reproducir un archivo
ms.assetid: 3d8c5d06-8690-4298-a1d1-f21af35bcfd4
title: Cómo reproducir un archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc84ef751db318354da36454e6a30fd2ce4bd8e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423084"
---
# <a name="how-to-play-a-file"></a><span data-ttu-id="821a0-103">Cómo reproducir un archivo</span><span class="sxs-lookup"><span data-stu-id="821a0-103">How To Play a File</span></span>

<span data-ttu-id="821a0-104">Este artículo está destinado a proporcionarle el tipo de programación de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="821a0-104">This article is intended to give you the flavor of DirectShow programming.</span></span> <span data-ttu-id="821a0-105">Presenta una sencilla aplicación de consola que reproduce un archivo de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="821a0-105">It presents a simple console application that plays an audio or video file.</span></span> <span data-ttu-id="821a0-106">El programa tiene solo unas pocas líneas, pero muestra parte de la eficacia de la programación de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="821a0-106">The program is only a few lines long, but it demonstrates some of the power of DirectShow programming.</span></span>

<span data-ttu-id="821a0-107">Como se describe [en el artículo Introducción a la programación de aplicaciones de DirectShow](introduction-to-directshow-application-programming.md) , una aplicación de DirectShow siempre realiza los mismos pasos básicos:</span><span class="sxs-lookup"><span data-stu-id="821a0-107">As the article [Introduction to DirectShow Application Programming](introduction-to-directshow-application-programming.md) describes, a DirectShow application always performs the same basic steps:</span></span>

1.  <span data-ttu-id="821a0-108">Cree una instancia del [Administrador de gráficos de filtro](filter-graph-manager.md).</span><span class="sxs-lookup"><span data-stu-id="821a0-108">Create an instance of the [Filter Graph Manager](filter-graph-manager.md).</span></span>
2.  <span data-ttu-id="821a0-109">Use el administrador de gráficos de filtro para generar un gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="821a0-109">Use the Filter Graph Manager to build a filter graph.</span></span>
3.  <span data-ttu-id="821a0-110">Ejecute el gráfico, haciendo que los datos se muevan a través de los filtros.</span><span class="sxs-lookup"><span data-stu-id="821a0-110">Run the graph, causing data to move through the filters.</span></span>

<span data-ttu-id="821a0-111">Para compilar y vincular el código de este tema, incluya el archivo de encabezado DShow. h y un vínculo al archivo de biblioteca estática strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="821a0-111">To compile and link the code in this topic, include the header file Dshow.h and link to the static library file strmiids.lib.</span></span> <span data-ttu-id="821a0-112">Para obtener más información, consulte [Building DirectShow Applications](setting-up-the-build-environment.md).</span><span class="sxs-lookup"><span data-stu-id="821a0-112">For more information, see [Building DirectShow Applications](setting-up-the-build-environment.md).</span></span>

<span data-ttu-id="821a0-113">Para empezar, llame a [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar la biblioteca com:</span><span class="sxs-lookup"><span data-stu-id="821a0-113">Start by calling [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library:</span></span>


```C++
HRESULT hr = CoInitialize(NULL);
if (FAILED(hr))
{
    // Add error-handling code here. (Omitted for clarity.)
}
```



<span data-ttu-id="821a0-114">Para simplificar las cosas, en este ejemplo se omite el valor devuelto, pero siempre debe comprobar el valor **HRESULT** de cualquier llamada al método.</span><span class="sxs-lookup"><span data-stu-id="821a0-114">To keep things simple, this example ignores the return value, but you should always check the **HRESULT** value from any method call.</span></span>

<span data-ttu-id="821a0-115">A continuación, llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el administrador de gráficos de filtro:</span><span class="sxs-lookup"><span data-stu-id="821a0-115">Next, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Filter Graph Manager:</span></span>


```C++
IGraphBuilder *pGraph;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);
```



<span data-ttu-id="821a0-116">Como se muestra, el identificador de clase (CLSID) es CLSID \_ FilterGraph.</span><span class="sxs-lookup"><span data-stu-id="821a0-116">As shown, the class identifier (CLSID) is CLSID\_FilterGraph.</span></span> <span data-ttu-id="821a0-117">El administrador de gráficos de filtro lo proporciona un archivo DLL en proceso, por lo que el contexto de ejecución es **CLSCTX \_ Inproc \_ Server**.</span><span class="sxs-lookup"><span data-stu-id="821a0-117">The Filter Graph Manager is provided by an in-process DLL, so the execution context is **CLSCTX\_INPROC\_SERVER**.</span></span> <span data-ttu-id="821a0-118">DirectShow admite el modelo de subprocesamiento libre, por lo que también puede llamar a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) con la marca de **coinit \_ multiproceso** .</span><span class="sxs-lookup"><span data-stu-id="821a0-118">DirectShow supports the free-threading model, so you can also call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.</span></span>

<span data-ttu-id="821a0-119">La llamada a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) devuelve la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , que principalmente contiene métodos para generar el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="821a0-119">The call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) returns the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface, which mostly contains methods for building the filter graph.</span></span> <span data-ttu-id="821a0-120">En este ejemplo se necesitan otras dos interfaces:</span><span class="sxs-lookup"><span data-stu-id="821a0-120">Two other interfaces are needed for this example:</span></span>

-   <span data-ttu-id="821a0-121">Streaming de controles [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) .</span><span class="sxs-lookup"><span data-stu-id="821a0-121">[**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) controls streaming.</span></span> <span data-ttu-id="821a0-122">Contiene métodos para detener e iniciar el gráfico.</span><span class="sxs-lookup"><span data-stu-id="821a0-122">It contains methods for stopping and starting the graph.</span></span>
-   <span data-ttu-id="821a0-123">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) tiene métodos para obtener eventos del administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="821a0-123">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) has methods for getting events from the Filter Graph Manager.</span></span> <span data-ttu-id="821a0-124">En este ejemplo, la interfaz se usa para esperar a que se complete la reproducción.</span><span class="sxs-lookup"><span data-stu-id="821a0-124">In this example, the interface is used to wait for playback to complete.</span></span>

<span data-ttu-id="821a0-125">Ambas interfaces las expone el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="821a0-125">Both of these interfaces are exposed by the Filter Graph Manager.</span></span> <span data-ttu-id="821a0-126">Use el puntero [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) devuelto para consultarlos:</span><span class="sxs-lookup"><span data-stu-id="821a0-126">Use the returned [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) pointer to query for them:</span></span>


```C++
IMediaControl *pControl;
IMediaEvent   *pEvent;
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="821a0-127">Ahora puede crear el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="821a0-127">Now you can build the filter graph.</span></span> <span data-ttu-id="821a0-128">Para la reproducción de archivos, esto se realiza mediante una única llamada al método:</span><span class="sxs-lookup"><span data-stu-id="821a0-128">For file playback, this is done by a single method call:</span></span>


```C++
hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
```



<span data-ttu-id="821a0-129">El método [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) crea un gráfico de filtro que puede reproducir el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="821a0-129">The [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) method builds a filter graph that can play the specified file.</span></span> <span data-ttu-id="821a0-130">El primer parámetro es el nombre de archivo, representado como una cadena de caracteres anchos (de 2 bytes).</span><span class="sxs-lookup"><span data-stu-id="821a0-130">The first parameter is the file name, represented as a wide character (2-byte) string.</span></span> <span data-ttu-id="821a0-131">El segundo parámetro está reservado y debe ser igual a **null**.</span><span class="sxs-lookup"><span data-stu-id="821a0-131">The second parameter is reserved and must equal **NULL**.</span></span>

<span data-ttu-id="821a0-132">Este método puede producir un error si el archivo especificado no existe o no se reconoce el formato del archivo.</span><span class="sxs-lookup"><span data-stu-id="821a0-132">This method can fail if the specified file does not exist, or the file format is not recognized.</span></span> <span data-ttu-id="821a0-133">Sin embargo, suponiendo que el método se ejecuta correctamente, el gráfico de filtro ya está listo para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="821a0-133">Assuming that the method succeeds, however, the filter graph is now ready for playback.</span></span> <span data-ttu-id="821a0-134">Para ejecutar el gráfico, llame al método [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) :</span><span class="sxs-lookup"><span data-stu-id="821a0-134">To run the graph, call the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method:</span></span>


```C++
hr = pControl->Run();
```



<span data-ttu-id="821a0-135">Cuando se ejecuta el gráfico de filtro, los datos se mueven a través de los filtros y se representan como vídeo y audio.</span><span class="sxs-lookup"><span data-stu-id="821a0-135">When the filter graph runs, data moves through the filters and is rendered as video and audio.</span></span> <span data-ttu-id="821a0-136">La reproducción se produce en un subproceso independiente.</span><span class="sxs-lookup"><span data-stu-id="821a0-136">Playback occurs on a separate thread.</span></span> <span data-ttu-id="821a0-137">Puede esperar a que se complete la reproducción llamando al método [**IMediaEvent:: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) :</span><span class="sxs-lookup"><span data-stu-id="821a0-137">You can wait for playback to complete by calling the [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) method:</span></span>


```C++
long evCode = 0;
pEvent->WaitForCompletion(INFINITE, &evCode);
```



<span data-ttu-id="821a0-138">Este método se bloquea hasta que se realiza la reproducción del archivo o hasta que transcurre el intervalo de tiempo de espera especificado.</span><span class="sxs-lookup"><span data-stu-id="821a0-138">This method blocks until the file is done playing, or until the specified time-out interval elapses.</span></span> <span data-ttu-id="821a0-139">El valor infinito significa que la aplicación se bloquea indefinidamente hasta que el archivo termina de reproducirse.</span><span class="sxs-lookup"><span data-stu-id="821a0-139">The value INFINITE means the application blocks indefinitely until the file is done playing.</span></span> <span data-ttu-id="821a0-140">Para obtener un ejemplo más realista del control de eventos, vea [responder a eventos](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="821a0-140">For a more realistic example of event handling, see [Responding to Events](responding-to-events.md).</span></span>

<span data-ttu-id="821a0-141">Una vez finalizada la aplicación, libere los punteros de interfaz y cierre la biblioteca COM:</span><span class="sxs-lookup"><span data-stu-id="821a0-141">When the application is finished, release the interface pointers and close the COM library:</span></span>


```C++
pControl->Release();
pEvent->Release();
pGraph->Release();
CoUninitialize();
```



## <a name="example-code"></a><span data-ttu-id="821a0-142">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="821a0-142">Example Code</span></span>

<span data-ttu-id="821a0-143">Este es el código completo para el ejemplo que se describe en este artículo:</span><span class="sxs-lookup"><span data-stu-id="821a0-143">Here is the complete code for the example described in this article:</span></span>


```C++
#include <dshow.h>
void main(void)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEvent   *pEvent = NULL;

    // Initialize the COM library.
    HRESULT hr = CoInitialize(NULL);
    if (FAILED(hr))
    {
        printf("ERROR - Could not initialize COM library");
        return;
    }

    // Create the filter graph manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file on your system.
    hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
    if (SUCCEEDED(hr))
    {
        // Run the graph.
        hr = pControl->Run();
        if (SUCCEEDED(hr))
        {
            // Wait for completion.
            long evCode;
            pEvent->WaitForCompletion(INFINITE, &evCode);

            // Note: Do not use INFINITE in a real application, because it
            // can block indefinitely.
        }
    }
    pControl->Release();
    pEvent->Release();
    pGraph->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a><span data-ttu-id="821a0-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="821a0-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="821a0-145">Tareas básicas de DirectShow</span><span class="sxs-lookup"><span data-stu-id="821a0-145">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 
