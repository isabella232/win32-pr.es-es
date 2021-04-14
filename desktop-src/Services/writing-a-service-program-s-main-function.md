---
description: El siguiente ejemplo se puede usar como punto de entrada para un programa de servicio que admite un servicio único.
ms.assetid: 7fdfc20a-9148-4ae1-8101-7a387c0d0edc
title: Escritura de una función principal de programas de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83aa743bfabbeafa2e05818c5bb068a949dce807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541102"
---
# <a name="writing-a-service-programs-main-function"></a><span data-ttu-id="650dd-103">Escribir la función principal de un programa de servicio</span><span class="sxs-lookup"><span data-stu-id="650dd-103">Writing a Service Program's main Function</span></span>

<span data-ttu-id="650dd-104">La función **principal** de un [programa de servicio](service-programs.md) llama a la función [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) para conectarse al administrador de [control de servicios](service-control-manager.md) (SCM) e iniciar el subproceso del distribuidor de control.</span><span class="sxs-lookup"><span data-stu-id="650dd-104">The **main** function of a [service program](service-programs.md) calls the [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function to connect to the [service control manager](service-control-manager.md) (SCM) and start the control dispatcher thread.</span></span> <span data-ttu-id="650dd-105">Los bucles de subprocesos de distribuidor esperan las solicitudes de control de entrada para los servicios especificados en la tabla de envío.</span><span class="sxs-lookup"><span data-stu-id="650dd-105">The dispatcher thread loops, waiting for incoming control requests for the services specified in the dispatch table.</span></span> <span data-ttu-id="650dd-106">Este subproceso devuelve cuando hay un error o cuando todos los servicios del proceso han terminado.</span><span class="sxs-lookup"><span data-stu-id="650dd-106">This thread returns when there is an error or when all of the services in the process have terminated.</span></span> <span data-ttu-id="650dd-107">Una vez finalizados todos los servicios en el proceso, el SCM envía una solicitud de control al subproceso de distribuidor para indicarle que salga.</span><span class="sxs-lookup"><span data-stu-id="650dd-107">When all services in the process have terminated, the SCM sends a control request to the dispatcher thread telling it to exit.</span></span> <span data-ttu-id="650dd-108">A continuación, este subproceso vuelve de la llamada a **StartServiceCtrlDispatcher** y el proceso puede finalizar.</span><span class="sxs-lookup"><span data-stu-id="650dd-108">This thread then returns from the **StartServiceCtrlDispatcher** call and the process can terminate.</span></span>

<span data-ttu-id="650dd-109">En este ejemplo se usan las siguientes definiciones globales.</span><span class="sxs-lookup"><span data-stu-id="650dd-109">The following global definitions are used in this sample.</span></span>


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



<span data-ttu-id="650dd-110">El siguiente ejemplo se puede usar como punto de entrada para un programa de servicio que admite un servicio único.</span><span class="sxs-lookup"><span data-stu-id="650dd-110">The following example can be used as the entry point for a service program that supports a single service.</span></span> <span data-ttu-id="650dd-111">Si el programa de servicio admite varios servicios, agregue los nombres de los servicios adicionales a la tabla de envío para que los pueda supervisar el subproceso de distribuidor.</span><span class="sxs-lookup"><span data-stu-id="650dd-111">If your service program supports multiple services, add the names of the additional services to the dispatch table so they can be monitored by the dispatcher thread.</span></span>

<span data-ttu-id="650dd-112">La \_ función tmain es el punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="650dd-112">The \_tmain function is the entry point.</span></span> <span data-ttu-id="650dd-113">La función SvcReportEvent escribe mensajes informativos y errores en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="650dd-113">The SvcReportEvent function writes informational messages and errors to the event log.</span></span> <span data-ttu-id="650dd-114">Para obtener información sobre cómo escribir la función SvcMain, vea [escribir una función ServiceMain](writing-a-servicemain-function.md).</span><span class="sxs-lookup"><span data-stu-id="650dd-114">For information about writing the SvcMain function, see [Writing a ServiceMain Function](writing-a-servicemain-function.md).</span></span> <span data-ttu-id="650dd-115">Para obtener más información acerca de la función SvcInstall, consulte [instalación de un servicio](installing-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="650dd-115">For more information about the SvcInstall function, see [Installing a Service](installing-a-service.md).</span></span> <span data-ttu-id="650dd-116">Para obtener información sobre cómo escribir la función SvcCtrlHandler, vea [escribir una función de controlador de control](writing-a-control-handler-function.md).</span><span class="sxs-lookup"><span data-stu-id="650dd-116">For information about writing the SvcCtrlHandler function, see [Writing a Control Handler Function](writing-a-control-handler-function.md).</span></span> <span data-ttu-id="650dd-117">Para obtener el servicio de ejemplo completo, incluido el origen de la función SvcReportEvent, vea [SVC. cpp](svc-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="650dd-117">For the complete example service, including the source for the SvcReportEvent function, see [Svc.cpp](svc-cpp.md).</span></span>


```C++
//
// Purpose: 
//   Entry point for the process
//
// Parameters:
//   None
// 
// Return value:
//   None, defaults to 0 (zero)
//
int __cdecl _tmain(int argc, TCHAR *argv[])
{ 
    // If command-line parameter is "install", install the service. 
    // Otherwise, the service is probably being started by the SCM.

    if( lstrcmpi( argv[1], TEXT("install")) == 0 )
    {
        SvcInstall();
        return;
    }

    // TO_DO: Add any additional services for the process to this table.
    SERVICE_TABLE_ENTRY DispatchTable[] = 
    { 
        { SVCNAME, (LPSERVICE_MAIN_FUNCTION) SvcMain }, 
        { NULL, NULL } 
    }; 
 
    // This call returns when the service has stopped. 
    // The process should simply terminate when the call returns.

    if (!StartServiceCtrlDispatcher( DispatchTable )) 
    { 
        SvcReportEvent(TEXT("StartServiceCtrlDispatcher")); 
    } 
} 

```



<span data-ttu-id="650dd-118">A continuación se muestra un ejemplo. h de ejemplo tal y como lo generó el compilador de mensajes.</span><span class="sxs-lookup"><span data-stu-id="650dd-118">The following is an example Sample.h as generated by the message compiler.</span></span> <span data-ttu-id="650dd-119">Para obtener más información, vea [sample.MC](sample-mc.md).</span><span class="sxs-lookup"><span data-stu-id="650dd-119">For more information, see [Sample.mc](sample-mc.md).</span></span>

``` syntax
 // The following are message definitions.
//
//  Values are 32 bit values layed out as follows:
//
//   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
//   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
//  +---+-+-+-----------------------+-------------------------------+
//  |Sev|C|R|     Facility          |               Code            |
//  +---+-+-+-----------------------+-------------------------------+
//
//  where
//
//      Sev - is the severity code
//
//          00 - Success
//          01 - Informational
//          10 - Warning
//          11 - Error
//
//      C - is the Customer code flag
//
//      R - is a reserved bit
//
//      Facility - is the facility code
//
//      Code - is the facility's status code
//
//
// Define the facility codes
//
#define FACILITY_SYSTEM                  0x0
#define FACILITY_STUBS                   0x3
#define FACILITY_RUNTIME                 0x2
#define FACILITY_IO_ERROR_CODE           0x4


//
// Define the severity codes
//
#define STATUS_SEVERITY_WARNING          0x2
#define STATUS_SEVERITY_SUCCESS          0x0
#define STATUS_SEVERITY_INFORMATIONAL    0x1
#define STATUS_SEVERITY_ERROR            0x3


//
// MessageId: SVC_ERROR
//
// MessageText:
//
//  An error has occurred (%2).
//  
//
#define SVC_ERROR                        ((DWORD)0xC0020001L)
```

## <a name="related-topics"></a><span data-ttu-id="650dd-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="650dd-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="650dd-121">Punto de entrada de servicio</span><span class="sxs-lookup"><span data-stu-id="650dd-121">Service Entry Point</span></span>](service-entry-point.md)
</dt> <dt>

[<span data-ttu-id="650dd-122">El ejemplo de servicio completo</span><span class="sxs-lookup"><span data-stu-id="650dd-122">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



