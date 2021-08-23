---
description: Eventos de sesión multimedia
ms.assetid: 882a01f2-8f5c-4640-a8ac-f4f5860d7ed1
title: Eventos de sesión multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bffecb3f4e3f4b3a3b30be95fcc45adcb81c1a84dd04ed8cf637bad759512a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724015"
---
# <a name="media-session-events"></a>Eventos de sesión multimedia

La mayoría de las operaciones de la sesión multimedia se realizan de forma asincrónica, por lo que la aplicación debe escuchar eventos mediante la interfaz [**DESMEDIAEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) de la sesión multimedia. (La [**interfaz IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) hereda **ELERMEDIAEVENTGenerator).** La secuencia exacta de eventos dependerá de la aplicación, pero la sesión multimedia genera los siguientes eventos en casi cualquier situación.



| Evento                                                                  | Descripción                                                                                                                                                                                                                    |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MEEndOfPresentation](meendofpresentation.md)                         | Se genera cuando el origen multimedia ha completado la presentación. En este momento, es posible que los datos se muevan a través de la canalización.                                                                                                     |
| [MEError](meerror.md)                                                 | Se genera si se produce un error durante el streaming.                                                                                                                                                                                    |
| [MESessionClosed](mesessionclosed.md)                                 | Se genera cuando se [**completa**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) el método Close. Este evento es el último evento que la sesión multimedia pone en cola. Después de recibir este evento, es seguro apagar los orígenes multimedia que haya creado. |
| [MESessionEnded](mesessionended.md)                                   | Se genera cuando la sesión multimedia se realiza con la última presentación.                                                                                                                                                              |
| [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) | Notifica a la aplicación la hora de presentación en la que se iniciará la nueva presentación.                                                                                                                                        |
| [MESessionStarted](mesessionstarted.md)                               | Se genera cuando se [**completa**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) el método Start. A menos que se haya producido un error, los datos se mueven a través de la canalización en este momento.                                                                          |
| [MESessionTopologySet](mesessiontopologyset.md)                       | Se genera cuando se completa el método [**SetTopology.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) A menos que se produzca un error, la aplicación no necesita realizar ninguna acción.                                                                 |
| [MESessionTopologyStatus](mesessiontopologystatus.md)                 | Se genera en varias ocasiones cuando cambia el estado de una topología.                                                                                                                                                                 |



 

El [**método IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) no genera un evento. El **método Shutdown** es sincrónico. Una vez que este método vuelve, es seguro liberar el puntero de devolución de llamada de eventos.

Además de los eventos de la sesión multimedia, la aplicación podría recibir eventos de los receptores de medios en la topología. Pueden ser eventos personalizados definidos por el receptor de medios, que pueden contener datos arbitrarios. Por ejemplo, el receptor podría derivar los datos de evento de los datos de origen, que pueden ser de un origen externo que no es de confianza. Una aplicación debe omitir los eventos que no reconoce y tener cuidado al analizar los datos de eventos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión multimedia](media-session.md)
</dt> </dl>

 

 



