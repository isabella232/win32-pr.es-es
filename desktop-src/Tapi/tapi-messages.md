---
description: Los mensajes se usan para notificar a la aplicación de eventos asincrónicos. Todos estos mensajes se envían a la aplicación a través del mecanismo de notificación de mensajes que la aplicación especificó en lineInitializeEx.
ms.assetid: d302819e-c522-470a-be5e-52625c9223a4
title: Mensajes TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd0a73a5ed845901d3cbe937a366a357c149541e8973a423310345dc241b92d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002733"
---
# <a name="tapi-messages"></a>Mensajes TAPI

Los mensajes se usan para notificar a la aplicación de eventos asincrónicos. Todos estos mensajes se envían a la aplicación a través del mecanismo de notificación de mensajes que la aplicación especificó [**en lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).

El mensaje siempre contiene un identificador para el objeto pertinente (teléfono, línea o llamada), que la aplicación puede usar para determinar el tipo de mensaje.

Determinados mensajes se usan para notificar a la aplicación sobre un cambio en el estado de un objeto. Estos mensajes proporcionan el identificador de objeto y proporcionan una indicación de qué elemento de estado ha cambiado. La aplicación puede llamar a la función "get status" adecuada del objeto para obtener el estado completo del objeto.

Cuando se produce un evento, los mensajes se pueden enviar a cero, una o varias aplicaciones. Las aplicaciones de destino para un mensaje están determinadas por una serie de factores diferentes, incluido el significado del mensaje, el privilegio de la aplicación para el objeto, si la aplicación inició o no la solicitud para la que el mensaje es un resultado directo y el enmascaramiento de mensajes establecido por la aplicación. Tenga en cuenta los siguientes puntos sobre los mensajes:

-   Los mensajes de respuesta asincrónicos solo se envían a la aplicación que originó la solicitud y no se pueden enmascarar.
-   Los mensajes que señalan la finalización de la generación de dígitos o tono o la recopilación de dígitos solo se envían a la aplicación que solicitó la generación de dígitos o tono.
-   Los mensajes que indican cambios de estado de línea o dirección se envían a todas las aplicaciones que han abierto la línea, siempre y cuando el mensaje se haya habilitado a través [**de lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).
-   Los mensajes que indican el estado de la llamada y los cambios en la información de llamada se envían a todas las aplicaciones que tienen un identificador para la llamada.
-   Los mensajes que señalan una detección de dígitos, la detección de tono o la detección de tipos de medios se envían a las aplicaciones que solicitaron la supervisión de ese evento.

Esta sección contiene la información de referencia de los siguientes mensajes TAPI:

-   [Mensajes de telefonía asistida](assisted-telephony-messages.md)
-   [Mensajes del centro de llamadas](call-center-messages.md)
-   [Mensajes de error con formato](formatted-error-messages.md)
-   [Mensajes de dispositivo de línea](line-device-messages.md)
-   [Teléfono Mensajes de dispositivo](phone-device-messages.md)

 

 



