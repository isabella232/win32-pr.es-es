---
description: Una sesión de seguimiento de eventos privada es una sesión de seguimiento de eventos en modo de usuario que se ejecuta en el mismo proceso que sus proveedores de seguimiento de eventos&8212; la sesión privada y los proveedores que habilita deben estar en el \# mismo proceso.
ms.assetid: fb6a3899-194e-4cb7-b9e5-a7ff85fb7891
title: Configuración e inicio de una sesión de registrador privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ef13728bfb3516197ab153cf90b301d5930ff2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063157"
---
# <a name="configuring-and-starting-a-private-logger-session"></a>Configuración e inicio de una sesión de registrador privado

Una sesión de seguimiento de eventos privada es una sesión de seguimiento de eventos en modo de usuario que se ejecuta en el mismo proceso que sus proveedores de seguimiento de eventos: la sesión privada y los proveedores que habilita deben estar en el mismo proceso. La ventaja de usar una sesión privada es que la sesión privada no cuenta con el máximo de 64 sesiones de seguimiento de eventos que se ejecutan simultáneamente.

La configuración e inicio de una sesión privada es similar a iniciar una sesión de seguimiento de eventos normal. La diferencia es que el miembro **Wnode.Guid** de la estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) debe contener el **GUID** del proveedor, no la sesión, y el proveedor debe haber registrado el GUID. Tenga en cuenta que si también establece el modo de registro EVENT TRACE PRIVATE IN PROC, puede usar un \_ GUID diferente para la sesión y el \_ \_ \_ proveedor.  Para obtener más información sobre cómo iniciar una sesión de seguimiento de eventos normal, vea [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).

Tenga en cuenta que no puede iniciar, detener ni vaciar una sesión de seguimiento privado desde DllMain; debe hacerlo en las rutinas de inicialización y fin del archivo DLL.

De Windows 8.1 a Windows 10, versión 1607, la carga de eventos, el ámbito y los filtros de recorrido de pila se pueden usar en la función [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) y las estructuras [**ENABLE TRACE \_ \_ PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) y [**EVENT FILTER \_ \_ DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) para filtrar por condiciones específicas en una sesión de registrador. Para obtener más información sobre los filtros de carga de eventos, vea las funciones [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)y [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) y las estructuras **ENABLE TRACE \_ \_ PARAMETERS**, **EVENT FILTER \_ \_ DESCRIPTOR** y [**PAYLOAD FILTER \_ \_ PREDICATE.**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

A partir Windows 10, versión 1703, los usuarios con pocos privilegios ahora pueden iniciar una sesión de registrador privado en los procesos que iniciaron. El proveedor ya no necesita registrarse antes de habilitar o iniciar la sesión privada, lo que significa que el proveedor está "habilitado previamente" de forma similar a como lo están los proveedores de sesiones no privados. Hay un límite de 8 registradores privados de todo el sistema a un proceso individual. Para aumentar el rendimiento en escenarios entre procesos, se recomienda usar el filtrado para las API de sesión [**(incluidos ControlTrace,**](/windows/win32/api/evntrace/nf-evntrace-controltracea) [**QueryTrace,**](/windows/win32/api/evntrace/nf-evntrace-querytrace) [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)y [**StopTrace)**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)al iniciar un registrador privado de todo el sistema. Tenga en cuenta que se deben pasar los mismos filtros a todas las API de sesión. Para obtener más información sobre los filtros, vea [**PROPIEDADES DE SEGUIMIENTO DE EVENTOS \_ \_ \_ V2.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)

Para obtener más información sobre cómo iniciar una sesión de seguimiento de eventos, vea [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).

Para obtener más información sobre cómo iniciar una sesión de registrador de kernel nt, vea [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).

Para obtener más información sobre cómo iniciar una sesión de registrador global, vea [Configuring and Starting a Global Logger Session](configuring-and-starting-the-global-logger-session.md).

Para obtener más información sobre cómo iniciar una sesión de AutoLogger, vea [Configuring and Starting an AutoLogger Session](configuring-and-starting-an-autologger-session.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración e inicio de una sesión de SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configuración e inicio de una sesión de Registrador automático](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Configuración e inicio de una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Configuración e inicio de la sesión del registrador de kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**HABILITAR \_ PARÁMETROS DE \_ SEGUIMIENTO**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**PROPIEDADES DE \_ SEGUIMIENTO \_ DE EVENTOS**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**PROPIEDADES DE \_ SEGUIMIENTO \_ DE EVENTOS \_ V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
</dt> <dt>

[**DESCRIPTOR \_ DE FILTRO DE \_ EVENTOS**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**PREDICADO \_ DE FILTRO DE CARGA \_ ÚTIL**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Actualizar una sesión de seguimiento de eventos](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
