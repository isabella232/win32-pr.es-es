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
# <a name="creating-playback-topologies"></a>Crear topologías de reproducción

En este tema se describe cómo crear una topología para la reproducción de audio o vídeo. Para la reproducción básica, puede crear una topología parcial, en la que los nodos de origen se conectan directamente a los nodos de salida. No es necesario insertar ningún nodo para las transformaciones intermedias, como descodificadores o convertidores de colores. La sesión multimedia usará el cargador de topología para resolver la topología y el cargador de topología insertará las transformaciones necesarias.

-   [Creación de la topología](#creating-the-topology)
-   [Conexión de secuencias a receptores de medios](#connecting-streams-to-media-sinks)
-   [Creación del receptor de medios](#creating-the-media-sink)
-   [Pasos siguientes](#next-steps)
-   [Temas relacionados](#related-topics)

## <a name="creating-the-topology"></a>Creación de la topología

Estos son los pasos generales para crear una topología de reproducción parcial desde un origen de medios:

1.  Cree el origen de medios. En la mayoría de los casos, utilizará la resolución de origen para crear el origen de medios. Para obtener más información, consulte [solucionador de código fuente](source-resolver.md).
2.  Obtiene el descriptor de presentación del origen del medio.
3.  Cree una topología vacía.
4.  Utilice el descriptor de presentación para enumerar los descriptores de flujo. Para cada descriptor de flujo:
    1.  Obtiene el tipo de medio principal de la secuencia, como audio o vídeo.
    2.  Compruebe si la secuencia está seleccionada actualmente. (Opcionalmente, puede seleccionar o anular la selección de una secuencia, en función del tipo de medio).
    3.  Si la secuencia está seleccionada, cree un objeto de activación para el receptor multimedia, basado en el tipo de archivo multimedia de la secuencia.
    4.  Agregue un nodo de origen para la secuencia y un nodo de salida para el receptor de medios.
    5.  Conecte el nodo de origen al nodo de salida.

Para facilitar el seguimiento de este proceso, el código de ejemplo de este tema se organiza en varias funciones. La función de nivel superior se denomina `CreatePlaybackTopology` . Toma tres parámetros:

-   Puntero a una interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) del origen multimedia.
-   Puntero a la interfaz [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) del descriptor de presentación. Obtenga este puntero llamando a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). En el caso de orígenes con varias presentaciones, los descriptores de presentación para presentaciones posteriores se entregan en el evento [MENewPresentation](menewpresentation.md) .
-   Identificador de una ventana de la aplicación. Si el origen tiene un flujo de vídeo, el vídeo se mostrará en esta ventana.

La función devuelve un puntero a una topología de reproducción parcial en el parámetro *ppTopology* .


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



Esta función lleva a cabo los pasos siguientes:

1.  Llame a [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) para crear la topología. Inicialmente, la topología no contiene ningún nodo.
2.  Llame a [**IMFPresentationDescriptor:: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) para obtener el número de secuencias de la presentación.
3.  Para cada flujo, llame a la función definida por la aplicación `AddBranchToPartialTopology` a una bifurcación en la topología. Esta función se muestra en la sección siguiente.

## <a name="connecting-streams-to-media-sinks"></a>Conexión de secuencias a receptores de medios

Para cada secuencia seleccionada, agregue un nodo de origen y un nodo de salida y, a continuación, conecte los dos nodos. El nodo de origen representa la secuencia. El nodo de salida representa el [representador de vídeo mejorado](enhanced-video-renderer.md) (EVR) o el [representador de audio de streaming](streaming-audio-renderer.md) (SAR).

La `AddBranchToPartialTopology` función, que se muestra en el ejemplo siguiente, toma los parámetros siguientes:

-   Puntero a la interfaz [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de la topología.
-   Puntero a la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) del origen multimedia.
-   Puntero a la interfaz [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) del descriptor de presentación.
-   Índice de base cero de la secuencia.
-   Identificador de la ventana de vídeo. Este identificador solo se usa para la secuencia de vídeo.


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



La función hace lo siguiente:

1.  Llama a [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) y pasa el índice de la secuencia. Este método devuelve un puntero al descriptor de flujo para esa secuencia, junto con un valor booleano que indica si la secuencia está seleccionada.
2.  Si la secuencia no está seleccionada, la función finaliza y devuelve S \_ , porque la aplicación no necesita crear una bifurcación de topología para una secuencia a menos que esté seleccionada.
3.  Si la secuencia está seleccionada, la función completa la rama de topología de la siguiente manera:
    1.  Crea un objeto de activación para el receptor, llamando a la función CreateMediaSinkActivate definida por la aplicación. Esta función se muestra en la sección siguiente.
    2.  Agrega un nodo de origen a la topología. El código de este paso se muestra en el tema [crear nodos de origen](creating-source-nodes.md).
    3.  Agrega un nodo de salida a la topología. El código de este paso se muestra en el tema [crear nodos de salida](creating-output-nodes.md).
    4.  Conecta los dos nodos mediante una llamada a [**IMFTopologyNode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) en el nodo de origen. Al conectar los nodos, la aplicación indica que el nodo ascendente debe proporcionar datos al nodo de nivel inferior. Un nodo de origen tiene una salida y un nodo de salida tiene una entrada, por lo que ambos índices de secuencia son cero.

Las aplicaciones más avanzadas pueden seleccionar o anular la selección de secuencias, en lugar de usar la configuración predeterminada del origen. Un origen puede tener varias secuencias y cualquiera de ellas podría estar seleccionada de forma predeterminada. El descriptor de presentación del origen multimedia tiene un conjunto predeterminado de selecciones de transmisión. En un archivo de vídeo simple con una sola secuencia de audio y una secuencia de vídeo, el origen de medios normalmente seleccionará ambas secuencias de forma predeterminada. Sin embargo, un archivo puede tener varios flujos de audio para distintos idiomas o varias secuencias de vídeo codificadas a velocidades de bits diferentes. En ese caso, algunas de las secuencias no se seleccionarán de forma predeterminada. La aplicación puede cambiar la selección mediante una llamada a [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) y [**IMFPresentationDescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) en el descriptor de presentación.

## <a name="creating-the-media-sink"></a>Creación del receptor de medios

La función siguiente crea un objeto de activación para el receptor de medios EVR o SAR.


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



Esta función lleva a cabo los pasos siguientes:

1.  Llama a [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) en el descriptor de flujo. Este método devuelve un puntero de la interfaz [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .

2.  Llama a [**IMFMediaTypeHandler:: GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype). Este método devuelve el GUID de tipo principal de la secuencia.

3.  Si el tipo de secuencia es audio, la función llama a [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) para crear el objeto de activación del representador de audio. Si el tipo de flujo es video, la función llama a [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para crear el objeto de activación del representador de vídeo. Ambas funciones devuelven un puntero a la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Este puntero se usa para inicializar el nodo de salida del receptor, como se mostró anteriormente.

Para cualquier otro tipo de flujo, este ejemplo devuelve un código de error. Como alternativa, puede simplemente anular la selección de la secuencia.

## <a name="next-steps"></a>Pasos siguientes

Para reproducir un archivo multimedia cada vez, pone en cola la topología en la sesión multimedia mediante una llamada a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology). La sesión multimedia usará el cargador de topología para resolver la topología. Para obtener un ejemplo completo, consulte [Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo reproducir archivos multimedia no protegidos](how-to-play-unprotected-media-files.md)
</dt> <dt>

[Sesión de medios](media-session.md)
</dt> <dt>

[Topologías](topologies.md)
</dt> </dl>

 

 



