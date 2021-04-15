---
description: EVR negociación de tipo de medio
ms.assetid: 3a12b80d-7aac-437d-b515-aab37c1e81b2
title: EVR negociación de tipo de medio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb1f87a24db866c9e80b211b0385c12dcd6b594
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361890"
---
# <a name="evr-media-type-negotiation"></a><span data-ttu-id="63faf-103">EVR negociación de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="63faf-103">EVR Media Type Negotiation</span></span>

<span data-ttu-id="63faf-104">En este tema se describe cómo el representador de vídeo mejorado (EVR) valida los tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="63faf-104">This topic describes how the enhanced video renderer (EVR) validates media types.</span></span>

-   <span data-ttu-id="63faf-105">En el caso del filtro EVR de DirectShow, la negociación de tipos se produce cuando se conectan los PIN del filtro.</span><span class="sxs-lookup"><span data-stu-id="63faf-105">For the DirectShow EVR filter, type negotiation occurs when the filter's pins are connected.</span></span>

-   <span data-ttu-id="63faf-106">En el caso del receptor de medios EVR, los tipos de medios se establecen a través de la interfaz [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) en los receptores de flujo.</span><span class="sxs-lookup"><span data-stu-id="63faf-106">For the EVR media sink, the media types are set through the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface on the stream sinks.</span></span> <span data-ttu-id="63faf-107">Normalmente, el cargador de topología negocia los tipos de medios, aunque la aplicación también puede establecer los tipos de medios directamente.</span><span class="sxs-lookup"><span data-stu-id="63faf-107">Typically the topology loader negotiates the media types, although the application can also set the media types directly.</span></span>

<span data-ttu-id="63faf-108">EVR no informa de ningún tipo de medio preferido.</span><span class="sxs-lookup"><span data-stu-id="63faf-108">The EVR does not report any preferred media types.</span></span> <span data-ttu-id="63faf-109">El cliente debe probar los tipos de medios hasta que encuentre un tipo aceptable.</span><span class="sxs-lookup"><span data-stu-id="63faf-109">The client must test media types until it finds an acceptable type.</span></span> <span data-ttu-id="63faf-110">El tipo de medio para la secuencia de referencia debe establecerse antes de que se puedan establecer los tipos en cualquiera de las subsecuencias.</span><span class="sxs-lookup"><span data-stu-id="63faf-110">The media type for the reference stream must be set before the types can be set on any of the substreams.</span></span>

<span data-ttu-id="63faf-111">En el flujo de referencia, el mezclador de EVR obtiene una lista de formatos de destino de representación de DirectX video Acceleration (DXVA) compatibles.</span><span class="sxs-lookup"><span data-stu-id="63faf-111">For the reference stream, the EVR mixer gets a list of compatible DirectX Video Acceleration (DXVA) render target formats.</span></span> <span data-ttu-id="63faf-112">El presentador de EVR usa esta lista para seleccionar el formato de la cadena de intercambio de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="63faf-112">The EVR presenter uses this list to select the format for the Direct3D swap chain.</span></span> <span data-ttu-id="63faf-113">Si no se puede encontrar ningún formato de destino de representación compatible, el EVR rechaza el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="63faf-113">If no compatible render target format can be found, the EVR rejects the media type.</span></span>

<span data-ttu-id="63faf-114">En el caso de las subsecuencias, el mezclador EVR consulta si el dispositivo DXVA admite ese formato de subsecuencia en combinación con el formato de destino de representación que se seleccionó para la secuencia de referencia.</span><span class="sxs-lookup"><span data-stu-id="63faf-114">For the substreams, the EVR mixer queries whether the DXVA device supports that substream format in combination with the render target format that was selected for the reference stream.</span></span> <span data-ttu-id="63faf-115">Como resultado, los formatos de subflujo disponibles pueden cambiar en función del flujo de referencia.</span><span class="sxs-lookup"><span data-stu-id="63faf-115">As a result, the available substream formats might change depending on the reference stream.</span></span>

<span data-ttu-id="63faf-116">Este es el proceso con más detalle.</span><span class="sxs-lookup"><span data-stu-id="63faf-116">Here is the process in more detail.</span></span> <span data-ttu-id="63faf-117">Estos detalles no son importantes para la mayoría de las aplicaciones, pero pueden resultar útiles si está escribiendo un presentador o mezclador personalizado.</span><span class="sxs-lookup"><span data-stu-id="63faf-117">These details are not important for most applications, but might be helpful if you are writing a custom mixer or presenter.</span></span>

<span data-ttu-id="63faf-118">En el flujo de referencia, la negociación se produce de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="63faf-118">For the reference stream, negotiation happens as follows:</span></span>

1.  <span data-ttu-id="63faf-119">EVR llama a [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) en el mezclador.</span><span class="sxs-lookup"><span data-stu-id="63faf-119">The EVR calls [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) on the mixer.</span></span>

2.  <span data-ttu-id="63faf-120">El mezclador convierte el tipo de medio en una descripción de DXVA 2,0 mediante la [**estructura \_ videodesc de DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) .</span><span class="sxs-lookup"><span data-stu-id="63faf-120">The mixer converts the media type to a DXVA 2.0 description, using the [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure.</span></span>

3.  <span data-ttu-id="63faf-121">El mezclador llama a [**IDirectXVideoProcessorService:: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) para obtener una lista de los GUID del procesador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="63faf-121">The mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) to get a list of video processor GUIDs.</span></span>

4.  <span data-ttu-id="63faf-122">Para cada GUID del procesador de vídeo, el mezclador llama a [**IDirectXVideoProcessorService:: GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) para obtener los formatos de destino de representación admitidos.</span><span class="sxs-lookup"><span data-stu-id="63faf-122">For each video processor GUID, the mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) to get the supported render target formats.</span></span>

5.  <span data-ttu-id="63faf-123">EVR llama a [**IMFVideoPresenter::P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) en el presentador con el mensaje MFVP \_ Message \_ INVALIDATEMEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="63faf-123">The EVR calls [**IMFVideoPresenter::ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) on the presenter with the MFVP\_MESSAGE\_INVALIDATEMEDIATYPE message.</span></span> <span data-ttu-id="63faf-124">Este mensaje hace que el presentador Seleccione un nuevo formato.</span><span class="sxs-lookup"><span data-stu-id="63faf-124">This message causes the presenter to select a new format.</span></span>

6.  <span data-ttu-id="63faf-125">El presentador llama a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obtener una lista de los formatos de salida disponibles del mezclador.</span><span class="sxs-lookup"><span data-stu-id="63faf-125">The presenter calls [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get a list of available output formats from the mixer.</span></span> <span data-ttu-id="63faf-126">El mezclador genera esta lista a partir de los formatos obtenidos en el paso 4.</span><span class="sxs-lookup"><span data-stu-id="63faf-126">The mixer generates this list from the formats obtained in step 4.</span></span>

7.  <span data-ttu-id="63faf-127">El presentador selecciona un formato y llama a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) en el mezclador.</span><span class="sxs-lookup"><span data-stu-id="63faf-127">The presenter selects a format and calls [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) on the mixer.</span></span>

<span data-ttu-id="63faf-128">En el caso de las subsecuencias, el proceso es más sencillo:</span><span class="sxs-lookup"><span data-stu-id="63faf-128">For substreams, the process is simpler:</span></span>

1.  <span data-ttu-id="63faf-129">EVR llama a [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) en el mezclador.</span><span class="sxs-lookup"><span data-stu-id="63faf-129">The EVR calls [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) on the mixer.</span></span>

2.  <span data-ttu-id="63faf-130">El mezclador llama a [**IDirectXVideoProcessorService:: GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) para obtener una lista de los formatos de subflujo disponibles.</span><span class="sxs-lookup"><span data-stu-id="63faf-130">The mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) to get a list of available substream formats.</span></span>

3.  <span data-ttu-id="63faf-131">Si el formato propuesto está contenido en esta lista, EVR acepta el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="63faf-131">If the proposed format is contained in this list, the EVR accepts the input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63faf-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="63faf-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63faf-133">Representador de vídeo mejorado</span><span class="sxs-lookup"><span data-stu-id="63faf-133">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 



