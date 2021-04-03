---
description: Obtener una vista previa del proyecto
ms.assetid: 00d72a39-f848-47ea-8460-8b826684eeea
title: Obtener una vista previa del proyecto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdf38fe19e500cfe9bd9a8dfb77f7ff56528a2f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997943"
---
# <a name="previewing-the-project"></a><span data-ttu-id="33b5a-103">Obtener una vista previa del proyecto</span><span class="sxs-lookup"><span data-stu-id="33b5a-103">Previewing the Project</span></span>

<span data-ttu-id="33b5a-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="33b5a-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="33b5a-105">Para obtener una vista previa del proyecto, necesita un componente denominado *motor de representación*, que genera un gráfico de filtros de DirectShow a partir de una escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="33b5a-105">To preview the project, you need a component called a *render engine*, which builds a DirectShow filter graph from a timeline.</span></span> <span data-ttu-id="33b5a-106">El gráfico de filtros es lo que realmente representa el proyecto.</span><span class="sxs-lookup"><span data-stu-id="33b5a-106">The filter graph is what actually renders the project.</span></span> <span data-ttu-id="33b5a-107">Puede usar el motor de representación para obtener una vista previa de un proyecto o para escribir el archivo de salida final.</span><span class="sxs-lookup"><span data-stu-id="33b5a-107">You can use the render engine to preview a project or to write the final output file.</span></span>

<span data-ttu-id="33b5a-108">En este artículo no se explica con detalle el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="33b5a-108">This article does not go into detail about the render engine.</span></span> <span data-ttu-id="33b5a-109">Para la versión preliminar, solo necesita algunas llamadas a métodos.</span><span class="sxs-lookup"><span data-stu-id="33b5a-109">For preview, you only need a few method calls.</span></span> <span data-ttu-id="33b5a-110">Puede encontrar una explicación más completa, incluida la forma de escribir archivos de salida, en la [representación de un proyecto](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="33b5a-110">You can find a more thorough discussion, including how to write output files, in [Rendering a Project](rendering-a-project.md).</span></span> <span data-ttu-id="33b5a-111">En el ejemplo de código siguiente se muestra cómo crear un gráfico de vista previa.</span><span class="sxs-lookup"><span data-stu-id="33b5a-111">The following code example shows how to construct a preview graph.</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
            IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
hr = pRender->RenderOutputPins( );
```



<span data-ttu-id="33b5a-112">Cree el motor de representación mediante la función **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="33b5a-112">Create the render engine using the **CoCreateInstance** function.</span></span> <span data-ttu-id="33b5a-113">A continuación, llame a los métodos siguientes en la interfaz [**IRenderEngine**](irenderengine.md) del motor de representación:</span><span class="sxs-lookup"><span data-stu-id="33b5a-113">Then call the following methods on the render engine's [**IRenderEngine**](irenderengine.md) interface:</span></span>

-   <span data-ttu-id="33b5a-114">[**SetTimelineObject**](irenderengine-settimelineobject.md).</span><span class="sxs-lookup"><span data-stu-id="33b5a-114">[**SetTimelineObject**](irenderengine-settimelineobject.md).</span></span> <span data-ttu-id="33b5a-115">Especifica la escala de tiempo que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="33b5a-115">Specifies the timeline to use.</span></span>
-   <span data-ttu-id="33b5a-116">[**ConnectFrontEnd**](irenderengine-connectfrontend.md).</span><span class="sxs-lookup"><span data-stu-id="33b5a-116">[**ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span> <span data-ttu-id="33b5a-117">Crea un gráfico de filtro parcial, con un PIN de salida para cada grupo de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="33b5a-117">Builds a partial filter graph, with one output pin for each group in the timeline.</span></span>
-   <span data-ttu-id="33b5a-118">[**RenderOutputPins**](irenderengine-renderoutputpins.md).</span><span class="sxs-lookup"><span data-stu-id="33b5a-118">[**RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span> <span data-ttu-id="33b5a-119">Completa el gráfico de vista previa conectando cada pin de salida a un representador de vídeo o audio.</span><span class="sxs-lookup"><span data-stu-id="33b5a-119">Completes the preview graph by connecting each output pin to a video or audio renderer.</span></span>

<span data-ttu-id="33b5a-120">Una vez creado el gráfico, puede obtener una vista previa del mismo ejecutando el gráfico, como haría con cualquier gráfico de filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="33b5a-120">Once the graph is built, you can preview the project by running the graph, as you would with any DirectShow filter graph.</span></span> <span data-ttu-id="33b5a-121">En primer lugar, obtenga un puntero al gráfico de filtros llamando al método [**IRenderEngine:: GetFilterGraph**](irenderengine-getfiltergraph.md) .</span><span class="sxs-lookup"><span data-stu-id="33b5a-121">First, obtain a pointer to the filter graph by calling the [**IRenderEngine::GetFilterGraph**](irenderengine-getfiltergraph.md) method.</span></span>


```C++
IGraphBuilder   *pGraph = NULL;
hr = pRender->GetFilterGraph(&pGraph);
```



<span data-ttu-id="33b5a-122">Consulte el gráfico de filtro para las interfaces [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .</span><span class="sxs-lookup"><span data-stu-id="33b5a-122">Query the filter graph for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interfaces.</span></span> <span data-ttu-id="33b5a-123">Use estas dos interfaces para ejecutar el gráfico y esperar a que se complete la reproducción.</span><span class="sxs-lookup"><span data-stu-id="33b5a-123">Use these two interfaces to run the graph and wait for playback to complete.</span></span> <span data-ttu-id="33b5a-124">Para obtener una explicación de cómo utilizar estas interfaces, vea [Cómo reproducir un archivo](how-to-play-a-file.md) y [responder a eventos](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="33b5a-124">For an explanation of how to use these interfaces, see [How To Play a File](how-to-play-a-file.md) and [Responding to Events](responding-to-events.md).</span></span> <span data-ttu-id="33b5a-125">En el código siguiente se muestra una manera de utilizar estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="33b5a-125">The following code shows one way to use these interfaces.</span></span>


```C++
IMediaControl   *pControl = NULL;
IMediaEvent     *pEvent = NULL;
long evCode;
pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
hr = pControl->Run();
hr = pEvent->WaitForCompletion(INFINITE, &evCode);
pControl->Stop();
```



<span data-ttu-id="33b5a-126">El código de este ejemplo bloquea la ejecución del programa hasta que se completa la reproducción, debido al parámetro infinito en la llamada al método [**IMediaEvent:: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) .</span><span class="sxs-lookup"><span data-stu-id="33b5a-126">The code in this example blocks program execution until playback completes, because of the INFINITE parameter in the [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) method call.</span></span> <span data-ttu-id="33b5a-127">Sin embargo, si se produce algún problema durante la reproducción, podría provocar que el programa dejara de responder.</span><span class="sxs-lookup"><span data-stu-id="33b5a-127">If something goes wrong during playback, however, it could cause the program to stop responding.</span></span> <span data-ttu-id="33b5a-128">En una aplicación real, use un bucle de mensajes para esperar a que se complete la reproducción.</span><span class="sxs-lookup"><span data-stu-id="33b5a-128">In a real application, use a message loop to wait for playback to complete.</span></span> <span data-ttu-id="33b5a-129">También se recomienda proporcionar al usuario una manera de interrumpir la reproducción.</span><span class="sxs-lookup"><span data-stu-id="33b5a-129">It's also recommended that you provide the user with a way to interrupt playback.</span></span>

<span data-ttu-id="33b5a-130">Cuando termine de usar el motor de representación, llame siempre al método [**IRenderEngine:: ScrapIt**](irenderengine-scrapit.md) .</span><span class="sxs-lookup"><span data-stu-id="33b5a-130">When you finish using the render engine, always call the [**IRenderEngine::ScrapIt**](irenderengine-scrapit.md) method.</span></span> <span data-ttu-id="33b5a-131">Este método elimina el gráfico de filtro y libera todos los recursos mantenidos por el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="33b5a-131">This method deletes the filter graph and releases any resources held by the render engine.</span></span>


```C++
pRender->ScrapIt();
```



## <a name="related-topics"></a><span data-ttu-id="33b5a-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="33b5a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33b5a-133">Cargar y obtener una vista previa de un proyecto</span><span class="sxs-lookup"><span data-stu-id="33b5a-133">Loading and Previewing a Project</span></span>](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



