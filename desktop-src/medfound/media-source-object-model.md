---
description: Modelo de objetos de origen de medios
ms.assetid: 88373028-8a34-4bf1-8300-d1a7e4c7dd75
title: Modelo de objetos de origen de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d05cc9d5341bff433d6276b5ee67505361b78f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361905"
---
# <a name="media-source-object-model"></a><span data-ttu-id="0e7c8-103">Modelo de objetos de origen de medios</span><span class="sxs-lookup"><span data-stu-id="0e7c8-103">Media Source Object Model</span></span>

<span data-ttu-id="0e7c8-104">En este tema se describe el modelo de objetos para orígenes multimedia en Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="0e7c8-104">This topic describes the object model for media sources in Microsoft Media Foundation.</span></span> <span data-ttu-id="0e7c8-105">Un origen multimedia debe implementar dos objetos:</span><span class="sxs-lookup"><span data-stu-id="0e7c8-105">A media source must implement two objects:</span></span>

-   <span data-ttu-id="0e7c8-106">Descriptor de presentación, que describe el contenido del origen, incluido el número de flujos y el formato de cada flujo.</span><span class="sxs-lookup"><span data-stu-id="0e7c8-106">A presentation descriptor, which describes the contents of the source, including the number of streams and the format of each stream.</span></span> <span data-ttu-id="0e7c8-107">Para obtener más información acerca de los descriptores de presentación, vea [descriptores de presentación](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="0e7c8-107">For more information about presentation descriptors, see [Presentation Descriptors](presentation-descriptors.md).</span></span>
-   <span data-ttu-id="0e7c8-108">Uno o más flujos multimedia, que generan los datos de origen.</span><span class="sxs-lookup"><span data-stu-id="0e7c8-108">One or more media streams, which generate the source data.</span></span>

<span data-ttu-id="0e7c8-109">El origen no crea los flujos hasta que se inicia la reproducción.</span><span class="sxs-lookup"><span data-stu-id="0e7c8-109">The source does not create the streams until playback starts.</span></span>

## <a name="media-source-interfaces"></a><span data-ttu-id="0e7c8-110">Interfaces de origen multimedia</span><span class="sxs-lookup"><span data-stu-id="0e7c8-110">Media Source Interfaces</span></span>

<span data-ttu-id="0e7c8-111">Un origen multimedia debe exponer las siguientes interfaces a través de **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="0e7c8-111">A media source must expose the following interfaces through **QueryInterface**.</span></span>



| <span data-ttu-id="0e7c8-112">Interfaz</span><span class="sxs-lookup"><span data-stu-id="0e7c8-112">Interface</span></span>                                                | <span data-ttu-id="0e7c8-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e7c8-113">Description</span></span>                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e7c8-114">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="0e7c8-114">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | <span data-ttu-id="0e7c8-115">Se requiere para todos los orígenes multimedia.</span><span class="sxs-lookup"><span data-stu-id="0e7c8-115">Required for all media sources.</span></span>                                                                                 |
| [<span data-ttu-id="0e7c8-116">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="0e7c8-116">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | <span data-ttu-id="0e7c8-117">Se requiere para todos los orígenes multimedia.</span><span class="sxs-lookup"><span data-stu-id="0e7c8-117">Required for all media sources.</span></span> <span data-ttu-id="0e7c8-118">La interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) hereda esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="0e7c8-118">The [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface inherits this interface.</span></span> |



 

<span data-ttu-id="0e7c8-119">Opcionalmente, un origen multimedia puede implementar la interfaz [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) e implementar cualquiera de las siguientes interfaces como servicios:</span><span class="sxs-lookup"><span data-stu-id="0e7c8-119">Optionally, a media source can implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface and implement any of the following interfaces as services:</span></span>



| <span data-ttu-id="0e7c8-120">Interfaz de servicio</span><span class="sxs-lookup"><span data-stu-id="0e7c8-120">Service interface</span></span>                                  | <span data-ttu-id="0e7c8-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e7c8-121">Description</span></span>                                                       |
|----------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="0e7c8-122">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="0e7c8-122">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)           | <span data-ttu-id="0e7c8-123">Controla la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="0e7c8-123">Controls the playback rate.</span></span>                                       |
| [<span data-ttu-id="0e7c8-124">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="0e7c8-124">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)           | <span data-ttu-id="0e7c8-125">Indica el intervalo de velocidades de reproducción que se admiten.</span><span class="sxs-lookup"><span data-stu-id="0e7c8-125">Reports the range of playback rates that are supported.</span></span>           |
| [<span data-ttu-id="0e7c8-126">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="0e7c8-126">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)       | <span data-ttu-id="0e7c8-127">Permite que el administrador de calidad ajuste la calidad de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="0e7c8-127">Enables the quality manager to adjust the audio or video quality.</span></span> |
| [<span data-ttu-id="0e7c8-128">**IMFMetadataProvider**</span><span class="sxs-lookup"><span data-stu-id="0e7c8-128">**IMFMetadataProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) | <span data-ttu-id="0e7c8-129">Proporciona metadatos.</span><span class="sxs-lookup"><span data-stu-id="0e7c8-129">Provides metadata.</span></span>                                                |



 

<span data-ttu-id="0e7c8-130">Si el origen de medios se puede reproducir a velocidades distintas de la velocidad normal (1,0), debe exponer el servicio de control de velocidad ([**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) y [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)).</span><span class="sxs-lookup"><span data-stu-id="0e7c8-130">If the media source can play at rates other than normal speed (1.0), it should expose the rate control service ([**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) and [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)).</span></span> <span data-ttu-id="0e7c8-131">De lo contrario, se supone que el origen solo admite la reproducción a velocidad normal.</span><span class="sxs-lookup"><span data-stu-id="0e7c8-131">Otherwise, it is assumed that the source only supports playback at normal speed.</span></span> <span data-ttu-id="0e7c8-132">Para obtener más información, vea [implementar el control de tasa](implementing-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="0e7c8-132">For more information, see [Implementing Rate Control](implementing-rate-control.md).</span></span>

<span data-ttu-id="0e7c8-133">Para obtener más información sobre las interfaces de servicio y [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice), consulte [interfaces de servicio](service-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="0e7c8-133">For more information about service interfaces and [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice), see [Service Interfaces](service-interfaces.md).</span></span>

## <a name="media-stream-interfaces"></a><span data-ttu-id="0e7c8-134">Interfaces de flujo multimedia</span><span class="sxs-lookup"><span data-stu-id="0e7c8-134">Media Stream Interfaces</span></span>

<span data-ttu-id="0e7c8-135">Los flujos multimedia deben implementar las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="0e7c8-135">Media streams must implement the following interfaces.</span></span>



| <span data-ttu-id="0e7c8-136">Interfaz</span><span class="sxs-lookup"><span data-stu-id="0e7c8-136">Interface</span></span>                                                | <span data-ttu-id="0e7c8-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e7c8-137">Description</span></span>                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e7c8-138">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="0e7c8-138">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)                 | <span data-ttu-id="0e7c8-139">Se requiere para todos los flujos multimedia.</span><span class="sxs-lookup"><span data-stu-id="0e7c8-139">Required for all media streams.</span></span>                                                                                 |
| [<span data-ttu-id="0e7c8-140">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="0e7c8-140">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | <span data-ttu-id="0e7c8-141">Se requiere para todos los flujos multimedia.</span><span class="sxs-lookup"><span data-stu-id="0e7c8-141">Required for all media streams.</span></span> <span data-ttu-id="0e7c8-142">La interfaz [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) hereda esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="0e7c8-142">The [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface inherits this interface.</span></span> |



 

<span data-ttu-id="0e7c8-143">Actualmente no hay interfaces de servicio definidas para flujos multimedia.</span><span class="sxs-lookup"><span data-stu-id="0e7c8-143">Currently no service interfaces are defined for media streams.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e7c8-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e7c8-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e7c8-145">Orígenes multimedia</span><span class="sxs-lookup"><span data-stu-id="0e7c8-145">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



