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
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a><span data-ttu-id="5dbb8-103">Configuración e inicio de una sesión de SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="5dbb8-103">Configuring and Starting a SystemTraceProvider Session</span></span>

<span data-ttu-id="5dbb8-104">SystemTraceProvider es un proveedor de kernel con conjuntos predefinidos de eventos de kernel compatibles con Windows 7, Windows Server 2008 R2 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="5dbb8-104">The SystemTraceProvider is a kernel provider with a predefined sets of kernel events supported on Windows 7, Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="5dbb8-105">En Windows 7 y Windows Server 2008 R2, SystemTraceProvider solo se podía usar para la sesión del registrador de kernel de NT.</span><span class="sxs-lookup"><span data-stu-id="5dbb8-105">On Windows 7 and Windows Server 2008 R2, the SystemTraceProvider could only be used for the NT Kernel Logger session.</span></span>

<span data-ttu-id="5dbb8-106">En Windows 8, Windows Server 2012 y versiones posteriores, SystemTraceProvider se puede multiplexar para hasta 8 sesiones de registrador.</span><span class="sxs-lookup"><span data-stu-id="5dbb8-106">On Windows 8, Windows Server 2012, and later, the SystemTraceProvider can be multiplexed for up to 8 logger sessions.</span></span> <span data-ttu-id="5dbb8-107">Las dos primeras ranuras para las sesiones de registrador están reservadas para el registrador de kernel nt y el registrador de contexto de kernel circular .</span><span class="sxs-lookup"><span data-stu-id="5dbb8-107">The first two slots for logger sessions are reserved for the NT Kernel Logger and the Circular Kernel Context Logger .</span></span>

<span data-ttu-id="5dbb8-108">Para obtener más información sobre el uso de la sesión nt kernel Logger como proveedor de seguimiento, vea [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="5dbb8-108">For more information on using the NT Kernel Logger session as a trace provider, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="5dbb8-109">En Windows 10 SDK 20348 y versiones posteriores, SystemTraceProvider se puede configurar a través de proveedores de sistema independientes, que se pueden controlar con [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) como proveedores de eventos Seguimiento de eventos para Windows estándar.</span><span class="sxs-lookup"><span data-stu-id="5dbb8-109">On Windows 10 SDK build 20348 and later, the SystemTraceProvider can be configured via separate System Providers, which can be controlled with [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) like standard Event Tracing for Windows event providers.</span></span> <span data-ttu-id="5dbb8-110">Para obtener una lista completa de los proveedores del sistema, las palabras clave y los grupos heredados correspondientes, consulte [Proveedores de sistemas.](system-providers.md)</span><span class="sxs-lookup"><span data-stu-id="5dbb8-110">For a full list of system providers, keywords, and corresponding legacy flags and groups, see [System Providers](system-providers.md)</span></span>

## <a name="enable-a-systemtraceprovider-session"></a><span data-ttu-id="5dbb8-111">Habilitación de una sesión de SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="5dbb8-111">Enable a SystemTraceProvider session</span></span>

<span data-ttu-id="5dbb8-112">Para permitir que SystemTraceProvider inicie una sesión que no sea el registrador de kernel de NT, ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="5dbb8-112">To enable the SystemTraceProvider to start a session other than the NT Kernel Logger, execute the following command:</span></span>

<span data-ttu-id="5dbb8-113">**tracelog -start MySession -f c: \\ Kernel1.etl -eflag PROC \_ THREAD+LOADER+CSWITCH**</span><span class="sxs-lookup"><span data-stu-id="5dbb8-113">**tracelog -start MySession -f c:\\Kernel1.etl -eflag PROC\_THREAD+LOADER+CSWITCH**</span></span>

<span data-ttu-id="5dbb8-114">Para permitir mediante programación que SystemTraceProvider inicie una sesión que no sea el registrador de kernel de NT, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="5dbb8-114">To programmatically enable the SystemTraceProvider to start a session other than the NT Kernel Logger, use the following steps.</span></span>

-   <span data-ttu-id="5dbb8-115">Defina un nombre de registrador privado.</span><span class="sxs-lookup"><span data-stu-id="5dbb8-115">Define a private logger name.</span></span>

    <span data-ttu-id="5dbb8-116">**\#define PRIVATE \_ LOGGER \_ NAME L"Some Private Trace Session"**</span><span class="sxs-lookup"><span data-stu-id="5dbb8-116">**\#define PRIVATE\_LOGGER\_NAME L”Some Private Trace Session”**</span></span>

-   <span data-ttu-id="5dbb8-117">En el controlador, establezca los siguientes miembros de la [**estructura EVENT \_ TRACE \_ PROPERTIES.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)</span><span class="sxs-lookup"><span data-stu-id="5dbb8-117">At the controller, set the following members of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

    <span data-ttu-id="5dbb8-118">Establezca **LogFileMode en** **EVENT TRACE SYSTEM \_ \_ \_ LOGGER \_ MODE**.</span><span class="sxs-lookup"><span data-stu-id="5dbb8-118">Set **LogFileMode** to **EVENT\_TRACE\_SYSTEM\_LOGGER\_MODE**.</span></span>

    <span data-ttu-id="5dbb8-119">Establezca **LoggerName en** registrador privado, en lugar de **KERNEL \_ LOGGER \_ NAME**.</span><span class="sxs-lookup"><span data-stu-id="5dbb8-119">Set **LoggerName** to private logger, instead of **KERNEL\_LOGGER\_NAME**.</span></span>

    <span data-ttu-id="5dbb8-120">Asegúrese de que **el miembro Wnode.Guid** de la [**estructura EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) no está establecido en **SystemTraceControlGuid.**</span><span class="sxs-lookup"><span data-stu-id="5dbb8-120">Make sure the **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure is not set to **SystemTraceControlGuid**.</span></span> <span data-ttu-id="5dbb8-121">Debe asignar un nuevo **GUID** a este miembro.</span><span class="sxs-lookup"><span data-stu-id="5dbb8-121">You must assign a new **GUID** to this member.</span></span>

-   <span data-ttu-id="5dbb8-122">En el consumidor, establezca el miembro **LoggerName** de la estructura [**\_ \_ LOGFILE de EVENT TRACE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) en este registrador privado.</span><span class="sxs-lookup"><span data-stu-id="5dbb8-122">At the consumer, set the **LoggerName** member of the [**EVENT\_TRACE\_LOGFILE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) structure to this private logger.</span></span>

> [!Note]  
> <span data-ttu-id="5dbb8-123">Si desea que un proceso que no sea de administrador o que no sea TCB pueda iniciar una sesión de seguimiento de generación de perfiles mediante SystemTraceProvider en nombre de aplicaciones de terceros, debe conceder el privilegio de perfil de usuario y, a continuación, agregar este usuario tanto al **GUID** de sesión (creado para la sesión del registrador) como al **GUID** del proveedor de seguimiento del sistema para habilitar el proveedor de seguimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="5dbb8-123">If you want a non-administrators or a non-TCB process to be able to start a profiling trace session using the SystemTraceProvider on behalf of third party applications, then you need to grant the user profile privilege and then add this user to both the session **GUID** (created for the logger session) and the system trace provider **GUID** to enable the system trace provider.</span></span> <span data-ttu-id="5dbb8-124">Para obtener más información, vea [**la función EventAccessControl.**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol)</span><span class="sxs-lookup"><span data-stu-id="5dbb8-124">For more information, see the [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5dbb8-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5dbb8-125">Related topics</span></span>

[<span data-ttu-id="5dbb8-126">Configuración e inicio de una sesión de registrador privado</span><span class="sxs-lookup"><span data-stu-id="5dbb8-126">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)

[<span data-ttu-id="5dbb8-127">Configuración e inicio de una sesión de Registrador automático</span><span class="sxs-lookup"><span data-stu-id="5dbb8-127">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)

[<span data-ttu-id="5dbb8-128">Configuración e inicio de una sesión de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="5dbb8-128">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)

[<span data-ttu-id="5dbb8-129">Configuración e inicio de la sesión del registrador de kernel de NT</span><span class="sxs-lookup"><span data-stu-id="5dbb8-129">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)

[<span data-ttu-id="5dbb8-130">Proveedores de sistemas</span><span class="sxs-lookup"><span data-stu-id="5dbb8-130">System Providers</span></span>](system-providers.md)

[<span data-ttu-id="5dbb8-131">Actualizar una sesión de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="5dbb8-131">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)

 

 
