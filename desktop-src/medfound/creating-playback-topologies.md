---
description: En este tema se describe cómo crear una topología para la reproducción de audio o vídeo.
ms.assetid: 9c536c4e-fbf8-4c16-932f-e5863b7652fe
title: Crear topologías de reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6d34e9237278766ccb1ee174ba6c09bf953933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696164"
---
# <a name="creating-playback-topologies"></a><span data-ttu-id="1d188-103">Crear topologías de reproducción</span><span class="sxs-lookup"><span data-stu-id="1d188-103">Creating Playback Topologies</span></span>

<span data-ttu-id="1d188-104">En este tema se describe cómo crear una topología para la reproducción de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="1d188-104">This topic describes how to create a topology for audio or video playback.</span></span> <span data-ttu-id="1d188-105">Para la reproducción básica, puede crear una topología parcial, en la que los nodos de origen se conectan directamente a los nodos de salida.</span><span class="sxs-lookup"><span data-stu-id="1d188-105">For basic playback, you can create a partial topology, in which the source nodes are connected directly to the output nodes.</span></span> <span data-ttu-id="1d188-106">No es necesario insertar ningún nodo para las transformaciones intermedias, como descodificadores o convertidores de colores.</span><span class="sxs-lookup"><span data-stu-id="1d188-106">You do not need to insert any nodes for the intermediate transforms, such as decoders or color converters.</span></span> <span data-ttu-id="1d188-107">La sesión multimedia usará el cargador de topología para resolver la topología y el cargador de topología insertará las transformaciones necesarias.</span><span class="sxs-lookup"><span data-stu-id="1d188-107">The Media Session will use the topology loader to resolve the topology, and the topology loader will insert the transforms that are required.</span></span>

-   [<span data-ttu-id="1d188-108">Creación de la topología</span><span class="sxs-lookup"><span data-stu-id="1d188-108">Creating the Topology</span></span>](#creating-the-topology)
-   [<span data-ttu-id="1d188-109">Conexión de secuencias a receptores de medios</span><span class="sxs-lookup"><span data-stu-id="1d188-109">Connecting Streams to Media Sinks</span></span>](#connecting-streams-to-media-sinks)
-   [<span data-ttu-id="1d188-110">Creación del receptor de medios</span><span class="sxs-lookup"><span data-stu-id="1d188-110">Creating the Media Sink</span></span>](#creating-the-media-sink)
-   [<span data-ttu-id="1d188-111">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="1d188-111">Next Steps</span></span>](#next-steps)
-   [<span data-ttu-id="1d188-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1d188-112">Related topics</span></span>](#related-topics)

## <a name="creating-the-topology"></a><span data-ttu-id="1d188-113">Creación de la topología</span><span class="sxs-lookup"><span data-stu-id="1d188-113">Creating the Topology</span></span>

<span data-ttu-id="1d188-114">Estos son los pasos generales para crear una topología de reproducción parcial desde un origen de medios:</span><span class="sxs-lookup"><span data-stu-id="1d188-114">Here are the overall steps for creating a partial playback topology from a media source:</span></span>

1.  <span data-ttu-id="1d188-115">Cree el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="1d188-115">Create the media source.</span></span> <span data-ttu-id="1d188-116">En la mayoría de los casos, utilizará la resolución de origen para crear el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="1d188-116">In most cases, you will use the source resolver to create the media source.</span></span> <span data-ttu-id="1d188-117">Para obtener más información, consulte [solucionador de código fuente](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="1d188-117">For more information, see [Source Resolver](source-resolver.md).</span></span>
2.  <span data-ttu-id="1d188-118">Obtiene el descriptor de presentación del origen del medio.</span><span class="sxs-lookup"><span data-stu-id="1d188-118">Get the media source's presentation descriptor.</span></span>
3.  <span data-ttu-id="1d188-119">Cree una topología vacía.</span><span class="sxs-lookup"><span data-stu-id="1d188-119">Create an empty topology.</span></span>
4.  <span data-ttu-id="1d188-120">Utilice el descriptor de presentación para enumerar los descriptores de flujo.</span><span class="sxs-lookup"><span data-stu-id="1d188-120">Use the presentation descriptor to enumerate the stream descriptors.</span></span> <span data-ttu-id="1d188-121">Para cada descriptor de flujo:</span><span class="sxs-lookup"><span data-stu-id="1d188-121">For each stream descriptor:</span></span>
    1.  <span data-ttu-id="1d188-122">Obtiene el tipo de medio principal de la secuencia, como audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="1d188-122">Get the stream's major media type, such as audio or video.</span></span>
    2.  <span data-ttu-id="1d188-123">Compruebe si la secuencia está seleccionada actualmente.</span><span class="sxs-lookup"><span data-stu-id="1d188-123">Check if the stream is currently selected.</span></span> <span data-ttu-id="1d188-124">(Opcionalmente, puede seleccionar o anular la selección de una secuencia, en función del tipo de medio).</span><span class="sxs-lookup"><span data-stu-id="1d188-124">(Optionally, you can select or deselect a stream, based on the media type.)</span></span>
    3.  <span data-ttu-id="1d188-125">Si la secuencia está seleccionada, cree un objeto de activación para el receptor multimedia, basado en el tipo de archivo multimedia de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1d188-125">If the stream is selected, create an activation object for the media sink, based on the stream's media type.</span></span>
    4.  <span data-ttu-id="1d188-126">Agregue un nodo de origen para la secuencia y un nodo de salida para el receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="1d188-126">Add a source node for the stream and an output node for the media sink.</span></span>
    5.  <span data-ttu-id="1d188-127">Conecte el nodo de origen al nodo de salida.</span><span class="sxs-lookup"><span data-stu-id="1d188-127">Connect the source node to the output node.</span></span>

<span data-ttu-id="1d188-128">Para facilitar el seguimiento de este proceso, el código de ejemplo de este tema se organiza en varias funciones.</span><span class="sxs-lookup"><span data-stu-id="1d188-128">To make this process easier to follow, the example code in this topic is organized into several functions.</span></span> <span data-ttu-id="1d188-129">La función de nivel superior se denomina `CreatePlaybackTopology` .</span><span class="sxs-lookup"><span data-stu-id="1d188-129">The top-level function is named `CreatePlaybackTopology`.</span></span> <span data-ttu-id="1d188-130">Toma tres parámetros:</span><span class="sxs-lookup"><span data-stu-id="1d188-130">It takes three parameters:</span></span>

-   <span data-ttu-id="1d188-131">Puntero a una interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) del origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="1d188-131">A pointer to a [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="1d188-132">Puntero a la interfaz [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) del descriptor de presentación.</span><span class="sxs-lookup"><span data-stu-id="1d188-132">A pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor.</span></span> <span data-ttu-id="1d188-133">Obtenga este puntero llamando a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="1d188-133">Get this pointer by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="1d188-134">En el caso de orígenes con varias presentaciones, los descriptores de presentación para presentaciones posteriores se entregan en el evento [MENewPresentation](menewpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="1d188-134">For sources with multiple presentations, the presentation descriptors for subsequent presentations are delivered in the [MENewPresentation](menewpresentation.md) event.</span></span>
-   <span data-ttu-id="1d188-135">Identificador de una ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1d188-135">A handle to an application window.</span></span> <span data-ttu-id="1d188-136">Si el origen tiene un flujo de vídeo, el vídeo se mostrará en esta ventana.</span><span class="sxs-lookup"><span data-stu-id="1d188-136">If the source has a video stream, the video will be displayed in this window.</span></span>

<span data-ttu-id="1d188-137">La función devuelve un puntero a una topología de reproducción parcial en el parámetro *ppTopology* .</span><span class="sxs-lookup"><span data-stu-id="1d188-137">The function returns a pointer to a partial playback topology in the *ppTopology* parameter.</span></span>


```C++
//  Create a playback topology from a media source.
HRESULT CreatePlaybackTopology(
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    HWND hVideoWnd,                   // Video window.
    IMFTopology **ppTopology)         // Receives a pointer to the topology.
{
    IMFTopology *pTopology = NULL;
    DWORD cSourceStreams = 0;

    // Create a new topology.
    HRESULT hr = MFCreateTopology(&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }




    // Get the number of streams in the media source.
    hr = pPD->GetStreamDescriptorCount(&cSourceStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    // For each stream, create the topology nodes and add them to the topology.
    for (DWORD i = 0; i < cSourceStreams; i++)
    {
        hr = AddBranchToPartialTopology(pTopology, pSource, pPD, i, hVideoWnd);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Return the IMFTopology pointer to the caller.
    *ppTopology = pTopology;
    (*ppTopology)->AddRef();

done:
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="1d188-138">Esta función lleva a cabo los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1d188-138">This function performs the following steps:</span></span>

1.  <span data-ttu-id="1d188-139">Llame a [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) para crear la topología.</span><span class="sxs-lookup"><span data-stu-id="1d188-139">Call [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) to create the topology.</span></span> <span data-ttu-id="1d188-140">Inicialmente, la topología no contiene ningún nodo.</span><span class="sxs-lookup"><span data-stu-id="1d188-140">Initially, the topology does not contain any nodes.</span></span>
2.  <span data-ttu-id="1d188-141">Llame a [**IMFPresentationDescriptor:: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) para obtener el número de secuencias de la presentación.</span><span class="sxs-lookup"><span data-stu-id="1d188-141">Call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) to get the number of streams in the presentation.</span></span>
3.  <span data-ttu-id="1d188-142">Para cada flujo, llame a la función definida por la aplicación `AddBranchToPartialTopology` a una bifurcación en la topología.</span><span class="sxs-lookup"><span data-stu-id="1d188-142">For each stream, call the application-defined `AddBranchToPartialTopology` function to a branch in the topology.</span></span> <span data-ttu-id="1d188-143">Esta función se muestra en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="1d188-143">This function is shown in the next section.</span></span>

## <a name="connecting-streams-to-media-sinks"></a><span data-ttu-id="1d188-144">Conexión de secuencias a receptores de medios</span><span class="sxs-lookup"><span data-stu-id="1d188-144">Connecting Streams to Media Sinks</span></span>

<span data-ttu-id="1d188-145">Para cada secuencia seleccionada, agregue un nodo de origen y un nodo de salida y, a continuación, conecte los dos nodos.</span><span class="sxs-lookup"><span data-stu-id="1d188-145">For each selected stream, add a source node and an output node, then connect the two nodes.</span></span> <span data-ttu-id="1d188-146">El nodo de origen representa la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1d188-146">The source node represents the stream.</span></span> <span data-ttu-id="1d188-147">El nodo de salida representa el [representador de vídeo mejorado](enhanced-video-renderer.md) (EVR) o el [representador de audio de streaming](streaming-audio-renderer.md) (SAR).</span><span class="sxs-lookup"><span data-stu-id="1d188-147">The output node represents either the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) or the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR).</span></span>

<span data-ttu-id="1d188-148">La `AddBranchToPartialTopology` función, que se muestra en el ejemplo siguiente, toma los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="1d188-148">The `AddBranchToPartialTopology` function, shown in the next example, takes the following parameters:</span></span>

-   <span data-ttu-id="1d188-149">Puntero a la interfaz [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de la topología.</span><span class="sxs-lookup"><span data-stu-id="1d188-149">A pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the topology.</span></span>
-   <span data-ttu-id="1d188-150">Puntero a la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) del origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="1d188-150">A pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="1d188-151">Puntero a la interfaz [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) del descriptor de presentación.</span><span class="sxs-lookup"><span data-stu-id="1d188-151">A pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor.</span></span>
-   <span data-ttu-id="1d188-152">Índice de base cero de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1d188-152">The zero-based index of the stream.</span></span>
-   <span data-ttu-id="1d188-153">Identificador de la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1d188-153">A handle to the video window.</span></span> <span data-ttu-id="1d188-154">Este identificador solo se usa para la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1d188-154">This handle is used only for the video stream.</span></span>


```C++
//  Add a topology branch for one stream.
//
//  For each stream, this function does the following:
//
//    1. Creates a source node associated with the stream. 
//    2. Creates an output node for the renderer. 
//    3. Connects the two nodes.
//
//  The media session will add any decoders that are needed.

HRESULT AddBranchToPartialTopology(
    IMFTopology *pTopology,         // Topology.
    IMFMediaSource *pSource,        // Media source.
    IMFPresentationDescriptor *pPD, // Presentation descriptor.
    DWORD iStream,                  // Stream index.
    HWND hVideoWnd)                 // Window for video playback.
{
    IMFStreamDescriptor *pSD = NULL;
    IMFActivate         *pSinkActivate = NULL;
    IMFTopologyNode     *pSourceNode = NULL;
    IMFTopologyNode     *pOutputNode = NULL;

    BOOL fSelected = FALSE;

    HRESULT hr = pPD->GetStreamDescriptorByIndex(iStream, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    if (fSelected)
    {
        // Create the media sink activation object.
        hr = CreateMediaSinkActivate(pSD, hVideoWnd, &pSinkActivate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Add a source node for this stream.
        hr = AddSourceNode(pTopology, pSource, pPD, pSD, &pSourceNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Create the output node for the renderer.
        hr = AddOutputNode(pTopology, pSinkActivate, 0, &pOutputNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Connect the source node to the output node.
        hr = pSourceNode->ConnectOutput(0, pOutputNode, 0);
    }
    // else: If not selected, don't add the branch. 

done:
    SafeRelease(&pSD);
    SafeRelease(&pSinkActivate);
    SafeRelease(&pSourceNode);
    SafeRelease(&pOutputNode);
    return hr;
}
```



<span data-ttu-id="1d188-155">La función hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="1d188-155">The function does the following:</span></span>

1.  <span data-ttu-id="1d188-156">Llama a [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) y pasa el índice de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1d188-156">Calls [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) and passes in the stream index.</span></span> <span data-ttu-id="1d188-157">Este método devuelve un puntero al descriptor de flujo para esa secuencia, junto con un valor booleano que indica si la secuencia está seleccionada.</span><span class="sxs-lookup"><span data-stu-id="1d188-157">This method returns a pointer to the stream descriptor for that stream, along with a Boolean value indicating whether the stream is selected.</span></span>
2.  <span data-ttu-id="1d188-158">Si la secuencia no está seleccionada, la función finaliza y devuelve S \_ , porque la aplicación no necesita crear una bifurcación de topología para una secuencia a menos que esté seleccionada.</span><span class="sxs-lookup"><span data-stu-id="1d188-158">If the stream is not selected, the function exits and returns S\_OK, because the application does not need to create a topology branch for a stream unless it is selected.</span></span>
3.  <span data-ttu-id="1d188-159">Si la secuencia está seleccionada, la función completa la rama de topología de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="1d188-159">If the stream is selected, the function completes the topology branch as follows:</span></span>
    1.  <span data-ttu-id="1d188-160">Crea un objeto de activación para el receptor, llamando a la función CreateMediaSinkActivate definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1d188-160">Creates an activation object for the sink, by calling the application-defined CreateMediaSinkActivate function.</span></span> <span data-ttu-id="1d188-161">Esta función se muestra en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="1d188-161">This function is shown in the next section.</span></span>
    2.  <span data-ttu-id="1d188-162">Agrega un nodo de origen a la topología.</span><span class="sxs-lookup"><span data-stu-id="1d188-162">Adds a source node to the topology.</span></span> <span data-ttu-id="1d188-163">El código de este paso se muestra en el tema [crear nodos de origen](creating-source-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="1d188-163">Code for this step is shown in the topic [Creating Source Nodes](creating-source-nodes.md).</span></span>
    3.  <span data-ttu-id="1d188-164">Agrega un nodo de salida a la topología.</span><span class="sxs-lookup"><span data-stu-id="1d188-164">Adds an output node to the topology.</span></span> <span data-ttu-id="1d188-165">El código de este paso se muestra en el tema [crear nodos de salida](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="1d188-165">Code for this step is shown in the topic [Creating Output Nodes](creating-output-nodes.md).</span></span>
    4.  <span data-ttu-id="1d188-166">Conecta los dos nodos mediante una llamada a [**IMFTopologyNode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) en el nodo de origen.</span><span class="sxs-lookup"><span data-stu-id="1d188-166">Connects the two nodes by calling [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) on the source node.</span></span> <span data-ttu-id="1d188-167">Al conectar los nodos, la aplicación indica que el nodo ascendente debe proporcionar datos al nodo de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="1d188-167">By connecting the nodes, the application indicates that the upstream node should deliver data to the downstream node.</span></span> <span data-ttu-id="1d188-168">Un nodo de origen tiene una salida y un nodo de salida tiene una entrada, por lo que ambos índices de secuencia son cero.</span><span class="sxs-lookup"><span data-stu-id="1d188-168">A source node has one output, and an output node has one input, so both stream indexes are zero.</span></span>

<span data-ttu-id="1d188-169">Las aplicaciones más avanzadas pueden seleccionar o anular la selección de secuencias, en lugar de usar la configuración predeterminada del origen.</span><span class="sxs-lookup"><span data-stu-id="1d188-169">More advanced applications can select or deselect streams, instead of using the source's default configuration.</span></span> <span data-ttu-id="1d188-170">Un origen puede tener varias secuencias y cualquiera de ellas podría estar seleccionada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1d188-170">A source could have multiple streams, and any of them might be selected by default.</span></span> <span data-ttu-id="1d188-171">El descriptor de presentación del origen multimedia tiene un conjunto predeterminado de selecciones de transmisión.</span><span class="sxs-lookup"><span data-stu-id="1d188-171">The media source's presentation descriptor has a default set of stream selections.</span></span> <span data-ttu-id="1d188-172">En un archivo de vídeo simple con una sola secuencia de audio y una secuencia de vídeo, el origen de medios normalmente seleccionará ambas secuencias de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1d188-172">In a simple video file with a single audio stream and video stream, the media source will usually select both streams by default.</span></span> <span data-ttu-id="1d188-173">Sin embargo, un archivo puede tener varios flujos de audio para distintos idiomas o varias secuencias de vídeo codificadas a velocidades de bits diferentes.</span><span class="sxs-lookup"><span data-stu-id="1d188-173">However, a file might have multiple audio streams for different languages, or multiple video streams encoded at different bit rates.</span></span> <span data-ttu-id="1d188-174">En ese caso, algunas de las secuencias no se seleccionarán de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1d188-174">In that case, some of the streams will be unselected by default.</span></span> <span data-ttu-id="1d188-175">La aplicación puede cambiar la selección mediante una llamada a [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) y [**IMFPresentationDescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) en el descriptor de presentación.</span><span class="sxs-lookup"><span data-stu-id="1d188-175">The application can change the selection by calling [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) and [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) on the presentation descriptor.</span></span>

## <a name="creating-the-media-sink"></a><span data-ttu-id="1d188-176">Creación del receptor de medios</span><span class="sxs-lookup"><span data-stu-id="1d188-176">Creating the Media Sink</span></span>

<span data-ttu-id="1d188-177">La función siguiente crea un objeto de activación para el receptor de medios EVR o SAR.</span><span class="sxs-lookup"><span data-stu-id="1d188-177">The next function creates an activation object for the EVR or SAR media sink.</span></span>


```C++
//  Create an activation object for a renderer, based on the stream media type.

HRESULT CreateMediaSinkActivate(
    IMFStreamDescriptor *pSourceSD,     // Pointer to the stream descriptor.
    HWND hVideoWindow,                  // Handle to the video clipping window.
    IMFActivate **ppActivate
)
{
    IMFMediaTypeHandler *pHandler = NULL;
    IMFActivate *pActivate = NULL;

    // Get the media type handler for the stream.
    HRESULT hr = pSourceSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the major media type.
    GUID guidMajorType;
    hr = pHandler->GetMajorType(&guidMajorType);
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Create an IMFActivate object for the renderer, based on the media type.
    if (MFMediaType_Audio == guidMajorType)
    {
        // Create the audio renderer.
        hr = MFCreateAudioRendererActivate(&pActivate);
    }
    else if (MFMediaType_Video == guidMajorType)
    {
        // Create the video renderer.
        hr = MFCreateVideoRendererActivate(hVideoWindow, &pActivate);
    }
    else
    {
        // Unknown stream type. 
        hr = E_FAIL;
        // Optionally, you could deselect this stream instead of failing.
    }
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Return IMFActivate pointer to caller.
    *ppActivate = pActivate;
    (*ppActivate)->AddRef();

done:
    SafeRelease(&pHandler);
    SafeRelease(&pActivate);
    return hr;
}
```



<span data-ttu-id="1d188-178">Esta función lleva a cabo los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1d188-178">This function performs the following steps:</span></span>

1.  <span data-ttu-id="1d188-179">Llama a [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) en el descriptor de flujo.</span><span class="sxs-lookup"><span data-stu-id="1d188-179">Calls [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span> <span data-ttu-id="1d188-180">Este método devuelve un puntero de la interfaz [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .</span><span class="sxs-lookup"><span data-stu-id="1d188-180">This method returns an [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface pointer.</span></span>

2.  <span data-ttu-id="1d188-181">Llama a [**IMFMediaTypeHandler:: GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span><span class="sxs-lookup"><span data-stu-id="1d188-181">Calls [**IMFMediaTypeHandler::GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span></span> <span data-ttu-id="1d188-182">Este método devuelve el GUID de tipo principal de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1d188-182">This method returns the major type GUID for the stream.</span></span>

3.  <span data-ttu-id="1d188-183">Si el tipo de secuencia es audio, la función llama a [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) para crear el objeto de activación del representador de audio.</span><span class="sxs-lookup"><span data-stu-id="1d188-183">If the stream type is audio, the function calls [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) to create the audio renderer activation object.</span></span> <span data-ttu-id="1d188-184">Si el tipo de flujo es video, la función llama a [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para crear el objeto de activación del representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1d188-184">If the stream type is video, the function calls [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the video renderer activation object.</span></span> <span data-ttu-id="1d188-185">Ambas funciones devuelven un puntero a la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="1d188-185">Both of these functions return a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="1d188-186">Este puntero se usa para inicializar el nodo de salida del receptor, como se mostró anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1d188-186">This pointer is used to initialize the output node for the sink, as shown previously.</span></span>

<span data-ttu-id="1d188-187">Para cualquier otro tipo de flujo, este ejemplo devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="1d188-187">For any other stream type, this example returns an error code.</span></span> <span data-ttu-id="1d188-188">Como alternativa, puede simplemente anular la selección de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1d188-188">Alternatively, you could simply deselect the stream.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1d188-189">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="1d188-189">Next Steps</span></span>

<span data-ttu-id="1d188-190">Para reproducir un archivo multimedia cada vez, pone en cola la topología en la sesión multimedia mediante una llamada a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="1d188-190">To play one media file at a time, queue the topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="1d188-191">La sesión multimedia usará el cargador de topología para resolver la topología.</span><span class="sxs-lookup"><span data-stu-id="1d188-191">The Media Session will use the topology loader to resolve the topology.</span></span> <span data-ttu-id="1d188-192">Para obtener un ejemplo completo, consulte [Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="1d188-192">For a complete example, see [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d188-193">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1d188-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d188-194">Cómo reproducir archivos multimedia no protegidos</span><span class="sxs-lookup"><span data-stu-id="1d188-194">How to Play Unprotected Media Files</span></span>](how-to-play-unprotected-media-files.md)
</dt> <dt>

[<span data-ttu-id="1d188-195">Sesión de medios</span><span class="sxs-lookup"><span data-stu-id="1d188-195">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="1d188-196">Topologías</span><span class="sxs-lookup"><span data-stu-id="1d188-196">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



