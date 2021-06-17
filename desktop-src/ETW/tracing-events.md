---
description: Obtenga información sobre cómo escribir eventos MOF en una sesión de seguimiento. Comience con el registro del proveedor para que esté listo para escribir eventos en una sesión de seguimiento.
ms.assetid: 21f62b5d-0a2d-468c-af88-2fab1512f0ec
title: Escribir eventos MOF (clásico)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d081c48567851d2fb570dd7bfa5c75e687b524
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "112261847"
---
# <a name="writing-mof-classic-events"></a>Escribir eventos MOF (clásico)

Para poder escribir eventos en una sesión de seguimiento, debe registrar el proveedor. El registro de un proveedor indica a ETW que el proveedor está listo para escribir eventos en una sesión de seguimiento. Un proceso puede registrar hasta 1024 GUID de proveedor; sin embargo, debe limitar el número de proveedores que registra el proceso a uno o dos.

**Antes de Windows Vista:** No hay ningún límite en el número de proveedores que un proceso puede registrar.

Para registrar un proveedor clásico, llame a [**la función RegisterTraceGuids.**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) La función registra el GUID del proveedor, los GUID de la clase de seguimiento de eventos e identifica la devolución de llamada a la que ETW llama cuando un controlador habilita o deshabilita el proveedor.

Si el proveedor llama a la función [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) para registrar eventos, no es necesario incluir la matriz de GUID de clase (puede ser **NULL)** al llamar a la [**función RegisterTraceGuids.**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) Solo debe incluir la matriz si el proveedor llama a la [**función TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) para registrar eventos.

**Windows XP y Windows 2000:** Siempre debe incluir la matriz de GUID de clase (no puede ser **NULL).**

Una vez que un proveedor se registra a sí mismo y el controlador lo habilita, el proveedor puede registrar eventos en la sesión de seguimiento del controlador.

Antes de que se cierre el proveedor, llame a la función [**UnregisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids) para quitar el registro del proveedor de ETW. La [**función RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) devuelve el identificador de registro que se pasa a **la función UnregisterTraceGuids.**

Si el proveedor solo registra eventos en la sesión del registrador global, no tiene que registrar el proveedor con ETW porque el controlador del registrador global no habilita ni deshabilita los proveedores. Para obtener más información, [vea Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).

Todos [los proveedores](about-event-tracing.md) clásicos (excepto los que trazan eventos a la sesión del registrador global) deben implementar la función [**ControlCallback.**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) El proveedor usa la información de la devolución de llamada para determinar si está habilitada o deshabilitada y qué eventos debe escribir.

El proveedor especifica el nombre de la función de devolución de llamada cuando llama a [**la función RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) para registrarse. ETW llama a la función de devolución de llamada cuando el controlador llama a la [**función EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para habilitar o deshabilitar el proveedor.

En la [**implementación de ControlCallback,**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) debe llamar a la [**función GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle) para recuperar el identificador de sesión. se usa el identificador de sesión al llamar a la [**función TraceEvent.**](/windows/win32/api/evntrace/nf-evntrace-traceevent) Solo tiene que llamar a la función [**GetTraceEnableFlags**](/windows/win32/api/evntrace/nf-evntrace-gettraceenableflags) o a la función [**GetTraceEnableLevel**](/windows/win32/api/evntrace/nf-evntrace-gettraceenablelevel) en la **implementación de ControlCallback** si el proveedor usa el nivel de habilitación o las marcas de habilitación.

Un proveedor puede registrar eventos de seguimiento en una sola sesión, pero no hay nada que impida que varios controladores habiliten un único proveedor. Para evitar que otro controlador redirija los eventos de seguimiento a su sesión, puede agregar lógica a la implementación [**de ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) para comparar los identificadores de sesión y omitir las solicitudes de habilitación de otros controladores.

Para registrar eventos, [los proveedores clásicos](about-event-tracing.md) llaman a la función [**TraceEvent.**](/windows/win32/api/evntrace/nf-evntrace-traceevent) Un evento consta de la estructura [**EVENT \_ TRACE \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) y de los datos específicos del evento que se anexan al encabezado.

El encabezado debe contener la siguiente información:

-   El **miembro Size** debe contener el número total de bytes que se registrarán para el evento (incluido el tamaño de la estructura EVENT TRACE [**\_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) y de los datos específicos del evento que se anexan al encabezado).
-   El **miembro Guid** debe contener el GUID de clase del evento (o el miembro **GuidPtr** debe contener un puntero al GUID de clase).

    **Windows XP y Windows 2000:** El GUID de clase se debe haber registrado previamente mediante [**la función RegisterTraceGuids.**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)

-   El **miembro Flags** debe contener la **marca GUID \_ \_ TRACED \_ de WNODE FLAG.** Si especifica el GUID de clase mediante el **miembro GuidPtr,** agregue también la marca **\_ \_ \_ \_ PTR USE GUID de WNODE FLAG.**
-   El **miembro Class.Type** debe contener el tipo de evento si usa MOF para publicar el diseño de los datos del evento.
-   El **miembro Class.Version** debe contener la versión del evento, si usa MOF para publicar el diseño de los datos del evento. La versión se usa para distinguir entre las revisiones de los datos del evento. Establezca el número de versión inicial en 0.

Si escribe el proveedor y el consumidor, puede usar una estructura para rellenar los datos específicos del evento que se anexan al encabezado. Sin embargo, si usa MOF para publicar los datos específicos del evento para que cualquier consumidor pueda procesar el evento, no debe usar una estructura para anexar los datos específicos del evento al encabezado. Esto se debe a que el compilador puede agregar bytes adicionales a los datos específicos del evento con fines de alineación de bytes. Dado que la definición de MOF no tiene en cuenta los bytes adicionales, el consumidor puede recuperar datos que no son válidos.

Debe asignar un bloque de memoria para el evento y copiar cada elemento de datos de evento en la memoria, o bien crear una estructura que incluya una matriz de estructuras [**MOF \_ FIELD;**](/windows/win32/api/evntrace/ns-evntrace-mof_field) la mayoría de las aplicaciones crearán una estructura que incluya una matriz de estructuras **MOF \_ FIELD.** Asegúrese de que **Header.Size** refleja el número real de estructuras **MOF \_ FIELD** que se establecen realmente antes de registrar el evento. Por ejemplo, si el evento contiene tres campos de datos, establezca **Header.Size** en sizeof(EVENT \_ TRACE \_ HEADER) + (sizeof(MOF \_ FIELD) \* 3).

Para obtener información sobre el seguimiento de eventos relacionados, vea Escribir eventos relacionados en un escenario [de un extremo a otro.](writing-related-events-in-an-end-to-end-scenario.md)

En el ejemplo siguiente se muestra cómo llamar a la [**función TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) para registrar eventos. En el ejemplo se hace referencia a los eventos definidos [en Publishing Your Event Schema for a Classic Provider](publishing-your-event-schema-for-a-classic-provider.md).


```C++
#include <windows.h>
#include <stdio.h>
#include <wmistr.h>
#include <evntrace.h>

// GUID that identifies the category of events that the provider can log. 
// The GUID is also used in the event MOF class. 
// Remember to change this GUID if you copy and paste this example.

// {B49D5931-AD85-4070-B1B1-3F81F1532875}
static const GUID MyCategoryGuid = 
{ 0xb49d5931, 0xad85, 0x4070, { 0xb1, 0xb1, 0x3f, 0x81, 0xf1, 0x53, 0x28, 0x75 } };

// GUID that identifies the provider that you are registering.
// The GUID is also used in the provider MOF class. 
// Remember to change this GUID if you copy and paste this example.

// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };

// Identifies the event type within the MyCategoryGuid category 
// of events to be logged. This is the same value as the EventType 
// qualifier that is defined in the event type MOF class for one of 
// the MyCategoryGuid category of events.

#define MY_EVENT_TYPE 1

// Event passed to TraceEvent

typedef struct _event
{
    EVENT_TRACE_HEADER Header;
    MOF_FIELD Data[MAX_MOF_FIELDS];  // Event-specific data
} MY_EVENT, *PMY_EVENT;

#define MAX_INDICES            3
#define MAX_SIGNATURE_LEN      32
#define EVENT_DATA_FIELDS_CNT  6

// Application data to be traced for Version 1 of the MOF class.

typedef struct _evtdata
{
    LONG Cost;
    DWORD Indices[MAX_INDICES];
    WCHAR Signature[MAX_SIGNATURE_LEN];
    BOOL IsComplete;
    GUID ID;
    DWORD Size;
}EVENT_DATA, *PEVENT_DATA;

// GUID used as the value for EVENT_DATA.ID.

// {25BAEDA9-C81A-4889-8764-184FE56750F2}
static const GUID tempID = 
{ 0x25baeda9, 0xc81a, 0x4889, { 0x87, 0x64, 0x18, 0x4f, 0xe5, 0x67, 0x50, 0xf2 } };

// Global variables to store tracing state information.

TRACEHANDLE g_SessionHandle = 0; // The handle to the session that enabled the provider.
ULONG g_EnableFlags = 0; // Determines which class of events to log.
UCHAR g_EnableLevel = 0; // Determines the severity of events to log.
BOOL g_TraceOn = FALSE;  // Used by the provider to determine whether it should log events.

ULONG WINAPI ControlCallback(WMIDPREQUESTCODE RequestCode, PVOID Context, ULONG* Reserved, PVOID Header);

// For this example to log the event, run the session example
// to enable the provider before running this example.

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    EVENT_DATA EventData;
    MY_EVENT MyEvent; 
    TRACEHANDLE RegistrationHandle = 0; 
    TRACE_GUID_REGISTRATION EventClassGuids[] = {
        (LPGUID)&MyCategoryGuid, NULL
        };

    // Register the provider and specify the control callback function
    // that receives the enable/disable notifications.

    status = RegisterTraceGuids(
        (WMIDPREQUEST)ControlCallback,
        NULL,
        (LPGUID)&ProviderGuid,
        sizeof(EventClassGuids)/sizeof(TRACE_GUID_REGISTRATION),
        EventClassGuids,
        NULL,
        NULL,
        &RegistrationHandle
        );

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegisterTraceGuids failed with %lu\n", status);
        goto cleanup;
    }

    // Set the event-specific data.

    EventData.Cost = 32;
    EventData.ID = tempID;
    EventData.Indices[0] = 4;
    EventData.Indices[1] = 5;
    EventData.Indices[2] = 6;
    EventData.IsComplete = TRUE;
    wcscpy_s(EventData.Signature, MAX_SIGNATURE_LEN, L"Signature");
    EventData.Size = 1024;

    // Log the event if the provider is enabled and the session
    // passed a severity level value >= TRACE_LEVEL_ERROR (or zero).
    // If your provider generates more than one class of events, you
    // would also need to check g_EnableFlags.

    if (g_TraceOn && (0 == g_EnableLevel || TRACE_LEVEL_ERROR <= g_EnableLevel))
    {
        // Initialize the event data structure.

        ZeroMemory(&MyEvent, sizeof(MY_EVENT));
        MyEvent.Header.Size = sizeof(EVENT_TRACE_HEADER) + (sizeof(MOF_FIELD) * EVENT_DATA_FIELDS_CNT);
        MyEvent.Header.Flags = WNODE_FLAG_TRACED_GUID | WNODE_FLAG_USE_MOF_PTR;
        MyEvent.Header.Guid = MyCategoryGuid;
        MyEvent.Header.Class.Type = MY_EVENT_TYPE;
        MyEvent.Header.Class.Version = 1;
        MyEvent.Header.Class.Level = g_EnableLevel;

        // Load the event data. You can also use the DEFINE_TRACE_MOF_FIELD
        // macro defined in evntrace.h to set the MOF_FIELD members. For example,
        // DEFINE_TRACE_MOF_FIELD(&EventData.Data[0], &EventData.Cost, sizeof(EventData.Cost), 0);

        MyEvent.Data[0].DataPtr = (ULONG64) &(EventData.Cost);
        MyEvent.Data[0].Length = sizeof(EventData.Cost);
        MyEvent.Data[1].DataPtr = (ULONG64) &(EventData.Indices);
        MyEvent.Data[1].Length = sizeof(EventData.Indices);
        MyEvent.Data[2].DataPtr = (ULONG64) &(EventData.Signature);
        MyEvent.Data[2].Length = (ULONG)(wcslen(EventData.Signature) + 1) * sizeof(WCHAR);
        MyEvent.Data[3].DataPtr = (ULONG64) &(EventData.IsComplete);
        MyEvent.Data[3].Length = sizeof(EventData.IsComplete);
        MyEvent.Data[4].DataPtr = (ULONG64) &(EventData.ID);
        MyEvent.Data[4].Length = sizeof(EventData.ID);
        MyEvent.Data[5].DataPtr = (ULONG64) &(EventData.Size);
        MyEvent.Data[5].Length = sizeof(EventData.Size);

        // Write the event.

        status = TraceEvent(g_SessionHandle, &(MyEvent.Header));

        if (ERROR_SUCCESS != status)
        {
            // Decide how you want to handle failures. Typically, you do not
            // want to terminate the application because you failed to
            // log an event. If the error is a memory failure, you may
            // may want to log a message to the system event log or turn
            // off logging.

            wprintf(L"TraceEvent() event failed with %lu\n", status);
            g_TraceOn = FALSE;
        }
    }

cleanup:

    if (RegistrationHandle)
    {
        UnregisterTraceGuids(RegistrationHandle);
    }
}


// The callback function that receives enable/disable notifications
// from one or more ETW sessions. Because more than one session
// can enable the provider, this example ignores requests from other 
// sessions if it is already enabled.

ULONG WINAPI ControlCallback(
    WMIDPREQUESTCODE RequestCode,
    PVOID Context,
    ULONG* Reserved, 
    PVOID Header
    )
{
    UNREFERENCED_PARAMETER(Context);
    UNREFERENCED_PARAMETER(Reserved);

    ULONG status = ERROR_SUCCESS;
    TRACEHANDLE TempSessionHandle = 0; 

    switch (RequestCode)
    {
        case WMI_ENABLE_EVENTS:  // Enable the provider.
        {
            SetLastError(0);

            // If the provider is already enabled to a provider, ignore 
            // the request. Get the session handle of the enabling session.
            // You need the session handle to call the TraceEvent function.
            // The session could be enabling the provider or it could be
            // updating the level and enable flags.

            TempSessionHandle = GetTraceLoggerHandle(Header);
            if (INVALID_HANDLE_VALUE == (HANDLE)TempSessionHandle)
            {
                wprintf(L"GetTraceLoggerHandle failed. Error code is %lu.\n", status = GetLastError());
                break;
            }

            if (0 == g_SessionHandle)
            {
                g_SessionHandle = TempSessionHandle;
            }
            else if (g_SessionHandle != TempSessionHandle)
            {
                break;
            }

            // Get the severity level of the events that the
            // session wants you to log.

            g_EnableLevel = GetTraceEnableLevel(g_SessionHandle); 
            if (0 == g_EnableLevel)
            {
                // If zero, determine whether the session passed zero
                // or an error occurred.

                if (ERROR_SUCCESS == (status = GetLastError()))
                {
                    // Decide what a zero enable level means to your provider.
                    // For this example, it means log all events.
                    ; 
                }
                else
                {
                    wprintf(L"GetTraceEnableLevel failed with, %lu.\n", status);
                    break;
                } 
            }

            // Get the enable flags that indicate the events that the
            // session wants you to log. The provider determines the
            // flags values. How it articulates the flag values and 
            // meanings to perspective sessions is up to it.

            g_EnableFlags = GetTraceEnableFlags(g_SessionHandle);
            if (0 == g_EnableFlags)
            {
                // If zero, determine whether the session passed zero
                // or an error occurred.

                if (ERROR_SUCCESS == (status = GetLastError()))
                {
                    // Decide what a zero enable flags value means to your provider.
                    ; 
                }
                else
                {
                    wprintf(L"GetTraceEnableFlags failed with, %lu.\n", status);
                    break;
                }
            }

            g_TraceOn = TRUE;
            break;
        }
 
        case WMI_DISABLE_EVENTS:  // Disable the provider.
        {
            // Disable the provider only if the request is coming from the
            // session that enabled the provider.

            TempSessionHandle = GetTraceLoggerHandle(Header);
            if (INVALID_HANDLE_VALUE == (HANDLE)TempSessionHandle)
            {
                wprintf(L"GetTraceLoggerHandle failed. Error code is %lu.\n", status = GetLastError());
                break;
            }

            if (g_SessionHandle == TempSessionHandle)
            {
                g_TraceOn = FALSE;
                g_SessionHandle = 0;
            }
            break;
        }

        default:
        {
            status = ERROR_INVALID_PARAMETER;
            break;
        }
    }

    return status;
}
```



 

 
