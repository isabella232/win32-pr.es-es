---
description: Atributos de eventos
ms.assetid: 25e77ee1-cffc-4f8b-ac07-b5607a125fc7
title: Atributos de evento (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633e8f3857582422fe4a2d65ba34e68be483e7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539550"
---
# <a name="event-attributes-microsoft-media-foundation"></a><span data-ttu-id="7af4a-103">Atributos de evento (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="7af4a-103">Event Attributes (Microsoft Media Foundation)</span></span>

<span data-ttu-id="7af4a-104">Los atributos siguientes se aplican a los eventos.</span><span class="sxs-lookup"><span data-stu-id="7af4a-104">The following attributes apply to events.</span></span>



| <span data-ttu-id="7af4a-105">Atributo</span><span class="sxs-lookup"><span data-stu-id="7af4a-105">Attribute</span></span>                                                                                                        | <span data-ttu-id="7af4a-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="7af4a-106">Description</span></span>                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7af4a-107">**el \_ evento \_ MF \_ simplifica**</span><span class="sxs-lookup"><span data-stu-id="7af4a-107">**MF\_EVENT\_DO\_THINNING**</span></span>](mf-event-do-thinning-attribute.md)                                                | <span data-ttu-id="7af4a-108">Cuando un origen multimedia solicita una nueva velocidad de reproducción, especifica si el origen también solicita el ligero.</span><span class="sxs-lookup"><span data-stu-id="7af4a-108">When a media source requests a new playback rate, specifies whether the source also requests thinning.</span></span>                |
| [<span data-ttu-id="7af4a-109">**\_nodo de \_ salida de evento MF \_**</span><span class="sxs-lookup"><span data-stu-id="7af4a-109">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)                                                | <span data-ttu-id="7af4a-110">Identifica el nodo de la topología para un receptor de flujo.</span><span class="sxs-lookup"><span data-stu-id="7af4a-110">Identifies the topology node for a stream sink.</span></span>                                                                       |
| [<span data-ttu-id="7af4a-111">**\_desplazamiento de \_ tiempo de presentación de evento MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7af4a-111">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)                     | <span data-ttu-id="7af4a-112">Desplazamiento entre el tiempo de presentación y las marcas de tiempo del origen del medio.</span><span class="sxs-lookup"><span data-stu-id="7af4a-112">Offset between the presentation time and the media source's time stamps.</span></span>                                              |
| [<span data-ttu-id="7af4a-113">**\_hora de \_ SCRUBSAMPLE de eventos de MF \_**</span><span class="sxs-lookup"><span data-stu-id="7af4a-113">**MF\_EVENT\_SCRUBSAMPLE\_TIME**</span></span>](mf-event-scrubsample-time-attribute.md)                                      | <span data-ttu-id="7af4a-114">Tiempo de presentación de un ejemplo que se representó durante la limpieza.</span><span class="sxs-lookup"><span data-stu-id="7af4a-114">Presentation time for a sample that was rendered while scrubbing.</span></span>                                                     |
| [<span data-ttu-id="7af4a-115">**\_evento MF \_ SESSIONCAPS**</span><span class="sxs-lookup"><span data-stu-id="7af4a-115">**MF\_EVENT\_SESSIONCAPS**</span></span>](mf-event-sessioncaps-attribute.md)                                                 | <span data-ttu-id="7af4a-116">Contiene marcas que definen las funciones de la sesión multimedia, basándose en la presentación actual.</span><span class="sxs-lookup"><span data-stu-id="7af4a-116">Contains flags that define the capabilities of the Media Session, based on the current presentation.</span></span>                  |
| [<span data-ttu-id="7af4a-117">**\_SESSIONCAPS de evento MF \_ \_ Delta**</span><span class="sxs-lookup"><span data-stu-id="7af4a-117">**MF\_EVENT\_SESSIONCAPS\_DELTA**</span></span>](mf-event-sessioncaps-delta-attribute.md)                                    | <span data-ttu-id="7af4a-118">Contiene marcas que indican qué capacidades han cambiado en la sesión multimedia, en función de la presentación actual.</span><span class="sxs-lookup"><span data-stu-id="7af4a-118">Contains flags that indicate which capabilities have changed in the Media Session, based on the current presentation.</span></span> |
| [<span data-ttu-id="7af4a-119">**\_ \_ Inicio real del origen de eventos MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7af4a-119">**MF\_EVENT\_SOURCE\_ACTUAL\_START**</span></span>](mf-event-source-actual-start-attribute.md)                               | <span data-ttu-id="7af4a-120">Contiene la hora de inicio cuando un origen multimedia se reinicia desde su posición actual.</span><span class="sxs-lookup"><span data-stu-id="7af4a-120">Contains the start time when a media source restarts from its current position.</span></span>                                       |
| [<span data-ttu-id="7af4a-121">**\_características del \_ origen de eventos MF \_**</span><span class="sxs-lookup"><span data-stu-id="7af4a-121">**MF\_EVENT\_SOURCE\_CHARACTERISTICS**</span></span>](mf-event-source-characteristics-attribute.md)                          | <span data-ttu-id="7af4a-122">Especifica las características actuales del origen de los medios.</span><span class="sxs-lookup"><span data-stu-id="7af4a-122">Specifies the current characteristics of the media source.</span></span>                                                            |
| [<span data-ttu-id="7af4a-123">**\_características de origen de eventos MF \_ \_ \_ anteriores**</span><span class="sxs-lookup"><span data-stu-id="7af4a-123">**MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD**</span></span>](mf-event-source-characteristics-old-attribute.md)                 | <span data-ttu-id="7af4a-124">Especifica las características anteriores del origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="7af4a-124">Specifies the previous characteristics of the media source.</span></span>                                                           |
| [<span data-ttu-id="7af4a-125">**\_ \_ Inicio falso de origen de evento MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7af4a-125">**MF\_EVENT\_SOURCE\_FAKE\_START**</span></span>](mf-event-source-fake-start-attribute.md)                                   | <span data-ttu-id="7af4a-126">Especifica si la topología de segmento actual está vacía.</span><span class="sxs-lookup"><span data-stu-id="7af4a-126">Specifies whether the current segment topology is empty.</span></span>                                                              |
| [<span data-ttu-id="7af4a-127">**\_origen de evento MF \_ \_ PROJECTSTART**</span><span class="sxs-lookup"><span data-stu-id="7af4a-127">**MF\_EVENT\_SOURCE\_PROJECTSTART**</span></span>](mf-event-source-projectstart-attribute.md)                                | <span data-ttu-id="7af4a-128">Especifica la hora de inicio de una topología de segmento.</span><span class="sxs-lookup"><span data-stu-id="7af4a-128">Specifies the start time for a segment topology.</span></span>                                                                      |
| [<span data-ttu-id="7af4a-129">**\_topología de origen de eventos MF \_ \_ \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="7af4a-129">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)                     | <span data-ttu-id="7af4a-130">Especifica si el origen del secuenciador canceló una topología.</span><span class="sxs-lookup"><span data-stu-id="7af4a-130">Specifies whether the sequencer source canceled a topology.</span></span>                                                           |
| [<span data-ttu-id="7af4a-131">**\_tiempo de \_ presentación de inicio de evento de MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7af4a-131">**MF\_EVENT\_START\_PRESENTATION\_TIME**</span></span>](mf-event-start-presentation-time-attribute.md)                       | <span data-ttu-id="7af4a-132">La hora de inicio de la presentación, en unidades de 100-nanosegundos, según lo medido por el reloj de la presentación.</span><span class="sxs-lookup"><span data-stu-id="7af4a-132">The starting time for the presentation, in 100-nanosecond units, as measured by the presentation clock.</span></span>               |
| [<span data-ttu-id="7af4a-133">**\_ \_ \_ \_ tiempo de presentación de inicio \_ de evento MF en la \_ salida**</span><span class="sxs-lookup"><span data-stu-id="7af4a-133">**MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT**</span></span>](mf-event-start-presentation-time-at-output-attribute.md) | <span data-ttu-id="7af4a-134">El momento de la presentación en el que los receptores de medios van a representar el primer ejemplo de la nueva topología.</span><span class="sxs-lookup"><span data-stu-id="7af4a-134">The presentation time at which the media sinks will render the first sample of the new topology.</span></span>                      |
| [<span data-ttu-id="7af4a-135">**Estado de la \_ topología de eventos MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7af4a-135">**MF\_EVENT\_TOPOLOGY\_STATUS**</span></span>](mf-event-topology-status-attribute.md)                                        | <span data-ttu-id="7af4a-136">Especifica el estado de una topología durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="7af4a-136">Specifies the status of a topology during playback.</span></span>                                                                   |
| [<span data-ttu-id="7af4a-137">**\_tiempo de \_ \_ repetición de \_ evento \_ de sesión MF aprox.**</span><span class="sxs-lookup"><span data-stu-id="7af4a-137">**MF\_SESSION\_APPROX\_EVENT\_OCCURRENCE\_TIME**</span></span>](mf-session-approx-event-occurrence-time-attribute.md)        | <span data-ttu-id="7af4a-138">La hora aproximada a la que la sesión multimedia generó un evento.</span><span class="sxs-lookup"><span data-stu-id="7af4a-138">The approximate time when the Media Session raised an event.</span></span>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="7af4a-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7af4a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7af4a-140">**IMFMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="7af4a-140">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
</dt> <dt>

[<span data-ttu-id="7af4a-141">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7af4a-141">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="7af4a-142">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7af4a-142">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



