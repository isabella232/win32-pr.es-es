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
# <a name="how-to-create-a-playlist"></a>Cómo crear una lista de reproducción

En este tema se describe cómo usar el origen de la secuencia para reproducir una secuencia de archivos.

## <a name="overview"></a>Información general

Para reproducir archivos multimedia en una secuencia, la aplicación debe agregar topologías en una secuencia para crear una lista de reproducción y poner en cola estas topologías en la sesión multimedia para su reproducción.

El origen del secuenciador garantiza una reproducción perfecta inicializando y cargando la topología siguiente antes de que la sesión de medios empiece a reproducir la topología actual. Esto permite a la aplicación iniciar la próxima topología rápidamente siempre que sea necesario.

La sesión multimedia es responsable de la alimentación de datos a los receptores y de la reproducción de las topologías del origen de la secuencia. Además, la sesión multimedia administra el tiempo de presentación de los segmentos.

Para obtener más información sobre cómo el origen del secuenciador administra las topologías, consulte [acerca del origen del secuenciador](about-the-sequencer-source.md).

Este tutorial contiene los siguientes pasos:

1.  [Requisitos previos](#prerequisites)
2.  [Inicializar Media Foundation](#initializing-media-foundation)
3.  [Crear objetos Media Foundation](#creating-media-foundation-objects)
4.  [Crear el origen de medios](#creating-the-media-source)
5.  [Crear topologías parciales](#creating-partial-topologies)
6.  [Agregar topologías al origen del secuenciador](#adding-topologies-to-the-sequencer-source)
7.  [Establecimiento de la primera topología en la sesión multimedia](#setting-the-first-topology-on-the-media-session)
8.  [Poner en cola la siguiente topología en la sesión multimedia](#queuing-the-next-topology-on-the-media-session)
9.  [Liberar el origen del secuenciador](#releasing-the-sequencer-source)

Los ejemplos de código que se muestran en este tema son fragmentos del [código de ejemplo de origen de Sequencer](sequencer-source-example-code.md)de tema, que contiene el código de ejemplo completo.

## <a name="prerequisites"></a>Requisitos previos

Antes de comenzar este tutorial, familiarícese con los siguientes conceptos de Media Foundation:

-   [Sesión de medios](media-session.md)
-   [Topologías](topologies.md)
-   [Generadores de eventos multimedia](media-event-generators.md)
-   [Descriptores de presentación](presentation-descriptors.md)

También puede leer [Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md), porque el código de ejemplo shwon aquí se expande en el código de ese tema.

## <a name="initializing-media-foundation"></a>Inicializar Media Foundation

Antes de poder usar cualquier método o interfaz de Media Foundation, inicialice Media Foundation mediante una llamada a la función [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) . Para obtener más información, vea [inicializar Media Foundation](initializing-media-foundation.md).


```C++
    hr = MFStartup(MF_VERSION);
```



## <a name="creating-media-foundation-objects"></a>Crear objetos Media Foundation

A continuación, cree los siguientes objetos de Media Foundation:

-   Sesión de medios. Este objeto expone la interfaz [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) , que proporciona métodos para reproducir, pausar y detener la topología actual.
-   Origen del secuenciador. Este objeto expone la interfaz [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) , que proporciona métodos para agregar, actualizar y eliminar topologías en una secuencia.

1.  Llame a la función [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para crear la sesión multimedia.
2.  Llame a [**IMFMediaEventQueue:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) para solicitar el primer evento de la sesión multimedia.
3.  Llame a la función [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) para crear el origen del secuenciador.

En el código siguiente se crea la sesión multimedia y se solicita el primer evento:


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



## <a name="creating-the-media-source"></a>Crear el origen de medios

A continuación, cree un origen de medios para el primer segmento de la lista de reproducción. Utilice el [solucionador de origen](source-resolver.md) para crear un origen de medios a partir de una dirección URL. Para ello, llame a la función [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) para crear un solucionador de origen y, a continuación, llame al método [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) para crear el origen de medios.

Para obtener información sobre los orígenes de medios, consulte [orígenes de medios](media-sources.md).

## <a name="creating-partial-topologies"></a>Crear topologías parciales

Cada segmento del origen del secuenciador tiene su propia topología parcial. A continuación, cree topologías parciales para los orígenes multimedia. En el caso de una topología parcial, los nodos de origen de la topología se conectan directamente a los nodos de salida, sin especificar las transformaciones intermedias. La sesión multimedia utiliza el objeto cargador de topología para resolver la topología. Una vez que se resuelve una topología, se agregan los descodificadores necesarios y otros nodos de transformación. El origen del secuenciador también puede contener topologías completas.

Para crear el objeto Topology, utilice la función [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) y, a continuación, use la interfaz [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) para crear nodos de secuencia.

Para obtener instrucciones completas sobre el uso de estos elementos de programación para crear topologías, vea [crear topologías de reproducción](creating-playback-topologies.md).

Una aplicación puede reproducir una parte seleccionada del código fuente nativo mediante la configuración del nodo de origen. Para ello, establezca el atributo [**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md) y el atributo [**MF \_ TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md) en los nodos de topología de nodo de la **\_ topología MF \_ SOURCESTREAM \_** . Especifique la hora de inicio del medio y la hora de detención del medio en relación con el inicio del origen nativo como tipos **UINT64** .

## <a name="adding-topologies-to-the-sequencer-source"></a>Agregar topologías al origen del secuenciador

A continuación, agregue al origen del secuenciador las topologías parciales que creó. A cada elemento de secuencia, denominado *segmento*, se le asigna un identificador **MFSequencerElementId** . Para obtener más información sobre cómo el origen del secuenciador administra las topologías, consulte [acerca del origen del secuenciador](about-the-sequencer-source.md).

Después de agregar todas las topologías al origen del secuenciador, la aplicación debe marcar el último segmento de la secuencia para finalizar la reproducción de la canalización. Sin esta marca, el origen del secuenciador espera que se agreguen más topologías.

1.  Llame al método [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) para agregar una topología específica al origen del secuenciador.

    ```C++
        hr = m_pSequencerSource->AppendTopology(
            pTopology, 
            SequencerTopologyFlags_Last, 
            &SegmentId
            );
    ```

    

    [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) agrega la topología especificada a la secuencia. Este método devuelve el identificador de segmento en el parámetro *pdwId* .

    Si la topología es la última del origen del secuenciador, pase SequencerTopologyFlags \_ en último lugar en el parámetro *dwFlags* . Este valor se define en la enumeración [**MFSequencerTopologyFlags**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) .

2.  Llame a [**IMFSequencerSource:: UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) para actualizar las marcas de la topología asociada al identificador de segmento en la lista de entrada. En este caso, la llamada indica que el segmento especificado es el último segmento del secuenciador. (Esta llamada es opcional si la última topología se especifica en la llamada a [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) ).

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

    

La aplicación puede reemplazar la topología de un segmento por otra topología llamando a [**IMFSequencerSource:: UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) y pasando la nueva topología en *pTopology*. Si hay nuevos orígenes nativos en la nueva topología, los orígenes se agregan a la caché de origen. También se actualiza la lista de preplantación.

## <a name="setting-the-first-topology-on-the-media-session"></a>Establecimiento de la primera topología en la sesión multimedia

A continuación, pone en cola la primera topología en el origen de la secuencia en la sesión multimedia. Para obtener la primera topología del origen del secuenciador, la aplicación debe llamar al método [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) . Este método devuelve la topología parcial, que se resuelve en la sesión multimedia.

Para obtener información acerca de las topologías parciales, vea [acerca de las topologías](about-topologies.md).

1.  Recupere el origen de medios nativo para la primera topología del origen de la secuencia.
2.  Cree un descriptor de presentación para el origen de medios llamando al método [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) .
3.  Recupere la topología asociada para la presentación llamando al método [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .
4.  Establezca la primera topología en la sesión de medios mediante una llamada a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

    Llame a [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) con el parámetro *DwSetTopologyFlags* establecido en **null**. Esto indica a la sesión de medios que inicie la topología especificada cuando se haya completado la topología actual. Como en este caso, la topología especificada es la primera y no hay ninguna presentación actual, la sesión multimedia inicia la nueva presentación inmediatamente.

    El valor **null** también indica que la sesión multimedia debe resolver la topología porque la topología devuelta por el proveedor de topologías siempre es una topología parcial.


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



## <a name="queuing-the-next-topology-on-the-media-session"></a>Poner en cola la siguiente topología en la sesión multimedia

A continuación, la aplicación debe controlar el evento [MENewPresentation](menewpresentation.md) .

El origen del secuenciador genera [MENewPresentation](menewpresentation.md) cuando la sesión multimedia empieza a reproducir un segmento que tiene otro segmento después. Este evento informa a la aplicación de la siguiente topología en el origen de la secuencia proporcionando el descriptor de presentación para el siguiente segmento en la lista de preplantación. La aplicación debe recuperar la topología asociada mediante el proveedor de topologías y ponerla en cola en la sesión de medios. Después, el origen del secuenciador prepara esta topología, lo que garantiza una transición sin problemas entre presentaciones.

Cuando la aplicación busca entre segmentos, la aplicación recibe varios eventos [MENewPresentation](menewpresentation.md) , ya que el origen del secuenciador actualiza la lista de preplantar y configura la topología correcta. La aplicación debe controlar cada evento y poner en cola la topología devuelta en los datos de evento, en la sesión de medios. Para obtener información acerca de cómo omitir segmentos, vea [usar el origen del secuenciador](using-the-sequencer-source.md).

Para obtener información sobre cómo obtener las notificaciones de origen de Sequencer, vea [Sequencer Source Events](sequencer-source-events.md).

1.  En el controlador de eventos [MENewPresentation](menewpresentation.md) , recupere el descriptor de presentación del segmento siguiente a partir de los datos del evento.
2.  Obtenga la topología asociada para la presentación llamando al método [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .
3.  Establezca la topología en la sesión de medios llamando al método [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) .

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

Por último, cierre el origen del secuenciador. Para ello, llame al método [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) en el origen del secuenciador. Esta llamada cierra todos los orígenes de medios nativos subyacentes en el origen del secuenciador.

Después de liberar el origen del secuenciador, la aplicación debe cerrar y cerrar la sesión multimedia llamando a [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) y [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown), en ese orden.

Para evitar pérdidas de memoria, la aplicación debe liberar los punteros a las interfaces de Media Foundation cuando ya no se necesiten.

## <a name="next-steps"></a>Pasos siguientes

En este tutorial se muestra cómo crear una lista de reproducción básica mediante el origen del secuenciador. Después de crear la lista de reproducción, puede que desee agregar características avanzadas, como omitir segmentos, cambiar el estado de reproducción y buscar en un segmento. En la lista siguiente se proporcionan vínculos a los temas relacionados:

-   [Cómo controlar los Estados](how-to-control-presentation-states.md)de la presentación: el origen del secuenciador se basa en la sesión multimedia para proporcionar control de transporte como, reproducir, pausar y detener.
-   [Cómo realizar la limpieza](how-to-perform-scrubbing.md) describe los pasos necesarios para buscar una posición específica en un flujo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Origen del secuenciador](sequencer-source.md)
</dt> </dl>

 

 



