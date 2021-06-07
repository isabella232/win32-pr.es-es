---
description: SystemTraceProvider es un proveedor de kernel con conjuntos predefinidos de eventos de kernel compatibles con Windows 7, Windows Server 2008 R2 y versiones posteriores.
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: Configuración e inicio de una sesión de SystemTraceProvider
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 66e9d672a7c8e6358c2a92e7661e0d4e2a5878ab
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386745"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a>Configuración e inicio de una sesión de SystemTraceProvider

SystemTraceProvider es un proveedor de kernel con conjuntos predefinidos de eventos de kernel compatibles con Windows 7, Windows Server 2008 R2 y versiones posteriores. En Windows 7 y Windows Server 2008 R2, SystemTraceProvider solo se podía usar para la sesión del registrador de kernel de NT.

En Windows 8, Windows Server 2012 y versiones posteriores, SystemTraceProvider se puede multiplexar para hasta 8 sesiones de registrador. Las dos primeras ranuras para las sesiones de registrador están reservadas para el registrador de kernel nt y el registrador de contexto de kernel circular .

Para obtener más información sobre el uso de la sesión nt kernel Logger como proveedor de seguimiento, vea [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).

En Windows 10 SDK 20348 y versiones posteriores, SystemTraceProvider se puede configurar a través de proveedores de sistema independientes, que se pueden controlar con [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) como proveedores de eventos Seguimiento de eventos para Windows estándar. Para obtener una lista completa de los proveedores del sistema, las palabras clave y los grupos heredados correspondientes, consulte [Proveedores de sistemas.](system-providers.md)

## <a name="enable-a-systemtraceprovider-session"></a>Habilitación de una sesión de SystemTraceProvider

Para permitir que SystemTraceProvider inicie una sesión que no sea el registrador de kernel de NT, ejecute el siguiente comando:

**tracelog -start MySession -f c: \\ Kernel1.etl -eflag PROC \_ THREAD+LOADER+CSWITCH**

Para permitir mediante programación que SystemTraceProvider inicie una sesión que no sea el registrador de kernel de NT, siga estos pasos.

-   Defina un nombre de registrador privado.

    **\#define PRIVATE \_ LOGGER \_ NAME L"Some Private Trace Session"**

-   En el controlador, establezca los siguientes miembros de la [**estructura EVENT \_ TRACE \_ PROPERTIES.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)

    Establezca **LogFileMode en** **EVENT TRACE SYSTEM \_ \_ \_ LOGGER \_ MODE**.

    Establezca **LoggerName en** registrador privado, en lugar de **KERNEL \_ LOGGER \_ NAME**.

    Asegúrese de que **el miembro Wnode.Guid** de la [**estructura EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) no está establecido en **SystemTraceControlGuid.** Debe asignar un nuevo **GUID** a este miembro.

-   En el consumidor, establezca el miembro **LoggerName** de la estructura [**\_ \_ LOGFILE de EVENT TRACE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) en este registrador privado.

> [!Note]  
> Si desea que un proceso que no sea de administrador o que no sea TCB pueda iniciar una sesión de seguimiento de generación de perfiles mediante SystemTraceProvider en nombre de aplicaciones de terceros, debe conceder el privilegio de perfil de usuario y, a continuación, agregar este usuario tanto al **GUID** de sesión (creado para la sesión del registrador) como al **GUID** del proveedor de seguimiento del sistema para habilitar el proveedor de seguimiento del sistema. Para obtener más información, vea [**la función EventAccessControl.**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol)

 

## <a name="related-topics"></a>Temas relacionados

[Configuración e inicio de una sesión de registrador privado](configuring-and-starting-a-private-logger-session.md)

[Configuración e inicio de una sesión de Registrador automático](configuring-and-starting-an-autologger-session.md)

[Configuración e inicio de una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md)

[Configuración e inicio de la sesión del registrador de kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md)

[Proveedores de sistemas](system-providers.md)

[Actualizar una sesión de seguimiento de eventos](updating-an-event-tracing-session.md)

 

 
