---
description: Objeto de streaming multimedia y jerarquía de la interfaz
ms.assetid: dbb6dc3b-b55e-4f6c-918f-068308e2dba9
title: Objeto de streaming multimedia y jerarquía de la interfaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52339644730139af22fd21fa2c24b8448a1afaf3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914229"
---
# <a name="multimedia-streaming-object-and-interface-hierarchy"></a><span data-ttu-id="f679a-103">Objeto de streaming multimedia y jerarquía de la interfaz</span><span class="sxs-lookup"><span data-stu-id="f679a-103">Multimedia Streaming Object and Interface Hierarchy</span></span>

> [!Note]  
> <span data-ttu-id="f679a-104">Estas API están en desuso.</span><span class="sxs-lookup"><span data-stu-id="f679a-104">These APIs are deprecated.</span></span> <span data-ttu-id="f679a-105">Las aplicaciones deben usar el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un gráfico de filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f679a-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="f679a-106">En el diagrama siguiente se muestra la jerarquía de objetos que se usa en el streaming multimedia.</span><span class="sxs-lookup"><span data-stu-id="f679a-106">The following diagram shows the object hierarchy used in multimedia streaming.</span></span>

![jerarquía de objetos multimediastreaming](images/mmstream02.png)

<span data-ttu-id="f679a-108">La arquitectura de transmisión por secuencias multimedia define tres tipos generales de objeto:</span><span class="sxs-lookup"><span data-stu-id="f679a-108">The multimedia streaming architecture defines three general type of object:</span></span>

-   <span data-ttu-id="f679a-109">El objeto **AMMultimediaStream** expone la interfaz [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) .</span><span class="sxs-lookup"><span data-stu-id="f679a-109">The **AMMultimediaStream** object exposes the [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) interface.</span></span> <span data-ttu-id="f679a-110">Internamente, este objeto ajusta el gráfico de filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f679a-110">Internally, this object wraps the DirectShow filter graph.</span></span>
-   <span data-ttu-id="f679a-111">Los objetos de *flujo de medios* exponen la interfaz [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) y son específicos de los datos.</span><span class="sxs-lookup"><span data-stu-id="f679a-111">*Media stream* objects expose the [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) interface and are data specific.</span></span> <span data-ttu-id="f679a-112">El objeto AMMultimediaStream contiene uno o más flujos multimedia.</span><span class="sxs-lookup"><span data-stu-id="f679a-112">The AMMultimediaStream object contains one or more media streams.</span></span>
-   <span data-ttu-id="f679a-113">Los objetos de *ejemplo de secuencia* contienen los datos de una secuencia determinada.</span><span class="sxs-lookup"><span data-stu-id="f679a-113">*Stream sample* objects contain the data for a particular stream.</span></span>

<span data-ttu-id="f679a-114">Se admiten los siguientes objetos de flujo multimedia:</span><span class="sxs-lookup"><span data-stu-id="f679a-114">The following media stream objects are supported:</span></span>

-   <span data-ttu-id="f679a-115">Secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="f679a-115">Audio stream.</span></span> <span data-ttu-id="f679a-116">Expone la interfaz [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) .</span><span class="sxs-lookup"><span data-stu-id="f679a-116">Exposes the [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) interface.</span></span>
-   <span data-ttu-id="f679a-117">Secuencia de DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="f679a-117">DirectDraw stream.</span></span> <span data-ttu-id="f679a-118">Representa una secuencia de vídeo que se representa en una superficie de DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="f679a-118">Represents a video stream that is rendered to a DirectDraw surface.</span></span> <span data-ttu-id="f679a-119">Expone la interfaz [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) .</span><span class="sxs-lookup"><span data-stu-id="f679a-119">Exposes the [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) interface.</span></span>
-   <span data-ttu-id="f679a-120">Secuencia de tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="f679a-120">Media type stream.</span></span> <span data-ttu-id="f679a-121">Representa datos arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="f679a-121">Represents arbitrary data.</span></span> <span data-ttu-id="f679a-122">Expone la interfaz [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) .</span><span class="sxs-lookup"><span data-stu-id="f679a-122">Exposes the [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) interface.</span></span>

<span data-ttu-id="f679a-123">Cada objeto de flujo multimedia crea su propio tipo de objeto de ejemplo de secuencia:</span><span class="sxs-lookup"><span data-stu-id="f679a-123">Each media stream object creates its own kind of stream sample object:</span></span>

-   <span data-ttu-id="f679a-124">Secuencias de audio cree ejemplos de audio, que exponen la interfaz [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) .</span><span class="sxs-lookup"><span data-stu-id="f679a-124">Audio streams create audio samples, which expose the [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) interface.</span></span>
-   <span data-ttu-id="f679a-125">Las secuencias DirectDraw crean ejemplos de DirectDraw, que exponen la interfaz [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) .</span><span class="sxs-lookup"><span data-stu-id="f679a-125">DirectDraw streams create DirectDraw samples, which expose the [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) interface.</span></span>
-   <span data-ttu-id="f679a-126">Los flujos de tipo de medio crean ejemplos de tipos de medios, que exponen la interfaz [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) .</span><span class="sxs-lookup"><span data-stu-id="f679a-126">Media type streams create media type samples, which expose the [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) interface.</span></span>

<span data-ttu-id="f679a-127">En el diagrama siguiente se muestra la jerarquía de la interfaz para las interfaces enumeradas anteriormente:</span><span class="sxs-lookup"><span data-stu-id="f679a-127">The following diagram shows the interface hierarchy for the interfaces listed previously:</span></span>

![jerarquía de la interfaz multimediastreaming](images/mmstream01.png)

 

 



