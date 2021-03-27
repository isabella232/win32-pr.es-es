---
description: Los proveedores clásicos usan la función TraceEventInstance para realizar un seguimiento de los eventos que forman parte de una única transacción. También puede usar esta función para realizar el seguimiento de eventos de elementos primarios y secundarios.
ms.assetid: 246e9443-3120-49bf-a6e3-64dddba348fa
title: Escritura de eventos relacionados en un proveedor clásico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771b08a66625d5cd6e723fbc2e12eed87bd1d434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361664"
---
# <a name="writing-related-events-in-a-classic-provider"></a>Escritura de eventos relacionados en un proveedor clásico

Los proveedores [clásicos](about-event-tracing.md) usan la función [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) para realizar un seguimiento de los eventos que forman parte de una única transacción. También puede usar esta función para realizar el seguimiento de eventos de elementos primarios y secundarios.

Antes de llamar a la función [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) , primero debe llamar a la función [**CreateTraceInstanceId**](/windows/win32/api/evntrace/nf-evntrace-createtraceinstanceid) para obtener un identificador de transacción. Esta función genera un identificador de transacción único y lo asigna a un identificador GUID de clase registrado. Los identificadores de los GUID de clase registrados están disponibles en los miembros de **RegHandle** de las estructuras de [**registro de \_ GUID \_ de seguimiento**](/windows/win32/api/evntrace/ns-evntrace-trace_guid_registration) , después de llamar a la función [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) . El identificador de la transacción se coloca en el miembro **InstanceID** de una estructura de [**información de \_ instancia \_ de evento**](/windows/win32/api/evntrace/ns-evntrace-event_instance_info) que se pasa a la función **CreateTraceInstanceId** .

La estructura de [**\_ \_ encabezado**](/windows/win32/api/evntrace/ns-evntrace-event_instance_header) de la instancia de evento que se pasa a la función [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) es similar a la estructura de encabezado del [**\_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) (vea [eventos de seguimiento](tracing-events.md)), salvo que contiene información adicional relacionada con las instancias y no contiene un miembro **GUID** .

Las instancias de eventos se pueden usar para establecer una relación jerárquica entre los eventos. La función [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) acepta información específica de la instancia de dos instancias de eventos. El parámetro *pInstInfo* apunta a la estructura de [**\_ \_ información de instancia de evento**](/windows/win32/api/evntrace/ns-evntrace-event_instance_info) de la instancia de evento y el parámetro *pParentInstInfo* apunta a la estructura de **\_ \_ información de instancia de evento** de una instancia de evento primaria. La definición de una instancia de evento "primario" está definida por la aplicación; el elemento primario puede ser cualquier instancia que ya se haya generado.

 

 
