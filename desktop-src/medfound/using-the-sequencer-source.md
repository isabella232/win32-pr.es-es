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
# <a name="using-the-sequencer-source"></a>Usar el origen del secuenciador

En este tema se describe cómo usar el [origen del secuenciador](sequencer-source.md). Contiene las secciones siguientes:

-   [Información general](#overview)
-   [Agregar topologías](#adding-topologies)
-   [Eliminar topologías](#deleting-topologies)
-   [Omitir un segmento](#skipping-to-a-segment)
-   [Temas relacionados](#related-topics)

Para obtener información general sobre el origen del secuenciador, vea [acerca del origen del secuenciador](about-the-sequencer-source.md).

## <a name="overview"></a>Información general

El origen del secuenciador expone las siguientes interfaces.



| Interfaz                                                                        | Descripción                                                                        |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                         | Expone la funcionalidad de origen de medios genéricos.                                        |
| [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)                                 | Permite a la aplicación agregar o quitar topologías.                               |
| [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)         | Recupera la siguiente topología que se va a poner en cola en la sesión multimedia.                         |
| [**IMFMediaSourcePresentationProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider) | Lo utiliza la sesión de medios para terminar segmentos. Las aplicaciones no usan esta interfaz. |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                           | Consulta el origen del secuenciador para las [interfaces de servicio](service-interfaces.md).     |



 

Para reproducir una secuencia de orígenes multimedia, realice los pasos siguientes:

1.  Para crear el origen del secuenciador, llame a la función [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) .
2.  Para cada segmento, cree una topología de reproducción, como se describe en [crear topologías de reproducción](creating-playback-topologies.md). Para agregar la topología a la presentación, llame a [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).
3.  Antes de iniciar la reproducción, llame a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) en el origen del secuenciador. Este método devuelve un puntero a un descriptor de presentación para el primer segmento. Para obtener la topología asociada a este segmento, llame a **QueryInterface** en el origen del secuenciador para la interfaz [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) . Pase el descriptor de presentación al método [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) . Este método devuelve un puntero a la topología.
4.  Pase la topología para el primer segmento a la sesión multimedia, llamando al método [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) de la sesión multimedia.
5.  Inicie la reproducción mediante una llamada a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).
6.  Cuando el origen del secuenciador está listo para prevertir el siguiente segmento, envía un evento [MENewPresentation](menewpresentation.md) cuyos datos de evento son un puntero de interfaz [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) . De nuevo, obtenga la topología del segmento mediante una llamada a [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) en el origen del secuenciador y establezca la topología en la sesión multimedia llamando a [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology). No es necesario reiniciar el origen del medio; se reproducirá automáticamente en el segmento siguiente.
7.  Antes de que se cierre la aplicación, cierre el origen del secuenciador mediante una llamada a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).

En el código siguiente se muestra cómo obtener la topología y establecerla en la sesión multimedia:


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



Para obtener un ejemplo de código completo, vea [código de ejemplo del origen del secuenciador](sequencer-source-example-code.md).

## <a name="adding-topologies"></a>Agregar topologías

El origen del secuenciador mantiene dos listas de topologías: la *lista de entrada* y la lista de *preplantación*.

La lista de entrada es una colección de topologías que corresponden a segmentos de lista de reproducción, en el orden en que la aplicación los agregó llamando a [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology). Este método asigna a cada topología un *identificador de segmento* único del tipo **MFSequencerElementId**. El identificador de segmento se establece como un atributo para todos los nodos de topología de origen. Una aplicación puede obtener el identificador de segmento de un nodo de origen mediante el atributo de la [ \_ \_ secuencia \_ TOPONODE de MF](mf-toponode-sequence-elementid-attribute.md) . La lista de entrada puede tener topologías duplicadas si la aplicación llama a **AppendTopology** en la misma topología más de una vez. sin embargo, se identifican por sus identificadores de segmento únicos.

La lista de preplantación es una colección de topologías de lista de entrada que se han inicializado como preparación para la reproducción. Esto permite a la sesión multimedia pasar a la siguiente topología sin problemas cuando finaliza la topología activa. La aplicación no puede Agregar o quitar directamente topologías de la lista de preplantación. lo genera el origen del secuenciador cuando se selecciona una topología de la lista de entrada para la reproducción. Esto hace que el origen del secuenciador agregue la siguiente topología de la lista de entrada a la lista de predistribución. Después de hacerlo, el origen del secuenciador genera asincrónicamente el evento [MENewPresentation](menewpresentation.md) y pasa el descriptor de presentación para la topología de predistribución como datos de evento. La aplicación debe realizar escuchas para este evento mediante la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) de la sesión multimedia y poner en cola la topología de predistribución en la sesión multimedia llamando a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology). Esto debe hacerse antes de que la sesión multimedia complete la reproducción de la topología activa. **SetTopology** informa a la sesión multimedia sobre la siguiente topología que debe reproducirse después de que haya finalizado la reproducción de la topología activa. Para garantizar un treansition sin problemas, la aplicación debe llamar a **SetTopology** antes de que la sesión multimedia complete la reproducción de la topología anterior. De lo contrario, habrá un hueco entre los segmentos.

El evento [MENewPresentation](menewpresentation.md) se desencadena siempre que haya una topología que siga a la topología activa. Por consiguiente, si la lista de entrada contiene solo una topología, o si la topología activa es la última de la lista de entrada, no se genera este evento.

La lista de preplantación se sincroniza con la lista de entrada y se actualiza cada vez que se agrega o se elimina una topología de la lista de entrada.

## <a name="deleting-topologies"></a>Eliminar topologías

Para quitar una topología del origen del secuenciador, una aplicación debe llamar al método [**IMFSequencerSource::D eletetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) y especificar el identificador de segmento.

Antes de llamar a [**DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology), la aplicación debe asegurarse de que la sesión multimedia no esté usando la topología que la aplicación desea eliminar. Para ello, se deben realizar las siguientes acciones antes de que la aplicación llame a **DeleteTopology**:

-   Se recibió un evento [MESessionTopologyStatus](mesessiontopologystatus.md) con MF \_ TOPOSTATUS \_ finalizado para la topología con el fin de asegurarse de que la sesión multimedia ha finalizado la reproducción.

-   [MESessionTopologyStatus](mesessiontopologystatus.md) con MF \_ TOPOSTATUS \_ se ha iniciado el \_ origen en la siguiente topología para asegurarse de que la sesión multimedia ha empezado a reproducir la topología siguiente, se recibe el evento [MESessionEnded](mesessionended.md) para asegurarse de que la sesión multimedia se realiza con la última topología del origen del secuenciador.

Si el segmento que se va a eliminar es la topología activa, la reproducción se detiene y el origen del secuenciador genera el evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) . Si la topología activa es también la última topología, se genera el evento [MEEndOfPresentation](meendofpresentation.md) .

## <a name="skipping-to-a-segment"></a>Omitir un segmento

Una aplicación puede saltar a un segmento determinado en la secuencia iniciando la [sesión de medios](media-session.md) con un desplazamiento de segmento, como se indica a continuación:

1.  Llame a la función [**MFCreateSequencerSegmentOffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) para crear el desplazamiento del segmento. Especifique el identificador del segmento en el parámetro *dwId* . (El método [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) devolvió el identificador al agregar por primera vez la topología al origen del secuenciador). El parámetro *hnsOffset* especifica un desplazamiento de tiempo, relativo al inicio del segmento. La reproducción se iniciará en este momento. Para el parámetro *pvarSegmentOffset* , pase la dirección de un **PROPVARIANT** vacío. Cuando la función devuelve, este **PROPVARIANT** contiene el desplazamiento del segmento.

2.  Llame al método [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) en la sesión multimedia. Para el parámetro *pguidTimeFormat* , use el \_ desplazamiento de segmento formato de hora MF de valor de GUID \_ \_ \_ . Este valor indica la búsqueda por desplazamiento del segmento. Para el parámetro *pvarStartPosition* , pase la dirección del **PROPVARIANT** creado en el paso anterior.

En el ejemplo de código siguiente se muestra cómo saltar al inicio de un segmento especificado en una secuencia.


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



Cuando la aplicación busca entre segmentos, la aplicación recibe varios eventos, ya que el origen del secuenciador finaliza el segmento actual y se prepara para reproducir el nuevo segmento. Dado que estos eventos se reciben de forma asincrónica, es difícil predecir la secuencia exacta de eventos. Estos eventos son los siguientes:

-   El origen del secuenciador envía un evento [MENewPresentation](menewpresentation.md) para el nuevo segmento al que se omite la sesión multimedia.

-   Cuando el origen del secuenciador finaliza el segmento activo, envía el evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) .
-   Después, el origen del secuenciador cancela la topología de predistribución. Esto produce los siguientes eventos para la topología cancelada:

    -   Evento [MESessionTopologyStatus](mesessiontopologystatus.md) con la \_ marca MF TOPOSTATUS \_ Ready.
    -   Evento [MESessionTopologyStatus](mesessiontopologystatus.md) con el marcador de origen de MF \_ TOPOSTATUS \_ iniciado \_ .
    -   Evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) con el atributo de [topología de origen de eventos MF \_ \_ \_ \_ cancelado](mf-event-source-topology-canceled-attribute.md) para indicar que el origen del secuenciador canceló la topología.

-   Después, el origen del secuenciador envía eventos para el nuevo segmento, incluidos varios eventos [MESessionTopologyStatus](mesessiontopologystatus.md) .
-   Si el nuevo segmento no es el último de la lista, el origen del secuenciador actualiza la lista de preplantación y genera otro [MENewPresentation](menewpresentation.md) para la nueva topología de predistribución. Para obtener información acerca de las topologías de la lista de preplantación, consulte [acerca del origen del secuenciador](about-the-sequencer-source.md).

Puede encontrar más detalles sobre los eventos enviados por el origen del secuenciador en el tema [eventos de origen de Sequencer](sequencer-source-events.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo crear una lista de reproducción](how-to-create-a-playlist.md)
</dt> <dt>

[Origen del secuenciador](sequencer-source.md)
</dt> </dl>

 

 



