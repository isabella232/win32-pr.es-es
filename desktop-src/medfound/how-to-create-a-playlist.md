---
description: En este tema se describe cómo usar el origen de secuencia para reproducir una secuencia de archivos.
ms.assetid: 5a760492-bd52-40b8-a652-8a62646db6ae
title: Cómo crear una lista de reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d2a36735d29510e0622882a399fff199fd2289261453a51f281414b5076826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828175"
---
# <a name="how-to-create-a-playlist"></a>Cómo crear una lista de reproducción

En este tema se describe cómo usar el origen de secuencia para reproducir una secuencia de archivos.

## <a name="overview"></a>Información general

Para reproducir archivos multimedia en una secuencia, la aplicación debe agregar topologías en una secuencia para crear una lista de reproducción y poner en cola estas topologías en la sesión multimedia para su reproducción.

El origen del secuenciador garantiza una reproducción sin problemas mediante la inicialización y carga de la siguiente topología antes de que la sesión multimedia empiece a reproducir la topología actual. Esto permite que la aplicación inicie la siguiente topología rápidamente siempre que sea necesario.

La sesión multimedia es responsable de alimentar los datos a los receptores y reproducir las topologías en el origen de secuencia. Además, la sesión multimedia administra el tiempo de presentación de los segmentos.

Para obtener más información sobre cómo el origen del secuenciador administra las topologías, vea [Acerca del origen del secuenciador.](about-the-sequencer-source.md)

Este recorrido contiene los pasos siguientes:

1.  [Requisitos previos](#prerequisites)
2.  [Inicializar Media Foundation](#initializing-media-foundation)
3.  [Crear Media Foundation objetos](#creating-media-foundation-objects)
4.  [Creación del origen de medios](#creating-the-media-source)
5.  [Crear topologías parciales](#creating-partial-topologies)
6.  [Agregar topologías al origen del secuenciador](#adding-topologies-to-the-sequencer-source)
7.  [Establecer la primera topología en la sesión multimedia](#setting-the-first-topology-on-the-media-session)
8.  [Cola de la siguiente topología en la sesión multimedia](#queuing-the-next-topology-on-the-media-session)
9.  [Liberar el origen del secuenciador](#releasing-the-sequencer-source)

Los ejemplos de código que se muestran en este tema son extractos del tema [Código](sequencer-source-example-code.md)de ejemplo de origen del secuenciador, que contiene el código de ejemplo completo.

## <a name="prerequisites"></a>Requisitos previos

Antes de comenzar este recorrido, familiarícese con los siguientes Media Foundation conceptos:

-   [Sesión multimedia](media-session.md)
-   [Topologías](topologies.md)
-   [Generadores de eventos multimedia](media-event-generators.md)
-   [Descriptores de presentación](presentation-descriptors.md)

Lea también [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md), porque el código de ejemplo shwon aquí se expande en el código de ese tema.

## <a name="initializing-media-foundation"></a>Inicializar Media Foundation

Para poder usar cualquier interfaz Media Foundation métodos, inicialice Media Foundation mediante una llamada a [**la función MFStartup.**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) Para obtener más información, vea [Inicializar Media Foundation](initializing-media-foundation.md).


```C++
    hr = MFStartup(MF_VERSION);
```



## <a name="creating-media-foundation-objects"></a>Crear Media Foundation objetos

A continuación, cree los Media Foundation siguientes:

-   Sesión multimedia. Este objeto expone la interfaz [**IMFMediaSession,**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) que proporciona métodos para reproducir, pausar y detener la topología actual.
-   Origen del secuenciador. Este objeto expone la interfaz [**IMFSequencerSource,**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) que proporciona métodos para agregar, actualizar y eliminar topologías en una secuencia.

1.  Llame a [**la función MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para crear la sesión multimedia.
2.  Llame [**a IMFMediaEventQueue::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) para solicitar el primer evento de la sesión multimedia.
3.  Llame a [**la función MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) para crear el origen del secuenciador.

El código siguiente crea la sesión multimedia y solicita el primer evento:


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



## <a name="creating-the-media-source"></a>Creación del origen de medios

A continuación, cree un origen multimedia para el primer segmento de lista de reproducción. Use el [solucionador de origen](source-resolver.md) para crear un origen multimedia a partir de una dirección URL. Para ello, llame a la función [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) para crear una resolución de origen y, a continuación, llame al método [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) para crear el origen multimedia.

Para obtener información sobre los orígenes de medios, vea [Orígenes de medios](media-sources.md).

## <a name="creating-partial-topologies"></a>Crear topologías parciales

Cada segmento del origen del secuenciador tiene su propia topología parcial. A continuación, cree topologías parciales para orígenes multimedia. En el caso de una topología parcial, los nodos de origen de la topología se conectan directamente a los nodos de salida, sin especificar ninguna transformación intermedia. La sesión multimedia usa el objeto del cargador de topologías para resolver la topología. Una vez resuelta una topología, se agregan los descodificadores necesarios y otros nodos de transformación. El origen del secuenciador también puede contener topologías completa.

Para crear el objeto de topología, use la [**función MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) y, a continuación, use la interfaz [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) para crear nodos de flujo.

Para obtener instrucciones completas sobre el uso de estos elementos de programación para crear topologías, vea [Crear topologías de reproducción.](creating-playback-topologies.md)

Una aplicación puede reproducir una parte seleccionada del origen nativo configurando el nodo de origen. Para ello, establezca el atributo [**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md) y el atributo [**MF \_ TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md) en los nodos de topología DEL NODO SOURCESTREAM DE **MF \_ TOPOLOGY. \_ \_** Especifique la hora de inicio del medio y la hora de detenerse del medio con respecto al inicio del origen nativo como **tipos UINT64.**

## <a name="adding-topologies-to-the-sequencer-source"></a>Agregar topologías al origen del secuenciador

A continuación, agregue al origen del secuenciador las topologías parciales que ha creado. A cada elemento de secuencia, denominado *segmento*, se le asigna un identificador **MFSequencerElementId.** Para obtener más información sobre cómo el origen del secuenciador administra las topologías, vea [Acerca del origen del secuenciador.](about-the-sequencer-source.md)

Después de agregar todas las topologías al origen del secuenciador, la aplicación debe marcar el último segmento de la secuencia para finalizar la reproducción en la canalización. Sin esta marca, el origen del secuenciador espera que se agregan más topologías.

1.  Llame al [**método IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) para agregar una topología específica al origen del secuenciador.

    ```C++
        hr = m_pSequencerSource->AppendTopology(
            pTopology, 
            SequencerTopologyFlags_Last, 
            &SegmentId
            );
    ```

    

    [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) agrega la topología especificada a la secuencia. Este método devuelve el identificador de segmento en el *parámetro pdwId.*

    Si la topología es la última del origen del secuenciador, pase SequencerTopologyFlags Last en el \_ *parámetro dwFlags.* Este valor se define en la [**enumeración MFSequencerTopologyFlags.**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags)

2.  Llame [**a IMFSequencerSource::UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) para actualizar las marcas de la topología asociada al identificador de segmento en la lista de entrada. En este caso, la llamada indica que el segmento especificado es el último segmento del secuenciador. (Esta llamada es opcional si se especifica la última topología en la [**llamada AppendTopology).**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology)

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

    

La aplicación puede reemplazar la topología de un segmento por otra mediante una llamada a [**IMFSequencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) y pasando la nueva topología en *pTopology*. Si hay nuevos orígenes nativos en la nueva topología, los orígenes se agregan a la caché de origen. También se actualiza la lista de inscripción previa.

## <a name="setting-the-first-topology-on-the-media-session"></a>Establecer la primera topología en la sesión multimedia

A continuación, poner en cola la primera topología en el origen de secuencia en la sesión multimedia. Para obtener la primera topología del origen del secuenciador, la aplicación debe llamar al método [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) Este método devuelve la topología parcial, que se resuelve mediante la sesión multimedia.

Para obtener información sobre las topologías parciales, vea [About Topologies](about-topologies.md).

1.  Recupere el origen de medios nativo para la primera topología del origen de secuencia.
2.  Cree un descriptor de presentación para el origen multimedia llamando al [**método IMFMediaSource::CreatePresentationDescriptor.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)
3.  Recupere la topología asociada para la presentación llamando al método [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology)
4.  Establezca la primera topología en la sesión multimedia llamando a [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

    Llame [**a SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) con el *parámetro dwSetTopologyFlags* establecido en **NULL.** Esto indica a la sesión multimedia que inicie la topología especificada cuando se haya completado la topología actual. Dado que en este caso, la topología especificada es la primera topología y no hay ninguna presentación actual, la sesión multimedia inicia la nueva presentación inmediatamente.

    El **valor NULL** también indica que la sesión multimedia debe resolver la topología porque la topología devuelta por el proveedor de topología siempre es una topología parcial.


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



## <a name="queuing-the-next-topology-on-the-media-session"></a>Cola de la siguiente topología en la sesión multimedia

A continuación, la aplicación debe controlar el [evento MENewPresentation.](menewpresentation.md)

El origen del secuenciador [genera MENewPresentation](menewpresentation.md) cuando la sesión multimedia comienza a reproducir un segmento que tiene otro segmento que lo sigue. Este evento informa a la aplicación sobre la siguiente topología en el origen de secuencia proporcionando el descriptor de presentación para el siguiente segmento en la lista de inscripción previa. La aplicación debe recuperar la topología asociada mediante el proveedor de topologías y ponerla en cola en la sesión multimedia. A continuación, el origen del secuenciador preinselección esta topología, lo que garantiza una transición sin problemas entre presentaciones.

Cuando la aplicación busca entre segmentos, la aplicación recibe varios eventos [MENewPresentation](menewpresentation.md) a medida que el origen del secuenciador actualiza la lista de inscripción previa y configura la topología correcta. La aplicación debe controlar cada evento y poner en cola la topología devuelta en los datos del evento, en la sesión multimedia. Para obtener información sobre cómo omitir segmentos, [vea Using the Sequencer Source](using-the-sequencer-source.md).

Para obtener información sobre cómo obtener notificaciones de origen del secuenciador, vea [Sequencer Source Events](sequencer-source-events.md).

1.  En el [controlador de eventos MENewPresentation,](menewpresentation.md) recupere el descriptor de presentación para el siguiente segmento de los datos del evento.
2.  Obtenga la topología asociada para la presentación mediante una llamada al método [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology)
3.  Establezca la topología en la sesión multimedia llamando al [**método IMFMediaSession::SetTopology.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)

    La sesión multimedia inicia la nueva presentación cuando se ha completado la presentación actual.


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



## <a name="releasing-the-sequencer-source"></a>Liberar el origen del secuenciador

Por último, apague el origen del secuenciador. Para ello, llame al [**método IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) en el origen del secuenciador. Esta llamada cierra todos los orígenes multimedia nativos subyacentes en el origen del secuenciador.

Después de liberar el origen del secuenciador, la aplicación debe cerrar y apagar la sesión multimedia mediante una llamada a [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) y [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown), en ese orden.

Para evitar pérdidas de memoria, la aplicación debe liberar punteros a Media Foundation interfaces cuando ya no sean necesarias.

## <a name="next-steps"></a>Pasos siguientes

En este recorrido se muestra cómo crear una lista de reproducción básica mediante el origen del secuenciador. Después de crear la lista de reproducción, es posible que quiera agregar características avanzadas, como la omisión de segmentos, el cambio del estado de reproducción y la búsqueda dentro de un segmento. En la lista siguiente se proporcionan vínculos a los temas relacionados:

-   [Cómo controlar los estados de presentación:](how-to-control-presentation-states.md)el origen del secuenciador se basa en la sesión multimedia para proporcionar control de transporte como, reproducir, pausar y detener.
-   [En How to Perform Scrubbing (Cómo](how-to-perform-scrubbing.md) realizar la limpieza) se describen los pasos necesarios para buscar una posición específica en una secuencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Origen del secuenciador](sequencer-source.md)
</dt> </dl>

 

 



