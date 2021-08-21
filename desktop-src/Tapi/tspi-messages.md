---
description: Esta sección contiene una lista de los mensajes de la interfaz del proveedor de servicios de telefonía (TSPI).
ms.assetid: 3d8bf980-81d6-49db-954f-af72458365dc
title: Mensajes TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27aadfd1c39babb8f848a0553ede8efab968a08b3219f85ea8eab988bb3064bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118860503"
---
# <a name="tspi-messages"></a>Mensajes TSPI

Esta sección contiene una lista de los mensajes de la interfaz del proveedor de servicios de telefonía (TSPI). Estos mensajes se usan para notificar a TAPI la aparición de eventos asincrónicos que se producen de forma asincrónica dentro del proveedor de servicios. El proveedor de servicios pasa estos eventos a TAPI mediante una llamada a una función de devolución de llamada [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) o [**PHONEEVENT,**](/windows/desktop/api/tspi/nc-tspi-phoneevent) en función de si el proveedor de servicios informa de un evento en un dispositivo de línea, llamada o teléfono. El **procedimiento LINEEVENT** para notificar eventos que se producen en una línea o llamada se proporciona al proveedor de servicios en el momento en que se abre la línea con la [**función TSPI \_ lineOpen.**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) El **procedimiento PHONEEVENT** para notificar eventos que se producen en un teléfono se proporciona con la [**función TSPI \_ phoneOpen.**](/windows/win32/api/tspi/nf-tspi-tspi_phoneopen)

TapI no solicita estos eventos de provocación en el sentido de que no son una respuesta directa a ninguna solicitud. Estos eventos contrastan con los que informan de la finalización de las solicitudes realizadas por TAPI. Estos eventos de finalización se notifican a través de la función de devolución de [**llamada \_ ASYNC COMPLETION.**](/windows/win32/api/tspi/nc-tspi-async_completion)

Los perfiles de parámetro para los procedimientos de evento de regresión incluyen parámetros que identifican el objeto pertinente para el que se notifica el evento (teléfono, línea o llamada). La identificación tiene el formato de un controlador opaco cuya interpretación exacta no está publicada por TSPI. TAPI determina internamente la relación entre estos controladores opacos y las estructuras de datos que usó para representar los dispositivos.

El perfil de parámetro para los procedimientos de eventos escotes también incluye un parámetro de mensaje que identifica el tipo del mensaje. Cada tipo de mensaje tiene una definición correspondiente que determina los identificadores que se incluyen, junto con otros parámetros y sus significados. Hay una correspondencia muy fuerte entre los mensajes que aparecen en el nivel de TSPI y los que aparecen en el nivel TAPI. Estas son las reglas generales de correspondencia:

-   El conjunto de mensajes es casi idéntico. Donde se corresponden los mensajes, se usa el mismo nombre y valor de mensaje en el nivel de TSPI.
-   Los identificadores que aparecen en el nivel de TSPI son los tipos opacos definidos por la especificación de TSPI. Estos tipos (y su interpretación) difieren de los del nivel TAPI, aunque hacen referencia a la misma clase de dispositivo. Por ejemplo, cuando un mensaje TAPI incluye un identificador HLINE, el mensaje TSPI correspondiente normalmente incluiría un [**identificador HTAPILINE.**](htapiline.md)
-   No hay ningún *dato dwCallbackInstance* pasado a la devolución de llamada.
-   Los *parámetros dwParam1,* *dwParam2* y *dwParam3* suelen ser idénticos a los parámetros correspondientes para el mensaje TAPI.
-   Los mensajes orientados a líneas y orientados a llamadas se pasan a un procedimiento de devolución de llamada diferente al de los mensajes orientados al teléfono.

Para cada mensaje, en esta sección se enumeran los siguientes elementos:

-   El propósito del mensaje
-   Procedimiento de devolución de llamada al que se pasa este mensaje
-   Descripción de los parámetros del mensaje
-   Comentarios opcionales sobre el uso del mensaje
-   Referencias opcionales a otras funciones, mensajes y estructuras de datos
-   Comentarios opcionales que comparan este mensaje con la interfaz TAPI

Ciertos mensajes se usan para notificar a TAPI un cambio en el estado de un objeto. Estos mensajes proporcionan el identificador de objeto opaco TAPI y una indicación de qué elemento de estado ha cambiado. TAPI puede llamar posteriormente a una función "get status" adecuada del objeto para obtener el estado completo del objeto.

Cuando se produce un evento, se puede enviar o no un mensaje a TAPI. Para algunos tipos de eventos, como los cambios de estado, TAPI especifica un conjunto de cambios de estado en los que está interesado. Se recomienda al proveedor de servicios limitar los eventos de mensaje de cambio de estado que notifica a los incluidos en este conjunto. No es necesario que el proveedor de servicios cumpla este límite. En otras palabras, puede notificar más cambios de los estrictamente necesarios. Sin embargo, debe intentar observar el límite por motivos de rendimiento.

El mensaje \_ LINE REPLY no se usa en el nivel TSPI. La finalización de una solicitud asincrónica se notifica mediante la [**devolución de llamada \_ ASYNC COMPLETION.**](/windows/win32/api/tspi/nc-tspi-async_completion)

El mensaje \_ PHONE REPLY no se usa en el nivel TSPI. La finalización de una solicitud asincrónica se notifica mediante la [**devolución de llamada \_ ASYNC COMPLETION.**](/windows/win32/api/tspi/nc-tspi-async_completion)

Para obtener más información, consulte los siguientes temas:

-   [Mensajes de dispositivo de línea TSPI](tspi-line-device-messages.md)
-   [Mensajes de Teléfono de TSPI](tspi-phone-device-messages.md)

 

 
