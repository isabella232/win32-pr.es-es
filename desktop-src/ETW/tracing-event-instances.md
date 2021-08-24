---
description: Los proveedores clásicos usan la función TraceEventInstance para realizar un seguimiento de los eventos que forman parte de una única transacción. También puede usar esta función para realizar un seguimiento de los eventos primarios y secundarios.
ms.assetid: 246e9443-3120-49bf-a6e3-64dddba348fa
title: Escribir eventos relacionados en un proveedor clásico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41443c0a05bd94e25ae4ca6a4549671c6aa0682b848660ca31683bb4bf8b75b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813817"
---
# <a name="writing-related-events-in-a-classic-provider"></a>Escribir eventos relacionados en un proveedor clásico

[Los](about-event-tracing.md) proveedores clásicos usan [**la función TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) para realizar un seguimiento de los eventos que forman parte de una única transacción. También puede usar esta función para realizar un seguimiento de los eventos primarios y secundarios.

Antes de llamar [**a la función TraceEventInstance,**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) primero debe llamar a la [**función CreateTraceInstanceId**](/windows/win32/api/evntrace/nf-evntrace-createtraceinstanceid) para obtener un identificador de transacción. Esta función genera un identificador de transacción único y lo asigna a un identificador GUID de clase registrado. Los identificadores de GUID de clase registrados están disponibles en los **miembros RegHandle** de las estructuras [**TRACE GUID \_ \_ REGISTRATION,**](/windows/win32/api/evntrace/ns-evntrace-trace_guid_registration) después de llamar a la [**función RegisterTraceGuids.**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) El identificador de transacción se coloca en el **miembro InstanceId** de una estructura [**EVENT INSTANCE \_ \_ INFO**](/windows/win32/api/evntrace/ns-evntrace-event_instance_info) que se pasa a la **función CreateTraceInstanceId.**

La estructura [**EVENT \_ INSTANCE \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_instance_header) que se pasa a la función [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) es similar a la estructura [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) (vea Eventos de seguimiento [),](tracing-events.md)salvo que contiene información adicional relacionada con las instancias de y no contiene un miembro **GUID.**

Las instancias de eventos se pueden usar para establecer una relación jerárquica entre eventos. La [**función TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) acepta información específica de la instancia de dos instancias de eventos. El *parámetro pInstInfo* apunta a la estructura [**EVENT INSTANCE \_ \_ INFO**](/windows/win32/api/evntrace/ns-evntrace-event_instance_info) de la instancia de evento y el parámetro *pParentInstInfo* apunta a la estructura **EVENT INSTANCE \_ \_ INFO** de una instancia de evento primaria. La definición de una instancia de evento "primaria" está definida por la aplicación; el elemento primario puede ser cualquier instancia que ya se haya generado.

 

 
