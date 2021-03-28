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
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a><span data-ttu-id="6e531-103">Configurar e iniciar una sesión de SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="6e531-103">Configuring and Starting a SystemTraceProvider Session</span></span>

<span data-ttu-id="6e531-104">SystemTraceProvider es un proveedor de kernel con un conjunto predefinido de eventos de kernel compatibles con Windows 7, Windows Server 2008 R2 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="6e531-104">The SystemTraceProvider is a kernel provider with a predefined sets of kernel events supported on Windows 7, Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="6e531-105">En Windows 7 y Windows Server 2008 R2, SystemTraceProvider solo se podía usar para la sesión del registrador del kernel de NT.</span><span class="sxs-lookup"><span data-stu-id="6e531-105">On Windows 7 and Windows Server 2008 R2, the SystemTraceProvider could only be used for the NT Kernel Logger session.</span></span>

<span data-ttu-id="6e531-106">En Windows 8, Windows Server 2012 y versiones posteriores, SystemTraceProvider se puede multiplexar hasta 8 sesiones de registrador.</span><span class="sxs-lookup"><span data-stu-id="6e531-106">On Windows 8, Windows Server 2012, and later, the SystemTraceProvider can be multiplexed for up to 8 logger sessions.</span></span> <span data-ttu-id="6e531-107">Las dos primeras ranuras para las sesiones del registrador se reservan para el registrador del kernel de NT y el registrador de contexto circular del kernel.</span><span class="sxs-lookup"><span data-stu-id="6e531-107">The first two slots for logger sessions are reserved for the NT Kernel Logger and the Circular Kernel Context Logger .</span></span>

<span data-ttu-id="6e531-108">Para obtener más información sobre el uso de la sesión del registrador del kernel de NT como proveedor de seguimiento, vea [configurar e iniciar la sesión del registrador del kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="6e531-108">For more information on using the NT Kernel Logger session as a trace provider, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="6e531-109">Para permitir que SystemTraceProvider inicie una sesión que no sea el registrador del kernel de NT, ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="6e531-109">To enable the SystemTraceProvider to start a session other than the NT Kernel Logger, execute the following command.</span></span>

<span data-ttu-id="6e531-110">**tracelog-Start mi sesión-f c: \\ Kernel1. ETL-EFLAG proc \_ Thread + Loader + CSWITCH**</span><span class="sxs-lookup"><span data-stu-id="6e531-110">**tracelog -start MySession -f c:\\Kernel1.etl -eflag PROC\_THREAD+LOADER+CSWITCH**</span></span>

<span data-ttu-id="6e531-111">Para habilitar mediante programación la SystemTraceProvider para iniciar una sesión que no sea el registrador del kernel de NT, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="6e531-111">To programmatically enable the SystemTraceProvider to start a session other than the NT Kernel Logger, use the following steps.</span></span>

-   <span data-ttu-id="6e531-112">Defina un nombre de registrador privado.</span><span class="sxs-lookup"><span data-stu-id="6e531-112">Define a private logger name.</span></span>

    <span data-ttu-id="6e531-113">**\#definir \_ el nombre del registrador privado \_ "Some sesión de seguimiento privado"**</span><span class="sxs-lookup"><span data-stu-id="6e531-113">**\#define PRIVATE\_LOGGER\_NAME L”Some Private Trace Session”**</span></span>

-   <span data-ttu-id="6e531-114">En el controlador, establezca los siguientes miembros de la estructura de [**\_ \_ propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .</span><span class="sxs-lookup"><span data-stu-id="6e531-114">At the controller, set the following members of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

    <span data-ttu-id="6e531-115">Establezca **LogFileMode** en **\_ modo de \_ \_ registrador \_ del sistema de seguimiento de eventos**.</span><span class="sxs-lookup"><span data-stu-id="6e531-115">Set **LogFileMode** to **EVENT\_TRACE\_SYSTEM\_LOGGER\_MODE**.</span></span>

    <span data-ttu-id="6e531-116">Establezca **LoggerName** en registrador privado, en lugar **del \_ \_ nombre del registrador de kernel**.</span><span class="sxs-lookup"><span data-stu-id="6e531-116">Set **LoggerName** to private logger, instead of **KERNEL\_LOGGER\_NAME**.</span></span>

    <span data-ttu-id="6e531-117">Asegúrese de que el miembro **Wnode. GUID** de la estructura de [**\_ \_ propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) no está establecido en **SystemTraceControlGuid**.</span><span class="sxs-lookup"><span data-stu-id="6e531-117">Make sure the **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure is not set to **SystemTraceControlGuid**.</span></span> <span data-ttu-id="6e531-118">Debe asignar un nuevo **GUID** a este miembro.</span><span class="sxs-lookup"><span data-stu-id="6e531-118">You must assign a new **GUID** to this member.</span></span>

-   <span data-ttu-id="6e531-119">En el consumidor, establezca el miembro **LoggerName** de la estructura de archivo de [**\_ \_ registro de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) en este registrador privado.</span><span class="sxs-lookup"><span data-stu-id="6e531-119">At the consumer, set the **LoggerName** member of the [**EVENT\_TRACE\_LOGFILE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) structure to this private logger.</span></span>

> [!Note]  
> <span data-ttu-id="6e531-120">Si desea que un proceso que no sea de administrador o que no sea TCB pueda iniciar una sesión de seguimiento de generación de perfiles con el SystemTraceProvider en nombre de aplicaciones de terceros, debe conceder el privilegio de Perfil de usuario y, a continuación, agregar este usuario tanto al **GUID** de sesión (creado para la sesión del registrador) como al **GUID** del proveedor de seguimiento del sistema para habilitar el proveedor de</span><span class="sxs-lookup"><span data-stu-id="6e531-120">If you want a non-administrators or a non-TCB process to be able to start a profiling trace session using the SystemTraceProvider on behalf of third party applications, then you need to grant the user profile privilege and then add this user to both the session **GUID** (created for the logger session) and the system trace provider **GUID** to enable the system trace provider.</span></span> <span data-ttu-id="6e531-121">Para obtener más información, vea la función [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="6e531-121">For more information, see the [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6e531-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6e531-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e531-123">Configurar e iniciar una sesión de registrador privado</span><span class="sxs-lookup"><span data-stu-id="6e531-123">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="6e531-124">Configurar e iniciar una sesión de registrador automático</span><span class="sxs-lookup"><span data-stu-id="6e531-124">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="6e531-125">Configurar e iniciar una sesión de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="6e531-125">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="6e531-126">Configuración e inicio de la sesión del registrador del kernel de NT</span><span class="sxs-lookup"><span data-stu-id="6e531-126">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="6e531-127">Actualizar una sesión de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="6e531-127">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
