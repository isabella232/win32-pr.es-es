---
description: Temas de captura avanzada
ms.assetid: 407702b2-5f4f-424d-a3ec-b0473e1b0da3
title: Temas de captura avanzada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c4e5a077f6f8b17543250efa0f10091f0917e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152518"
---
# <a name="advanced-capture-topics"></a><span data-ttu-id="d03ca-103">Temas de captura avanzada</span><span class="sxs-lookup"><span data-stu-id="d03ca-103">Advanced Capture Topics</span></span>

<span data-ttu-id="d03ca-104">En esta sección se describen algunos aspectos avanzados de la captura de vídeo en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d03ca-104">This section describes some advanced aspects of video capture in DirectShow.</span></span> <span data-ttu-id="d03ca-105">La mayoría de los problemas descritos en esta sección se controlan automáticamente mediante la interfaz [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .</span><span class="sxs-lookup"><span data-stu-id="d03ca-105">Most of the issues described in this section are automatically handled by the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="d03ca-106">Sin embargo, esta información puede ser útil si necesita solucionar problemas de una aplicación de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d03ca-106">However, the information here may be useful if you need to troubleshoot a video capture application.</span></span> <span data-ttu-id="d03ca-107">También debe leer esta sección si la aplicación genera un gráfico de captura personalizado de algún tipo y observa que ICaptureGraphBuilder2 no se adapta a sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="d03ca-107">You should also read this section if your application builds a custom capture graph of some kind and you find that ICaptureGraphBuilder2 does not suit your needs.</span></span> <span data-ttu-id="d03ca-108">Por último, en esta sección se incluye información sobre el uso del filtro de representador de mezcla de vídeo (VMR) en una aplicación de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d03ca-108">Finally, this section contains some information about using the Video Mixing Renderer (VMR) filter in a video capture application.</span></span>

<span data-ttu-id="d03ca-109">Es posible crear un gráfico de captura de vídeo completamente mediante métodos [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="d03ca-109">It is possible to build a video capture graph entirely using [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) methods.</span></span> <span data-ttu-id="d03ca-110">También puede combinar las dos interfaces, usando ICaptureGraphBuilder2 para algunas tareas y IGraphBuilder para otras.</span><span class="sxs-lookup"><span data-stu-id="d03ca-110">You can also combine the two interfaces, using ICaptureGraphBuilder2 for some tasks and IGraphBuilder for others.</span></span>

<span data-ttu-id="d03ca-111">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="d03ca-111">This section contains the following topics:</span></span>

-   [<span data-ttu-id="d03ca-112">Control de eventos Repaint en la captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="d03ca-112">Handling Repaint Events in Video Capture</span></span>](handling-repaint-events-in-video-capture.md)
-   [<span data-ttu-id="d03ca-113">Trabajar con categorías de PIN</span><span class="sxs-lookup"><span data-stu-id="d03ca-113">Working with Pin Categories</span></span>](working-with-pin-categories.md)
-   [<span data-ttu-id="d03ca-114">Usar el filtro Smart Tee</span><span class="sxs-lookup"><span data-stu-id="d03ca-114">Using the Smart Tee Filter</span></span>](using-the-smart-tee-filter.md)
-   [<span data-ttu-id="d03ca-115">Usar el mezclador de superposición en la captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="d03ca-115">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
-   [<span data-ttu-id="d03ca-116">PIN de puerto de vídeo</span><span class="sxs-lookup"><span data-stu-id="d03ca-116">Video Port Pins</span></span>](video-port-pins.md)
-   [<span data-ttu-id="d03ca-117">Tipo de formato VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="d03ca-117">VideoInfo2 Format Type</span></span>](videoinfo2-format-type.md)
-   [<span data-ttu-id="d03ca-118">Crear filtros de Kernel-Mode</span><span class="sxs-lookup"><span data-stu-id="d03ca-118">Creating Kernel-Mode Filters</span></span>](creating-kernel-mode-filters.md)
-   [<span data-ttu-id="d03ca-119">Filtros de controlador de clase WDM</span><span class="sxs-lookup"><span data-stu-id="d03ca-119">WDM Class Driver Filters</span></span>](wdm-class-driver-filters.md)
-   [<span data-ttu-id="d03ca-120">Usar la captura de WDDM en DirectShow</span><span class="sxs-lookup"><span data-stu-id="d03ca-120">Using WDDM Capture in DirectShow</span></span>](using-wddm-capture-in-directshow.md)

## <a name="related-topics"></a><span data-ttu-id="d03ca-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d03ca-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d03ca-122">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="d03ca-122">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



