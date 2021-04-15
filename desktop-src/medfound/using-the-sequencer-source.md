---
description: En este tema se describe cómo usar el origen del secuenciador.
ms.assetid: 7ce8dc67-02b1-4fd4-9e4d-6614fdb40620
title: Usar el origen del secuenciador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba99202838fbdc8be86f2f1d8931e5aa99ae9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715481"
---
# <a name="using-the-sequencer-source"></a><span data-ttu-id="7eec5-103">Usar el origen del secuenciador</span><span class="sxs-lookup"><span data-stu-id="7eec5-103">Using the Sequencer Source</span></span>

<span data-ttu-id="7eec5-104">En este tema se describe cómo usar el [origen del secuenciador](sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="7eec5-104">This topic describes how to use the [Sequencer Source](sequencer-source.md).</span></span> <span data-ttu-id="7eec5-105">Contiene las secciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="7eec5-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="7eec5-106">Información general</span><span class="sxs-lookup"><span data-stu-id="7eec5-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="7eec5-107">Agregar topologías</span><span class="sxs-lookup"><span data-stu-id="7eec5-107">Adding Topologies</span></span>](#adding-topologies)
-   [<span data-ttu-id="7eec5-108">Eliminar topologías</span><span class="sxs-lookup"><span data-stu-id="7eec5-108">Deleting Topologies</span></span>](#deleting-topologies)
-   [<span data-ttu-id="7eec5-109">Omitir un segmento</span><span class="sxs-lookup"><span data-stu-id="7eec5-109">Skipping to a Segment</span></span>](#skipping-to-a-segment)
-   [<span data-ttu-id="7eec5-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7eec5-110">Related topics</span></span>](#related-topics)

<span data-ttu-id="7eec5-111">Para obtener información general sobre el origen del secuenciador, vea [acerca del origen del secuenciador](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="7eec5-111">For a general overview of the sequencer source, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

## <a name="overview"></a><span data-ttu-id="7eec5-112">Información general</span><span class="sxs-lookup"><span data-stu-id="7eec5-112">Overview</span></span>

<span data-ttu-id="7eec5-113">El origen del secuenciador expone las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="7eec5-113">The sequencer source exposes the following interfaces.</span></span>



| <span data-ttu-id="7eec5-114">Interfaz</span><span class="sxs-lookup"><span data-stu-id="7eec5-114">Interface</span></span>                                                                        | <span data-ttu-id="7eec5-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7eec5-115">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="7eec5-116">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="7eec5-116">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                         | <span data-ttu-id="7eec5-117">Expone la funcionalidad de origen de medios genéricos.</span><span class="sxs-lookup"><span data-stu-id="7eec5-117">Exposes generic media source functionality.</span></span>                                        |
| [<span data-ttu-id="7eec5-118">**IMFSequencerSource**</span><span class="sxs-lookup"><span data-stu-id="7eec5-118">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)                                 | <span data-ttu-id="7eec5-119">Permite a la aplicación agregar o quitar topologías.</span><span class="sxs-lookup"><span data-stu-id="7eec5-119">Enables the application to add or remove topologies.</span></span>                               |
| [<span data-ttu-id="7eec5-120">**IMFMediaSourceTopologyProvider**</span><span class="sxs-lookup"><span data-stu-id="7eec5-120">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)         | <span data-ttu-id="7eec5-121">Recupera la siguiente topología que se va a poner en cola en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="7eec5-121">Retrieves the next topology to queue on the Media Session.</span></span>                         |
| [<span data-ttu-id="7eec5-122">**IMFMediaSourcePresentationProvider**</span><span class="sxs-lookup"><span data-stu-id="7eec5-122">**IMFMediaSourcePresentationProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider) | <span data-ttu-id="7eec5-123">Lo utiliza la sesión de medios para terminar segmentos.</span><span class="sxs-lookup"><span data-stu-id="7eec5-123">Used by the Media Session to end segments.</span></span> <span data-ttu-id="7eec5-124">Las aplicaciones no usan esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="7eec5-124">Applications do not use this interface.</span></span> |
| [<span data-ttu-id="7eec5-125">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="7eec5-125">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                           | <span data-ttu-id="7eec5-126">Consulta el origen del secuenciador para las [interfaces de servicio](service-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="7eec5-126">Queries the sequencer source for [Service Interfaces](service-interfaces.md).</span></span>     |



 

<span data-ttu-id="7eec5-127">Para reproducir una secuencia de orígenes multimedia, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7eec5-127">To play a sequence of media sources, perform the following steps:</span></span>

1.  <span data-ttu-id="7eec5-128">Para crear el origen del secuenciador, llame a la función [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) .</span><span class="sxs-lookup"><span data-stu-id="7eec5-128">To create the sequencer source, call the [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) function.</span></span>
2.  <span data-ttu-id="7eec5-129">Para cada segmento, cree una topología de reproducción, como se describe en [crear topologías de reproducción](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="7eec5-129">For each segment, create a playback topology, as described in [Creating Playback Topologies](creating-playback-topologies.md).</span></span> <span data-ttu-id="7eec5-130">Para agregar la topología a la presentación, llame a [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span><span class="sxs-lookup"><span data-stu-id="7eec5-130">To add the topology to the presentation, call [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span></span>
3.  <span data-ttu-id="7eec5-131">Antes de iniciar la reproducción, llame a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) en el origen del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="7eec5-131">Before starting playback, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the sequencer source.</span></span> <span data-ttu-id="7eec5-132">Este método devuelve un puntero a un descriptor de presentación para el primer segmento.</span><span class="sxs-lookup"><span data-stu-id="7eec5-132">This method returns a pointer to a presentation descriptor for the first segment.</span></span> <span data-ttu-id="7eec5-133">Para obtener la topología asociada a este segmento, llame a **QueryInterface** en el origen del secuenciador para la interfaz [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) .</span><span class="sxs-lookup"><span data-stu-id="7eec5-133">To get the topology associated with this segment, call **QueryInterface** on the sequencer source for the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface.</span></span> <span data-ttu-id="7eec5-134">Pase el descriptor de presentación al método [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="7eec5-134">Pass the presentation descriptor to the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span> <span data-ttu-id="7eec5-135">Este método devuelve un puntero a la topología.</span><span class="sxs-lookup"><span data-stu-id="7eec5-135">This method returns a pointer to the topology.</span></span>
4.  <span data-ttu-id="7eec5-136">Pase la topología para el primer segmento a la sesión multimedia, llamando al método [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="7eec5-136">Pass the topology for the first segment to the Media Session, by calling the Media Session's [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method.</span></span>
5.  <span data-ttu-id="7eec5-137">Inicie la reproducción mediante una llamada a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="7eec5-137">Start playback by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>
6.  <span data-ttu-id="7eec5-138">Cuando el origen del secuenciador está listo para prevertir el siguiente segmento, envía un evento [MENewPresentation](menewpresentation.md) cuyos datos de evento son un puntero de interfaz [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="7eec5-138">When the sequencer source is ready to preroll the next segment, it sends an [MENewPresentation](menewpresentation.md) event whose event data is an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface pointer.</span></span> <span data-ttu-id="7eec5-139">De nuevo, obtenga la topología del segmento mediante una llamada a [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) en el origen del secuenciador y establezca la topología en la sesión multimedia llamando a [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="7eec5-139">Again, get the topology for the segment by calling [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) on the sequencer source, and set the topology on the Media Session by calling [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="7eec5-140">No es necesario reiniciar el origen del medio; se reproducirá automáticamente en el segmento siguiente.</span><span class="sxs-lookup"><span data-stu-id="7eec5-140">It is not necessary to re-start the media source; it will automatically play through to the next segment.</span></span>
7.  <span data-ttu-id="7eec5-141">Antes de que se cierre la aplicación, cierre el origen del secuenciador mediante una llamada a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="7eec5-141">Before the application quits, shut down the sequencer source by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>

<span data-ttu-id="7eec5-142">En el código siguiente se muestra cómo obtener la topología y establecerla en la sesión multimedia:</span><span class="sxs-lookup"><span data-stu-id="7eec5-142">The following code shows how to get the topology and set it on the Media Session:</span></span>


```C++
// Queues the next topology on the session.

HRESULT CPlaylist::QueueNextSegment(IMFPresentationDescriptor *pPD)
{
    IMFMediaSourceTopologyProvider *pTopoProvider = NULL;
    IMFTopology *pTopology = NULL;

    //Get the topology for the presentation descriptor
    HRESULT hr = m_pSequencerSource->QueryInterface(IID_PPV_ARGS(&pTopoProvider));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pTopoProvider->GetMediaSourceTopology(pPD, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the topology on the media session
    m_pSession->SetTopology(NULL, pTopology);

done:
    SafeRelease(&pTopoProvider);
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="7eec5-143">Para obtener un ejemplo de código completo, vea [código de ejemplo del origen del secuenciador](sequencer-source-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="7eec5-143">For a complete code example, see [Sequencer Source Example Code](sequencer-source-example-code.md).</span></span>

## <a name="adding-topologies"></a><span data-ttu-id="7eec5-144">Agregar topologías</span><span class="sxs-lookup"><span data-stu-id="7eec5-144">Adding Topologies</span></span>

<span data-ttu-id="7eec5-145">El origen del secuenciador mantiene dos listas de topologías: la *lista de entrada* y la lista de *preplantación*.</span><span class="sxs-lookup"><span data-stu-id="7eec5-145">The sequencer source maintains two lists of topologies: the *input list* and the *preroll list*.</span></span>

<span data-ttu-id="7eec5-146">La lista de entrada es una colección de topologías que corresponden a segmentos de lista de reproducción, en el orden en que la aplicación los agregó llamando a [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span><span class="sxs-lookup"><span data-stu-id="7eec5-146">The input list is a collection of topologies corresponding to playlist segments, in the order that they were added by the application by calling [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span></span> <span data-ttu-id="7eec5-147">Este método asigna a cada topología un *identificador de segmento* único del tipo **MFSequencerElementId**.</span><span class="sxs-lookup"><span data-stu-id="7eec5-147">This method assigns each topology a unique *segment identifier* of the type **MFSequencerElementId**.</span></span> <span data-ttu-id="7eec5-148">El identificador de segmento se establece como un atributo para todos los nodos de topología de origen.</span><span class="sxs-lookup"><span data-stu-id="7eec5-148">The segment identifier is set as an attribute for all source topology nodes.</span></span> <span data-ttu-id="7eec5-149">Una aplicación puede obtener el identificador de segmento de un nodo de origen mediante el atributo de la [ \_ \_ secuencia \_ TOPONODE de MF](mf-toponode-sequence-elementid-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="7eec5-149">An application can get the segment identifier from a source node by using the [MF\_TOPONODE\_SEQUENCE\_ELEMENTID](mf-toponode-sequence-elementid-attribute.md) attribute.</span></span> <span data-ttu-id="7eec5-150">La lista de entrada puede tener topologías duplicadas si la aplicación llama a **AppendTopology** en la misma topología más de una vez. sin embargo, se identifican por sus identificadores de segmento únicos.</span><span class="sxs-lookup"><span data-stu-id="7eec5-150">The input list can have duplicate topologies if the application called **AppendTopology** on the same topology more than once; however, they are identified by their unique segment identifiers.</span></span>

<span data-ttu-id="7eec5-151">La lista de preplantación es una colección de topologías de lista de entrada que se han inicializado como preparación para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="7eec5-151">The preroll list is a collection of input list topologies that have been initialized in preparation for playback.</span></span> <span data-ttu-id="7eec5-152">Esto permite a la sesión multimedia pasar a la siguiente topología sin problemas cuando finaliza la topología activa.</span><span class="sxs-lookup"><span data-stu-id="7eec5-152">This enables the Media Session to transition to the next topology seamlessly when the active topology ends.</span></span> <span data-ttu-id="7eec5-153">La aplicación no puede Agregar o quitar directamente topologías de la lista de preplantación. lo genera el origen del secuenciador cuando se selecciona una topología de la lista de entrada para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="7eec5-153">The application cannot directly add or remove topologies from the preroll list; it is generated by the sequencer source when a topology from the input list is selected for playback.</span></span> <span data-ttu-id="7eec5-154">Esto hace que el origen del secuenciador agregue la siguiente topología de la lista de entrada a la lista de predistribución.</span><span class="sxs-lookup"><span data-stu-id="7eec5-154">This causes the sequencer source to add the next topology from the input list to the preroll list.</span></span> <span data-ttu-id="7eec5-155">Después de hacerlo, el origen del secuenciador genera asincrónicamente el evento [MENewPresentation](menewpresentation.md) y pasa el descriptor de presentación para la topología de predistribución como datos de evento.</span><span class="sxs-lookup"><span data-stu-id="7eec5-155">After doing so, the sequencer source asynchronously raises the [MENewPresentation](menewpresentation.md) event and passes the presentation descriptor for the preroll topology as event data.</span></span> <span data-ttu-id="7eec5-156">La aplicación debe realizar escuchas para este evento mediante la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) de la sesión multimedia y poner en cola la topología de predistribución en la sesión multimedia llamando a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="7eec5-156">The application must listen for this event by using the Media Session's [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface and queue the preroll topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="7eec5-157">Esto debe hacerse antes de que la sesión multimedia complete la reproducción de la topología activa.</span><span class="sxs-lookup"><span data-stu-id="7eec5-157">This must be done before the Media Session completes playback of the active topology.</span></span> <span data-ttu-id="7eec5-158">**SetTopology** informa a la sesión multimedia sobre la siguiente topología que debe reproducirse después de que haya finalizado la reproducción de la topología activa.</span><span class="sxs-lookup"><span data-stu-id="7eec5-158">**SetTopology** informs the Media Session about the next topology that it must play after playback of the active topology has ended.</span></span> <span data-ttu-id="7eec5-159">Para garantizar un treansition sin problemas, la aplicación debe llamar a **SetTopology** antes de que la sesión multimedia complete la reproducción de la topología anterior.</span><span class="sxs-lookup"><span data-stu-id="7eec5-159">To ensure a seamless treansition, the application must call **SetTopology** before the Media Session completes playing the previous topology.</span></span> <span data-ttu-id="7eec5-160">De lo contrario, habrá un hueco entre los segmentos.</span><span class="sxs-lookup"><span data-stu-id="7eec5-160">Otherwise, there will be a gap between the segments.</span></span>

<span data-ttu-id="7eec5-161">El evento [MENewPresentation](menewpresentation.md) se desencadena siempre que haya una topología que siga a la topología activa.</span><span class="sxs-lookup"><span data-stu-id="7eec5-161">The [MENewPresentation](menewpresentation.md) event is raised as long as there is a topology following the active topology.</span></span> <span data-ttu-id="7eec5-162">Por consiguiente, si la lista de entrada contiene solo una topología, o si la topología activa es la última de la lista de entrada, no se genera este evento.</span><span class="sxs-lookup"><span data-stu-id="7eec5-162">Consequently, if the input list contains only one topology, or if the active topology is the last one in the input list, this event is not raised.</span></span>

<span data-ttu-id="7eec5-163">La lista de preplantación se sincroniza con la lista de entrada y se actualiza cada vez que se agrega o se elimina una topología de la lista de entrada.</span><span class="sxs-lookup"><span data-stu-id="7eec5-163">The preroll list is synchronized with the input list and is refreshed each time a topology is added to or deleted from the input list.</span></span>

## <a name="deleting-topologies"></a><span data-ttu-id="7eec5-164">Eliminar topologías</span><span class="sxs-lookup"><span data-stu-id="7eec5-164">Deleting Topologies</span></span>

<span data-ttu-id="7eec5-165">Para quitar una topología del origen del secuenciador, una aplicación debe llamar al método [**IMFSequencerSource::D eletetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) y especificar el identificador de segmento.</span><span class="sxs-lookup"><span data-stu-id="7eec5-165">To remove a topology from the sequencer source, an application must call the [**IMFSequencerSource::DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) method and specify the segment identifier.</span></span>

<span data-ttu-id="7eec5-166">Antes de llamar a [**DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology), la aplicación debe asegurarse de que la sesión multimedia no esté usando la topología que la aplicación desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="7eec5-166">Before calling [**DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology), the application must make sure that Media Session is not using the topology that the application wants to delete.</span></span> <span data-ttu-id="7eec5-167">Para ello, se deben realizar las siguientes acciones antes de que la aplicación llame a **DeleteTopology**:</span><span class="sxs-lookup"><span data-stu-id="7eec5-167">To do this, both of the following must occur before the application calls **DeleteTopology**:</span></span>

-   <span data-ttu-id="7eec5-168">Se recibió un evento [MESessionTopologyStatus](mesessiontopologystatus.md) con MF \_ TOPOSTATUS \_ finalizado para la topología con el fin de asegurarse de que la sesión multimedia ha finalizado la reproducción.</span><span class="sxs-lookup"><span data-stu-id="7eec5-168">[MESessionTopologyStatus](mesessiontopologystatus.md) event with MF\_TOPOSTATUS\_ENDED is received for the topology to ensure that Media Session has completed playback.</span></span>

-   <span data-ttu-id="7eec5-169">[MESessionTopologyStatus](mesessiontopologystatus.md) con MF \_ TOPOSTATUS \_ se ha iniciado el \_ origen en la siguiente topología para asegurarse de que la sesión multimedia ha empezado a reproducir la topología siguiente, se recibe el evento [MESessionEnded](mesessionended.md) para asegurarse de que la sesión multimedia se realiza con la última topología del origen del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="7eec5-169">[MESessionTopologyStatus](mesessiontopologystatus.md) with MF\_TOPOSTATUS\_STARTED\_SOURCE is received for the next topology to ensure that the Media Session has started playing the next topology, [MESessionEnded](mesessionended.md) event is received to ensure that Media Session is done with the last topology in the sequencer source.</span></span>

<span data-ttu-id="7eec5-170">Si el segmento que se va a eliminar es la topología activa, la reproducción se detiene y el origen del secuenciador genera el evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="7eec5-170">If the segment being deleted is the active topology, playback is stopped and the sequencer source raises the [MEEndOfPresentationSegment](meendofpresentationsegment.md) event.</span></span> <span data-ttu-id="7eec5-171">Si la topología activa es también la última topología, se genera el evento [MEEndOfPresentation](meendofpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="7eec5-171">If the active topology is also the last topology, the [MEEndOfPresentation](meendofpresentation.md) event is raised.</span></span>

## <a name="skipping-to-a-segment"></a><span data-ttu-id="7eec5-172">Omitir un segmento</span><span class="sxs-lookup"><span data-stu-id="7eec5-172">Skipping to a Segment</span></span>

<span data-ttu-id="7eec5-173">Una aplicación puede saltar a un segmento determinado en la secuencia iniciando la [sesión de medios](media-session.md) con un desplazamiento de segmento, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="7eec5-173">An application can skip to a particular segment in the sequence by starting the [Media Session](media-session.md) with a segment offset, as follows:</span></span>

1.  <span data-ttu-id="7eec5-174">Llame a la función [**MFCreateSequencerSegmentOffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) para crear el desplazamiento del segmento.</span><span class="sxs-lookup"><span data-stu-id="7eec5-174">Call the [**MFCreateSequencerSegmentOffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) function to create the segment offset.</span></span> <span data-ttu-id="7eec5-175">Especifique el identificador del segmento en el parámetro *dwId* .</span><span class="sxs-lookup"><span data-stu-id="7eec5-175">Specify the identifier of the segment in the *dwId* parameter.</span></span> <span data-ttu-id="7eec5-176">(El método [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) devolvió el identificador al agregar por primera vez la topología al origen del secuenciador). El parámetro *hnsOffset* especifica un desplazamiento de tiempo, relativo al inicio del segmento.</span><span class="sxs-lookup"><span data-stu-id="7eec5-176">(The identifier was returned by the [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) method when you first added the topology to the sequencer source.) The *hnsOffset* parameter specifies a time offset, relative to the start of the segment.</span></span> <span data-ttu-id="7eec5-177">La reproducción se iniciará en este momento.</span><span class="sxs-lookup"><span data-stu-id="7eec5-177">Playback will start at this time.</span></span> <span data-ttu-id="7eec5-178">Para el parámetro *pvarSegmentOffset* , pase la dirección de un **PROPVARIANT** vacío.</span><span class="sxs-lookup"><span data-stu-id="7eec5-178">For the *pvarSegmentOffset* parameter, pass in the address of an empty **PROPVARIANT**.</span></span> <span data-ttu-id="7eec5-179">Cuando la función devuelve, este **PROPVARIANT** contiene el desplazamiento del segmento.</span><span class="sxs-lookup"><span data-stu-id="7eec5-179">When the function returns, this **PROPVARIANT** contains the segment offset.</span></span>

2.  <span data-ttu-id="7eec5-180">Llame al método [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="7eec5-180">Call the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method on the Media Session.</span></span> <span data-ttu-id="7eec5-181">Para el parámetro *pguidTimeFormat* , use el \_ desplazamiento de segmento formato de hora MF de valor de GUID \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7eec5-181">For the *pguidTimeFormat* parameter, use the GUID value MF\_TIME\_FORMAT\_SEGMENT\_OFFSET.</span></span> <span data-ttu-id="7eec5-182">Este valor indica la búsqueda por desplazamiento del segmento.</span><span class="sxs-lookup"><span data-stu-id="7eec5-182">This value indicates seeking by segment offset.</span></span> <span data-ttu-id="7eec5-183">Para el parámetro *pvarStartPosition* , pase la dirección del **PROPVARIANT** creado en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="7eec5-183">For the *pvarStartPosition* parameter, pass the address of the **PROPVARIANT** created in the previous step.</span></span>

<span data-ttu-id="7eec5-184">En el ejemplo de código siguiente se muestra cómo saltar al inicio de un segmento especificado en una secuencia.</span><span class="sxs-lookup"><span data-stu-id="7eec5-184">The following code example shows how to skip to the start of a specified segment in a sequence.</span></span>


```C++
// Skips to the specified segment in the sequencer source

HRESULT CPlaylist::SkipTo(DWORD index)
{
    if (index >= m_count)
    {
        return E_INVALIDARG;
    }

    MFSequencerElementId ID = m_segments[index].SegmentID;

    PROPVARIANT var;

    HRESULT hr = MFCreateSequencerSegmentOffset(ID, NULL, &var);
    
    if (SUCCEEDED(hr))
    {
        hr = m_pSession->Start(&MF_TIME_FORMAT_SEGMENT_OFFSET, &var);
        PropVariantClear(&var);
    }
    return hr;
}
```



<span data-ttu-id="7eec5-185">Cuando la aplicación busca entre segmentos, la aplicación recibe varios eventos, ya que el origen del secuenciador finaliza el segmento actual y se prepara para reproducir el nuevo segmento.</span><span class="sxs-lookup"><span data-stu-id="7eec5-185">When the application seeks across segments, the application receives several events as the sequencer source ends the current segment and prepares to play the new segment.</span></span> <span data-ttu-id="7eec5-186">Dado que estos eventos se reciben de forma asincrónica, es difícil predecir la secuencia exacta de eventos.</span><span class="sxs-lookup"><span data-stu-id="7eec5-186">Because these events are received asynchronously, it is difficult to predict the exact sequence of events.</span></span> <span data-ttu-id="7eec5-187">Estos eventos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7eec5-187">These events are as follows:</span></span>

-   <span data-ttu-id="7eec5-188">El origen del secuenciador envía un evento [MENewPresentation](menewpresentation.md) para el nuevo segmento al que se omite la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="7eec5-188">The sequencer source sends an [MENewPresentation](menewpresentation.md) event for the new segment to which the Media Session is skipping.</span></span>

-   <span data-ttu-id="7eec5-189">Cuando el origen del secuenciador finaliza el segmento activo, envía el evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="7eec5-189">When the sequencer source ends the active segment, it sends the [MEEndOfPresentationSegment](meendofpresentationsegment.md) event.</span></span>
-   <span data-ttu-id="7eec5-190">Después, el origen del secuenciador cancela la topología de predistribución.</span><span class="sxs-lookup"><span data-stu-id="7eec5-190">The sequencer source then cancels the preroll topology.</span></span> <span data-ttu-id="7eec5-191">Esto produce los siguientes eventos para la topología cancelada:</span><span class="sxs-lookup"><span data-stu-id="7eec5-191">This results in the following events for the canceled topology:</span></span>

    -   <span data-ttu-id="7eec5-192">Evento [MESessionTopologyStatus](mesessiontopologystatus.md) con la \_ marca MF TOPOSTATUS \_ Ready.</span><span class="sxs-lookup"><span data-stu-id="7eec5-192">[MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag.</span></span>
    -   <span data-ttu-id="7eec5-193">Evento [MESessionTopologyStatus](mesessiontopologystatus.md) con el marcador de origen de MF \_ TOPOSTATUS \_ iniciado \_ .</span><span class="sxs-lookup"><span data-stu-id="7eec5-193">[MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_STARTED\_SOURCE flag.</span></span>
    -   <span data-ttu-id="7eec5-194">Evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) con el atributo de [topología de origen de eventos MF \_ \_ \_ \_ cancelado](mf-event-source-topology-canceled-attribute.md) para indicar que el origen del secuenciador canceló la topología.</span><span class="sxs-lookup"><span data-stu-id="7eec5-194">[MEEndOfPresentationSegment](meendofpresentationsegment.md) event with the [MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED](mf-event-source-topology-canceled-attribute.md) attribute to indicate that the topology was canceled by the sequencer source.</span></span>

-   <span data-ttu-id="7eec5-195">Después, el origen del secuenciador envía eventos para el nuevo segmento, incluidos varios eventos [MESessionTopologyStatus](mesessiontopologystatus.md) .</span><span class="sxs-lookup"><span data-stu-id="7eec5-195">Next, the sequencer source sends events for the new segment, including various [MESessionTopologyStatus](mesessiontopologystatus.md) events.</span></span>
-   <span data-ttu-id="7eec5-196">Si el nuevo segmento no es el último de la lista, el origen del secuenciador actualiza la lista de preplantación y genera otro [MENewPresentation](menewpresentation.md) para la nueva topología de predistribución.</span><span class="sxs-lookup"><span data-stu-id="7eec5-196">If the new segment is not the last on the list, the sequencer source refreshes the preroll list and raises another [MENewPresentation](menewpresentation.md) for the new preroll topology.</span></span> <span data-ttu-id="7eec5-197">Para obtener información acerca de las topologías de la lista de preplantación, consulte [acerca del origen del secuenciador](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="7eec5-197">For information about topologies in the preroll list, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="7eec5-198">Puede encontrar más detalles sobre los eventos enviados por el origen del secuenciador en el tema [eventos de origen de Sequencer](sequencer-source-events.md).</span><span class="sxs-lookup"><span data-stu-id="7eec5-198">More details about the events sent by the sequencer source can be found in the topic [Sequencer Source Events](sequencer-source-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7eec5-199">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7eec5-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7eec5-200">Cómo crear una lista de reproducción</span><span class="sxs-lookup"><span data-stu-id="7eec5-200">How to Create a Playlist</span></span>](how-to-create-a-playlist.md)
</dt> <dt>

[<span data-ttu-id="7eec5-201">Origen del secuenciador</span><span class="sxs-lookup"><span data-stu-id="7eec5-201">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



