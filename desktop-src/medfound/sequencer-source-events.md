---
description: Eventos de origen de Sequencer
ms.assetid: 28654bae-9ce2-467b-b769-63279d69b173
title: Eventos de origen de Sequencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf97cc5ff25c8a5fc40fa4990bf38c652f94e63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677553"
---
# <a name="sequencer-source-events"></a>Eventos de origen de Sequencer

Cuando el [origen del secuenciador](sequencer-source.md) reproduce una secuencia de archivos, la sesión multimedia envía normalmente todos los mismos eventos que se envían durante la reproducción normal y que se enumeran en [los eventos de la sesión multimedia](media-session-events.md). La aplicación obtiene estos eventos mediante la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) de la sesión multimedia.

Además, hay algunos eventos que son específicos de los segmentos de lista de reproducción.



| Evento                                                                                                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MENewPresentation](menewpresentation.md)                                                              | Indica a la aplicación que previerta la siguiente topología.<br/> Para proporcionar una transición sin problemas entre dos presentaciones consecutivas, el origen del secuenciador carga la siguiente topología de antemano. Mientras se sigue reproduciendo la topología activa, el origen del secuenciador envía este evento para la topología siguiente, siempre y cuando haya una topología posterior disponible en el origen.<br/> Estos datos de eventos para este evento son el descriptor de presentación de la siguiente topología. La aplicación es responsable de establecer la topología correspondiente en la sesión multimedia, tal como se describe en [uso del origen del secuenciador](using-the-sequencer-source.md).<br/> |
| [MEEndOfPresentationSegment](meendofpresentationsegment.md)                                            | El origen del secuenciador genera este evento cuando la sesión multimedia ha finalizado la reproducción del segmento actual, si ese segmento va seguido de otro segmento. (Si el segmento actual es el último, el origen del secuenciador genera el evento [MEEndOfPresentation](meendofpresentation.md) en su lugar).<br/> La sesión multimedia reenvía este evento a la aplicación. Normalmente, la aplicación recibe [MEEndOfPresentationSegment](meendofpresentationsegment.md) después de que la sesión multimedia haya empezado a procesar el segmento siguiente, pero mientras los receptores de medios sigan ofreciendo los ejemplos del segmento anterior.<br/>                            |
| [MESessionTopologyStatus](mesessiontopologystatus.md), con estado **MF \_ TOPOSTATUS \_ receptor \_ cambiado**. | La sesión multimedia genera este evento cuando realiza una transición a la topología siguiente en el origen del secuenciador y los receptores de medios han completado la reproducción de la topología anterior. Este evento contiene un puntero a la topología siguiente.                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="example-1-playback-without-skipping"></a>Ejemplo 1: reproducción sin omitir

Cuando el origen del secuenciador está implicado, el número de eventos que obtiene de la sesión de medios puede ser confuso, especialmente porque los eventos asociados a un segmento se intercalan a menudo con eventos para el siguiente segmento.

En el primer ejemplo, la aplicación pone en cola tres segmentos, S1, S2 y S3. El tercer segmento tiene la **\_ última marca SequencerTopologyFlags** para indicar que es el último segmento de la secuencia. El segmento al que corresponde cada evento se indica entre paréntesis. También se enumeran las llamadas a [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) de la aplicación para que el orden de las operaciones sea más claro.

-   La aplicación llama a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S1)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S1)
-   [MENewPresentation](menewpresentation.md) (preroll S2)
-   La aplicación llama a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ \_** inicio de origen (inicio de S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S2)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (final de S1)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ finalizó** (S1)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ receptor \_ cambiado** (transición a S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ \_** inicio de origen (inicio de S2)
-   [MENewPresentation](menewpresentation.md) (preroll S3)
-   La aplicación llama a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [MESessionTopologySet](mesessiontopologyset.md) (S3)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (final de S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ finalizó** (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ receptor \_ cambiado** (transición a S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ inició el \_ origen** (inicio de S3)
-   [MEEndOfPresentation](meendofpresentation.md) (final de S3; último segmento)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ finalizó**
-   [MESessionEnded](mesessionended.md)

Esta lista no incluye todos los eventos que puede recibir. (Por ejemplo, omite el evento [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) , que se envía cada vez que cambian las capacidades de la sesión. Normalmente, una aplicación recibe varios eventos MESessionCapabilitiesChanged a lo largo de una presentación). Los eventos que se muestran aquí son los que muestran la transición de un segmento al siguiente. Los eventos más importantes son [MENewPresentation](menewpresentation.md), que indica a la aplicación que previerta la siguiente topología y [MEEndOfPresentationSegment](meendofpresentationsegment.md), que indica el final de un segmento (excepto el último segmento).

Dado que los eventos de Media Foundation son asincrónicos y no se serializan con llamadas a métodos, el orden exacto podría variar. Por ejemplo, podría recibir el **\_ \_ \_ código fuente MF TOPOSTATUS iniciado** para S1 antes de que la aplicación llame a [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para S2.

Además, es posible que no obtenga todos los eventos que se muestran aquí. Los eventos [MEEndOfPresentation](meendofpresentation.md) y [MESessionEnded](mesessionended.md) , por ejemplo, no se envían a menos que el último segmento tenga la marca **SequencerTopologyFlags \_ Last** .

Por último, esta lista no indica el paso del tiempo. El tiempo desde el "Inicio de S1" hasta el "final de S1" es la duración total de S1, que puede ser unos segundos o varias horas, dependiendo del origen.

## <a name="example-2-playback-with-segment-skipping"></a>Ejemplo 2: reproducción con omisión de segmentos

En este ejemplo, la aplicación pone en cola los mismos segmentos, pero salta al segmento 3 mientras se reproduce el segmento 1. En este caso, se envían los siguientes eventos:

-   La aplicación llama a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S1)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S1)
-   [MENewPresentation](menewpresentation.md) (preroll S2)
-   La aplicación llama a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ \_** inicio de origen (inicio de S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S2)
-   La aplicación llama a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) (saltar a S3)
-   [MENewPresentation](menewpresentation.md) (preroll S3)
-   La aplicación llama a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S3)
-   [MESessionStarted](mesessionstarted.md)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (S1 cancelado)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ finalizó** (S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ receptor \_ cambiado** (transición a S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ de \_ origen iniciado** (S2)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (S2 cancelado)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ finalizó** (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ receptor \_ cambiado** (transición a S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **TOPOSTATUS \_ Ready** (S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ de \_ origen iniciado** (S3)

Cuando la aplicación llama a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) para saltar al segmento 3, el origen del secuenciador cancela el segmento 1, que todavía se está reproduciendo. El evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) para este segmento contiene el atributo de la [**topología de origen de eventos MF \_ \_ \_ \_ cancelado**](mf-event-source-topology-canceled-attribute.md) , que indica que el segmento finalizó porque se canceló. Después, dado que el segmento 2 ya está previamente sobrecargado, ese segmento se inicia pero se cancela inmediatamente. El evento MEEndOfPresentationSegment para el segmento 2 también contiene el atributo **MF de topología de \_ \_ origen \_ \_ de eventos** . A continuación, la sesión puede cambiar al segmento 3 y reproducirla con normalidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del origen del secuenciador](about-the-sequencer-source.md)
</dt> <dt>

[Origen del secuenciador](sequencer-source.md)
</dt> </dl>

 

 




