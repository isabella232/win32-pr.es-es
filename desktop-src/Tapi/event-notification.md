---
description: La notificación de eventos es el medio principal por el que una aplicación obtiene información de TAPI y los proveedores de servicios.
ms.assetid: 02160f10-dc3f-484c-9cd3-bcfb07ded822
title: Notificación de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63aa232b0e712a76442c298ea04e24ec7671cb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677808"
---
# <a name="event-notification"></a>Notificación de evento

La notificación de eventos es el medio principal por el que una aplicación obtiene información de TAPI y los proveedores de servicios. Esta información puede ser el estado de una operación asincrónica inactiva por la aplicación o que puede afectar a un proceso que se inició fuera de la aplicación, como notificaciones de nuevas llamadas entrantes.

**TAPI 2. x:** Las aplicaciones controlan la notificación de una de estas tres maneras: ventana oculta, identificador de evento o puerto de finalización. Para obtener información adicional sobre estos mecanismos de notificación, consulte la sección Comentarios de [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa). Una aplicación especifica el mecanismo estableciendo el miembro **dwOptions** de la estructura [**LINEINITIALIZEEXPARAMS**](/windows/win32/api/tapi/ns-tapi-lineinitializeexparams) antes de llamar a [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).

La función [**lineSetStatusMessages**](/windows/win32/api/tapi/nf-tapi-linesetstatusmessages) permite a una aplicación especificar los mensajes de notificación que se van a recibir para los eventos relacionados con los cambios de estado de la línea especificada o de cualquiera de sus direcciones.

**TAPI 3. x:** Las aplicaciones controlan la notificación general mediante [objetos conectables](../com/events-in-com-and-connectable-objects.md)estándar com. [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) es la interfaz de salida que se debe registrar con el objeto de contenedor de TAPI y [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) es el método que llama a TAPI para determinar la respuesta de la aplicación. El método [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) indica a TAPI qué eventos son de interés para la aplicación. Si no se especifica un filtro de eventos, la aplicación no recibirá ninguna notificación de ningún evento. El método [**ITTAPI:: RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) indica a TAPI los tipos de medios y las direcciones para los que la aplicación controlará las sesiones entrantes. Para obtener información adicional sobre el control de eventos TAPI 3, vea la información general sobre [eventos](events.md) o el ejemplo de código [registrar eventos](register-events.md) .

Los proveedores de servicios de telefonía implementan [**TSPI \_ LineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) y [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages). TAPI llama a estas funciones para indicar el conjunto de todos los eventos de línea, dirección y tipo de medio solicitados por las aplicaciones.

 

 
