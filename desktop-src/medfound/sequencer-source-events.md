---
description: Eventos de origen del secuenciador
ms.assetid: 28654bae-9ce2-467b-b769-63279d69b173
title: Eventos de origen del secuenciador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf97cc5ff25c8a5fc40fa4990bf38c652f94e63
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363715"
---
# <a name="sequencer-source-events"></a>Eventos de origen del secuenciador

Cuando [el origen del secuenciador](sequencer-source.md) reproduce una secuencia de archivos, la sesión multimedia generalmente envía todos los mismos eventos que se envían durante la reproducción normal y que aparecen en Eventos de sesión [multimedia](media-session-events.md). La aplicación obtiene estos eventos mediante la interfaz [**DEDAMEDIAEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) de la sesión multimedia.

Además, hay algunos eventos que son específicos de los segmentos de lista de reproducción.



| Evento                                                                                                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MENewPresentation](menewpresentation.md)                                                              | Indica a la aplicación que preselecte la topología siguiente.<br/> Para proporcionar una transición sin problemas entre dos presentaciones consecutivas, el origen del secuenciador carga la siguiente topología de antemano. Mientras se sigue reproduciendo la topología activa, el origen del secuenciador envía este evento para la siguiente topología, siempre y cuando haya una topología posterior disponible en el origen.<br/> Estos datos de evento para este evento son el descriptor de presentación de la topología siguiente. La aplicación es responsable de establecer la topología correspondiente en la sesión multimedia, como se describe en [Uso del origen del secuenciador](using-the-sequencer-source.md).<br/> |
| [MEEndOfPresentationSegment](meendofpresentationsegment.md)                                            | El origen del secuenciador genera este evento cuando la sesión multimedia ha completado la reproducción del segmento actual, si ese segmento va seguido de otro segmento. (Si el segmento actual es el último, el origen del secuenciador genera el [evento MEEndOfPresentation](meendofpresentation.md) en su lugar).<br/> La sesión multimedia reenvía este evento a la aplicación. Normalmente, la aplicación recibe [MEEndOfPresentationSegment](meendofpresentationsegment.md) después de que la sesión multimedia haya empezado a procesar el siguiente segmento, pero mientras los receptores multimedia siguen entregando los ejemplos del segmento anterior.<br/>                            |
| [MESessionTopologyStatus](mesessiontopologystatus.md), con el estado **MF \_ TOPOSTATUS \_ SINK \_ SWITCHED**. | La sesión multimedia genera este evento cuando realiza una transición a la siguiente topología en el origen del secuenciador y los receptores multimedia han completado la reproducción de la topología anterior. Este evento contiene un puntero a la topología siguiente.                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="example-1-playback-without-skipping"></a>Ejemplo 1: Reproducción sin omitir

Cuando el origen del secuenciador está implicado, el número de eventos que obtiene de la sesión multimedia puede resultar confuso, especialmente porque los eventos asociados a un segmento a menudo se intercalan con eventos para el segmento siguiente.

En el primer ejemplo, la aplicación pone en cola tres segmentos, S1, S2 y S3. El tercer segmento tiene **la marca SequencerTopologyFlags \_ Last,** para indicar que es el último segmento de la secuencia. El segmento al que se corresponde cada evento se da entre paréntesis. También se enumeran las [**llamadas SetTopology de**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) la aplicación para que el orden de las operaciones sea más claro.

-   La aplicación [**llama a IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S1)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ READY** (S1)
-   [MENewPresentation](menewpresentation.md) (inscripción previa de S2)
-   La aplicación [**llama a IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ STARTED \_ SOURCE** (inicio de S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S2)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (final de S1)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ ENDED** (S1)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ SINK \_ SWITCHED** (transición a S2)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ READY** (S2)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ STARTED \_ SOURCE** (inicio de S2)
-   [MENewPresentation](menewpresentation.md) (inscripción previa S3)
-   La aplicación [**llama a IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [MESessionTopologySet](mesessiontopologyset.md) (S3)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (final de S2)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ ENDED** (S2)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ SINK \_ SWITCHED** (transición a S3)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ READY** (S3)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ STARTED \_ SOURCE** (inicio de S3)
-   [MEEndOfPresentation](meendofpresentation.md) (final de S3; último segmento)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ ENDED**
-   [MESessionEnded](mesessionended.md)

Esta lista no incluye todos los eventos que pueda recibir. (Por ejemplo, omite el evento [MESessionCapabilitiesChanged,](mesessioncapabilitieschanged.md) que se envía cada vez que cambian las funcionalidades de sesión. Normalmente, una aplicación recibe varios eventos MESessionCapabilitiesChanged a lo largo de una presentación). Los eventos enumerados aquí son los que muestran la transición de un segmento al siguiente. Los eventos más importantes son [MENewPresentation](menewpresentation.md), que indica a la aplicación que preseleccione la topología siguiente, y [MEEndOfPresentationSegment](meendofpresentationsegment.md), que señala el final de un segmento (excepto el último segmento).

Dado que los eventos Media Foundation son asincrónicos y no se serializan con llamadas a métodos, el orden exacto puede variar. Por ejemplo, podría recibir **MF \_ TOPOSTATUS \_ STARTED \_ SOURCE** para S1 antes de que la aplicación llame a [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para S2.

Además, es posible que no aparezcan todos los eventos aquí. Los [eventos MEEndOfPresentation](meendofpresentation.md) y [MESessionEnded,](mesessionended.md) por ejemplo, no se envían a menos que el último segmento tenga la marca **SequencerTopologyFlags \_ Last.**

Por último, esta lista no indica el paso del tiempo. El tiempo desde "inicio de S1" hasta "final de S1" es la duración completa de S1, que podría ser de unos segundos o muchas horas, dependiendo del origen.

## <a name="example-2-playback-with-segment-skipping"></a>Ejemplo 2: Reproducción con omisión de segmento

En este ejemplo, la aplicación pone en cola los mismos segmentos, pero omite el segmento 3 mientras se reproduce el segmento 1. En este caso, se envían los siguientes eventos:

-   La aplicación [**llama a IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S1)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ READY** (S1)
-   [MENewPresentation](menewpresentation.md) (inscripción previa de S2)
-   La aplicación [**llama a IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ STARTED \_ SOURCE** (inicio de S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S2)
-   La aplicación [**llama a IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) (vaya directamente a S3)
-   [MENewPresentation](menewpresentation.md) (inscripción previa S3)
-   La aplicación [**llama a IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S3)
-   [MESessionStarted](mesessionstarted.md)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (S1 cancelado)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ ENDED** (S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S3)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ SINK \_ SWITCHED** (transición a S2)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ READY** (S2)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ STARTED \_ SOURCE** (S2)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (S2 cancelado)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ ENDED** (S2)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ SINK \_ SWITCHED** (transición a S3)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **TOPOSTATUS \_ READY** (S3)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ STARTED \_ SOURCE** (S3)

Cuando la aplicación llama [**a Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) para pasar al segmento 3, el origen del secuenciador cancela el segmento 1, que sigue reproduciendo. El [evento MEEndOfPresentationSegment](meendofpresentationsegment.md) de este segmento contiene el atributo [**MF EVENT SOURCE \_ \_ \_ TOPOLOGY \_ CANCELED,**](mf-event-source-topology-canceled-attribute.md) que indica que el segmento finalizó porque se canceló. A continuación, dado que el segmento 2 ya está preconfigurado, ese segmento se inicia pero, a continuación, se cancela inmediatamente. El evento MEEndOfPresentationSegment para el segmento 2 también contiene el atributo **MF \_ EVENT SOURCE \_ \_ TOPOLOGY \_ CANCELED.** Después, la sesión puede cambiar al segmento 3 y reproducirla con normalidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del origen del secuenciador](about-the-sequencer-source.md)
</dt> <dt>

[Origen del secuenciador](sequencer-source.md)
</dt> </dl>

 

 




