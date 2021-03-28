---
description: SystemTraceProvider es un proveedor de kernel con un conjunto predefinido de eventos de kernel compatibles con Windows 7, Windows Server 2008 R2 y versiones posteriores.
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: Configurar e iniciar una sesión de SystemTraceProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b718269801a7677572e7bb5b74cd8b89d3711e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984515"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a>Configurar e iniciar una sesión de SystemTraceProvider

SystemTraceProvider es un proveedor de kernel con un conjunto predefinido de eventos de kernel compatibles con Windows 7, Windows Server 2008 R2 y versiones posteriores. En Windows 7 y Windows Server 2008 R2, SystemTraceProvider solo se podía usar para la sesión del registrador del kernel de NT.

En Windows 8, Windows Server 2012 y versiones posteriores, SystemTraceProvider se puede multiplexar hasta 8 sesiones de registrador. Las dos primeras ranuras para las sesiones del registrador se reservan para el registrador del kernel de NT y el registrador de contexto circular del kernel.

Para obtener más información sobre el uso de la sesión del registrador del kernel de NT como proveedor de seguimiento, vea [configurar e iniciar la sesión del registrador del kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md).

Para permitir que SystemTraceProvider inicie una sesión que no sea el registrador del kernel de NT, ejecute el siguiente comando.

**tracelog-Start mi sesión-f c: \\ Kernel1. ETL-EFLAG proc \_ Thread + Loader + CSWITCH**

Para habilitar mediante programación la SystemTraceProvider para iniciar una sesión que no sea el registrador del kernel de NT, siga estos pasos.

-   Defina un nombre de registrador privado.

    **\#definir \_ el nombre del registrador privado \_ "Some sesión de seguimiento privado"**

-   En el controlador, establezca los siguientes miembros de la estructura de [**\_ \_ propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .

    Establezca **LogFileMode** en **\_ modo de \_ \_ registrador \_ del sistema de seguimiento de eventos**.

    Establezca **LoggerName** en registrador privado, en lugar **del \_ \_ nombre del registrador de kernel**.

    Asegúrese de que el miembro **Wnode. GUID** de la estructura de [**\_ \_ propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) no está establecido en **SystemTraceControlGuid**. Debe asignar un nuevo **GUID** a este miembro.

-   En el consumidor, establezca el miembro **LoggerName** de la estructura de archivo de [**\_ \_ registro de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) en este registrador privado.

> [!Note]  
> Si desea que un proceso que no sea de administrador o que no sea TCB pueda iniciar una sesión de seguimiento de generación de perfiles con el SystemTraceProvider en nombre de aplicaciones de terceros, debe conceder el privilegio de Perfil de usuario y, a continuación, agregar este usuario tanto al **GUID** de sesión (creado para la sesión del registrador) como al **GUID** del proveedor de seguimiento del sistema para habilitar el proveedor de Para obtener más información, vea la función [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) .

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configurar e iniciar una sesión de registrador privado](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Configurar e iniciar una sesión de registrador automático](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Configurar e iniciar una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Configuración e inicio de la sesión del registrador del kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[Actualizar una sesión de seguimiento de eventos](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
