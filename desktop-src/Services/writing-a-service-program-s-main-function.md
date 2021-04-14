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
# <a name="writing-a-service-programs-main-function"></a>Escribir la función principal de un programa de servicio

La función **principal** de un [programa de servicio](service-programs.md) llama a la función [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) para conectarse al administrador de [control de servicios](service-control-manager.md) (SCM) e iniciar el subproceso del distribuidor de control. Los bucles de subprocesos de distribuidor esperan las solicitudes de control de entrada para los servicios especificados en la tabla de envío. Este subproceso devuelve cuando hay un error o cuando todos los servicios del proceso han terminado. Una vez finalizados todos los servicios en el proceso, el SCM envía una solicitud de control al subproceso de distribuidor para indicarle que salga. A continuación, este subproceso vuelve de la llamada a **StartServiceCtrlDispatcher** y el proceso puede finalizar.

En este ejemplo se usan las siguientes definiciones globales.


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



El siguiente ejemplo se puede usar como punto de entrada para un programa de servicio que admite un servicio único. Si el programa de servicio admite varios servicios, agregue los nombres de los servicios adicionales a la tabla de envío para que los pueda supervisar el subproceso de distribuidor.

La \_ función tmain es el punto de entrada. La función SvcReportEvent escribe mensajes informativos y errores en el registro de eventos. Para obtener información sobre cómo escribir la función SvcMain, vea [escribir una función ServiceMain](writing-a-servicemain-function.md). Para obtener más información acerca de la función SvcInstall, consulte [instalación de un servicio](installing-a-service.md). Para obtener información sobre cómo escribir la función SvcCtrlHandler, vea [escribir una función de controlador de control](writing-a-control-handler-function.md). Para obtener el servicio de ejemplo completo, incluido el origen de la función SvcReportEvent, vea [SVC. cpp](svc-cpp.md).


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



A continuación se muestra un ejemplo. h de ejemplo tal y como lo generó el compilador de mensajes. Para obtener más información, vea [sample.MC](sample-mc.md).

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

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Punto de entrada de servicio](service-entry-point.md)
</dt> <dt>

[El ejemplo de servicio completo](the-complete-service-sample.md)
</dt> </dl>

 

 



