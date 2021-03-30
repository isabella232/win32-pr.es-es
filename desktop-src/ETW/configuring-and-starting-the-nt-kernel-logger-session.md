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
# <a name="configuring-and-starting-the-nt-kernel-logger-session"></a>Configuración e inicio de la sesión del registrador del kernel de NT

La sesión del registrador del kernel de NT es una sesión de seguimiento de eventos que registra un conjunto predefinido de eventos de kernel. No se llama a la función [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para habilitar los proveedores de kernel. En su lugar, se usa el miembro **EnableFlags** de la estructura de [**propiedades de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) para especificar los eventos de kernel que se desean recibir. La función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) usa las marcas de habilitación que se especifican para habilitar los proveedores de kernel.

Solo hay una sesión del registrador del kernel de NT. Si la sesión ya está en uso, la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) devuelve el error \_ ya \_ existe.

Para obtener más información sobre cómo iniciar una sesión de seguimiento de eventos, vea [configurar e iniciar una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md).

Para obtener información detallada sobre cómo iniciar una sesión de registrador privada, vea [configurar e iniciar una sesión de registrador privado](configuring-and-starting-a-private-logger-session.md).

Para obtener más información sobre cómo iniciar una sesión del registrador global, vea [configurar e iniciar la sesión del registrador global](configuring-and-starting-the-global-logger-session.md).

Para obtener más información sobre cómo iniciar una sesión del registrador automático, vea [configurar e iniciar una sesión de registrador automático](configuring-and-starting-an-autologger-session.md).

En el ejemplo siguiente se muestra cómo configurar e iniciar una sesión del registrador del kernel de NT que recopila eventos de kernel TCP/IP de red y los escribe en un archivo circular de 5 MB.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configurar e iniciar una sesión de registrador privado](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Configurar e iniciar una sesión de SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configurar e iniciar una sesión de registrador automático](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Configurar e iniciar una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Actualizar una sesión de seguimiento de eventos](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
