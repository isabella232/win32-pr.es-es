---
description: Seguimiento de eventos en DirectShow
ms.assetid: e78c4514-25f4-441d-bfd0-6dac4f7567fd
title: Seguimiento de eventos en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c567d8a2e75d838570323d8ad6be04f11502c9c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255230"
---
# <a name="event-tracing-in-directshow"></a>Seguimiento de eventos en DirectShow

DirectShow seguimiento de eventos para Windows (ETW), que se puede usar para crear registros de eventos para instrumentación o depuración. Para más información sobre ETW, consulte la documentación Windows SDK. Para consumir eventos ETW en una DirectShow, debe habilitar el seguimiento y, a continuación, procesar los eventos de seguimiento. Siga los pasos que se describen a continuación.

**Establecer las claves del Registro necesarias**

Para habilitar el seguimiento en el equipo del usuario, establezca primero las siguientes claves del Registro:


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\DirectX
    GlitchInstrumentation = 0x00000001 (REG_DWORD)
HKEY_LOCAL_MACHINE\SOFTWARE\DEBUG\Quartz.dll
    PERFLOG = 0x00000001 (REG_DWORD) 
```



Estas claves se aplican a los archivos binarios de versión y depuración.

**Habilitar el seguimiento en la aplicación**

Para habilitar el seguimiento en la aplicación, realice los pasos siguientes:

1.  Llame **a StartTrace** para iniciar una nueva sesión de seguimiento.
2.  Llame **a EnableTrace** para habilitar el seguimiento. El GUID del proveedor DirectShow es GUID \_ DSHOW \_ CTL.
3.  Antes de que se cierre la aplicación, llame a **StopTrace** para cerrar la sesión de seguimiento.

**Procesar los eventos**

Para procesar los eventos, realice los pasos siguientes:

1.  Llame **a OpenTrace** para abrir el seguimiento para su procesamiento.
2.  Llame **a ProcessTrace** para procesar los eventos.
3.  En la devolución de llamada de **ProcessTrace,** use el GUID del evento para buscar el tipo de evento. El GUID del evento indica la estructura que se usa para los datos del evento. Consulte [GUID de eventos de seguimiento.](trace-guids.md)
4.  Llame **a CloseTrace** para cerrar el identificador de seguimiento.

**Código de ejemplo**

En el código siguiente se muestra una clase auxiliar que habilita el seguimiento. Este código muestra cómo escribir eventos en un archivo de registro, que se puede procesar una vez completada la sesión. También puede procesar eventos en tiempo real. Para obtener más información, consulte la documentación de ETW en Windows SDK.


```C++
#include <wmistr.h>
#include <evntrace.h>
#include <perfstruct.h>

// Event classes. These are defined in dxmperf.h.
#ifndef DXMPERF_VIDEOREND
#define DXMPERF_VIDEOREND   0x00000001
#endif

#ifndef AUDIOBREAK_BIT
#define AUDIOBREAK_BIT      0x00000010
#endif

// This structure extends the EVENT_TRACE_PROPERTIES by adding fields
// for the name of the WMI session name and the log file.
struct PERFMON_LOGGERINFO
{
    EVENT_TRACE_PROPERTIES TraceProperties;
    WCHAR wcSessionName[ MAX_PATH ];    // Session name.
    WCHAR wcLogFileName[ MAX_PATH ];    // Log file.
};

// Helper class for DirectShow event tracing.
class CTrace
{
public:
    CTrace() : m_SessionLogger((TRACEHANDLE) INVALID_HANDLE_VALUE)
    {
        ZeroMemory(&m_LogInfo, sizeof(&m_LogInfo));
    }

    // Start: Starts a trace session.
    HRESULT Start(WCHAR *wszLogFile)
    {
        const WCHAR* wszSessionName = L"PerfMon_DirectShow"; 
        HRESULT hr = S_OK;
        ULONG result; 

        ZeroMemory(&m_LogInfo, sizeof(m_LogInfo));
        
        EVENT_TRACE_PROPERTIES& prop = m_LogInfo.TraceProperties;

        prop.Wnode.BufferSize = sizeof(m_LogInfo);  // Size of the structure.
        prop.Wnode.Flags = WNODE_FLAG_TRACED_GUID;  // Must be this value.

        // Use the QPC (high resolution timer).
        prop.Wnode.ClientContext = 1;        

        prop.Wnode.Guid = GUID_DSHOW_CTL;           // Event provider GUID.
        prop.LogFileMode = 
            EVENT_TRACE_FILE_MODE_CIRCULAR | EVENT_TRACE_USE_PAGED_MEMORY; 
        prop.EnableFlags = 
            EVENT_TRACE_FLAG_PROCESS;   // Process events.

        // Set the offset from the start of the structure to the log file name.
        prop.LogFileNameOffset = 
            sizeof(m_LogInfo.TraceProperties) + sizeof(m_LogInfo.wcSessionName);  

        // Set the offset from the start of the structure to the session name.
        prop.LoggerNameOffset = sizeof(m_LogInfo.TraceProperties); 

        // Copy the names into the structure.
        StringCchCopy(m_LogInfo.wcSessionName, MAX_PATH, wszSessionName);
        StringCchCopy(m_LogInfo.wcLogFileName, MAX_PATH, wszLogFile);

        // Start the trace.
        result = StartTrace(
            &m_SessionLogger, 
            m_LogInfo.wcSessionName, 
            &m_LogInfo.TraceProperties
            );

        if (result == ERROR_SUCCESS)
        {
            result = EnableTrace(
                TRUE,                                   // Enable.
                AUDIOBREAK_BIT | DXMPERF_VIDEOREND,     // Event classes.
                TRACE_LEVEL_VERBOSE,                    // Trace level.
                &GUID_DSHOW_CTL,                        // Event provider.
                m_SessionLogger                         // Session handle.
                );
        }
        if (result != ERROR_SUCCESS)
        { 
            hr = __HRESULT_FROM_WIN32(result);
        }
        return hr;
    }

    HRESULT Stop()
    {
        HRESULT hr = S_OK;

        // Stop the trace.
        if (m_SessionLogger != (TRACEHANDLE)INVALID_HANDLE_VALUE)
        {
            LONG result = 0;

            result = EnableTrace(FALSE, 0, 0, &GUID_DSHOW_CTL, m_SessionLogger);
            if (result == ERROR_SUCCESS)
            {
                result = StopTrace(
                    m_SessionLogger, 
                    m_LogInfo.wcSessionName, 
                    &m_LogInfo.TraceProperties);
            }

            m_SessionLogger = (TRACEHANDLE)INVALID_HANDLE_VALUE;
            if (result != ERROR_SUCCESS)
            { 
                hr = __HRESULT_FROM_WIN32(result);
            }
        }
        return hr;
    }

protected:
    TRACEHANDLE         m_SessionLogger;
    PERFMON_LOGGERINFO  m_LogInfo;
};
```



El código siguiente muestra cómo procesar el registro de eventos:


```C++
// Callback for event processing.
VOID WINAPI EventCallback(PEVENT_TRACE pEvent)
{
    PERFINFO_DSHOW_STREAMTRACE  *pStreamTrace = NULL;
    PERFINFO_DSHOW_AVREND       *pVideoRender = NULL;
    PERFINFO_DSHOW_AUDIOBREAK   *pAudioBreak = NULL;

    if (pEvent->Header.Guid == GUID_STREAMTRACE) 
    {
        pStreamTrace = (PPERFINFO_DSHOW_STREAMTRACE)pEvent->MofData;

        switch (pStreamTrace->id)
        {
            // TODO: Handle the event.
        }
    }
    else if(pEvent->Header.Guid == GUID_VIDEOREND)
    {      
        pVideoRender = (PPERFINFO_DSHOW_AVREND)pEvent->MofData;
        // TODO: Handle the event.
    }
    else if(pEvent->Header.Guid == GUID_AUDIOBREAK)
    {
        pAudioBreak = (PPERFINFO_DSHOW_AUDIOBREAK)pEvent->MofData;
        // TODO: Handle the event.
    }
}

void ProcessTraceEvents(WCHAR *wszLogFile)
{
    ULONG result = 0;        
    EVENT_TRACE_LOGFILE logfile;

    ZeroMemory(&logfile, sizeof(logfile));
    logfile.LogFileName = wszLogFile;
    logfile.EventCallback  = EventCallback;   

    TRACEHANDLE handle = OpenTrace(&logfile);
    if (handle != (TRACEHANDLE)INVALID_HANDLE_VALUE)
    {
        result = ProcessTrace(&handle, 1, NULL, NULL);
        CloseTrace(handle);
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Depuración en DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



