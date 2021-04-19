---
description: Esta sección contiene una lista de los mensajes de la interfaz del proveedor de servicios de telefonía (TSPI).
ms.assetid: 3d8bf980-81d6-49db-954f-af72458365dc
title: Mensajes TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5772a1ccb0c07f03b2a17348ecf5e4834bb97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678349"
---
# <a name="tspi-messages"></a>Mensajes TSPI

Esta sección contiene una lista de los mensajes de la interfaz del proveedor de servicios de telefonía (TSPI). Estos mensajes se utilizan para notificar a TAPI la aparición de eventos asincrónicos que se producen espontáneamente en el proveedor de servicios. El proveedor de servicios pasa estos eventos a TAPI mediante una llamada a una función de devolución de llamada [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) o [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) , en función de si el proveedor de servicios informa de un evento en una línea, una llamada o un dispositivo telefónico. El procedimiento **LINEEVENT** para notificar eventos que se producen en una línea o llamada se proporciona al proveedor de servicios en el momento en que se abre la línea con la función [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) . El procedimiento **PHONEEVENT** para notificar eventos que se producen en un teléfono se suministra con la función [**TSPI \_ phoneOpen**](/windows/win32/api/tspi/nf-tspi-tspi_phoneopen) .

TAPI no solicita estos eventos espontáneos en el sentido de que no son una respuesta directa a ninguna solicitud. Estos eventos contrastan con los informes de finalización de las solicitudes realizadas por TAPI. Estos eventos de finalización se registran a través de la función de devolución de llamada de [**\_ finalización asincrónica**](/windows/win32/api/tspi/nc-tspi-async_completion) .

Los perfiles de parámetro para los procedimientos de eventos espontáneos incluyen parámetros que identifican el objeto pertinente para el que se está informando del evento (teléfono, línea o llamada). La identificación está en forma de un identificador opaco cuya interpretación exacta no es publicada por TSPI. TAPI determina internamente la relación entre estos manipuladores opacos y las estructuras de datos que se usan para representar los dispositivos.

El perfil de parámetro para los procedimientos de eventos espontáneos también incluye un parámetro de mensaje que identifica el tipo de mensaje. Cada tipo de mensaje tiene una definición correspondiente que determina los identificadores que se incluyen, junto con otros parámetros y su significado. Existe una correspondencia muy segura entre los mensajes que aparecen en el nivel de TSPI y los que aparecen en el nivel de TAPI. Estas son las reglas generales de correspondencia:

-   El conjunto de mensajes es casi idéntico. Cuando los mensajes corresponden, se usa el mismo nombre de mensaje y valor en el nivel de TSPI.
-   Los identificadores que aparecen en el nivel de TSPI son los tipos opacos definidos por la especificación TSPI. Estos tipos (y su interpretación) difieren de los del nivel TAPI, aunque hacen referencia a la misma clase de dispositivo. Por ejemplo, donde un mensaje TAPI incluye un identificador HLINE, el mensaje TSPI correspondiente normalmente incluiría un identificador [**HTAPILINE**](htapiline.md) .
-   No hay datos *dwCallbackInstance* pasados a la devolución de llamada.
-   Los parámetros *dwParam1*, *dwParam2* y *dwParam3* suelen ser idénticos a los parámetros correspondientes del mensaje TAPI.
-   Los mensajes orientados a líneas y orientados a llamadas se pasan a un procedimiento de devolución de llamada diferente del de los mensajes orientados al teléfono.

Para cada mensaje, en esta sección se enumeran los elementos siguientes:

-   El propósito del mensaje
-   El procedimiento de devolución de llamada al que se pasa este mensaje
-   Una descripción de los parámetros del mensaje
-   Comentarios opcionales sobre el uso del mensaje
-   Referencias opcionales a otras funciones, mensajes y estructuras de datos
-   Comentarios opcionales que comparan este mensaje con la interfaz TAPI

Algunos mensajes se utilizan para notificar a TAPI sobre un cambio en el estado de un objeto. Estos mensajes proporcionan el identificador de objeto opaco TAPI y una indicación de qué elemento de Estado ha cambiado. A continuación, TAPI puede llamar a una función "get status" adecuada del objeto para obtener el estado completo del objeto.

Cuando se produce un evento, se puede enviar un mensaje o no a TAPI. En algunos tipos de eventos, como los cambios de estado, TAPI especifica un conjunto de cambios de estado en los que está interesado. Se recomienda que el proveedor de servicios limite los eventos de mensaje de cambio de estado que notifica a los incluidos en este conjunto. No es necesario que el proveedor de servicios cumpla este límite. En otras palabras, puede notificar más cambios de los estrictamente necesarios. Sin embargo, debe intentar observar el límite por motivos de rendimiento.

El mensaje de respuesta de línea \_ no se utiliza en el nivel de TSPI. La finalización de una solicitud asincrónica se registra mediante la devolución de llamada de [**\_ finalización asincrónica**](/windows/win32/api/tspi/nc-tspi-async_completion) .

El mensaje de respuesta del teléfono \_ no se utiliza en el nivel de TSPI. La finalización de una solicitud asincrónica se registra mediante la devolución de llamada de [**\_ finalización asincrónica**](/windows/win32/api/tspi/nc-tspi-async_completion) .

Para obtener más información, consulte los siguientes temas:

-   [Mensajes de dispositivo de línea de TSPI](tspi-line-device-messages.md)
-   [TSPI mensajes de dispositivo telefónico](tspi-phone-device-messages.md)

 

 
