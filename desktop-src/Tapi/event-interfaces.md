---
description: Las interfaces de evento (notificación) permiten que una aplicación TAPI 3 responda a eventos asincrónicos.
ms.assetid: 27fd91e8-b628-49ee-af4e-9aec0afa5449
title: Interfaces de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a4ecf097d761e98b723b37d9de6adcfd7ebb60696ce5e389426965534d63f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660845"
---
# <a name="event-interfaces"></a>Interfaces de eventos

Las interfaces de evento (notificación) permiten que una aplicación TAPI 3 responda a eventos asincrónicos.

Debe llamar al método [**\_ EVENTFilter ITTAPI::p ut**](/windows/win32/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) y establecer una máscara de filtro de eventos para habilitar la recepción de eventos de solicitud. Si no llama a **ITTAPI::p ut \_ EventFilter**, la aplicación no recibirá ningún evento.

Consulte información general [sobre eventos](./asynchronous-spontaneous-events.md) para obtener una descripción de cómo una aplicación garantiza la recepción de notificaciones. Consulte las interfaces individuales enumeradas en la tabla siguiente para obtener más información sobre cómo establecer una máscara de filtro para tipos de eventos individuales.



| Interfaz                                                           | Descripción                                                                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITAddressEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itaddressevent)                   | Recupera la descripción de los eventos de dirección.                                                                                                |
| [**ITASRTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itasrterminalevent)           | Recupera la descripción de los eventos del terminal de reconocimiento automático de voz.                                                                  |
| [**ITCallHubEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallhubevent)                   | Recupera la descripción de los eventos de CallHub.                                                                                                |
| [**ITCallInfoChangeEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallinfochangeevent)     | Recupera la descripción de los eventos de cambio de información de llamada.                                                                                |
| [**ITCallMediaEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallmediaevent)               | Recupera la descripción de los eventos multimedia de llamada.                                                                                             |
| [**ITCallNotificationEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallnotificationevent) | Recupera la descripción de los eventos de notificación de llamadas.                                                                                      |
| [**ITCallStateEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallstateevent)               | Recupera la descripción de los eventos de estado de llamada.                                                                                             |
| [**ITDigitDetectionEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitdetectionevent)     | Recupera información sobre los eventos de dígitos dtmf durante una llamada.                                                                                |
| [**ITDigitGenerationEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitgenerationevent)   | Recupera información sobre las llamadas que requieren la generación de dígitos DTMF.                                                               |
| [**ITDigitsGatheredEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitsgatheredevent)     | Recupera los datos relacionados con la solicitud de recopilación de dígitos de una aplicación.                                                                         |
| [**ITFileTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itfileterminalevent)         | Recupera la descripción de los eventos de terminal de archivo.                                                                                          |
| [**ITParticipantEvent**](./itparticipantevent.md)           | Recupera la descripción de los eventos de participantes de la conferencia.                                                                                 |
| [**ITPhoneEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itphoneevent)                       | Recupera la descripción de los eventos de teléfono.                                                                                                  |
| [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)                           | Recupera la descripción de los eventos de calidad de servicio (QOS).                                                                               |
| [**ITQueueEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueueevent)                       | Recupera la descripción de los eventos de cola de distribución automática de llamadas (ACD).                                                                |
| [**ITRequestEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itrequestevent)                   | Recupera la descripción de los eventos [de solicitud de telefonía asistida.](./assisted-telephony-overview.md)                                 |
| [**ITTAPIObjectEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | Recupera la descripción de los eventos del objeto TAPI.                                                                                            |
| [**ITTAPIObjectEvent2**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | Extiende [**ITTAPIObjectEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent); recupera un puntero al objeto de teléfono que produjo el evento de objeto TAPI. |
| [**ITToneDetectionEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittonedetectionevent)       | Recupera información sobre un evento de detección de tono.                                                                                         |
| [**ITToneTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittoneterminalevent)         | Recupera la descripción de los eventos de terminal de tono.                                                                                          |
| [**ITTTSTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itttsterminalevent)           | Recupera la descripción de los eventos de terminal de texto a voz (TTS).                                                                          |



 



| Interfaz                                                                                             | Descripción                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**ITPluggableTerminalEventSink**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsink)                         | Notifica a las aplicaciones cliente los cambios en un terminal conectable.                              |
| [**ITPluggableTerminalEventSinkRegistration**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsinkregistration) | Registra y anula el registro de una aplicación cliente para recibir notificaciones sobre eventos de terminal conectables. |



 

 

 
