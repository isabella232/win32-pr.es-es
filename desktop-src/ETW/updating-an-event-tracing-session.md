---
description: Para actualizar las propiedades de una sesión de seguimiento de eventos, llame a la función ControlTrace mediante el código de control EVENT \_ TRACE \_ CONTROL \_ UPDATE.
ms.assetid: 1496bf88-a989-4fa1-888a-90385c4ca8ee
title: Actualizar una sesión de seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa4f092211d59dda080906f01380f8751fbc099f79dc8f1cd8ea1f7a2ba36fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383345"
---
# <a name="updating-an-event-tracing-session"></a>Actualizar una sesión de seguimiento de eventos

Para actualizar las propiedades de una sesión de seguimiento de eventos, llame a la [**función ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) mediante el código de control **EVENT TRACE CONTROL \_ \_ \_ UPDATE.** Puede especificar la sesión que se va a actualizar mediante un identificador de sesión obtenido de una llamada anterior a [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)o un nombre de sesión. Las propiedades de la sesión de seguimiento de eventos se actualizan con los valores especificados en la [**estructura EVENT \_ TRACE \_ PROPERTIES.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) Solo puede actualizar un subconjunto de las propiedades. Para obtener una lista de las propiedades que puede actualizar, vea el *parámetro Properties* de la **función ControlTrace.**

Si la [**llamada a ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) se realiza correctamente, la [**estructura EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) se actualiza para reflejar los nuevos valores de propiedad. La estructura también contendrá las nuevas estadísticas de ejecución para la sesión de seguimiento de eventos.

En el ejemplo siguiente se muestra cómo actualizar la sesión de seguimiento de eventos de kernel. En el ejemplo se consultan los valores de propiedad actuales y se actualiza la estructura antes de actualizar la sesión.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración e inicio de una sesión de registrador privado](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Configuración e inicio de una sesión de SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configuración e inicio de una sesión de Registrador automático](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Configuración e inicio de una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Configuración e inicio de la sesión del registrador de kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> </dl>

 

 
