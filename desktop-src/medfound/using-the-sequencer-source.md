---
description: En este tema se describe cómo usar el origen del secuenciador.
ms.assetid: 7ce8dc67-02b1-4fd4-9e4d-6614fdb40620
title: Usar el origen del secuenciador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b0607d65d02e507f576a5177ea432f3f7e0fab57c3b575fbb34240a46e91be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972734"
---
# <a name="using-the-sequencer-source"></a>Usar el origen del secuenciador

En este tema se describe cómo usar el [origen del secuenciador](sequencer-source.md). Contiene las secciones siguientes:

-   [Información general](#overview)
-   [Agregar topologías](#adding-topologies)
-   [Eliminación de topologías](#deleting-topologies)
-   [Omisión a un segmento](#skipping-to-a-segment)
-   [Temas relacionados](#related-topics)

Para obtener información general sobre el origen del secuenciador, vea [Acerca del origen del secuenciador.](about-the-sequencer-source.md)

## <a name="overview"></a>Información general

El origen del secuenciador expone las interfaces siguientes.



| Interfaz                                                                        | Descripción                                                                        |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                         | Expone la funcionalidad de origen multimedia genérico.                                        |
| [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)                                 | Permite que la aplicación agregue o quite topologías.                               |
| [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)         | Recupera la siguiente topología que se pone en cola en la sesión multimedia.                         |
| [**IMFMediaSourcePresentationProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider) | Usado por la sesión multimedia para los segmentos finales. Las aplicaciones no usan esta interfaz. |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                           | Consulta el origen del secuenciador para [interfaces de servicio.](service-interfaces.md)     |



 

Para reproducir una secuencia de orígenes multimedia, realice los pasos siguientes:

1.  Para crear el origen del secuenciador, llame a [**la función MFCreateSequencerSource.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource)
2.  Para cada segmento, cree una topología de reproducción, como se describe en [Creación de topologías de reproducción.](creating-playback-topologies.md) Para agregar la topología a la presentación, llame [**a IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).
3.  Antes de iniciar la reproducción, llame [**a IMFMediaSource::CreatePresentationDescriptor en**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) el origen del secuenciador. Este método devuelve un puntero a un descriptor de presentación para el primer segmento. Para obtener la topología asociada a este segmento, llame a **QueryInterface** en el origen del secuenciador para la interfaz [**IMFMediaSourceTopologyProvider.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) Pase el descriptor de presentación [**al método IMFMediaSourceTopologyProvider::GetMediaSourceTopology.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) Este método devuelve un puntero a la topología.
4.  Pase la topología para el primer segmento a la sesión de medios, llamando al método [**DEMEDIASession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) de la sesión multimedia.
5.  Inicie la reproducción mediante una llamada [**a IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).
6.  Cuando el origen del secuenciador está listo para preinscripción del segmento siguiente, envía un evento [MENewPresentation](menewpresentation.md) cuyos datos de evento son un puntero de interfaz [**IMFPresentationDescriptor.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) De nuevo, obtenga la topología del segmento llamando a [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) en el origen del secuenciador y establezca la topología en la sesión multimedia llamando a [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology). No es necesario volver a iniciar el origen multimedia; se reproducirá automáticamente en el segmento siguiente.
7.  Antes de que se cierre la aplicación, apague el origen del secuenciador mediante una llamada [**a IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).

El código siguiente muestra cómo obtener la topología y establecerla en la sesión multimedia:


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



Para obtener un ejemplo de código completo, vea [Código de ejemplo de origen del secuenciador](sequencer-source-example-code.md).

## <a name="adding-topologies"></a>Agregar topologías

El origen del secuenciador mantiene dos listas de topologías: la *lista de entrada* y la lista de inscripción *previa.*

La lista de entrada es una colección de topologías correspondientes a los segmentos de lista de reproducción, en el orden en que la aplicación las agregó mediante una llamada a [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology). Este método asigna a cada topología un identificador de *segmento único* del tipo **MFSequencerElementId**. El identificador de segmento se establece como un atributo para todos los nodos de topología de origen. Una aplicación puede obtener el identificador de segmento de un nodo de origen mediante el atributo [MF \_ TOPONODE \_ SEQUENCE \_ ELEMENTID.](mf-toponode-sequence-elementid-attribute.md) La lista de entrada puede tener topologías duplicadas si la aplicación llamó **a AppendTopology** en la misma topología más de una vez; sin embargo, se identifican por sus identificadores de segmento únicos.

La lista de inscripción previa es una colección de topologías de lista de entrada que se han inicializado como preparación para la reproducción. Esto permite a la sesión multimedia realizar la transición a la siguiente topología sin problemas cuando finaliza la topología activa. La aplicación no puede agregar ni quitar topologías directamente de la lista de inscripción previa; lo genera el origen del secuenciador cuando se selecciona una topología de la lista de entrada para la reproducción. Esto hace que el origen del secuenciador agregue la siguiente topología de la lista de entrada a la lista de inscripción previa. Después de hacerlo, el origen del secuenciador genera de forma asincrónica el evento [MENewPresentation](menewpresentation.md) y pasa el descriptor de presentación de la topología de inscripción previa como datos de evento. La aplicación debe escuchar este evento mediante la interfaz [**DELATORMEDIAEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) de la sesión multimedia y poner en cola la topología de inscripción previa en la sesión multimedia mediante una llamada a [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology). Esto debe hacerse antes de que la sesión multimedia complete la reproducción de la topología activa. **SetTopology informa** a la sesión multimedia sobre la siguiente topología que debe reproducir una vez finalizada la reproducción de la topología activa. Para garantizar una triplez sin problemas, la aplicación debe llamar a **SetTopology** antes de que la sesión multimedia finalice la reproducción de la topología anterior. De lo contrario, habrá una brecha entre los segmentos.

El [evento MENewPresentation](menewpresentation.md) se genera siempre que haya una topología después de la topología activa. Por lo tanto, si la lista de entrada contiene solo una topología o si la topología activa es la última de la lista de entrada, este evento no se genera.

La lista de inscripción previa se sincroniza con la lista de entrada y se actualiza cada vez que se agrega o elimina una topología de la lista de entrada.

## <a name="deleting-topologies"></a>Eliminación de topologías

Para quitar una topología del origen del secuenciador, una aplicación debe llamar al método [**IMFSequencerSource::D eleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) y especificar el identificador de segmento.

Antes de [**llamar a DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology), la aplicación debe asegurarse de que Media Session no usa la topología que la aplicación quiere eliminar. Para ello, deben producirse las dos acciones siguientes antes de que la aplicación llame **a DeleteTopology**:

-   Se recibe el evento [MESessionTopologyStatus](mesessiontopologystatus.md) con MF TOPOSTATUS ENDED para la topología a fin de asegurarse de que \_ la sesión multimedia ha completado la \_ reproducción.

-   [MESessionTopologyStatus](mesessiontopologystatus.md) con MF TOPOSTATUS STARTED SOURCE se recibe para la siguiente topología a fin de asegurarse de que la sesión multimedia ha empezado a reproducir la siguiente topología, se recibe el evento \_ \_ \_ [MESessionEnded](mesessionended.md) para asegurarse de que la sesión multimedia se realiza con la última topología en el origen del secuenciador.

Si el segmento que se elimina es la topología activa, la reproducción se detiene y el origen del secuenciador genera el [evento MEEndOfPresentationSegment.](meendofpresentationsegment.md) Si la topología activa también es la última topología, se genera el evento [MEEndOfPresentation.](meendofpresentation.md)

## <a name="skipping-to-a-segment"></a>Omisión a un segmento

Una aplicación puede ir directamente a un segmento determinado de la secuencia iniciando la [sesión multimedia](media-session.md) con un desplazamiento de segmento, como se muestra a continuación:

1.  Llame a [**la función MFCreateSequencerSegmentOffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) para crear el desplazamiento del segmento. Especifique el identificador del segmento en el *parámetro dwId.* (El método [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) devolvió el identificador cuando agregó por primera vez la topología al origen del secuenciador). El *parámetro hnsOffset* especifica un desplazamiento de tiempo, en relación con el inicio del segmento. La reproducción se iniciará en este momento. Para el *parámetro pvarSegmentOffset,* pase la dirección de un **elemento PROPVARIANT vacío.** Cuando la función devuelve un resultado, **este VALOR PROPVARIANT** contiene el desplazamiento del segmento.

2.  Llame al [**método IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) en la sesión multimedia. Para el *parámetro pguidTimeFormat,* use el valor GUID MF \_ TIME FORMAT SEGMENT \_ \_ \_ OFFSET. Este valor indica la búsqueda por desplazamiento de segmento. Para el *parámetro pvarStartPosition,* pase la dirección del **PROPVARIANT** creado en el paso anterior.

En el ejemplo de código siguiente se muestra cómo ir al principio de un segmento especificado en una secuencia.


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



Cuando la aplicación busca entre segmentos, la aplicación recibe varios eventos cuando el origen del secuenciador finaliza el segmento actual y se prepara para reproducir el nuevo segmento. Dado que estos eventos se reciben de forma asincrónica, es difícil predecir la secuencia exacta de eventos. Estos eventos son los siguientes:

-   El origen del secuenciador envía un [evento MENewPresentation](menewpresentation.md) para el nuevo segmento al que se omite la sesión multimedia.

-   Cuando el origen del secuenciador finaliza el segmento activo, envía el [evento MEEndOfPresentationSegment.](meendofpresentationsegment.md)
-   A continuación, el origen del secuenciador cancela la topología de inscripción previa. Esto da como resultado los siguientes eventos para la topología cancelada:

    -   [Evento MESessionTopologyStatus](mesessiontopologystatus.md) con la marca MF \_ TOPOSTATUS \_ READY.
    -   [Evento MESessionTopologyStatus](mesessiontopologystatus.md) con la marca MF \_ TOPOSTATUS \_ STARTED \_ SOURCE.
    -   [Evento MEEndOfPresentationSegment](meendofpresentationsegment.md) con el atributo [MF EVENT SOURCE \_ \_ \_ TOPOLOGY \_ CANCELED](mf-event-source-topology-canceled-attribute.md) para indicar que el origen del secuenciador canceló la topología.

-   A continuación, el origen del secuenciador envía eventos para el nuevo segmento, incluidos [varios eventos MESessionTopologyStatus.](mesessiontopologystatus.md)
-   Si el nuevo segmento no es el último de la lista, el origen del secuenciador actualiza la lista de inscripción previa y genera otra [menewpresentation](menewpresentation.md) para la nueva topología de inscripción previa. Para obtener información sobre las topologías de la lista de inscripción previa, vea [Acerca del origen del secuenciador.](about-the-sequencer-source.md)

Puede encontrar más detalles sobre los eventos enviados por el origen del secuenciador en el tema [Sequencer Source Events](sequencer-source-events.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo crear una lista de reproducción](how-to-create-a-playlist.md)
</dt> <dt>

[Origen del secuenciador](sequencer-source.md)
</dt> </dl>

 

 



