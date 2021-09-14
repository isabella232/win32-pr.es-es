---
description: Los consumidores de seguimiento de eventos pueden procesar eventos de uno o varios proveedores.
ms.assetid: 039a9f66-228e-4258-9967-2b2cd7d31091
title: Consumo de eventos (seguimiento de eventos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad8234cc66d07b5a52c10ab39c7d7b3c8aa029
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063152"
---
# <a name="consuming-events-event-tracing"></a>Consumo de eventos (seguimiento de eventos)

Los consumidores de seguimiento de eventos pueden procesar eventos de uno o varios proveedores. Los consumidores pueden procesar eventos desde un archivo de registro o en tiempo real. Solo puede consumir eventos en tiempo real si el controlador especifica el modo de registro en tiempo real para la sesión. Por motivos de rendimiento, no se recomienda el procesamiento en tiempo real antes de Windows Vista.

Para especificar la sesión de seguimiento desde la que desea procesar eventos, use la [**estructura \_ \_ LOGFILE DE SEGUIMIENTO DE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) EVENTOS. Debe inicializar una copia de esta estructura para cada archivo de registro o sesión en tiempo real que desee procesar.

Para consumir eventos de un archivo de registro, establezca el **miembro LogFileName** en el nombre del archivo de registro. Para consumir eventos de la sesión en tiempo real, establezca el **miembro LoggerName** en el nombre de la sesión. También se usa esta estructura para especificar la devolución de llamada [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka) y la devolución de llamada [*EventCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback) o [**EventRecordCallback**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback) utilizadas para procesar los eventos.

-   [**EventRecordCallback:**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback)recibe y procesa todos los eventos (incluido el evento de encabezado) de uno o varios archivos de registro y una sesión en tiempo real. Implemente esta devolución de llamada si usa las funciones auxiliares de datos de seguimiento para analizar los datos del evento o si desea recuperar metadatos sobre el evento.
-   [*EventCallback:*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback)recibe y procesa todos los eventos (incluido el evento de encabezado) de uno o varios archivos de registro y una sesión en tiempo real.
-   [*BufferCallback:*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka)recibe y procesa información de resumen sobre el búfer actual, como los eventos perdidos. ETW llama a la devolución de llamada después de entregar todos los eventos del búfer al consumidor. El consumidor también puede usar esta devolución de llamada para cancelar el procesamiento de eventos. sin embargo, si está consumiendo eventos en tiempo real, ETW entrega eventos hasta que el controlador detiene la sesión.

Después de definir una o varias sesiones de seguimiento, llame a la [**función OpenTrace**](/windows/win32/api/evntrace/nf-evntrace-opentracea) para cada sesión de seguimiento que desee procesar. puede procesar eventos de uno o varios archivos de registro, pero solo desde una sesión en tiempo real. A continuación, pase la lista de identificadores de sesión de seguimiento que **OpenTrace** devuelve a la [**función ProcessTrace.**](/windows/win32/api/evntrace/nf-evntrace-processtrace) La **función ProcessTrace** combina los eventos, los ordena en orden cronológico y, a continuación, los entrega a las devoluciones de llamada de una en una. Los eventos se pueden filtrar para incluir solo aquellos que se encuentran en un período de tiempo específico mediante los *parámetros StartTime* y *EndTime.* La **función ProcessTrace bloquea** el subproceso hasta que el consumidor procesa todos los eventos de las sesiones de seguimiento, [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka) devuelve **FALSE** o se llama a [**CloseTrace**](/windows/win32/api/evntrace/nf-evntrace-closetrace).

**Antes de Windows Vista:** Solo puede llamar a [**CloseTrace**](/windows/win32/api/evntrace/nf-evntrace-closetrace) después de que [**processTrace vuelva.**](/windows/win32/api/evntrace/nf-evntrace-processtrace)

Para obtener un ejemplo en el que se muestra cómo consumir eventos publicados mediante un manifiesto, MOF o archivos TMF, vea Recuperar datos de eventos [mediante TDH.](retrieving-event-data-using-tdh.md) Tenga en cuenta que a Windows Vista, debe usar las funciones del asistente de datos de seguimiento (TDH) para consumir eventos.

Para obtener un ejemplo en el que se muestra cómo consumir eventos publicados mediante MOF, vea [Retrieving Event Data Using MOF](retrieving-event-data-using-mof.md).

 

 
