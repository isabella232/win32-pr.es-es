---
description: Eventos de origen de medios
ms.assetid: c7b6ea86-e919-45b8-a1f9-bd18c3aed163
title: Eventos de origen de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c40755a32f610b33ef3a5c66d3acb448223813
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717393"
---
# <a name="media-source-events"></a><span data-ttu-id="fa11e-103">Eventos de origen de medios</span><span class="sxs-lookup"><span data-stu-id="fa11e-103">Media Source Events</span></span>

<span data-ttu-id="fa11e-104">En este tema se enumeran los eventos enviados por los orígenes multimedia y los flujos multimedia.</span><span class="sxs-lookup"><span data-stu-id="fa11e-104">This topic lists the events that are sent by media sources and media streams.</span></span> <span data-ttu-id="fa11e-105">Los orígenes multimedia también pueden enviar eventos personalizados que no se enumeran aquí.</span><span class="sxs-lookup"><span data-stu-id="fa11e-105">Media sources can also send custom events not listed here.</span></span>

## <a name="media-source-events"></a><span data-ttu-id="fa11e-106">Eventos de origen de medios</span><span class="sxs-lookup"><span data-stu-id="fa11e-106">Media Source Events</span></span>



| <span data-ttu-id="fa11e-107">Evento</span><span class="sxs-lookup"><span data-stu-id="fa11e-107">Event</span></span>                                                                      | <span data-ttu-id="fa11e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa11e-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa11e-109">Evento MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="fa11e-109">MEEndOfPresentation Event</span></span>](meendofpresentation.md)                       | <span data-ttu-id="fa11e-110">Finalizó la presentación.</span><span class="sxs-lookup"><span data-stu-id="fa11e-110">The presentation ended.</span></span> <span data-ttu-id="fa11e-111">Todas las secuencias de la presentación han alcanzado el final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="fa11e-111">All streams in the presentation have reached the end of the stream.</span></span>      |
| [<span data-ttu-id="fa11e-112">Evento MENewStream</span><span class="sxs-lookup"><span data-stu-id="fa11e-112">MENewStream Event</span></span>](menewstream.md)                                       | <span data-ttu-id="fa11e-113">Se creó una nueva secuencia.</span><span class="sxs-lookup"><span data-stu-id="fa11e-113">A new stream was created.</span></span> <span data-ttu-id="fa11e-114">El evento contiene un puntero a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="fa11e-114">The event contains a pointer to the stream.</span></span>                            |
| [<span data-ttu-id="fa11e-115">Evento MESourceCharacteristicsChanged</span><span class="sxs-lookup"><span data-stu-id="fa11e-115">MESourceCharacteristicsChanged Event</span></span>](mesourcecharacteristicschanged.md) | <span data-ttu-id="fa11e-116">Las características del origen han cambiado.</span><span class="sxs-lookup"><span data-stu-id="fa11e-116">The characteristics of the source have changed.</span></span> <span data-ttu-id="fa11e-117">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="fa11e-117">(Optional.)</span></span>                                      |
| [<span data-ttu-id="fa11e-118">Evento MESourceMetadataChanged</span><span class="sxs-lookup"><span data-stu-id="fa11e-118">MESourceMetadataChanged Event</span></span>](mesourcemetadatachanged.md)               | <span data-ttu-id="fa11e-119">Los metadatos del origen han cambiado.</span><span class="sxs-lookup"><span data-stu-id="fa11e-119">The source's metadata has changed.</span></span> <span data-ttu-id="fa11e-120">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="fa11e-120">(Optional.)</span></span>                                                   |
| [<span data-ttu-id="fa11e-121">Evento MESourcePaused</span><span class="sxs-lookup"><span data-stu-id="fa11e-121">MESourcePaused Event</span></span>](mesourcepaused.md)                                 | <span data-ttu-id="fa11e-122">El origen está en pausa.</span><span class="sxs-lookup"><span data-stu-id="fa11e-122">The source was paused.</span></span> <span data-ttu-id="fa11e-123">No todos los orígenes admiten la pausa.</span><span class="sxs-lookup"><span data-stu-id="fa11e-123">Not all sources support pausing.</span></span>                                          |
| [<span data-ttu-id="fa11e-124">Evento MESourceRateChanged</span><span class="sxs-lookup"><span data-stu-id="fa11e-124">MESourceRateChanged Event</span></span>](mesourceratechanged.md)                       | <span data-ttu-id="fa11e-125">La velocidad de reproducción del origen ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="fa11e-125">The source's playback rate has changed.</span></span> <span data-ttu-id="fa11e-126">(Opcional; se aplica si el origen admite el control de tasas).</span><span class="sxs-lookup"><span data-stu-id="fa11e-126">(Optional; applies if the source supports rate control.)</span></span> |
| [<span data-ttu-id="fa11e-127">Evento MESourceRateChangeRequested</span><span class="sxs-lookup"><span data-stu-id="fa11e-127">MESourceRateChangeRequested Event</span></span>](mesourceratechangerequested.md)       | <span data-ttu-id="fa11e-128">El origen está solicitando una nueva velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="fa11e-128">The source is requesting a new playback rate.</span></span> <span data-ttu-id="fa11e-129">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="fa11e-129">(Optional.)</span></span>                                        |
| [<span data-ttu-id="fa11e-130">Evento MESourceSeeked</span><span class="sxs-lookup"><span data-stu-id="fa11e-130">MESourceSeeked Event</span></span>](mesourceseeked.md)                                 | <span data-ttu-id="fa11e-131">Se ha buscado el origen.</span><span class="sxs-lookup"><span data-stu-id="fa11e-131">The source was seeked.</span></span> <span data-ttu-id="fa11e-132">No todos los orígenes admiten búsquedas.</span><span class="sxs-lookup"><span data-stu-id="fa11e-132">Not all sources support seeking.</span></span>                                          |
| [<span data-ttu-id="fa11e-133">Evento MESourceStarted</span><span class="sxs-lookup"><span data-stu-id="fa11e-133">MESourceStarted Event</span></span>](mesourcestarted.md)                               | <span data-ttu-id="fa11e-134">Se inició el origen.</span><span class="sxs-lookup"><span data-stu-id="fa11e-134">The source was started.</span></span>                                                                          |
| [<span data-ttu-id="fa11e-135">Evento MESourceStopped</span><span class="sxs-lookup"><span data-stu-id="fa11e-135">MESourceStopped Event</span></span>](mesourcestopped.md)                               | <span data-ttu-id="fa11e-136">El origen se detuvo.</span><span class="sxs-lookup"><span data-stu-id="fa11e-136">The source was stopped.</span></span>                                                                          |
| [<span data-ttu-id="fa11e-137">Evento MEUpdatedStream</span><span class="sxs-lookup"><span data-stu-id="fa11e-137">MEUpdatedStream Event</span></span>](meupdatedstream.md)                               | <span data-ttu-id="fa11e-138">Se ha buscado o se ha vuelto a iniciar una secuencia existente.</span><span class="sxs-lookup"><span data-stu-id="fa11e-138">An existing stream was seeked or re-started.</span></span> <span data-ttu-id="fa11e-139">El evento contiene un puntero a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="fa11e-139">The event contains a pointer to the stream.</span></span>         |



 

## <a name="media-stream-events"></a><span data-ttu-id="fa11e-140">Eventos de flujo de medios</span><span class="sxs-lookup"><span data-stu-id="fa11e-140">Media Stream Events</span></span>



| <span data-ttu-id="fa11e-141">Evento</span><span class="sxs-lookup"><span data-stu-id="fa11e-141">Event</span></span>                                                    | <span data-ttu-id="fa11e-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa11e-142">Description</span></span>                                                                                                                    |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa11e-143">Evento MEEndOfStream</span><span class="sxs-lookup"><span data-stu-id="fa11e-143">MEEndOfStream Event</span></span>](meendofstream.md)                 | <span data-ttu-id="fa11e-144">La secuencia finalizó.</span><span class="sxs-lookup"><span data-stu-id="fa11e-144">The stream ended.</span></span>                                                                                                              |
| [<span data-ttu-id="fa11e-145">Evento MEError</span><span class="sxs-lookup"><span data-stu-id="fa11e-145">MEError Event</span></span>](meerror.md)                             | <span data-ttu-id="fa11e-146">Se ha producido un error durante el streaming.</span><span class="sxs-lookup"><span data-stu-id="fa11e-146">An error has occurred during streaming.</span></span> <span data-ttu-id="fa11e-147">Utilice este evento para los errores que no están relacionados con ninguno de los otros eventos que se enumeran aquí.</span><span class="sxs-lookup"><span data-stu-id="fa11e-147">Use this event for errors that are not related to any of the other events listed here.</span></span> |
| [<span data-ttu-id="fa11e-148">Evento MEMediaSample</span><span class="sxs-lookup"><span data-stu-id="fa11e-148">MEMediaSample Event</span></span>](memediasample.md)                 | <span data-ttu-id="fa11e-149">La secuencia ha generado un nuevo ejemplo.</span><span class="sxs-lookup"><span data-stu-id="fa11e-149">The stream has generated a new sample.</span></span>                                                                                         |
| [<span data-ttu-id="fa11e-150">Evento MEStreamFormatChanged</span><span class="sxs-lookup"><span data-stu-id="fa11e-150">MEStreamFormatChanged Event</span></span>](mestreamformatchanged.md) | <span data-ttu-id="fa11e-151">El tipo de medio ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="fa11e-151">The media type has changed.</span></span> <span data-ttu-id="fa11e-152">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="fa11e-152">(Optional.)</span></span>                                                                                        |
| [<span data-ttu-id="fa11e-153">Evento MEStreamPaused</span><span class="sxs-lookup"><span data-stu-id="fa11e-153">MEStreamPaused Event</span></span>](mestreampaused.md)               | <span data-ttu-id="fa11e-154">La secuencia está en pausa.</span><span class="sxs-lookup"><span data-stu-id="fa11e-154">The stream was paused.</span></span>                                                                                                         |
| [<span data-ttu-id="fa11e-155">Evento MEStreamSeeked</span><span class="sxs-lookup"><span data-stu-id="fa11e-155">MEStreamSeeked Event</span></span>](mestreamseeked.md)               | <span data-ttu-id="fa11e-156">Se ha buscado en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="fa11e-156">The stream was seeked.</span></span>                                                                                                         |
| [<span data-ttu-id="fa11e-157">Evento MEStreamStarted</span><span class="sxs-lookup"><span data-stu-id="fa11e-157">MEStreamStarted Event</span></span>](mestreamstarted.md)             | <span data-ttu-id="fa11e-158">Se inició el flujo.</span><span class="sxs-lookup"><span data-stu-id="fa11e-158">The stream was started.</span></span>                                                                                                        |
| [<span data-ttu-id="fa11e-159">Evento MEStreamStopped</span><span class="sxs-lookup"><span data-stu-id="fa11e-159">MEStreamStopped Event</span></span>](mestreamstopped.md)             | <span data-ttu-id="fa11e-160">La secuencia se detuvo.</span><span class="sxs-lookup"><span data-stu-id="fa11e-160">The stream was stopped.</span></span>                                                                                                        |
| [<span data-ttu-id="fa11e-161">Evento MEStreamThinMode</span><span class="sxs-lookup"><span data-stu-id="fa11e-161">MEStreamThinMode Event</span></span>](mestreamthinmode.md)           | <span data-ttu-id="fa11e-162">El modo delgado se ha iniciado o detenido.</span><span class="sxs-lookup"><span data-stu-id="fa11e-162">Thinning mode has started or stopped.</span></span> <span data-ttu-id="fa11e-163">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="fa11e-163">(Optional.)</span></span>                                                                              |
| [<span data-ttu-id="fa11e-164">Evento MEStreamTick</span><span class="sxs-lookup"><span data-stu-id="fa11e-164">MEStreamTick Event</span></span>](mestreamtick.md)                   | <span data-ttu-id="fa11e-165">Hay una brecha en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="fa11e-165">There is a gap in the stream.</span></span> <span data-ttu-id="fa11e-166">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="fa11e-166">(Optional.)</span></span>                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="fa11e-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fa11e-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa11e-168">Orígenes multimedia</span><span class="sxs-lookup"><span data-stu-id="fa11e-168">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



