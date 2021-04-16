---
description: Acerca del origen del secuenciador
ms.assetid: 0d7ce9ca-9f34-4842-bd49-9211ae4454de
title: Acerca del origen del secuenciador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d8de3e0ff46cab1e68b767294633ecd09ebc161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542174"
---
# <a name="about-the-sequencer-source"></a><span data-ttu-id="f2b2f-103">Acerca del origen del secuenciador</span><span class="sxs-lookup"><span data-stu-id="f2b2f-103">About the Sequencer Source</span></span>

<span data-ttu-id="f2b2f-104">El origen del secuenciador permite a una aplicación reproducir de forma secuencial una colección de [orígenes multimedia](media-sources.md) , con transiciones perfectas entre los orígenes.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-104">The sequencer source enables an application to play a collection of [Media Sources](media-sources.md) sequentially, with seamless transitions between the sources.</span></span> <span data-ttu-id="f2b2f-105">El origen del secuenciador se puede usar para los escenarios siguientes:</span><span class="sxs-lookup"><span data-stu-id="f2b2f-105">The sequencer source can be used for the following scenarios:</span></span>

-   <span data-ttu-id="f2b2f-106">Cree una lista de reproducción que se conmutará sin problemas desde un origen de medios hasta el siguiente.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-106">Create a playlist that switches seamlessly from one media source to the next.</span></span>
-   <span data-ttu-id="f2b2f-107">Reproducir secuencias de varios orígenes simultáneamente; por ejemplo, reproduzca el audio de un archivo con el vídeo de otro.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-107">Play streams from multiple sources simultaneously; for example, play the audio from one file with the video from another.</span></span>
-   <span data-ttu-id="f2b2f-108">Cambiar entre secuencias en diferentes fuentes de medios en entradas de lista de reproducción consecutivas; por ejemplo, una lista de reproducción puede tener entradas que comparten el mismo origen de vídeo, mientras que cada entrada contiene un origen de audio diferente.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-108">Switch between streams in different media sources in consecutive playlist entries; for example, a playlist can have entries that share the same video source while each entry contains a different audio source.</span></span>

<span data-ttu-id="f2b2f-109">Para cada elemento de una lista de reproducción, la aplicación crea una topología independiente.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-109">For each element of a playlist, the application creates a separate topology.</span></span> <span data-ttu-id="f2b2f-110">Los orígenes multimedia de estas topologías se conocen como *orígenes nativos* para distinguirlos del origen del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-110">The media sources in these topologies are referred to as *native sources*, to distinguish them from the sequencer source.</span></span> <span data-ttu-id="f2b2f-111">Durante la reproducción, toda la secuencia de topologías se denomina *presentación* y cada topología de la secuencia se denomina *segmento*.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-111">During playback, the entire sequence of topologies is called a *presentation*, and each topology within the sequence is called a *segment*.</span></span>

<span data-ttu-id="f2b2f-112">La reproducción se controla mediante la [sesión multimedia](media-session.md), que proporciona controles de transporte, como reproducir, pausar y detener.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-112">Playback is controlled by the [Media Session](media-session.md), which provides transport controls, such as play, pause, and stop.</span></span> <span data-ttu-id="f2b2f-113">La sesión multimedia también administra el tiempo de presentación y envía eventos a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-113">The Media Session also manages the presentation time and sends events to the application.</span></span> <span data-ttu-id="f2b2f-114">(Los eventos del origen del secuenciador se reenvían a la aplicación a través de la sesión multimedia).</span><span class="sxs-lookup"><span data-stu-id="f2b2f-114">(Events from the sequencer source are forwarded to the application through the Media Session.)</span></span>

<span data-ttu-id="f2b2f-115">Para crear una lista de reproducción, la aplicación crea una o más topologías de reproducción y las pone en cola en el origen del secuenciador en el orden de reproducción deseado.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-115">To create a playlist, the application creates one or more playback topologies and queues them on the sequencer source in the desired order of playback.</span></span> <span data-ttu-id="f2b2f-116">Internamente, el origen del secuenciador modifica las topologías para que los nodos de origen señalen al origen del secuenciador en lugar de al origen nativo.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-116">Internally, the sequencer source modifies the topologies so that the source nodes point to the sequencer source instead of the native source.</span></span> <span data-ttu-id="f2b2f-117">La aplicación envía estas topologías modificadas, en lugar de las topologías originales, a la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-117">The application sends these modified topologies, rather than the original topologies, to the Media Session.</span></span> <span data-ttu-id="f2b2f-118">Esto permite que el origen del secuenciador agregue los orígenes nativos y se comunique con la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-118">This enables the sequencer source to aggregate the native sources and to communicate with the Media Session.</span></span>

<span data-ttu-id="f2b2f-119">Para lograr transiciones perfectas entre segmentos, el origen del secuenciador realiza una reversión de cada segmento.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-119">To achieve seamless transitions between segments, the sequencer source prerolls each segment.</span></span> <span data-ttu-id="f2b2f-120">Mientras se reproduce un segmento y antes de que sea el momento de reproducir el segmento siguiente, el origen del secuenciador desencadena un evento [MENewPresentation](menewpresentation.md) que contiene un descriptor de presentación.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-120">While one segment is playing, and before it is time to play the following segment, the sequencer source fires an [MENewPresentation](menewpresentation.md) event that contains a presentation descriptor.</span></span> <span data-ttu-id="f2b2f-121">La aplicación utiliza este descriptor de presentación para obtener la topología para el siguiente segmento de la presentación y pone en cola la topología en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-121">The application uses this presentation descriptor to get the topology for the next segment in the presentation, and queues the topology on the Media Session.</span></span>

<span data-ttu-id="f2b2f-122">En la ilustración siguiente se muestra el flujo de datos para las entradas de la lista de reproducción a través del origen del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-122">The following illustration shows the data flow for playlist entries through the sequencer source.</span></span> <span data-ttu-id="f2b2f-123">La aplicación utiliza la resolución de origen para crear los orígenes nativos, crea topologías para cada segmento y pone en cola las topologías en el origen del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-123">The application uses the source resolver to create the native sources, builds topologies for each segment, and queues the topologies on the sequencer source.</span></span>

![diagrama que muestra el flujo de datos desde los segmentos imfmediasession, imfsequencersource y playlist que conducen a imfmediasource](images/dbf41a05-d8cc-4502-9cd3-74e5d1ce04a0.gif)

## <a name="related-topics"></a><span data-ttu-id="f2b2f-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f2b2f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2b2f-126">Cómo crear una lista de reproducción</span><span class="sxs-lookup"><span data-stu-id="f2b2f-126">How to Create a Playlist</span></span>](how-to-create-a-playlist.md)
</dt> <dt>

[<span data-ttu-id="f2b2f-127">Topologías</span><span class="sxs-lookup"><span data-stu-id="f2b2f-127">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="f2b2f-128">Usar el origen del secuenciador</span><span class="sxs-lookup"><span data-stu-id="f2b2f-128">Using the Sequencer Source</span></span>](using-the-sequencer-source.md)
</dt> <dt>

[<span data-ttu-id="f2b2f-129">Origen del secuenciador</span><span class="sxs-lookup"><span data-stu-id="f2b2f-129">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



