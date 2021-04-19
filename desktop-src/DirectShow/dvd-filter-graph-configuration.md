---
description: Configuración del gráfico de filtros de DVD
ms.assetid: 0c68c456-2240-4090-b45c-bd098cfea645
title: Configuración del gráfico de filtros de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec7bb8757e5246fc01309fbef55e654436560b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537954"
---
# <a name="dvd-filter-graph-configuration"></a><span data-ttu-id="14083-103">Configuración del gráfico de filtros de DVD</span><span class="sxs-lookup"><span data-stu-id="14083-103">DVD Filter Graph Configuration</span></span>

<span data-ttu-id="14083-104">En esta sección se describen las distintas configuraciones de gráficos de filtros para la reproducción de DVD en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="14083-104">This section describes the various filter graph configurations for DVD playback in DirectShow.</span></span> <span data-ttu-id="14083-105">Estos diagramas se proporcionan principalmente como referencia.</span><span class="sxs-lookup"><span data-stu-id="14083-105">These diagrams are provided mainly for reference.</span></span> <span data-ttu-id="14083-106">El navegador de DVD crea el gráfico, por lo que en general no es necesario comprender los detalles de cómo se configura el gráfico.</span><span class="sxs-lookup"><span data-stu-id="14083-106">The DVD Navigator builds the graph, so in general it is not necessary to understand the details of how the graph is configured.</span></span> <span data-ttu-id="14083-107">Para obtener más información, vea [crear el gráfico de filtros de DVD](building-the-dvd-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="14083-107">For more information, see [Building the DVD Filter Graph](building-the-dvd-filter-graph.md).</span></span>

<span data-ttu-id="14083-108">En la ilustración siguiente se muestra un gráfico de filtros de DVD con un descodificador de software.</span><span class="sxs-lookup"><span data-stu-id="14083-108">The following illustration shows a DVD filter graph with a software decoder.</span></span>

![gráfico de filtros de DVD para Windows XP](images/dvd-graph-xp.png)

<span data-ttu-id="14083-110">Cuando un descodificador de hardware está presente, normalmente se conecta directamente a la tarjeta de vídeo mediante un puerto de vídeo.</span><span class="sxs-lookup"><span data-stu-id="14083-110">When a hardware decoder is present, it is typically connected directly to the video card by a video port.</span></span> <span data-ttu-id="14083-111">Esto permite que los bits de vídeo descodificados se envíen directamente al búfer de fotogramas de la tarjeta gráfica sin pasar a la memoria del host.</span><span class="sxs-lookup"><span data-stu-id="14083-111">This enables the decoded video bits to be sent directly to the frame buffer on the graphics card without passing into host memory.</span></span> <span data-ttu-id="14083-112">Para administrar esta conexión directa en versiones anteriores de Windows, DirectShow es compatible con las extensiones de puerto de vídeo (VPE) de DirectDraw a través de una interfaz en el [filtro de mezclador de superposición](overlay-mixer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="14083-112">To manage this direct connection on earlier versions of Windows, DirectShow supports DirectDraw Video Port Extensions (VPE) through an interface on the [Overlay Mixer Filter](overlay-mixer-filter.md).</span></span>

> [!Note]  
> <span data-ttu-id="14083-113">El mezclador de superposición está ahora en desuso.</span><span class="sxs-lookup"><span data-stu-id="14083-113">The Overlay Mixer is now deprecated.</span></span>

 

<span data-ttu-id="14083-114">En Windows XP y versiones posteriores, un descodificador de hardware puede conectarse al filtro del [Administrador de puertos de vídeo](video-port-manager.md) .</span><span class="sxs-lookup"><span data-stu-id="14083-114">In Windows XP and later, a hardware decoder can connect to the [Video Port Manager](video-port-manager.md) filter.</span></span>

![DVD Graph para Windows XP con un descodificador de hardware](images/dvd-hwgraph-xp.png)

<span data-ttu-id="14083-116">En todos estos gráficos, el explorador de DVD es el filtro de origen; realiza varias tareas:</span><span class="sxs-lookup"><span data-stu-id="14083-116">In all these graphs, the DVD Navigator is the source filter; it performs several tasks:</span></span>

-   <span data-ttu-id="14083-117">Lee los datos de navegación y vídeo del disco.</span><span class="sxs-lookup"><span data-stu-id="14083-117">Reads the navigation and video data from the disc.</span></span>
-   <span data-ttu-id="14083-118">Desmultiplexa los datos de vídeo, audio y subimagen en flujos independientes.</span><span class="sxs-lookup"><span data-stu-id="14083-118">Demultiplexes the video, audio, and subpicture data into separate streams.</span></span>
-   <span data-ttu-id="14083-119">Bombea los flujos en el gráfico para su posterior procesamiento y representación final.</span><span class="sxs-lookup"><span data-stu-id="14083-119">Pumps the streams into the graph for further processing and eventual rendering.</span></span>
-   <span data-ttu-id="14083-120">Informa a la aplicación de eventos relacionados con DVD.</span><span class="sxs-lookup"><span data-stu-id="14083-120">Informs your application of DVD-related events.</span></span>

<span data-ttu-id="14083-121">En la secuencia de audio, el explorador de DVD se conecta de nivel inferior a un descodificador de audio, que se conecta al [filtro de representador de DirectSound](directsound-renderer-filter.md), el representador de audio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="14083-121">On the audio stream, the DVD Navigator connects downstream to an audio decoder, which connects to the [DirectSound Renderer Filter](directsound-renderer-filter.md), the default audio renderer.</span></span> <span data-ttu-id="14083-122">En las secuencias de vídeo y de subimagen, los filtros de nivel inferior son el descodificador de vídeo de terceros y el representador de mezcla de vídeo (o el [mezclador de superposición](overlay-mixer-filter.md)y el [representador de vídeo](video-renderer-filter.md) en aplicaciones de nivel inferior).</span><span class="sxs-lookup"><span data-stu-id="14083-122">On the video and subpicture streams, the downstream filters are the third-party video decoder, and the Video Mixing Renderer (or the [Overlay Mixer](overlay-mixer-filter.md), and the [Video Renderer](video-renderer-filter.md) on downlevel applications).</span></span> <span data-ttu-id="14083-123">Si la aplicación va a controlar los datos de subtítulos (CC) de la línea 21, debe agregar el filtro de la línea de código 21 de DirectShow al gráfico.</span><span class="sxs-lookup"><span data-stu-id="14083-123">If your application will handle line 21 closed-captioned data, you must add the DirectShow Line 21 Decoder 2 filter to the graph.</span></span> <span data-ttu-id="14083-124">Esto implica una única llamada al método; el filtro se conectará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="14083-124">This involves a single method call; the filter will be connected automatically.</span></span>

<span data-ttu-id="14083-125">La aplicación se comunica con el navegador de DVD y lo controla a través de las interfaces personalizadas que expone el navegador de DVD: [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2): los métodos "SET" (y [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)).</span><span class="sxs-lookup"><span data-stu-id="14083-125">Your application communicates with and controls the DVD Navigator through the custom interfaces that the DVD Navigator exposes: [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)—the "set" methods—and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)—the "get" methods.</span></span> <span data-ttu-id="14083-126">También debe comunicarse con el administrador de gráficos de filtro (a través de [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) para detener, iniciar y, de lo contrario, controlar el gráfico.</span><span class="sxs-lookup"><span data-stu-id="14083-126">It also must communicate with the filter graph manager (through [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) to stop, start, and otherwise control the graph.</span></span> <span data-ttu-id="14083-127">Es posible que también necesite controlar otros filtros individuales, como el filtro de mezclador de superposición para cambiar entre la presentación en ventanas y la pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="14083-127">You might also need to control other individual filters, such as the Overlay Mixer filter for switching between windowed and full-screen display.</span></span> <span data-ttu-id="14083-128">Para obtener más información, vea [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2).</span><span class="sxs-lookup"><span data-stu-id="14083-128">For more information, see [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2).</span></span> <span data-ttu-id="14083-129">La configuración exacta del gráfico variará en función del tipo de descodificador MPEG-2 que haya instalado, independientemente de que sea necesario controlar los datos de subtítulos (CC) de línea 21 y otros factores.</span><span class="sxs-lookup"><span data-stu-id="14083-129">The exact configuration of the graph will vary depending on what type of MPEG-2 decoder you have installed, whether you need to handle line 21 closed-captioned data, and other factors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14083-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="14083-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14083-131">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="14083-131">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



