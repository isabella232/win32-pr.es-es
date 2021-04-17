---
description: Una sesión de seguimiento de eventos privados es una sesión de seguimiento de eventos de modo usuario que se ejecuta en el mismo proceso que sus proveedores de seguimiento de eventos&\# 8212; la sesión privada y los proveedores que habilita deben estar todos en el mismo proceso.
ms.assetid: fb6a3899-194e-4cb7-b9e5-a7ff85fb7891
title: Configurar e iniciar una sesión de registrador privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ef13728bfb3516197ab153cf90b301d5930ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497711"
---
# <a name="configuring-and-starting-a-private-logger-session"></a>Configurar e iniciar una sesión de registrador privado

Una sesión de seguimiento de eventos privados es una sesión de seguimiento de eventos de modo usuario que se ejecuta en el mismo proceso que sus proveedores de seguimiento de eventos: la sesión privada y los proveedores que habilita deben estar todos en el mismo proceso. La ventaja de utilizar una sesión privada es que la sesión privada no cuenta con el máximo de 64 sesiones de seguimiento de eventos que se ejecutan simultáneamente.

Configurar e iniciar una sesión privada es similar a iniciar una sesión de seguimiento de eventos normal. La diferencia es que el miembro **Wnode. GUID** de la estructura de [**\_ \_ propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) debe contener el **GUID** del proveedor, no la sesión, y el proveedor debe haber registrado ya el GUID. Tenga en cuenta que si también establece el \_ seguimiento \_ de eventos privado \_ en \_ modo de registro de procedimientos, puede usar un **GUID** diferente para la sesión y el proveedor. Para obtener más información sobre cómo iniciar una sesión de seguimiento de eventos normal, vea [configurar e iniciar una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md).

Tenga en cuenta que no puede iniciar, detener o vaciar una sesión de seguimiento privada desde DllMain; debe hacerlo en las rutinas de inicialización y finalización de la DLL.

De Windows 8.1 a Windows 10, la versión 1607, los filtros de carga de eventos, ámbito y recorrido de pila se pueden usar en la función [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) y en las estructuras de [**\_ \_ descriptor de filtro de eventos**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) y [**habilitar \_ \_ parámetros de seguimiento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) para filtrar determinadas condiciones en una sesión del registrador. Para obtener más información sobre los filtros de carga de eventos, vea las funciones [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)y [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) , así como las estructuras de [**\_ \_ predicado**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) **habilitar \_ \_ parámetros de seguimiento**, **\_ \_ descriptor de filtro de eventos** y filtro de carga.

A partir de Windows 10, versión 1703, los usuarios con pocos privilegios ahora pueden iniciar una sesión de registrador privada en los procesos que han iniciado. Ya no es necesario registrar el proveedor antes de habilitar o iniciar la sesión privada, lo que significa que el proveedor está "habilitado previamente" similar al de los proveedores de sesiones no privados. Hay un límite de 8 registradores privados del sistema para un proceso individual. Para mejorar el rendimiento en escenarios de proceso cruzado, se recomienda usar el filtrado para las API de sesión (incluidas [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea), [**QueryTrace**](/windows/win32/api/evntrace/nf-evntrace-querytrace), [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)y [**StopTrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) al iniciar un registrador de sistema privado. Tenga en cuenta que los mismos filtros se deben pasar a todas las API de sesión. Para obtener más información acerca de los filtros, consulte [**propiedades de seguimiento de eventos \_ \_ \_ V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).

Para obtener más información sobre cómo iniciar una sesión de seguimiento de eventos, vea [configurar e iniciar una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md).

Para obtener información detallada sobre cómo iniciar una sesión del registrador del kernel de NT, vea [configurar e iniciar la sesión del registrador del kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md).

Para obtener más información sobre cómo iniciar una sesión del registrador global, vea [configurar e iniciar una sesión del registrador global](configuring-and-starting-the-global-logger-session.md).

Para obtener más información sobre cómo iniciar una sesión del registrador automático, vea [configurar e iniciar una sesión de registrador automático](configuring-and-starting-an-autologger-session.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configurar e iniciar una sesión de SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configurar e iniciar una sesión de registrador automático](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Configurar e iniciar una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Configuración e inicio de la sesión del registrador del kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**HABILITAR \_ parámetros de seguimiento \_**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**\_propiedades de seguimiento de eventos \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**Propiedades de seguimiento de eventos \_ \_ \_ V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
</dt> <dt>

[**descriptor de filtro de eventos \_ \_**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**\_predicado de filtro de carga \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Actualizar una sesión de seguimiento de eventos](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
