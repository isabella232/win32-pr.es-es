---
description: Para configurar una sesión de seguimiento de eventos, use la estructura EVENT \_ TRACE PROPERTIES para especificar las propiedades de la \_ sesión.
ms.assetid: 8a6aa39c-ec81-42ac-a26e-29f1f6960220
title: Configuración e inicio de una sesión de seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f86ec57975e8f12ede17e5e2cda962c010aa1af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063156"
---
# <a name="configuring-and-starting-an-event-tracing-session"></a>Configuración e inicio de una sesión de seguimiento de eventos

Para configurar una sesión de seguimiento de eventos, use la [**estructura EVENT \_ TRACE \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) para especificar las propiedades de la sesión. La memoria que asigne para la estructura **EVENT \_ TRACE \_ PROPERTIES** debe ser lo suficientemente grande como para contener también los nombres de archivo de sesión y registro que siguen a la estructura en memoria.

Después de especificar las propiedades de la sesión, llame a la [**función StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) para iniciar la sesión. Si la función se realiza correctamente, el parámetro *SessionHandle* contendrá el identificador de sesión y la propiedad **LoggerNameOffset** contendrá el desplazamiento al nombre de la sesión.

Para habilitar los proveedores que desea registrar eventos en la sesión, llame a la función [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para habilitar los proveedores clásicos y a la función [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) para habilitar proveedores basados [en](about-event-tracing.md) manifiestos. Para habilitar los proveedores que desea que registren eventos en la sesión filtrando en condiciones específicas en Windows 8.1,Windows Server 2012 R2 y versiones posteriores, llame a la [**función EnableTraceEx2.**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)

Además, también puede realizar un seguimiento de información adicional sobre un evento con una llamada a la [**función TraceSetInformation.**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) **TraceSetInformation** coloca información de seguimiento adicional en la sección de datos extendidos de un evento y puede incluir información como la información de la versión de seguimiento o qué proveedores están registrados actualmente en el sistema. Para obtener más información, vea [Recuperación de datos de seguimiento de eventos adicionales.](retrieving-additional-event-tracing-data.md)

Hasta ocho sesiones de seguimiento pueden habilitar y recibir eventos del mismo proveedor [basado en](about-event-tracing.md) manifiesto. Sin embargo, solo una sesión de seguimiento puede habilitar un [proveedor](about-event-tracing.md) clásico. Si más de una sesión de seguimiento intenta habilitar un proveedor clásico, la primera sesión dejará de recibir eventos cuando la segunda sesión habilite el proveedor. Por ejemplo, si la sesión A habilitaba el proveedor 1 y la sesión B habilitaba el proveedor 1, solo la sesión B recibiría eventos del proveedor 1.

Puede usar cualquiera de las tres funciones para habilitar un proveedor, pero puede perder la funcionalidad si usa [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para habilitar un proveedor basado en manifiesto porque no podrá proporcionar un valor MatchAllKeyword, especificar elementos de datos extendidos para incluir en el evento o proporcionar datos de filtro definidos por el proveedor. Para obtener más información, vea la sección Comentarios de cada función.

En Windows 8.1,Windows Server 2012 R2 y versiones posteriores, la función [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) y las estructuras [**ENABLE TRACE \_ \_ PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) y [**EVENT \_ FILTER \_ DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) pueden usar filtros de carga de eventos, ámbito y recorrido de pila para filtrar condiciones específicas en una sesión de registrador. Para obtener más información sobre los filtros de carga de eventos, vea las funciones [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)y [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) y las estructuras **ENABLE TRACE \_ \_ PARAMETERS**, **EVENT FILTER \_ \_ DESCRIPTOR** y [**PAYLOAD FILTER \_ \_ PREDICATE.**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

Para determinar el nivel y las palabras clave usadas para habilitar un proveedor basado en manifiestos, use uno de los siguientes comandos:

-   **Logman** **query** *provider-name*
-   **Wevtutil** **gp** *provider-name*

Los comandos solo enumeran el nivel y las palabras clave; el proveedor debe documentar los requisitos de datos de filtro para posibles controladores.

Para enumerar los proveedores basados en manifiestos, use **Wevtutil** **ep**.

En el caso de los proveedores clásicos, es el proveedor el que debe documentar y hacer que esté disponible para los controladores potenciales los niveles de gravedad o habilitar las marcas que admite. Si el proveedor desea que lo habilite cualquier controlador, el proveedor debe aceptar 0 para el nivel de gravedad y habilitar las marcas e interpretar 0 como una solicitud para realizar el registro predeterminado (sea cual sea).

Puede habilitar el proveedor antes o después de que el proveedor se registre a sí mismo. Después de habilitar el proveedor, ETW llamará a la función de devolución de llamada del proveedor. Si el proveedor no está registrado, ETW llamará a la función de devolución de llamada del proveedor después de registrarse.

También puede usar la función [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para deshabilitar el proveedor (impedir que se registrasen eventos en la sesión) o para actualizar el nivel de registro o habilitar las marcas del proveedor. Con la [**función EnableTraceEx,**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) puede deshabilitar el proveedor o actualizar el nivel, las palabras clave, los datos extendidos y los datos de filtro. Cada vez que se llama a **las funciones EnableTrace** **o EnableTraceEx,** ETW llama a la función de devolución de llamada del proveedor. El proveedor permanece habilitado para la sesión hasta que la sesión deshabilita el proveedor.

Para detener la sesión de seguimiento después de recopilar eventos, llame a la [**función ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) y pase EVENT \_ TRACE CONTROL STOP como código de \_ \_ control. Para especificar la sesión que se va a detener, puede pasar el identificador de sesión de seguimiento de eventos obtenido de una llamada anterior a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) o el nombre de una sesión iniciada anteriormente. Asegúrese de deshabilitar todos los proveedores antes de detener la sesión. Si detiene la sesión antes de deshabilitar primero el proveedor, ETW deshabilitará el proveedor e intentará llamar a la función de devolución de llamada de control del proveedor. Si la aplicación que inició la sesión finaliza sin deshabilitar el proveedor ni llamar a la **función ControlTrace,** el proveedor permanece habilitado.

Si [**ControlTrace se**](/windows/win32/api/evntrace/nf-evntrace-controltracea) realiza correctamente, las propiedades de sesión se actualizan para reflejar los valores de propiedad finales y ejecutar estadísticas para la sesión de seguimiento de eventos.

Para obtener un ejemplo que inicia una sesión de seguimiento de eventos, vea lo siguiente:

-   [Ejemplo que crea una](example-that-creates-a-session-and-enables-a-manifest-based-provider.md) sesión y habilita un proveedor basado en manifiestos: inicia una sesión de seguimiento, habilita un proveedor basado en manifiestos, deshabilita el proveedor y, a continuación, detiene la sesión.

Para más información sobre cómo iniciar una sesión de seguimiento, consulte una de las siguientes opciones:

-   [Configuración e inicio de una sesión de SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
-   [Configuración e inicio de la sesión del registrador de kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md)
-   [Configuración e inicio de una sesión de Registrador automático](configuring-and-starting-an-autologger-session.md)
-   [Configuración e inicio de la sesión de registrador global](configuring-and-starting-the-global-logger-session.md)
-   [Configuración e inicio de una sesión de registrador privado](configuring-and-starting-a-private-logger-session.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración e inicio de una sesión de registrador privado](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Configuración e inicio de una sesión de SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configuración e inicio de una sesión de Registrador automático](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Configuración e inicio de la sesión del registrador de kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea)
</dt> <dt>

[**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace)
</dt> <dt>

[**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**HABILITAR \_ PARÁMETROS DE \_ SEGUIMIENTO**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**DESCRIPTOR \_ DE FILTRO DE \_ EVENTOS**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**PROPIEDADES DE \_ SEGUIMIENTO \_ DE EVENTOS**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**PREDICADO \_ DE FILTRO DE CARGA \_ ÚTIL**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Actualizar una sesión de seguimiento de eventos](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
