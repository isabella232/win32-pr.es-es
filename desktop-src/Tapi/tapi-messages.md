---
description: Los mensajes se utilizan para notificar a la aplicación de eventos asincrónicos. Todos estos mensajes se envían a la aplicación a través del mecanismo de notificación de mensajes que la aplicación especificó en lineInitializeEx.
ms.assetid: d302819e-c522-470a-be5e-52625c9223a4
title: Mensajes TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58307a0230b76c6ad98c57f4590098f0dcf6b236
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688134"
---
# <a name="tapi-messages"></a>Mensajes TAPI

Los mensajes se utilizan para notificar a la aplicación de eventos asincrónicos. Todos estos mensajes se envían a la aplicación a través del mecanismo de notificación de mensajes que la aplicación especificó en [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).

El mensaje siempre contiene un identificador para el objeto pertinente (teléfono, línea o llamada), que la aplicación puede usar para determinar el tipo de mensaje.

Algunos mensajes se utilizan para notificar a la aplicación sobre un cambio en el estado de un objeto. Estos mensajes proporcionan el identificador de objeto y proporcionan una indicación de qué elemento de Estado ha cambiado. La aplicación puede llamar a la función "get status" correspondiente del objeto para obtener el estado completo del objeto.

Cuando se produce un evento, los mensajes se pueden enviar a cero, una o más aplicaciones. Las aplicaciones de destino para un mensaje se determinan mediante una serie de factores diferentes, incluido el significado del mensaje, el privilegio de la aplicación en el objeto, si la aplicación inició o no la solicitud para la que el mensaje es un resultado directo y el enmascaramiento de mensajes que ha establecido la aplicación. Tenga en cuenta los siguientes puntos acerca de los mensajes:

-   Los mensajes de respuesta asincrónica solo se envían a la aplicación que originó la solicitud y no se pueden enmascarar.
-   Los mensajes que señalan la finalización de la generación de dígitos o de tono o la recopilación de dígitos solo se envían a la aplicación que solicitó la generación de dígitos o tono.
-   Los mensajes que indican que los cambios de estado de línea o dirección se envían a todas las aplicaciones que han abierto la línea, siempre y cuando el mensaje se haya habilitado a través de [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).
-   Los mensajes que indican el estado de la llamada y los cambios de la información de llamada se envían a todas las aplicaciones que tienen un identificador a la llamada.
-   Los mensajes que señalan una detección de dígitos, detección de tono o detección de tipo de medio se envían a las aplicaciones que solicitaron la supervisión de ese evento.

Esta sección contiene la información de referencia para los siguientes mensajes TAPI:

-   [Mensajes de telefonía asistidos](assisted-telephony-messages.md)
-   [Mensajes del centro de llamadas](call-center-messages.md)
-   [Mensajes de error con formato](formatted-error-messages.md)
-   [Mensajes de dispositivo de línea](line-device-messages.md)
-   [Mensajes de dispositivo telefónico](phone-device-messages.md)

 

 



