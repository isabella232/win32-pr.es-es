---
description: Obtener una vista previa de un proyecto
ms.assetid: 2efa3f25-a93f-4362-b461-b67475e5d78c
title: Obtener una vista previa de un proyecto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd9d299a99a0a7315cec986fbc044d427385647
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359945"
---
# <a name="previewing-a-project"></a><span data-ttu-id="a2618-103">Obtener una vista previa de un proyecto</span><span class="sxs-lookup"><span data-stu-id="a2618-103">Previewing a Project</span></span>

<span data-ttu-id="a2618-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="a2618-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="a2618-105">Para obtener una vista previa de un proyecto, llame primero a **CoCreateInstance** para crear una instancia del motor de representación básico.</span><span class="sxs-lookup"><span data-stu-id="a2618-105">To preview a project, first call **CoCreateInstance** to create an instance of the Basic Render Engine.</span></span> <span data-ttu-id="a2618-106">El identificador de clase es CLSID \_ RenderEngine.</span><span class="sxs-lookup"><span data-stu-id="a2618-106">The class identifier is CLSID\_RenderEngine.</span></span> <span data-ttu-id="a2618-107">A continuación, llame al método [**IRenderEngine:: SetTimelineObject**](irenderengine-settimelineobject.md) para especificar la escala de tiempo que está representando.</span><span class="sxs-lookup"><span data-stu-id="a2618-107">Then call the [**IRenderEngine::SetTimelineObject**](irenderengine-settimelineobject.md) method to specify the timeline that you are rendering.</span></span>

<span data-ttu-id="a2618-108">La primera vez que obtenga una vista previa de la escala de tiempo, realice las siguientes llamadas en el orden indicado:</span><span class="sxs-lookup"><span data-stu-id="a2618-108">The first time that you preview the timeline, perform the following calls in the order listed:</span></span>

1.  <span data-ttu-id="a2618-109">Llame a [**IRenderEngine:: SetRenderRange**](irenderengine-setrenderrange.md) para especificar qué parte de la escala de tiempo se va a mostrar en la vista previa.</span><span class="sxs-lookup"><span data-stu-id="a2618-109">Call [**IRenderEngine::SetRenderRange**](irenderengine-setrenderrange.md) to specify which portion of the timeline to preview.</span></span> <span data-ttu-id="a2618-110">(Opcional)</span><span class="sxs-lookup"><span data-stu-id="a2618-110">(Optional)</span></span>
2.  <span data-ttu-id="a2618-111">Llame a [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) para compilar el front-end del gráfico.</span><span class="sxs-lookup"><span data-stu-id="a2618-111">Call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span>
3.  <span data-ttu-id="a2618-112">Llame a [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md).</span><span class="sxs-lookup"><span data-stu-id="a2618-112">Call [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span> <span data-ttu-id="a2618-113">Este método conecta cada pin de salida a un representador de vídeo o representador de audio y completa el gráfico.</span><span class="sxs-lookup"><span data-stu-id="a2618-113">This method connects each output pin to a video renderer or audio renderer, completing the graph.</span></span>

<span data-ttu-id="a2618-114">En el ejemplo de código siguiente se muestran estos pasos:</span><span class="sxs-lookup"><span data-stu-id="a2618-114">The following code example shows these steps:</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, 
    CLSCTX_INPROC_SERVER, IID_IRenderEngine, (void**)&pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd();
hr = pRender->RenderOutputPins();
```



<span data-ttu-id="a2618-115">Ahora, ejecute el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="a2618-115">Now run the filter graph.</span></span> <span data-ttu-id="a2618-116">En primer lugar, llame al método [**IRenderEngine:: GetFilterGraph**](irenderengine-getfiltergraph.md) para recuperar un puntero a la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="a2618-116">First, call the [**IRenderEngine::GetFilterGraph**](irenderengine-getfiltergraph.md) method to retrieve a pointer to the Filter Graph Manager's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="a2618-117">A continuación, consulte el administrador de gráficos de filtro para la interfaz [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) y llame a [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), tal como se muestra en el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="a2618-117">Then query the Filter Graph Manager for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface and call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), as shown in the following code:</span></span>


```C++
IGraphBuilder   *pGraph = NULL;
IMediaControl   *pControl = NULL;
hr = pRender->GetFilterGraph(&pGraph);
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pControl->Run();
```



<span data-ttu-id="a2618-118">Use la interfaz [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) del administrador de gráficos de filtro para esperar a que se complete la vista previa.</span><span class="sxs-lookup"><span data-stu-id="a2618-118">Use the Filter Graph Manager's [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface to wait for the preview to complete.</span></span> <span data-ttu-id="a2618-119">También puede buscar el gráfico mediante la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) del administrador de gráficos de filtro, tal como lo haría con un gráfico de reproducción de archivos.</span><span class="sxs-lookup"><span data-stu-id="a2618-119">You can also seek the graph using the Filter Graph Manager's [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, just as you would with a file playback graph.</span></span>

<span data-ttu-id="a2618-120">Para volver a obtener una vista previa del proyecto, busque el gráfico de nuevo en el tiempo cero y vuelva a llamar a **Ejecutar** .</span><span class="sxs-lookup"><span data-stu-id="a2618-120">To preview the project again, seek the graph back to time zero and call **Run** again.</span></span> <span data-ttu-id="a2618-121">Si cambia el contenido de la escala de tiempo, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a2618-121">If you change the contents of the timeline, do the following:</span></span>

1.  <span data-ttu-id="a2618-122">Llame a **SetRenderRange**.</span><span class="sxs-lookup"><span data-stu-id="a2618-122">Call **SetRenderRange**.</span></span> <span data-ttu-id="a2618-123">(Opcional)</span><span class="sxs-lookup"><span data-stu-id="a2618-123">(Optional)</span></span>
2.  <span data-ttu-id="a2618-124">Llame a **ConnectFrontEnd**.</span><span class="sxs-lookup"><span data-stu-id="a2618-124">Call **ConnectFrontEnd**.</span></span>
3.  <span data-ttu-id="a2618-125">Si el método **ConnectFrontEnd** devuelve S \_ WARN \_ OUTPUTRESET, llame a **RenderOutputPins**.</span><span class="sxs-lookup"><span data-stu-id="a2618-125">If the **ConnectFrontEnd** method returns S\_WARN\_OUTPUTRESET, call **RenderOutputPins**.</span></span> <span data-ttu-id="a2618-126">(Si **ConnectFrontEnd** devuelve S \_ Bien, puede omitir este paso).</span><span class="sxs-lookup"><span data-stu-id="a2618-126">(If **ConnectFrontEnd** returns S\_OK, you can skip this step.)</span></span>
4.  <span data-ttu-id="a2618-127">Vuelva a buscar el gráfico en el tiempo cero.</span><span class="sxs-lookup"><span data-stu-id="a2618-127">Seek the graph back to time zero.</span></span>
5.  <span data-ttu-id="a2618-128">Ejecute el gráfico.</span><span class="sxs-lookup"><span data-stu-id="a2618-128">Run the graph.</span></span>

<span data-ttu-id="a2618-129">En el ejemplo siguiente se muestran estos pasos:</span><span class="sxs-lookup"><span data-stu-id="a2618-129">The following example shows these steps:</span></span>


```C++
hr = pRender->ConnectFrontEnd();
if (hr == S_WARN_OUTPUTRESET)
{
    hr = pRender->RenderOutputPins();
}
LONGLONG llStart = 0; 
hr = pSeek->SetPositions(&llStart, AM_SEEKING_AbsolutePositioning, 0, 0); 
hr = pControl->Run();
```



<span data-ttu-id="a2618-130">Para obtener un ejemplo completo en el que se carga y se muestra una vista previa de un archivo de proyecto, vea [cargar y obtener una vista previa de un proyecto](loading-and-previewing-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="a2618-130">For a complete example that loads and previews a project file, see [Loading and Previewing a Project](loading-and-previewing-a-project.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2618-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a2618-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2618-132">Administrar proyectos de edición de vídeo</span><span class="sxs-lookup"><span data-stu-id="a2618-132">Managing Video Editing Projects</span></span>](managing-video-editing-projects.md)
</dt> <dt>

[<span data-ttu-id="a2618-133">Representar un proyecto</span><span class="sxs-lookup"><span data-stu-id="a2618-133">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



