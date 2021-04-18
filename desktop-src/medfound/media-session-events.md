---
description: Eventos de sesión multimedia
ms.assetid: 882a01f2-8f5c-4640-a8ac-f4f5860d7ed1
title: Eventos de sesión multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e128fc5e11f70fe47d02356ce44629b98bfdfe
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717377"
---
# <a name="media-session-events"></a>Eventos de sesión multimedia

La mayoría de las operaciones de la sesión multimedia se realizan de forma asincrónica, por lo que la aplicación debe escuchar eventos mediante la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) de la sesión multimedia. (La interfaz [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) hereda **IMFMediaEventGenerator**). La secuencia exacta de eventos dependerá de la aplicación, pero la sesión multimedia genera los siguientes eventos en casi cualquier situación.



| Evento                                                                  | Descripción                                                                                                                                                                                                                    |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MEEndOfPresentation](meendofpresentation.md)                         | Se genera cuando el origen multimedia ha completado la presentación. En este momento, es posible que los datos sigan en movimiento a través de la canalización.                                                                                                     |
| [MEError](meerror.md)                                                 | Se produce si se produce un error durante el streaming.                                                                                                                                                                                    |
| [MESessionClosed](mesessionclosed.md)                                 | Se genera cuando se completa el método [**Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) . Este evento es el último evento que la sesión multimedia pone en cola. Después de recibir este evento, es seguro apagar los orígenes multimedia que haya creado. |
| [MESessionEnded](mesessionended.md)                                   | Se genera cuando la sesión multimedia se realiza con la última presentación.                                                                                                                                                              |
| [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) | Notifica a la aplicación el tiempo de presentación en el que se iniciará la nueva presentación.                                                                                                                                        |
| [MESessionStarted](mesessionstarted.md)                               | Se genera cuando se completa el método de [**Inicio**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) . A menos que se produzca un error, los datos se mueven a través de la canalización en este momento.                                                                          |
| [MESessionTopologySet](mesessiontopologyset.md)                       | Se genera cuando se completa el método [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) . A menos que se produzca un error, la aplicación no tiene que realizar ninguna acción.                                                                 |
| [MESessionTopologyStatus](mesessiontopologystatus.md)                 | Se produce en varias ocasiones en que cambia el estado de una topología.                                                                                                                                                                 |



 

El método [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) no genera un evento. El método **Shutdown** es sincrónico. Una vez que este método devuelve, es seguro liberar el puntero de devolución de llamada de evento.

Además de los eventos de la sesión multimedia, la aplicación puede recibir eventos de los receptores de medios en la topología. Estos pueden ser eventos personalizados definidos por el receptor de medios, que podrían contener datos arbitrarios. Por ejemplo, el receptor podría derivar los datos de evento de los datos de origen, que pueden proceder de un origen externo que no es de confianza. Una aplicación debe omitir los eventos que no reconozca y tener cuidado al analizar los datos de eventos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión de medios](media-session.md)
</dt> </dl>

 

 



