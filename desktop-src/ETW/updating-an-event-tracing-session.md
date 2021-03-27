---
description: Para actualizar las propiedades de una sesión de seguimiento de eventos, llame a la función ControlTrace con el código de control de actualización de control de seguimiento de eventos \_ \_ \_ .
ms.assetid: 1496bf88-a989-4fa1-888a-90385c4ca8ee
title: Actualizar una sesión de seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e580c2e84dec6682e5fad323fe0cad427300a21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001334"
---
# <a name="updating-an-event-tracing-session"></a><span data-ttu-id="999f3-103">Actualizar una sesión de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="999f3-103">Updating an Event Tracing Session</span></span>

<span data-ttu-id="999f3-104">Para actualizar las propiedades de una sesión de seguimiento de eventos, llame a la función [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) con el código de control de **actualización de control de seguimiento de eventos \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="999f3-104">To update the properties of an event tracing session, call the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) function using the **EVENT\_TRACE\_CONTROL\_UPDATE** control code.</span></span> <span data-ttu-id="999f3-105">Puede especificar la sesión que se va a actualizar mediante un identificador de sesión Obtenido de una llamada anterior a [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)o un nombre de sesión.</span><span class="sxs-lookup"><span data-stu-id="999f3-105">You can specify the session to update using a session handle obtained from an earlier call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), or a session name.</span></span> <span data-ttu-id="999f3-106">Las propiedades de la sesión de seguimiento de eventos se actualizan con los valores especificados en la estructura de [**\_ \_ propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .</span><span class="sxs-lookup"><span data-stu-id="999f3-106">The properties of the event tracing session are updated using the values specified in the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span> <span data-ttu-id="999f3-107">Solo puede actualizar un subconjunto de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="999f3-107">You can update only a subset of the properties.</span></span> <span data-ttu-id="999f3-108">Para obtener una lista de las propiedades que se pueden actualizar, vea el parámetro *Properties* de la función **ControlTrace** .</span><span class="sxs-lookup"><span data-stu-id="999f3-108">For a list of the properties you can update, see the *Properties* parameter of the **ControlTrace** function.</span></span>

<span data-ttu-id="999f3-109">Si la llamada a [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) se realiza correctamente, la estructura de [**propiedades de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) se actualiza para reflejar los nuevos valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="999f3-109">If the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) call is successful, the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure is updated to reflect the new property values.</span></span> <span data-ttu-id="999f3-110">La estructura también contendrá las nuevas estadísticas de ejecución de la sesión de seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="999f3-110">The structure will also contain the new run statistics for the event tracing session.</span></span>

<span data-ttu-id="999f3-111">En el ejemplo siguiente se muestra cómo actualizar la sesión de seguimiento de eventos de kernel.</span><span class="sxs-lookup"><span data-stu-id="999f3-111">The following example shows how to update the kernel event tracing session.</span></span> <span data-ttu-id="999f3-112">En el ejemplo se consultan los valores de propiedad actuales y se actualiza la estructura antes de actualizar la sesión.</span><span class="sxs-lookup"><span data-stu-id="999f3-112">The example queries for the current property values and updates the structure before updating the session.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <wmistr.h>
#include <evntrace.h>

#define MAX_SESSION_NAME_LEN 1024
#define MAX_LOGFILE_PATH_LEN 1024

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    EVENT_TRACE_PROPERTIES* pSessionProperties = NULL;
    ULONG BufferSize = 0;

    // Allocate memory for the session properties. The memory must
    // be large enough to include the log file name and session name.
    // This example specifies the maximum size for the session name 
    // and log file name.
    
    BufferSize = sizeof(EVENT_TRACE_PROPERTIES) + 
        (MAX_SESSION_NAME_LEN * sizeof(WCHAR)) + 
        (MAX_LOGFILE_PATH_LEN * sizeof(WCHAR));

    pSessionProperties = (EVENT_TRACE_PROPERTIES*) malloc(BufferSize);    
    if (NULL == pSessionProperties)
    {
        wprintf(L"Unable to allocate %d bytes for properties structure.\n", BufferSize);
        goto cleanup;
    }
    
    ZeroMemory(pSessionProperties, BufferSize);
    pSessionProperties->Wnode.BufferSize = BufferSize;

    // Query for the kernel trace session's current property values.

    status = ControlTrace((TRACEHANDLE)NULL, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_QUERY);

    if (ERROR_SUCCESS != status)
    {
        if (ERROR_WMI_INSTANCE_NOT_FOUND == status)
        {
            wprintf(L"The Kernel Logger is not running.\n");
        }
        else
        {
            wprintf(L"ControlTrace(query) failed with %lu\n", status);
        }

        goto cleanup;
    }

    // Update the enable flags to also enable the Process and Thread providers.

    pSessionProperties->LogFileNameOffset = 0;  // Zero tells ETW not to update the file name
    pSessionProperties->Wnode.Flags = WNODE_FLAG_TRACED_GUID;
    pSessionProperties->EnableFlags |= EVENT_TRACE_FLAG_PROCESS | EVENT_TRACE_FLAG_THREAD;

    // Update the session's properties.

    status = ControlTrace((TRACEHANDLE)NULL, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_UPDATE);
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"ControlTrace(update) failed with %lu.\n", status);
        goto cleanup;
    }

    wprintf(L"\nUpdated session");

cleanup:

    if (pSessionProperties)
    {
        free(pSessionProperties);
        pSessionProperties = NULL;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="999f3-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="999f3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="999f3-114">Configurar e iniciar una sesión de registrador privado</span><span class="sxs-lookup"><span data-stu-id="999f3-114">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="999f3-115">Configurar e iniciar una sesión de SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="999f3-115">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="999f3-116">Configurar e iniciar una sesión de registrador automático</span><span class="sxs-lookup"><span data-stu-id="999f3-116">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="999f3-117">Configurar e iniciar una sesión de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="999f3-117">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="999f3-118">Configuración e inicio de la sesión del registrador del kernel de NT</span><span class="sxs-lookup"><span data-stu-id="999f3-118">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> </dl>

 

 
