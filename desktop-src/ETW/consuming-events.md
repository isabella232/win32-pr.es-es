---
description: Los consumidores de seguimiento de eventos pueden procesar eventos de uno o más proveedores.
ms.assetid: 039a9f66-228e-4258-9967-2b2cd7d31091
title: Consumir eventos (seguimiento de eventos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad8234cc66d07b5a52c10ab39c7d7b3c8aa029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986087"
---
# <a name="consuming-events-event-tracing"></a>Consumir eventos (seguimiento de eventos)

Los consumidores de seguimiento de eventos pueden procesar eventos de uno o más proveedores. Los consumidores pueden procesar eventos desde un archivo de registro o en tiempo real. Solo puede consumir eventos en tiempo real si el controlador especifica el modo de registro en tiempo real para la sesión. Por motivos de rendimiento, no se recomienda el procesamiento en tiempo real antes de Windows Vista.

Para especificar la sesión de seguimiento desde la que desea procesar eventos, use la estructura de archivo de [**\_ \_ registro de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) . Debe inicializar una copia de esta estructura para cada archivo de registro o sesión en tiempo real que desee procesar.

Para consumir eventos de un archivo de registro, establezca el miembro **LogFileName** en el nombre del archivo de registro. Para consumir eventos de una sesión en tiempo real, establezca el miembro **LoggerName** en el nombre de sesión. También puede usar esta estructura para especificar la devolución de llamada de [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka) y la devolución de llamada [*EventCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback) o [**EventRecordCallback**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback) utilizada para procesar los eventos.

-   [**EventRecordCallback**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback): recibe y procesa todos los eventos (incluido el evento de encabezado) de uno o varios archivos de registro y una sesión en tiempo real. Puede implementar esta devolución de llamada si usa las funciones auxiliares de datos de seguimiento para analizar los datos de evento o si desea recuperar metadatos sobre el evento.
-   [*EventCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback): recibe y procesa todos los eventos (incluido el evento de encabezado) de uno o varios archivos de registro y una sesión en tiempo real.
-   [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka): recibe y procesa información de resumen sobre el búfer actual, como los eventos perdidos. ETW llama a la devolución de llamada después de entregar todos los eventos del búfer al consumidor. El consumidor también puede utilizar esta devolución de llamada para cancelar el procesamiento de eventos; sin embargo, si está consumiendo eventos en tiempo real, ETW entrega eventos hasta que el controlador detenga la sesión.

Después de definir una o más sesiones de seguimiento, llame a la función [**OpenTrace**](/windows/win32/api/evntrace/nf-evntrace-opentracea) para cada sesión de seguimiento que desee procesar; puede procesar eventos de uno o varios archivos de registro, pero solo de una sesión en tiempo real. A continuación, se pasa la lista de identificadores de sesión de seguimiento que **OpenTrace** devuelve a la función [**ProcessTrace**](/windows/win32/api/evntrace/nf-evntrace-processtrace) . La función **ProcessTrace** combina los eventos, los ordena en orden cronológico y los entrega a las devoluciones de llamada de uno en uno. Los eventos se pueden filtrar para incluir solo los que se encuentran en un intervalo de tiempo específico mediante los parámetros *startTime* y *EndTime* . La función **ProcessTrace** bloquea el subproceso hasta que el consumidor procesa todos los eventos en las sesiones de seguimiento, el [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka) devuelve **false** o se llama [**CloseTrace**](/windows/win32/api/evntrace/nf-evntrace-closetrace).

**Antes de Windows Vista:** Solo puede llamar a [**CloseTrace**](/windows/win32/api/evntrace/nf-evntrace-closetrace) después de que [**ProcessTrace**](/windows/win32/api/evntrace/nf-evntrace-processtrace) devuelva.

Para obtener un ejemplo en el que se muestra cómo consumir eventos publicados mediante un manifiesto, MOF o archivos TMF, vea [recuperar datos de eventos mediante TDH](retrieving-event-data-using-tdh.md). Tenga en cuenta que, a partir de Windows Vista, debe usar las funciones de la aplicación auxiliar de datos de seguimiento (TDH) para consumir eventos.

Para obtener un ejemplo en el que se muestra cómo consumir eventos publicados mediante MOF, vea [recuperar datos de eventos mediante MOF](retrieving-event-data-using-mof.md).

 

 
