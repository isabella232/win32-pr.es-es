---
description: En este tema se describe cómo usar el origen de la secuencia para reproducir una secuencia de archivos.
ms.assetid: 5a760492-bd52-40b8-a652-8a62646db6ae
title: Cómo crear una lista de reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2e6e19766c3fa569a701fea9bed0f05d11a4324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543611"
---
# <a name="how-to-create-a-playlist"></a><span data-ttu-id="6918c-103">Cómo crear una lista de reproducción</span><span class="sxs-lookup"><span data-stu-id="6918c-103">How to Create a Playlist</span></span>

<span data-ttu-id="6918c-104">En este tema se describe cómo usar el origen de la secuencia para reproducir una secuencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="6918c-104">This topic describes how to use the Sequence Source to play a sequence of files.</span></span>

## <a name="overview"></a><span data-ttu-id="6918c-105">Información general</span><span class="sxs-lookup"><span data-stu-id="6918c-105">Overview</span></span>

<span data-ttu-id="6918c-106">Para reproducir archivos multimedia en una secuencia, la aplicación debe agregar topologías en una secuencia para crear una lista de reproducción y poner en cola estas topologías en la sesión multimedia para su reproducción.</span><span class="sxs-lookup"><span data-stu-id="6918c-106">To play media files in a sequence, the application must add topologies in a sequence to create a playlist, and queue these topologies on the Media Session for playback.</span></span>

<span data-ttu-id="6918c-107">El origen del secuenciador garantiza una reproducción perfecta inicializando y cargando la topología siguiente antes de que la sesión de medios empiece a reproducir la topología actual.</span><span class="sxs-lookup"><span data-stu-id="6918c-107">The sequencer source ensures seamless playback by initializing and loading the next topology before the Media Session starts playing the current topology.</span></span> <span data-ttu-id="6918c-108">Esto permite a la aplicación iniciar la próxima topología rápidamente siempre que sea necesario.</span><span class="sxs-lookup"><span data-stu-id="6918c-108">This enables the application to start the next topology quickly whenever it is required.</span></span>

<span data-ttu-id="6918c-109">La sesión multimedia es responsable de la alimentación de datos a los receptores y de la reproducción de las topologías del origen de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6918c-109">The Media Session is responsible for feeding data to the sinks and playing the topologies in the sequence source.</span></span> <span data-ttu-id="6918c-110">Además, la sesión multimedia administra el tiempo de presentación de los segmentos.</span><span class="sxs-lookup"><span data-stu-id="6918c-110">In addition, the Media Session manages the presentation time for the segments.</span></span>

<span data-ttu-id="6918c-111">Para obtener más información sobre cómo el origen del secuenciador administra las topologías, consulte [acerca del origen del secuenciador](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="6918c-111">For more information about how the sequencer source manages topologies, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="6918c-112">Este tutorial contiene los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="6918c-112">This walk-through contains the following steps:</span></span>

1.  [<span data-ttu-id="6918c-113">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6918c-113">Prerequisites</span></span>](#prerequisites)
2.  [<span data-ttu-id="6918c-114">Inicializar Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6918c-114">Initializing Media Foundation</span></span>](#initializing-media-foundation)
3.  [<span data-ttu-id="6918c-115">Crear objetos Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6918c-115">Creating Media Foundation Objects</span></span>](#creating-media-foundation-objects)
4.  [<span data-ttu-id="6918c-116">Crear el origen de medios</span><span class="sxs-lookup"><span data-stu-id="6918c-116">Creating the Media Source</span></span>](#creating-the-media-source)
5.  [<span data-ttu-id="6918c-117">Crear topologías parciales</span><span class="sxs-lookup"><span data-stu-id="6918c-117">Creating Partial Topologies</span></span>](#creating-partial-topologies)
6.  [<span data-ttu-id="6918c-118">Agregar topologías al origen del secuenciador</span><span class="sxs-lookup"><span data-stu-id="6918c-118">Adding Topologies to the Sequencer Source</span></span>](#adding-topologies-to-the-sequencer-source)
7.  [<span data-ttu-id="6918c-119">Establecimiento de la primera topología en la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="6918c-119">Setting the First Topology on the Media Session</span></span>](#setting-the-first-topology-on-the-media-session)
8.  [<span data-ttu-id="6918c-120">Poner en cola la siguiente topología en la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="6918c-120">Queuing the Next Topology on the Media Session</span></span>](#queuing-the-next-topology-on-the-media-session)
9.  [<span data-ttu-id="6918c-121">Liberar el origen del secuenciador</span><span class="sxs-lookup"><span data-stu-id="6918c-121">Releasing the Sequencer Source</span></span>](#releasing-the-sequencer-source)

<span data-ttu-id="6918c-122">Los ejemplos de código que se muestran en este tema son fragmentos del [código de ejemplo de origen de Sequencer](sequencer-source-example-code.md)de tema, que contiene el código de ejemplo completo.</span><span class="sxs-lookup"><span data-stu-id="6918c-122">The code examples shown this topic are excerpts from the topic [Sequencer Source Example Code](sequencer-source-example-code.md), which contains the complete example code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6918c-123">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6918c-123">Prerequisites</span></span>

<span data-ttu-id="6918c-124">Antes de comenzar este tutorial, familiarícese con los siguientes conceptos de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="6918c-124">Before starting this walk-through, familiarize yourself with the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="6918c-125">Sesión de medios</span><span class="sxs-lookup"><span data-stu-id="6918c-125">Media Session</span></span>](media-session.md)
-   [<span data-ttu-id="6918c-126">Topologías</span><span class="sxs-lookup"><span data-stu-id="6918c-126">Topologies</span></span>](topologies.md)
-   [<span data-ttu-id="6918c-127">Generadores de eventos multimedia</span><span class="sxs-lookup"><span data-stu-id="6918c-127">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="6918c-128">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="6918c-128">Presentation Descriptors</span></span>](presentation-descriptors.md)

<span data-ttu-id="6918c-129">También puede leer [Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md), porque el código de ejemplo shwon aquí se expande en el código de ese tema.</span><span class="sxs-lookup"><span data-stu-id="6918c-129">Also read [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md), because the example code shwon here expands on the code in that topic.</span></span>

## <a name="initializing-media-foundation"></a><span data-ttu-id="6918c-130">Inicializar Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6918c-130">Initializing Media Foundation</span></span>

<span data-ttu-id="6918c-131">Antes de poder usar cualquier método o interfaz de Media Foundation, inicialice Media Foundation mediante una llamada a la función [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) .</span><span class="sxs-lookup"><span data-stu-id="6918c-131">Before you can use any Media Foundation interfaces or methods, initialize Media Foundation by calling the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function.</span></span> <span data-ttu-id="6918c-132">Para obtener más información, vea [inicializar Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="6918c-132">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>


```C++
    hr = MFStartup(MF_VERSION);
```



## <a name="creating-media-foundation-objects"></a><span data-ttu-id="6918c-133">Crear objetos Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6918c-133">Creating Media Foundation Objects</span></span>

<span data-ttu-id="6918c-134">A continuación, cree los siguientes objetos de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="6918c-134">Next, create the following Media Foundation objects:</span></span>

-   <span data-ttu-id="6918c-135">Sesión de medios.</span><span class="sxs-lookup"><span data-stu-id="6918c-135">Media session.</span></span> <span data-ttu-id="6918c-136">Este objeto expone la interfaz [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) , que proporciona métodos para reproducir, pausar y detener la topología actual.</span><span class="sxs-lookup"><span data-stu-id="6918c-136">This object exposes the [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface, which provides methods to play, pause, and stop the current topology.</span></span>
-   <span data-ttu-id="6918c-137">Origen del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="6918c-137">Sequencer source.</span></span> <span data-ttu-id="6918c-138">Este objeto expone la interfaz [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) , que proporciona métodos para agregar, actualizar y eliminar topologías en una secuencia.</span><span class="sxs-lookup"><span data-stu-id="6918c-138">This object exposes the [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) interface, which provides methods to add, update, and delete topologies in a sequence.</span></span>

1.  <span data-ttu-id="6918c-139">Llame a la función [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para crear la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="6918c-139">Call the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) function to create the Media Session.</span></span>
2.  <span data-ttu-id="6918c-140">Llame a [**IMFMediaEventQueue:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) para solicitar el primer evento de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="6918c-140">Call [**IMFMediaEventQueue::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) to request the first event from the Media Session.</span></span>
3.  <span data-ttu-id="6918c-141">Llame a la función [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) para crear el origen del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="6918c-141">Call the [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) function to create the sequencer source.</span></span>

<span data-ttu-id="6918c-142">En el código siguiente se crea la sesión multimedia y se solicita el primer evento:</span><span class="sxs-lookup"><span data-stu-id="6918c-142">The following code creates the Media Session and requests the first event:</span></span>


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



## <a name="creating-the-media-source"></a><span data-ttu-id="6918c-143">Crear el origen de medios</span><span class="sxs-lookup"><span data-stu-id="6918c-143">Creating the Media Source</span></span>

<span data-ttu-id="6918c-144">A continuación, cree un origen de medios para el primer segmento de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="6918c-144">Next, create a media source for the first playlist segment.</span></span> <span data-ttu-id="6918c-145">Utilice el [solucionador de origen](source-resolver.md) para crear un origen de medios a partir de una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="6918c-145">Use the [Source Resolver](source-resolver.md) to create a media source from a URL.</span></span> <span data-ttu-id="6918c-146">Para ello, llame a la función [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) para crear un solucionador de origen y, a continuación, llame al método [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) para crear el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="6918c-146">To do this, call the [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) function to create a source resolver and then call the [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) method to create the media source.</span></span>

<span data-ttu-id="6918c-147">Para obtener información sobre los orígenes de medios, consulte [orígenes de medios](media-sources.md).</span><span class="sxs-lookup"><span data-stu-id="6918c-147">For information about media sources, see [Media Sources](media-sources.md).</span></span>

## <a name="creating-partial-topologies"></a><span data-ttu-id="6918c-148">Crear topologías parciales</span><span class="sxs-lookup"><span data-stu-id="6918c-148">Creating Partial Topologies</span></span>

<span data-ttu-id="6918c-149">Cada segmento del origen del secuenciador tiene su propia topología parcial.</span><span class="sxs-lookup"><span data-stu-id="6918c-149">Each segment in the sequencer source has its own partial topology.</span></span> <span data-ttu-id="6918c-150">A continuación, cree topologías parciales para los orígenes multimedia.</span><span class="sxs-lookup"><span data-stu-id="6918c-150">Next, create partial topologies for media sources.</span></span> <span data-ttu-id="6918c-151">En el caso de una topología parcial, los nodos de origen de la topología se conectan directamente a los nodos de salida, sin especificar las transformaciones intermedias.</span><span class="sxs-lookup"><span data-stu-id="6918c-151">For a partial topology, the topology source nodes are connected directly to the output nodes, without specifying any intermediate transforms.</span></span> <span data-ttu-id="6918c-152">La sesión multimedia utiliza el objeto cargador de topología para resolver la topología.</span><span class="sxs-lookup"><span data-stu-id="6918c-152">The Media Session uses the topology loader object to resolve the topology.</span></span> <span data-ttu-id="6918c-153">Una vez que se resuelve una topología, se agregan los descodificadores necesarios y otros nodos de transformación.</span><span class="sxs-lookup"><span data-stu-id="6918c-153">After a topology is resolved, the required decoders and other transform nodes are added.</span></span> <span data-ttu-id="6918c-154">El origen del secuenciador también puede contener topologías completas.</span><span class="sxs-lookup"><span data-stu-id="6918c-154">The sequencer source can also contain full topologies.</span></span>

<span data-ttu-id="6918c-155">Para crear el objeto Topology, utilice la función [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) y, a continuación, use la interfaz [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) para crear nodos de secuencia.</span><span class="sxs-lookup"><span data-stu-id="6918c-155">To create the topology object, use the [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) function and then use the [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) interface to create stream nodes.</span></span>

<span data-ttu-id="6918c-156">Para obtener instrucciones completas sobre el uso de estos elementos de programación para crear topologías, vea [crear topologías de reproducción](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="6918c-156">For complete instructions on using these programming elements to create topologies, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

<span data-ttu-id="6918c-157">Una aplicación puede reproducir una parte seleccionada del código fuente nativo mediante la configuración del nodo de origen.</span><span class="sxs-lookup"><span data-stu-id="6918c-157">An application can play a selected portion of the native source by configuring the source node.</span></span> <span data-ttu-id="6918c-158">Para ello, establezca el atributo [**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md) y el atributo [**MF \_ TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md) en los nodos de topología de nodo de la **\_ topología MF \_ SOURCESTREAM \_** .</span><span class="sxs-lookup"><span data-stu-id="6918c-158">To do this, set the [**MF\_TOPONODE\_MEDIASTART**](mf-toponode-mediastart-attribute.md) attribute and the [**MF\_TOPONODE\_MEDIASTOP**](mf-toponode-mediastop-attribute.md) attribute on **MF\_TOPOLOGY\_SOURCESTREAM\_NODE** topology nodes.</span></span> <span data-ttu-id="6918c-159">Especifique la hora de inicio del medio y la hora de detención del medio en relación con el inicio del origen nativo como tipos **UINT64** .</span><span class="sxs-lookup"><span data-stu-id="6918c-159">Specify the media start time and the media stop time relative to the start of the native source as **UINT64** types.</span></span>

## <a name="adding-topologies-to-the-sequencer-source"></a><span data-ttu-id="6918c-160">Agregar topologías al origen del secuenciador</span><span class="sxs-lookup"><span data-stu-id="6918c-160">Adding Topologies to the Sequencer Source</span></span>

<span data-ttu-id="6918c-161">A continuación, agregue al origen del secuenciador las topologías parciales que creó.</span><span class="sxs-lookup"><span data-stu-id="6918c-161">Next, add to the sequencer source the partial topologies that you created.</span></span> <span data-ttu-id="6918c-162">A cada elemento de secuencia, denominado *segmento*, se le asigna un identificador **MFSequencerElementId** .</span><span class="sxs-lookup"><span data-stu-id="6918c-162">Each sequence element, called a *segment*, is assigned an **MFSequencerElementId** identifier.</span></span> <span data-ttu-id="6918c-163">Para obtener más información sobre cómo el origen del secuenciador administra las topologías, consulte [acerca del origen del secuenciador](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="6918c-163">For more information about how the sequencer source manages topologies, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="6918c-164">Después de agregar todas las topologías al origen del secuenciador, la aplicación debe marcar el último segmento de la secuencia para finalizar la reproducción de la canalización.</span><span class="sxs-lookup"><span data-stu-id="6918c-164">After all of the topologies are added to the sequencer source, the application must flag the last segment in the sequence to end playback in the pipeline.</span></span> <span data-ttu-id="6918c-165">Sin esta marca, el origen del secuenciador espera que se agreguen más topologías.</span><span class="sxs-lookup"><span data-stu-id="6918c-165">Without this flag, the sequencer source expects more topologies to be added.</span></span>

1.  <span data-ttu-id="6918c-166">Llame al método [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) para agregar una topología específica al origen del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="6918c-166">Call the [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) method to add a specific topology to the sequencer source.</span></span>

    ```C++
        hr = m_pSequencerSource->AppendTopology(
            pTopology, 
            SequencerTopologyFlags_Last, 
            &SegmentId
            );
    ```

    

    <span data-ttu-id="6918c-167">[**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) agrega la topología especificada a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6918c-167">[**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) adds the specified topology to the sequence.</span></span> <span data-ttu-id="6918c-168">Este método devuelve el identificador de segmento en el parámetro *pdwId* .</span><span class="sxs-lookup"><span data-stu-id="6918c-168">This method returns the segment identifier in the *pdwId* parameter.</span></span>

    <span data-ttu-id="6918c-169">Si la topología es la última del origen del secuenciador, pase SequencerTopologyFlags \_ en último lugar en el parámetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="6918c-169">If the topology is the last one in the sequencer source, pass SequencerTopologyFlags\_Last in the *dwFlags* parameter.</span></span> <span data-ttu-id="6918c-170">Este valor se define en la enumeración [**MFSequencerTopologyFlags**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) .</span><span class="sxs-lookup"><span data-stu-id="6918c-170">This value is defined in the [**MFSequencerTopologyFlags**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) enumeration.</span></span>

2.  <span data-ttu-id="6918c-171">Llame a [**IMFSequencerSource:: UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) para actualizar las marcas de la topología asociada al identificador de segmento en la lista de entrada.</span><span class="sxs-lookup"><span data-stu-id="6918c-171">Call [**IMFSequencerSource::UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) to update the flags for the topology associated with the segment identifier in the input list.</span></span> <span data-ttu-id="6918c-172">En este caso, la llamada indica que el segmento especificado es el último segmento del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="6918c-172">In this case, the call indicates that the specified segment is the last segment in the sequencer.</span></span> <span data-ttu-id="6918c-173">(Esta llamada es opcional si la última topología se especifica en la llamada a [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) ).</span><span class="sxs-lookup"><span data-stu-id="6918c-173">(This call is optional if the last topology is specified in the [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) call.)</span></span>

    ```C++
        BOOL bFirstSegment = (NumSegments() == 0);

        if (!bFirstSegment)
        {
            // Remove the "last segment" flag from the last segment.
            hr = m_pSequencerSource->UpdateTopologyFlags(LastSegment(), 0);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    ```

    

<span data-ttu-id="6918c-174">La aplicación puede reemplazar la topología de un segmento por otra topología llamando a [**IMFSequencerSource:: UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) y pasando la nueva topología en *pTopology*.</span><span class="sxs-lookup"><span data-stu-id="6918c-174">The application can replace a segment's topology with another topology by calling the [**IMFSequencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) and passing the new topology in *pTopology*.</span></span> <span data-ttu-id="6918c-175">Si hay nuevos orígenes nativos en la nueva topología, los orígenes se agregan a la caché de origen.</span><span class="sxs-lookup"><span data-stu-id="6918c-175">If there are new native sources in the new topology, the sources are added to the source cache.</span></span> <span data-ttu-id="6918c-176">También se actualiza la lista de preplantación.</span><span class="sxs-lookup"><span data-stu-id="6918c-176">The preroll list is also refreshed.</span></span>

## <a name="setting-the-first-topology-on-the-media-session"></a><span data-ttu-id="6918c-177">Establecimiento de la primera topología en la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="6918c-177">Setting the First Topology on the Media Session</span></span>

<span data-ttu-id="6918c-178">A continuación, pone en cola la primera topología en el origen de la secuencia en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="6918c-178">Next, queue the first topology in the sequence source on the Media Session.</span></span> <span data-ttu-id="6918c-179">Para obtener la primera topología del origen del secuenciador, la aplicación debe llamar al método [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="6918c-179">To get the first topology from the sequencer source, the application must call the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span> <span data-ttu-id="6918c-180">Este método devuelve la topología parcial, que se resuelve en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="6918c-180">This method returns the partial topology, which is resolved by the Media Session.</span></span>

<span data-ttu-id="6918c-181">Para obtener información acerca de las topologías parciales, vea [acerca de las topologías](about-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="6918c-181">For information about partial topologies, see [About Topologies](about-topologies.md).</span></span>

1.  <span data-ttu-id="6918c-182">Recupere el origen de medios nativo para la primera topología del origen de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6918c-182">Retrieve the native media source for the first topology of the sequence source.</span></span>
2.  <span data-ttu-id="6918c-183">Cree un descriptor de presentación para el origen de medios llamando al método [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="6918c-183">Create a presentation descriptor for the media source by calling the [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) method.</span></span>
3.  <span data-ttu-id="6918c-184">Recupere la topología asociada para la presentación llamando al método [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="6918c-184">Retrieve the associated topology for the presentation by calling the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span>
4.  <span data-ttu-id="6918c-185">Establezca la primera topología en la sesión de medios mediante una llamada a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="6918c-185">Set the first topology on the Media Session by Calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

    <span data-ttu-id="6918c-186">Llame a [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) con el parámetro *DwSetTopologyFlags* establecido en **null**.</span><span class="sxs-lookup"><span data-stu-id="6918c-186">Call [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) with the *dwSetTopologyFlags* parameter set to **NULL**.</span></span> <span data-ttu-id="6918c-187">Esto indica a la sesión de medios que inicie la topología especificada cuando se haya completado la topología actual.</span><span class="sxs-lookup"><span data-stu-id="6918c-187">This instructs the Media Session to start the specified topology when the current topology has been completed.</span></span> <span data-ttu-id="6918c-188">Como en este caso, la topología especificada es la primera y no hay ninguna presentación actual, la sesión multimedia inicia la nueva presentación inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="6918c-188">Because in this case, the specified topology is the first topology and there is no current presentation, the Media Session starts the new presentation immediately.</span></span>

    <span data-ttu-id="6918c-189">El valor **null** también indica que la sesión multimedia debe resolver la topología porque la topología devuelta por el proveedor de topologías siempre es una topología parcial.</span><span class="sxs-lookup"><span data-stu-id="6918c-189">The **NULL** value also indicates that Media Session must resolve the topology because the topology returned by the topology provider is always a partial topology.</span></span>


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



## <a name="queuing-the-next-topology-on-the-media-session"></a><span data-ttu-id="6918c-190">Poner en cola la siguiente topología en la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="6918c-190">Queuing the Next Topology on the Media Session</span></span>

<span data-ttu-id="6918c-191">A continuación, la aplicación debe controlar el evento [MENewPresentation](menewpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="6918c-191">Next, the application needs to handle the [MENewPresentation](menewpresentation.md) event.</span></span>

<span data-ttu-id="6918c-192">El origen del secuenciador genera [MENewPresentation](menewpresentation.md) cuando la sesión multimedia empieza a reproducir un segmento que tiene otro segmento después.</span><span class="sxs-lookup"><span data-stu-id="6918c-192">Sequencer source raises [MENewPresentation](menewpresentation.md) when the Media Session starts playing a segment that has another segment following it.</span></span> <span data-ttu-id="6918c-193">Este evento informa a la aplicación de la siguiente topología en el origen de la secuencia proporcionando el descriptor de presentación para el siguiente segmento en la lista de preplantación.</span><span class="sxs-lookup"><span data-stu-id="6918c-193">This event informs the application about the next topology in the sequence source by providing the presentation descriptor for the next segment in the preroll list.</span></span> <span data-ttu-id="6918c-194">La aplicación debe recuperar la topología asociada mediante el proveedor de topologías y ponerla en cola en la sesión de medios.</span><span class="sxs-lookup"><span data-stu-id="6918c-194">The application must retrieve the associated topology, by using the topology provider, and queue it on the Media Session.</span></span> <span data-ttu-id="6918c-195">Después, el origen del secuenciador prepara esta topología, lo que garantiza una transición sin problemas entre presentaciones.</span><span class="sxs-lookup"><span data-stu-id="6918c-195">The sequencer source then prerolls this topology, which ensures a seamless transition between presentations.</span></span>

<span data-ttu-id="6918c-196">Cuando la aplicación busca entre segmentos, la aplicación recibe varios eventos [MENewPresentation](menewpresentation.md) , ya que el origen del secuenciador actualiza la lista de preplantar y configura la topología correcta.</span><span class="sxs-lookup"><span data-stu-id="6918c-196">When the application seeks across segments, the application receives several [MENewPresentation](menewpresentation.md) events as the sequencer source refreshes the preroll list and sets up the correct topology.</span></span> <span data-ttu-id="6918c-197">La aplicación debe controlar cada evento y poner en cola la topología devuelta en los datos de evento, en la sesión de medios.</span><span class="sxs-lookup"><span data-stu-id="6918c-197">The application must handle each event and queue the topology returned in the event data, on the Media Session.</span></span> <span data-ttu-id="6918c-198">Para obtener información acerca de cómo omitir segmentos, vea [usar el origen del secuenciador](using-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="6918c-198">For information about skipping segments, see [Using the Sequencer Source](using-the-sequencer-source.md).</span></span>

<span data-ttu-id="6918c-199">Para obtener información sobre cómo obtener las notificaciones de origen de Sequencer, vea [Sequencer Source Events](sequencer-source-events.md).</span><span class="sxs-lookup"><span data-stu-id="6918c-199">For information about getting sequencer source notifications, see [Sequencer Source Events](sequencer-source-events.md).</span></span>

1.  <span data-ttu-id="6918c-200">En el controlador de eventos [MENewPresentation](menewpresentation.md) , recupere el descriptor de presentación del segmento siguiente a partir de los datos del evento.</span><span class="sxs-lookup"><span data-stu-id="6918c-200">In the [MENewPresentation](menewpresentation.md) event handler, retrieve the presentation descriptor for the next segment from the event data.</span></span>
2.  <span data-ttu-id="6918c-201">Obtenga la topología asociada para la presentación llamando al método [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="6918c-201">Get the associated topology for the presentation by calling the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span>
3.  <span data-ttu-id="6918c-202">Establezca la topología en la sesión de medios llamando al método [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) .</span><span class="sxs-lookup"><span data-stu-id="6918c-202">Set the topology on the Media Session by calling the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method.</span></span>

    <span data-ttu-id="6918c-203">La sesión multimedia inicia la nueva presentación cuando se ha completado la presentación actual.</span><span class="sxs-lookup"><span data-stu-id="6918c-203">The Media Session starts the new presentation when the current presentation has been completed.</span></span>


```C++
HRESULT CPlaylist::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = GetEventObject(pEvent, &pPD);

    if (SUCCEEDED(hr))
    {
        // Queue the next segment on the media session
        hr = QueueNextSegment(pPD);
    }

    SafeRelease(&pPD);
    return hr;
}
```



## <a name="releasing-the-sequencer-source"></a><span data-ttu-id="6918c-204">Liberar el origen del secuenciador</span><span class="sxs-lookup"><span data-stu-id="6918c-204">Releasing the Sequencer Source</span></span>

<span data-ttu-id="6918c-205">Por último, cierre el origen del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="6918c-205">Finally, shut down the sequencer source.</span></span> <span data-ttu-id="6918c-206">Para ello, llame al método [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) en el origen del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="6918c-206">To do so, call the [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) method on the sequencer source.</span></span> <span data-ttu-id="6918c-207">Esta llamada cierra todos los orígenes de medios nativos subyacentes en el origen del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="6918c-207">This call shuts down all of the underlying native media sources in the sequencer source.</span></span>

<span data-ttu-id="6918c-208">Después de liberar el origen del secuenciador, la aplicación debe cerrar y cerrar la sesión multimedia llamando a [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) y [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown), en ese orden.</span><span class="sxs-lookup"><span data-stu-id="6918c-208">After releasing the sequencer source, the application should close and shut down the Media Session by calling [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) and [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown), in that order.</span></span>

<span data-ttu-id="6918c-209">Para evitar pérdidas de memoria, la aplicación debe liberar los punteros a las interfaces de Media Foundation cuando ya no se necesiten.</span><span class="sxs-lookup"><span data-stu-id="6918c-209">To avoid memory leaks, the application must release pointers to Media Foundation interfaces when they are no longer needed.</span></span>

## <a name="next-steps"></a><span data-ttu-id="6918c-210">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="6918c-210">Next Steps</span></span>

<span data-ttu-id="6918c-211">En este tutorial se muestra cómo crear una lista de reproducción básica mediante el origen del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="6918c-211">This walk-through illustrated how to create a basic playlist by using the sequencer source.</span></span> <span data-ttu-id="6918c-212">Después de crear la lista de reproducción, puede que desee agregar características avanzadas, como omitir segmentos, cambiar el estado de reproducción y buscar en un segmento.</span><span class="sxs-lookup"><span data-stu-id="6918c-212">After creating the playlist, you might want to add advanced features such as segment skipping, changing the playback state, and seeking within a segment.</span></span> <span data-ttu-id="6918c-213">En la lista siguiente se proporcionan vínculos a los temas relacionados:</span><span class="sxs-lookup"><span data-stu-id="6918c-213">The following list provides links to the related topics:</span></span>

-   <span data-ttu-id="6918c-214">[Cómo controlar los Estados](how-to-control-presentation-states.md)de la presentación: el origen del secuenciador se basa en la sesión multimedia para proporcionar control de transporte como, reproducir, pausar y detener.</span><span class="sxs-lookup"><span data-stu-id="6918c-214">[How to Control Presentation States](how-to-control-presentation-states.md): The sequencer source relies on the Media Session to provide transport control such as, Play, Pause, and Stop.</span></span>
-   <span data-ttu-id="6918c-215">[Cómo realizar la limpieza](how-to-perform-scrubbing.md) describe los pasos necesarios para buscar una posición específica en un flujo.</span><span class="sxs-lookup"><span data-stu-id="6918c-215">[How to Perform Scrubbing](how-to-perform-scrubbing.md) describes the steps required to seek to a specific position in a stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6918c-216">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6918c-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6918c-217">Origen del secuenciador</span><span class="sxs-lookup"><span data-stu-id="6918c-217">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



