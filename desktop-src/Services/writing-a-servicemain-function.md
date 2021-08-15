---
description: La función SvcMain del ejemplo siguiente es la función ServiceMain para el servicio de ejemplo.
ms.assetid: 7aa9371d-676c-4633-9831-edf0e74d15f0
title: Escribir una función ServiceMain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca28b09efdc228457ae85d8a3343f334a26f246b6e48e49208d7416551e7f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887978"
---
# <a name="writing-a-servicemain-function"></a>Escribir una función ServiceMain

La función SvcMain del ejemplo siguiente es la [**función ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) para el servicio de ejemplo. SvcMain tiene acceso a los argumentos de la línea  de comandos para el servicio de la manera en que lo hace la función principal de una aplicación de consola. El primer parámetro contiene el número de argumentos que se pasan al servicio en el segundo parámetro. Siempre habrá al menos un argumento. El segundo parámetro es un puntero a una matriz de punteros de cadena. El primer elemento de la matriz es siempre el nombre del servicio.

La función SvcMain llama primero a la función [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) para registrar la función SvcCtrlHandler como función [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) del servicio y comenzar la inicialización. **RegisterServiceCtrlHandler** debe ser la primera función no permanente en [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) para que el servicio pueda usar el identificador de estado devuelto por esta función para llamar a [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) con el estado SERVICE STOPPED si se produce un \_ error.

A continuación, la función SvcMain llama a la función ReportSvcStatus para indicar que su estado inicial es SERVICE \_ START \_ PENDING. Mientras el servicio está en este estado, no se acepta ningún control. Para simplificar la lógica del servicio, se recomienda que el servicio no acepte ningún control mientras realiza su inicialización.

Por último, la función SvcMain llama a la función SvcInit para realizar la inicialización específica del servicio y comenzar el trabajo que va a realizar el servicio.

La función de inicialización de ejemplo, SvcInit, es un ejemplo muy sencillo; no realiza tareas de inicialización más complejas, como la creación de subprocesos adicionales. Crea un evento que el controlador de control de servicio puede indicar para indicar que el servicio debe detenerse y, a continuación, llama a ReportSvcStatus para indicar que el servicio ha entrado en el estado SERVICE \_ RUNNING. En este momento, el servicio ha completado su inicialización y está listo para aceptar controles. Para obtener el mejor rendimiento del sistema, la aplicación debe entrar en el estado de ejecución en un plazo de entre 25 y 100 milisegundos.

Dado que este servicio de ejemplo no completa ninguna tarea real, SvcInit simplemente espera a que se señale el evento de detención del servicio mediante una llamada a la función [**WaitForSingleObject,**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) llama a ReportSvcStatus para indicar que el servicio ha entrado en el estado SERVICE STOPPED y devuelve \_ . (Tenga en cuenta que es importante que la función devuelva , en lugar de llamar a la función [**ExitThread,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) porque devolver permite limpiar la memoria asignada para los argumentos). Puede realizar tareas de limpieza adicionales mediante [**la función RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) en lugar de **WaitForSingleObject**. El subproceso que ejecuta la [**función ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) finaliza, pero el propio servicio continúa ejecutándose. Cuando el controlador de control de servicio señala el evento, un subproceso del grupo de subprocesos ejecuta la devolución de llamada para realizar la limpieza adicional, incluido el establecimiento del estado en SERVICE \_ STOPPED.

Tenga en cuenta que en este ejemplo se usa SvcReportEvent para escribir eventos de error en el registro de eventos. Para obtener el código fuente de SvcReportEvent, vea [Svc.cpp](svc-cpp.md). Para obtener una función de controlador de control de ejemplo, vea [Escribir una función de controlador de control](writing-a-control-handler-function.md).

En este ejemplo se usan las siguientes definiciones globales.


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



El fragmento de ejemplo siguiente se toma del ejemplo de servicio completo.


```C++
//
// Purpose: 
//   Entry point for the service
//
// Parameters:
//   dwArgc - Number of arguments in the lpszArgv array
//   lpszArgv - Array of strings. The first string is the name of
//     the service and subsequent strings are passed by the process
//     that called the StartService function to start the service.
// 
// Return value:
//   None.
//
VOID WINAPI SvcMain( DWORD dwArgc, LPTSTR *lpszArgv )
{
    // Register the handler function for the service

    gSvcStatusHandle = RegisterServiceCtrlHandler( 
        SVCNAME, 
        SvcCtrlHandler);

    if( !gSvcStatusHandle )
    { 
        SvcReportEvent(TEXT("RegisterServiceCtrlHandler")); 
        return; 
    } 

    // These SERVICE_STATUS members remain as set here

    gSvcStatus.dwServiceType = SERVICE_WIN32_OWN_PROCESS; 
    gSvcStatus.dwServiceSpecificExitCode = 0;    

    // Report initial status to the SCM

    ReportSvcStatus( SERVICE_START_PENDING, NO_ERROR, 3000 );

    // Perform service-specific initialization and work.

    SvcInit( dwArgc, lpszArgv );
}

//
// Purpose: 
//   The service code
//
// Parameters:
//   dwArgc - Number of arguments in the lpszArgv array
//   lpszArgv - Array of strings. The first string is the name of
//     the service and subsequent strings are passed by the process
//     that called the StartService function to start the service.
// 
// Return value:
//   None
//
VOID SvcInit( DWORD dwArgc, LPTSTR *lpszArgv)
{
    // TO_DO: Declare and set any required variables.
    //   Be sure to periodically call ReportSvcStatus() with 
    //   SERVICE_START_PENDING. If initialization fails, call
    //   ReportSvcStatus with SERVICE_STOPPED.

    // Create an event. The control handler function, SvcCtrlHandler,
    // signals this event when it receives the stop control code.

    ghSvcStopEvent = CreateEvent(
                         NULL,    // default security attributes
                         TRUE,    // manual reset event
                         FALSE,   // not signaled
                         NULL);   // no name

    if ( ghSvcStopEvent == NULL)
    {
        ReportSvcStatus( SERVICE_STOPPED, NO_ERROR, 0 );
        return;
    }

    // Report running status when initialization is complete.

    ReportSvcStatus( SERVICE_RUNNING, NO_ERROR, 0 );

    // TO_DO: Perform work until service stops.

    while(1)
    {
        // Check whether to stop the service.

        WaitForSingleObject(ghSvcStopEvent, INFINITE);

        ReportSvcStatus( SERVICE_STOPPED, NO_ERROR, 0 );
        return;
    }
}

//
// Purpose: 
//   Sets the current service status and reports it to the SCM.
//
// Parameters:
//   dwCurrentState - The current state (see SERVICE_STATUS)
//   dwWin32ExitCode - The system error code
//   dwWaitHint - Estimated time for pending operation, 
//     in milliseconds
// 
// Return value:
//   None
//
VOID ReportSvcStatus( DWORD dwCurrentState,
                      DWORD dwWin32ExitCode,
                      DWORD dwWaitHint)
{
    static DWORD dwCheckPoint = 1;

    // Fill in the SERVICE_STATUS structure.

    gSvcStatus.dwCurrentState = dwCurrentState;
    gSvcStatus.dwWin32ExitCode = dwWin32ExitCode;
    gSvcStatus.dwWaitHint = dwWaitHint;

    if (dwCurrentState == SERVICE_START_PENDING)
        gSvcStatus.dwControlsAccepted = 0;
    else gSvcStatus.dwControlsAccepted = SERVICE_ACCEPT_STOP;

    if ( (dwCurrentState == SERVICE_RUNNING) ||
           (dwCurrentState == SERVICE_STOPPED) )
        gSvcStatus.dwCheckPoint = 0;
    else gSvcStatus.dwCheckPoint = dwCheckPoint++;

    // Report the status of the service to the SCM.
    SetServiceStatus( gSvcStatusHandle, &gSvcStatus );
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Service ServiceMain (Función)](service-servicemain-function.md)
</dt> <dt>

[Ejemplo de servicio completo](the-complete-service-sample.md)
</dt> </dl>

 

 
