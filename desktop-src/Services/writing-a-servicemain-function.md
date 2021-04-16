---
description: La función SvcMain del ejemplo siguiente es la función ServiceMain para el servicio de ejemplo.
ms.assetid: 7aa9371d-676c-4633-9831-edf0e74d15f0
title: Escribir una función ServiceMain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad3e947c356bad6c6d54395a671aa192c93de1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666437"
---
# <a name="writing-a-servicemain-function"></a><span data-ttu-id="843bd-103">Escribir una función ServiceMain</span><span class="sxs-lookup"><span data-stu-id="843bd-103">Writing a ServiceMain Function</span></span>

<span data-ttu-id="843bd-104">La función SvcMain del ejemplo siguiente es la función [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) para el servicio de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="843bd-104">The SvcMain function in the following example is the [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function for the example service.</span></span> <span data-ttu-id="843bd-105">SvcMain tiene acceso a los argumentos de la línea de comandos para el servicio en la forma en que lo hace la función **principal** de una aplicación de consola.</span><span class="sxs-lookup"><span data-stu-id="843bd-105">SvcMain has access to the command-line arguments for the service in the way that the **main** function of a console application does.</span></span> <span data-ttu-id="843bd-106">El primer parámetro contiene el número de argumentos que se pasan al servicio en el segundo parámetro.</span><span class="sxs-lookup"><span data-stu-id="843bd-106">The first parameter contains the number of arguments being passed to the service in the second parameter.</span></span> <span data-ttu-id="843bd-107">Siempre habrá al menos un argumento.</span><span class="sxs-lookup"><span data-stu-id="843bd-107">There will always be at least one argument.</span></span> <span data-ttu-id="843bd-108">El segundo parámetro es un puntero a una matriz de punteros de cadena.</span><span class="sxs-lookup"><span data-stu-id="843bd-108">The second parameter is a pointer to an array of string pointers.</span></span> <span data-ttu-id="843bd-109">El primer elemento de la matriz siempre es el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="843bd-109">The first item in the array is always the service name.</span></span>

<span data-ttu-id="843bd-110">La función SvcMain llama primero a la función [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) para registrar la función SvcCtrlHandler como la función de [**controlador**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) del servicio y comenzar la inicialización.</span><span class="sxs-lookup"><span data-stu-id="843bd-110">The SvcMain function first calls the [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) function to register the SvcCtrlHandler function as the service's [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function and begin initialization.</span></span> <span data-ttu-id="843bd-111">**RegisterServiceCtrlHandler** debe ser la primera función sin error de [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) , de modo que el servicio pueda usar el identificador de estado devuelto por esta función para llamar a [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) con el estado de detención del servicio \_ si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="843bd-111">**RegisterServiceCtrlHandler** should be the first nonfailing function in [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) so the service can use the status handle returned by this function to call [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) with the SERVICE\_STOPPED state if an error occurs.</span></span>

<span data-ttu-id="843bd-112">A continuación, la función SvcMain llama a la función ReportSvcStatus para indicar que su estado inicial es servicio de \_ Inicio \_ pendiente.</span><span class="sxs-lookup"><span data-stu-id="843bd-112">Next, the SvcMain function calls the ReportSvcStatus function to indicate that its initial status is SERVICE\_START\_PENDING.</span></span> <span data-ttu-id="843bd-113">Mientras el servicio se encuentra en este estado, no se acepta ningún control.</span><span class="sxs-lookup"><span data-stu-id="843bd-113">While the service is in this state, no controls are accepted.</span></span> <span data-ttu-id="843bd-114">Para simplificar la lógica del servicio, se recomienda que el servicio no acepte ningún control mientras se está realizando su inicialización.</span><span class="sxs-lookup"><span data-stu-id="843bd-114">To simplify the logic of the service, it is recommended that the service not accept any controls while it is performing its initialization.</span></span>

<span data-ttu-id="843bd-115">Por último, la función SvcMain llama a la función SvcInit para realizar la inicialización específica del servicio e iniciar el trabajo que debe realizar el servicio.</span><span class="sxs-lookup"><span data-stu-id="843bd-115">Finally, the SvcMain function calls the SvcInit function to perform the service-specific initialization and begin the work to be performed by the service.</span></span>

<span data-ttu-id="843bd-116">La función de inicialización de ejemplo, SvcInit, es un ejemplo muy sencillo; no realiza tareas de inicialización más complejas, como la creación de subprocesos adicionales.</span><span class="sxs-lookup"><span data-stu-id="843bd-116">The sample initialization function, SvcInit, is a very simple example; it does not perform more complex initialization tasks such as creating additional threads.</span></span> <span data-ttu-id="843bd-117">Crea un evento que el controlador de control de servicio puede señalar para indicar que el servicio debe detenerse y, a continuación, llama a ReportSvcStatus para indicar que el servicio ha entrado en el estado de ejecución del servicio \_ .</span><span class="sxs-lookup"><span data-stu-id="843bd-117">It creates an event that the service control handler can signal to indicate that the service should stop, then calls ReportSvcStatus to indicate that the service has entered the SERVICE\_RUNNING state.</span></span> <span data-ttu-id="843bd-118">En este momento, el servicio ha completado su inicialización y está listo para aceptar controles.</span><span class="sxs-lookup"><span data-stu-id="843bd-118">At this point, the service has completed its initialization and is ready to accept controls.</span></span> <span data-ttu-id="843bd-119">Para mejorar el rendimiento del sistema, la aplicación debe entrar en el estado de ejecución en un plazo de 25-100 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="843bd-119">For best system performance, your application should enter the running state within 25-100 milliseconds.</span></span>

<span data-ttu-id="843bd-120">Dado que este servicio de ejemplo no completa ninguna tarea real, SvcInit simplemente espera a que se señale el evento de detención de servicio llamando a la función [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) , llama a ReportSvcStatus para indicar que el servicio ha entrado en el \_ estado detenido del servicio y devuelve.</span><span class="sxs-lookup"><span data-stu-id="843bd-120">Because this sample service does not complete any real tasks, SvcInit simply waits for the service stop event to be signaled by calling the [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function, calls ReportSvcStatus to indicate that the service has entered the SERVICE\_STOPPED state, and returns.</span></span> <span data-ttu-id="843bd-121">(Tenga en cuenta que es importante que la función devuelva, en lugar de llamar a la función [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) , ya que la devolución de permite la limpieza de la memoria asignada para los argumentos). Puede realizar otras tareas de limpieza mediante la función [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) en lugar de **WaitForSingleObject**.</span><span class="sxs-lookup"><span data-stu-id="843bd-121">(Note that it is important for the function to return, rather than call the [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) function, because returning allows for cleanup of the memory allocated for the arguments.) You can perform additional cleanup tasks by using the [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) function instead of **WaitForSingleObject**.</span></span> <span data-ttu-id="843bd-122">El subproceso que está ejecutando la función [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) finaliza, pero el propio servicio continúa ejecutándose.</span><span class="sxs-lookup"><span data-stu-id="843bd-122">The thread that is running the [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function terminates, but the service itself continues to run.</span></span> <span data-ttu-id="843bd-123">Cuando el controlador de control de servicio indica el evento, un subproceso del grupo de subprocesos ejecuta la devolución de llamada para realizar la limpieza adicional, incluida la configuración del estado en \_ detenido.</span><span class="sxs-lookup"><span data-stu-id="843bd-123">When the service control handler signals the event, a thread from the thread pool executes your callback to perform the additional cleanup, including setting the status to SERVICE\_STOPPED.</span></span>

<span data-ttu-id="843bd-124">Tenga en cuenta que en este ejemplo se usa SvcReportEvent para escribir eventos de error en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="843bd-124">Note that this example uses SvcReportEvent to write error events to the event log.</span></span> <span data-ttu-id="843bd-125">Para el código fuente de SvcReportEvent, consulte [SVC. cpp](svc-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="843bd-125">For the source code for SvcReportEvent, see [Svc.cpp](svc-cpp.md).</span></span> <span data-ttu-id="843bd-126">Para obtener una función de controlador de control de ejemplo, vea [escribir una función de controlador de control](writing-a-control-handler-function.md).</span><span class="sxs-lookup"><span data-stu-id="843bd-126">For an example control handler function, see [Writing a Control Handler Function](writing-a-control-handler-function.md).</span></span>

<span data-ttu-id="843bd-127">En este ejemplo se usan las siguientes definiciones globales.</span><span class="sxs-lookup"><span data-stu-id="843bd-127">The following global definitions are used in this sample.</span></span>


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



<span data-ttu-id="843bd-128">El siguiente fragmento de ejemplo se toma del ejemplo de servicio completo.</span><span class="sxs-lookup"><span data-stu-id="843bd-128">The following sample fragment is taken from the complete service sample.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="843bd-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="843bd-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="843bd-130">Función ServiceMain del servicio</span><span class="sxs-lookup"><span data-stu-id="843bd-130">Service ServiceMain Function</span></span>](service-servicemain-function.md)
</dt> <dt>

[<span data-ttu-id="843bd-131">El ejemplo de servicio completo</span><span class="sxs-lookup"><span data-stu-id="843bd-131">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 
