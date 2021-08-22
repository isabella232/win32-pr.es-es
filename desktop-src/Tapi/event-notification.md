---
description: La notificación de eventos es el medio principal por el que una aplicación obtiene información de TAPI y los proveedores de servicios.
ms.assetid: 02160f10-dc3f-484c-9cd3-bcfb07ded822
title: Notificación de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a83ed721ed22049baeaf3de15626ed8deecf2a7562d883658195eb1eb590f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003673"
---
# <a name="event-notification"></a>Notificación de evento

La notificación de eventos es el medio principal por el que una aplicación obtiene información de TAPI y los proveedores de servicios. Esta información puede ser el estado de una operación asincrónica iniciada por la aplicación o puede afectar a un proceso que se inició fuera de la aplicación, como las notificaciones de nuevas llamadas entrantes.

**TAPI 2.x:** Las aplicaciones controlan la notificación de una de estas tres maneras: Ventana oculta, Identificador de eventos o Puerto de finalización. Para obtener información adicional sobre estos mecanismos de notificación, consulte la sección Comentarios de [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa). Una aplicación especifica el mecanismo estableciendo el miembro **dwOptions** de la estructura [**LINEINITIALIZEEXPARAMS**](/windows/win32/api/tapi/ns-tapi-lineinitializeexparams) antes de llamar a [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).

La [**función lineSetStatusMessages**](/windows/win32/api/tapi/nf-tapi-linesetstatusmessages) permite a una aplicación especificar qué mensajes de notificación recibir para los eventos relacionados con los cambios de estado de la línea especificada o de cualquiera de sus direcciones.

**TAPI 3.x:** Las aplicaciones controlan la notificación general mediante objetos [conectables estándar COM](../com/events-in-com-and-connectable-objects.md). [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) es la interfaz saliente que se debe registrar con el objeto contenedor de TAPI y [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) es el método que llama a TAPI para determinar la respuesta de la aplicación. El [**método ITTAPI::p ut \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) indica a TAPI qué eventos son de interés para la aplicación. Si no se introduce un filtro de eventos, la aplicación no recibirá notificación de ningún evento. El [**método ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) indica a TAPI los tipos de medios y las direcciones para las que la aplicación controlará las sesiones entrantes. Para obtener información adicional sobre el control [](events.md) de eventos tapi 3, consulte la información general sobre eventos o el [ejemplo de](register-events.md) código Registrar eventos.

Los proveedores de servicios de telefonía [**implementan las líneas \_ TSPIDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) y [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages). TAPI llama a estas funciones para indicar el conjunto de todos los eventos de línea, dirección y tipo de medio solicitados por las aplicaciones.

 

 
