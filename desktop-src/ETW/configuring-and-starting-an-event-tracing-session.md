---
description: Para configurar una sesión de seguimiento de eventos, use \_ la \_ estructura propiedades de seguimiento de eventos para especificar las propiedades de la sesión.
ms.assetid: 8a6aa39c-ec81-42ac-a26e-29f1f6960220
title: Configurar e iniciar una sesión de seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f86ec57975e8f12ede17e5e2cda962c010aa1af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986135"
---
# <a name="configuring-and-starting-an-event-tracing-session"></a>Configurar e iniciar una sesión de seguimiento de eventos

Para configurar una sesión de seguimiento de eventos, use la estructura [**\_ \_ propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) para especificar las propiedades de la sesión. La memoria asignada para la estructura de **\_ \_ propiedades de seguimiento de eventos** debe ser lo suficientemente grande como para contener también los nombres de archivo de registro y sesión que siguen la estructura en memoria.

Después de especificar las propiedades de la sesión, llame a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) para iniciar la sesión. Si la función se ejecuta correctamente, el parámetro *SessionHandle* contendrá el identificador de sesión y la propiedad **LoggerNameOffset** contendrá el desplazamiento al nombre de la sesión.

Para habilitar los proveedores que desea que registren eventos en la sesión, llame a la función [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para habilitar los proveedores clásicos y la función [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) para habilitar los proveedores [basados en manifiestos](about-event-tracing.md) . Para habilitar los proveedores que desea que registren eventos en el filtrado de sesión en condiciones específicas en Windows 8.1, Windows Server 2012 R2 y versiones posteriores, llame a la función [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) .

Además, también puede realizar un seguimiento de información adicional sobre un evento con una llamada a la función [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) . **TraceSetInformation** coloca información de seguimiento adicional en la sección de datos extendidos de un evento y puede incluir información como la información de versión de seguimiento o los proveedores que están registrados actualmente en el sistema. Para obtener más información, vea [recuperar datos de seguimiento de eventos adicionales](retrieving-additional-event-tracing-data.md).

Hasta ocho sesiones de seguimiento pueden habilitar y recibir eventos del mismo proveedor [basado en manifiesto](about-event-tracing.md) . Sin embargo, solo una sesión de seguimiento puede habilitar un proveedor [clásico](about-event-tracing.md) . Si más de una sesión de seguimiento intenta habilitar un proveedor clásico, la primera sesión dejará de recibir eventos cuando la segunda sesión habilite el proveedor. Por ejemplo, si la sesión es un proveedor habilitado 1 y, a continuación, la sesión B habilita el proveedor 1, solo la sesión B recibirá eventos del proveedor 1.

Puede usar cualquiera de las tres funciones para habilitar un proveedor, pero puede perder funcionalidad si usa [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para habilitar un proveedor basado en manifiestos porque no podrá proporcionar un valor de MatchAllKeyword, especificar los elementos de datos extendidos que se van a incluir en el evento o proporcionar datos de filtro definidos por el proveedor. Para obtener más información, vea la sección Comentarios de cada función.

En Windows 8.1, Windows Server 2012 R2 y versiones posteriores, los filtros de carga de eventos, ámbito y recorrido de pila se pueden usar con la función [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) y las estructuras de [**habilitar \_ \_ parámetros de seguimiento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) y [**\_ \_ descriptor de filtro de eventos**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) para filtrar según condiciones específicas en una sesión del registrador. Para obtener más información sobre los filtros de carga de eventos, vea las funciones [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)y [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) , así como las estructuras de [**\_ \_ predicado**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) **habilitar \_ \_ parámetros de seguimiento**, **\_ \_ descriptor de filtro de eventos** y filtro de carga.

Para determinar el nivel y las palabras clave que se usan para habilitar un proveedor basado en manifiesto, use uno de los siguientes comandos:

-   *Nombre del proveedor de* **consultas** **Logman**
-    *Proveedor de GP de wevtutil: nombre* 

Los comandos solo muestran el nivel y las palabras clave, el proveedor debe documentar los requisitos de datos de filtro para los posibles controladores.

Para enumerar los proveedores basados en manifiestos, use **wevtutil** **EP**.

En el caso de los proveedores clásicos, es el proveedor quien debe documentar y poner a disposición de los posibles controladores los niveles de gravedad o habilitar las marcas que admite. Si el proveedor desea estar habilitado por cualquier controlador, el proveedor debe aceptar 0 para el nivel de gravedad y habilitar los marcadores e interpretar 0 como una solicitud para realizar el registro predeterminado (lo que pueda ser).

Puede habilitar el proveedor antes o después de que el proveedor se registre. Después de habilitar el proveedor, ETW llamará a la función de devolución de llamada del proveedor. Si el proveedor no está registrado, ETW llamará a la función de devolución de llamada del proveedor después de registrarse.

También puede usar la función [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para deshabilitar el proveedor (detener el registro de eventos a su sesión) o para actualizar el nivel de registro o habilitar las marcas del proveedor. Con la función [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) , puede deshabilitar el proveedor o actualizar el nivel, las palabras clave, los datos extendidos y filtrar los datos. Cada vez que se llama a la función **EnableTrace** o **EnableTraceEx** , ETW llama a la función de devolución de llamada del proveedor. El proveedor permanece habilitado para la sesión hasta que la sesión deshabilita el proveedor.

Para detener la sesión de seguimiento después de recopilar eventos, llame a la función [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) y pase \_ \_ \_ la detención del control de seguimiento de eventos como código de control. Para especificar la sesión que se va a detener, puede pasar el identificador de sesión de seguimiento de eventos Obtenido de una llamada anterior a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) o el nombre de una sesión iniciada previamente. Asegúrese de deshabilitar todos los proveedores antes de detener la sesión. Si detiene la sesión antes de deshabilitar el proveedor por primera vez, ETW deshabilitará el proveedor e intentará llamar a la función de devolución de llamada del control del proveedor. Si la aplicación que inició la sesión finaliza sin deshabilitar el proveedor o llamar a la función **ControlTrace** , el proveedor permanece habilitado.

Si [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) se realiza correctamente, se actualizan las propiedades de la sesión para reflejar los valores de propiedad finales y las estadísticas de ejecución de la sesión de seguimiento de eventos.

Para obtener un ejemplo en el que se inicia una sesión de seguimiento de eventos, vea lo siguiente:

-   [Ejemplo que crea una sesión y habilita un proveedor basado en manifiesto](example-that-creates-a-session-and-enables-a-manifest-based-provider.md) : inicia una sesión de seguimiento, habilita un proveedor basado en manifiesto, deshabilita el proveedor y, a continuación, detiene la sesión.

Para obtener más información acerca de cómo iniciar una sesión de seguimiento, consulte una de las siguientes opciones:

-   [Configurar e iniciar una sesión de SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
-   [Configuración e inicio de la sesión del registrador del kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md)
-   [Configurar e iniciar una sesión de registrador automático](configuring-and-starting-an-autologger-session.md)
-   [Configurar e iniciar la sesión del registrador global](configuring-and-starting-the-global-logger-session.md)
-   [Configurar e iniciar una sesión de registrador privado](configuring-and-starting-a-private-logger-session.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configurar e iniciar una sesión de registrador privado](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Configurar e iniciar una sesión de SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configurar e iniciar una sesión de registrador automático](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Configuración e inicio de la sesión del registrador del kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea)
</dt> <dt>

[**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace)
</dt> <dt>

[**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**HABILITAR \_ parámetros de seguimiento \_**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**descriptor de filtro de eventos \_ \_**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**\_propiedades de seguimiento de eventos \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**\_predicado de filtro de carga \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Actualizar una sesión de seguimiento de eventos](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
