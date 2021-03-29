---
description: Filtrar el administrador de gráficos
ms.assetid: b1a53193-27c6-4e86-a5b9-f3c1e4401690
title: Filtrar el administrador de gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161f15ea04e1404425d4671ca7991420e0aa993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906353"
---
# <a name="filter-graph-manager"></a><span data-ttu-id="0327c-103">Filtrar el administrador de gráficos</span><span class="sxs-lookup"><span data-stu-id="0327c-103">Filter Graph Manager</span></span>

<span data-ttu-id="0327c-104">El administrador de gráficos de filtros genera y controla los gráficos de filtros.</span><span class="sxs-lookup"><span data-stu-id="0327c-104">The Filter Graph Manager builds and controls filter graphs.</span></span> <span data-ttu-id="0327c-105">Este objeto es el componente central de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0327c-105">This object is the central component in DirectShow.</span></span> <span data-ttu-id="0327c-106">Las aplicaciones lo utilizan para compilar y controlar gráficos de filtros.</span><span class="sxs-lookup"><span data-stu-id="0327c-106">Applications use it to build and control filter graphs.</span></span> <span data-ttu-id="0327c-107">El administrador de gráficos de filtro también controla la sincronización, la notificación de eventos y otros aspectos del control del gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="0327c-107">The Filter Graph Manager also handles synchronization, event notification, and other aspects of the controlling the filter graph.</span></span> <span data-ttu-id="0327c-108">Cree este objeto llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="0327c-108">Create this object by calling **CoCreateInstance**.</span></span>

### <a name="clsid"></a><span data-ttu-id="0327c-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="0327c-109">CLSID</span></span>

<span data-ttu-id="0327c-110">Hay dos CLSID para crear el administrador de gráficos de filtro:</span><span class="sxs-lookup"><span data-stu-id="0327c-110">There are two CLSIDs for creating the Filter Graph Manager:</span></span>



| <span data-ttu-id="0327c-111">CLSID</span><span class="sxs-lookup"><span data-stu-id="0327c-111">CLSID</span></span>                      | <span data-ttu-id="0327c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="0327c-112">Description</span></span>                                                 |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="0327c-113">CLSID \_ FilterGraph</span><span class="sxs-lookup"><span data-stu-id="0327c-113">CLSID\_FilterGraph</span></span>         | <span data-ttu-id="0327c-114">Crea el administrador de gráficos de filtro en un subproceso de trabajo compartido.</span><span class="sxs-lookup"><span data-stu-id="0327c-114">Creates the Filter Graph Manager on a shared worker thread.</span></span> |
| <span data-ttu-id="0327c-115">CLSID \_ FilterGraphNoThread</span><span class="sxs-lookup"><span data-stu-id="0327c-115">CLSID\_FilterGraphNoThread</span></span> | <span data-ttu-id="0327c-116">Crea el administrador de gráficos de filtro en el subproceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0327c-116">Creates the Filter Graph Manager on the application thread.</span></span> |



 

<span data-ttu-id="0327c-117">Por lo general, las aplicaciones deben usar CLSID \_ FilterGraph.</span><span class="sxs-lookup"><span data-stu-id="0327c-117">Generally, applications should use CLSID\_FilterGraph.</span></span> <span data-ttu-id="0327c-118">Ambos CLSID crean el mismo objeto, pero usan diferentes modelos de subprocesos:</span><span class="sxs-lookup"><span data-stu-id="0327c-118">Both CLSIDs create the same object, but they use different threading models:</span></span>

-   <span data-ttu-id="0327c-119">CLSID \_ FilterGraph crea el administrador de gráficos de filtro en un subproceso de trabajo, que comparten todas \_ las instancias de FILTERGRAPH de CLSID dentro del mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="0327c-119">CLSID\_FilterGraph creates the Filter Graph Manager on a worker thread, which is shared by all CLSID\_FilterGraph instances within the same process.</span></span> <span data-ttu-id="0327c-120">El subproceso envía los mensajes enviados por los filtros y controla la duración de las ventanas creadas por los filtros.</span><span class="sxs-lookup"><span data-stu-id="0327c-120">The thread dispatches messages sent by filters, and controls the lifetime of any windows created by filters.</span></span>
-   <span data-ttu-id="0327c-121">CLSID \_ FilterGraphNoThread crea el administrador de gráficos de filtro en el subproceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0327c-121">CLSID\_FilterGraphNoThread creates the Filter Graph Manager on the application's thread.</span></span> <span data-ttu-id="0327c-122">Si usa este CLSID, el subproceso que llama a **CoCreateInstance** debe tener un bucle de mensajes que envíe los mensajes; de lo contrario, pueden producirse interbloqueos.</span><span class="sxs-lookup"><span data-stu-id="0327c-122">If you use this CLSID, the thread that calls **CoCreateInstance** must have a message loop that dispatches messages; otherwise, deadlocks can occur.</span></span> <span data-ttu-id="0327c-123">Además, antes de que el subproceso de la aplicación salga, debe liberar el administrador de gráficos de filtro y todos los objetos de gráfico (como filtros, PIN, relojes de referencia, etc.).</span><span class="sxs-lookup"><span data-stu-id="0327c-123">Also, before the application thread exits, it must release the Filter Graph Manager and all graph objects (such as filters, pins, reference clocks, and so forth).</span></span>

### <a name="interfaces"></a><span data-ttu-id="0327c-124">Interfaces</span><span class="sxs-lookup"><span data-stu-id="0327c-124">Interfaces</span></span>

<span data-ttu-id="0327c-125">El administrador de gráficos de filtro expone las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="0327c-125">The Filter Graph Manager exposes the following interfaces:</span></span>

-   [<span data-ttu-id="0327c-126">**IAMGraphStreams**</span><span class="sxs-lookup"><span data-stu-id="0327c-126">**IAMGraphStreams**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams)
-   [<span data-ttu-id="0327c-127">**IAMStats**</span><span class="sxs-lookup"><span data-stu-id="0327c-127">**IAMStats**</span></span>](/windows/desktop/api/Control/nn-control-iamstats)
-   [<span data-ttu-id="0327c-128">**IBasicAudio**</span><span class="sxs-lookup"><span data-stu-id="0327c-128">**IBasicAudio**</span></span>](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   [<span data-ttu-id="0327c-129">**IBasicVideo**</span><span class="sxs-lookup"><span data-stu-id="0327c-129">**IBasicVideo**</span></span>](/windows/desktop/api/Control/nn-control-ibasicvideo)
-   [<span data-ttu-id="0327c-130">**IBasicVideo2**</span><span class="sxs-lookup"><span data-stu-id="0327c-130">**IBasicVideo2**</span></span>](/windows/desktop/api/Control/nn-control-ibasicvideo2)
-   [<span data-ttu-id="0327c-131">**IFilterChain**</span><span class="sxs-lookup"><span data-stu-id="0327c-131">**IFilterChain**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)
-   [<span data-ttu-id="0327c-132">**IFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="0327c-132">**IFilterGraph**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph)
-   [<span data-ttu-id="0327c-133">**IFilterGraph2**</span><span class="sxs-lookup"><span data-stu-id="0327c-133">**IFilterGraph2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)
-   [<span data-ttu-id="0327c-134">**IFilterGraph3**</span><span class="sxs-lookup"><span data-stu-id="0327c-134">**IFilterGraph3**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph3)
-   [<span data-ttu-id="0327c-135">**IFilterMapper2**</span><span class="sxs-lookup"><span data-stu-id="0327c-135">**IFilterMapper2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)
-   [<span data-ttu-id="0327c-136">**IGraphBuilder**</span><span class="sxs-lookup"><span data-stu-id="0327c-136">**IGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)
-   [<span data-ttu-id="0327c-137">**IGraphConfig**</span><span class="sxs-lookup"><span data-stu-id="0327c-137">**IGraphConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)
-   [<span data-ttu-id="0327c-138">**IGraphVersion**</span><span class="sxs-lookup"><span data-stu-id="0327c-138">**IGraphVersion**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphversion)
-   [<span data-ttu-id="0327c-139">**IMediaControl**</span><span class="sxs-lookup"><span data-stu-id="0327c-139">**IMediaControl**</span></span>](/windows/desktop/api/Control/nn-control-imediacontrol)
-   [<span data-ttu-id="0327c-140">**IMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="0327c-140">**IMediaEvent**</span></span>](/windows/desktop/api/Control/nn-control-imediaevent)
-   [<span data-ttu-id="0327c-141">**IMediaEventEx**</span><span class="sxs-lookup"><span data-stu-id="0327c-141">**IMediaEventEx**</span></span>](/windows/desktop/api/Control/nn-control-imediaeventex)
-   [<span data-ttu-id="0327c-142">**IMediaEventSink**</span><span class="sxs-lookup"><span data-stu-id="0327c-142">**IMediaEventSink**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)
-   [<span data-ttu-id="0327c-143">**IMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="0327c-143">**IMediaFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediafilter)
-   [<span data-ttu-id="0327c-144">**IMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="0327c-144">**IMediaPosition**</span></span>](/windows/desktop/api/Control/nn-control-imediaposition)
-   [<span data-ttu-id="0327c-145">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="0327c-145">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)
-   [<span data-ttu-id="0327c-146">**IQueueCommand**</span><span class="sxs-lookup"><span data-stu-id="0327c-146">**IQueueCommand**</span></span>](/windows/desktop/api/Control/nn-control-iqueuecommand)
-   [<span data-ttu-id="0327c-147">**IRegisterServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="0327c-147">**IRegisterServiceProvider**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iregisterserviceprovider)
-   [<span data-ttu-id="0327c-148">**IResourceManager**</span><span class="sxs-lookup"><span data-stu-id="0327c-148">**IResourceManager**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager)
-   <span data-ttu-id="0327c-149">**IServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="0327c-149">**IServiceProvider**</span></span>
-   [<span data-ttu-id="0327c-150">**IVideoFrameStep**</span><span class="sxs-lookup"><span data-stu-id="0327c-150">**IVideoFrameStep**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)
-   [<span data-ttu-id="0327c-151">**IVideoWindow**</span><span class="sxs-lookup"><span data-stu-id="0327c-151">**IVideoWindow**</span></span>](/windows/desktop/api/Control/nn-control-ivideowindow)

## <a name="related-topics"></a><span data-ttu-id="0327c-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0327c-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0327c-153">Objetos de DirectShow</span><span class="sxs-lookup"><span data-stu-id="0327c-153">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



