---
description: La sesión del registrador del kernel de NT es una sesión de seguimiento de eventos que registra un conjunto predefinido de eventos de kernel.
ms.assetid: 3c4258d8-8073-4cc5-a29d-ce485a3fdc14
title: Configuración e inicio de la sesión del registrador del kernel de NT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d13cb0d429bc4b0e01e02c33e2686040f0b7454b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986134"
---
# <a name="configuring-and-starting-the-nt-kernel-logger-session"></a><span data-ttu-id="85e6e-103">Configuración e inicio de la sesión del registrador del kernel de NT</span><span class="sxs-lookup"><span data-stu-id="85e6e-103">Configuring and Starting the NT Kernel Logger Session</span></span>

<span data-ttu-id="85e6e-104">La sesión del registrador del kernel de NT es una sesión de seguimiento de eventos que registra un conjunto predefinido de eventos de kernel.</span><span class="sxs-lookup"><span data-stu-id="85e6e-104">The NT Kernel Logger session is an event tracing session that records a predefined set of kernel events.</span></span> <span data-ttu-id="85e6e-105">No se llama a la función [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para habilitar los proveedores de kernel.</span><span class="sxs-lookup"><span data-stu-id="85e6e-105">You do not call the [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) function to enable the kernel providers.</span></span> <span data-ttu-id="85e6e-106">En su lugar, se usa el miembro **EnableFlags** de la estructura de [**propiedades de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) para especificar los eventos de kernel que se desean recibir.</span><span class="sxs-lookup"><span data-stu-id="85e6e-106">Instead, you use the **EnableFlags** member of [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure to specify the kernel events that you want to receive.</span></span> <span data-ttu-id="85e6e-107">La función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) usa las marcas de habilitación que se especifican para habilitar los proveedores de kernel.</span><span class="sxs-lookup"><span data-stu-id="85e6e-107">The [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function uses the enable flags that you specify to enable the kernel providers.</span></span>

<span data-ttu-id="85e6e-108">Solo hay una sesión del registrador del kernel de NT.</span><span class="sxs-lookup"><span data-stu-id="85e6e-108">There is only one NT Kernel Logger session.</span></span> <span data-ttu-id="85e6e-109">Si la sesión ya está en uso, la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) devuelve el error \_ ya \_ existe.</span><span class="sxs-lookup"><span data-stu-id="85e6e-109">If the session is already in use, the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function returns ERROR\_ALREADY\_EXISTS.</span></span>

<span data-ttu-id="85e6e-110">Para obtener más información sobre cómo iniciar una sesión de seguimiento de eventos, vea [configurar e iniciar una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="85e6e-110">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="85e6e-111">Para obtener información detallada sobre cómo iniciar una sesión de registrador privada, vea [configurar e iniciar una sesión de registrador privado](configuring-and-starting-a-private-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="85e6e-111">For details on starting a private logger session, see [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).</span></span>

<span data-ttu-id="85e6e-112">Para obtener más información sobre cómo iniciar una sesión del registrador global, vea [configurar e iniciar la sesión del registrador global](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="85e6e-112">For details on starting a Global Logger session, see [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="85e6e-113">Para obtener más información sobre cómo iniciar una sesión del registrador automático, vea [configurar e iniciar una sesión de registrador automático](configuring-and-starting-an-autologger-session.md).</span><span class="sxs-lookup"><span data-stu-id="85e6e-113">For details on starting an AutoLogger session, see [Configuring and Starting an AutoLogger Session](configuring-and-starting-an-autologger-session.md).</span></span>

<span data-ttu-id="85e6e-114">En el ejemplo siguiente se muestra cómo configurar e iniciar una sesión del registrador del kernel de NT que recopila eventos de kernel TCP/IP de red y los escribe en un archivo circular de 5 MB.</span><span class="sxs-lookup"><span data-stu-id="85e6e-114">The following example shows how to configure and start an NT Kernel Logger session that collects network TCP/IP kernel events and writes them to a 5MB circular file.</span></span>


```C++
#define INITGUID  // Include this #define to use SystemTraceControlGuid in Evntrace.h.

#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <strsafe.h>
#include <wmistr.h>
#include <evntrace.h>

#define LOGFILE_PATH L"<FULLPATHTOTHELOGFILE.etl>"

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    TRACEHANDLE SessionHandle = 0;
    EVENT_TRACE_PROPERTIES* pSessionProperties = NULL;
    ULONG BufferSize = 0;

    // Allocate memory for the session properties. The memory must
    // be large enough to include the log file name and session name,
    // which get appended to the end of the session properties structure.
    
    BufferSize = sizeof(EVENT_TRACE_PROPERTIES) + sizeof(LOGFILE_PATH) + sizeof(KERNEL_LOGGER_NAME);
    pSessionProperties = (EVENT_TRACE_PROPERTIES*) malloc(BufferSize);    
    if (NULL == pSessionProperties)
    {
        wprintf(L"Unable to allocate %d bytes for properties structure.\n", BufferSize);
        goto cleanup;
    }
    
    // Set the session properties. You only append the log file name
    // to the properties structure; the StartTrace function appends
    // the session name for you.

    ZeroMemory(pSessionProperties, BufferSize);
    pSessionProperties->Wnode.BufferSize = BufferSize;
    pSessionProperties->Wnode.Flags = WNODE_FLAG_TRACED_GUID;
    pSessionProperties->Wnode.ClientContext = 1; //QPC clock resolution
    pSessionProperties->Wnode.Guid = SystemTraceControlGuid; 
    pSessionProperties->EnableFlags = EVENT_TRACE_FLAG_NETWORK_TCPIP;
    pSessionProperties->LogFileMode = EVENT_TRACE_FILE_MODE_CIRCULAR;
    pSessionProperties->MaximumFileSize = 5;  // 5 MB
    pSessionProperties->LoggerNameOffset = sizeof(EVENT_TRACE_PROPERTIES);
    pSessionProperties->LogFileNameOffset = sizeof(EVENT_TRACE_PROPERTIES) + sizeof(KERNEL_LOGGER_NAME); 
    StringCbCopy((LPWSTR)((char*)pSessionProperties + pSessionProperties->LogFileNameOffset), sizeof(LOGFILE_PATH), LOGFILE_PATH);

    // Create the trace session.

    status = StartTrace((PTRACEHANDLE)&SessionHandle, KERNEL_LOGGER_NAME, pSessionProperties);

    if (ERROR_SUCCESS != status)
    {
        if (ERROR_ALREADY_EXISTS == status)
        {
            wprintf(L"The NT Kernel Logger session is already in use.\n");
        }
        else
        {
            wprintf(L"EnableTrace() failed with %lu\n", status);
        }

        goto cleanup;
    }

    wprintf(L"Press any key to end trace session ");
    _getch();

cleanup:

    if (SessionHandle)
    {
        status = ControlTrace(SessionHandle, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_STOP);

        if (ERROR_SUCCESS != status)
        {
            wprintf(L"ControlTrace(stop) failed with %lu\n", status);
        }
    }

    if (pSessionProperties)
        free(pSessionProperties);
}
```



## <a name="related-topics"></a><span data-ttu-id="85e6e-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="85e6e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85e6e-116">Configurar e iniciar una sesión de registrador privado</span><span class="sxs-lookup"><span data-stu-id="85e6e-116">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="85e6e-117">Configurar e iniciar una sesión de SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="85e6e-117">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="85e6e-118">Configurar e iniciar una sesión de registrador automático</span><span class="sxs-lookup"><span data-stu-id="85e6e-118">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="85e6e-119">Configurar e iniciar una sesión de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="85e6e-119">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="85e6e-120">Actualizar una sesión de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="85e6e-120">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
