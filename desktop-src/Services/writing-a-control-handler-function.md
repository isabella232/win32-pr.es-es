---
description: Cuando el subproceso de distribuidor llama a una función Handler, controla el código de control pasado en el parámetro Opcode y, a continuación, llama a la función ReportSvcStatus para actualizar el estado del servicio.
ms.assetid: bf1932bd-496b-46a1-95f4-1581da98299f
title: Escribir una función de controlador de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724a04aa20143d2c4a506da7ac17119388a8c82e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170774"
---
# <a name="writing-a-control-handler-function"></a>Escribir una función de controlador de control

Cuando el [**subproceso**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) de distribuidor llama a una función Handler, controla el código de control pasado en el *parámetro Opcode* y, a continuación, llama a la función ReportSvcStatus para actualizar el estado del servicio. Cuando una [**función Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) recibe un código de control, solo debe notificar el estado del servicio si el control del código de control hace que cambie el estado del servicio. Si el servicio no actúa sobre el control , no debe notificar el estado al administrador de control de servicio. Para obtener el código fuente de ReportSvcStatus, vea [Writing a ServiceMain Function](writing-a-servicemain-function.md).

En el ejemplo siguiente, la función SvcCtrlHandler es un ejemplo de una [**función Handler.**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) Tenga en cuenta que la variable ghSvcStopEvent es una variable global que se debe inicializar y usar como se muestra en Escritura de [una función de ServiceMain](writing-a-servicemain-function.md).


```C++
//
// Purpose: 
//   Called by SCM whenever a control code is sent to the service
//   using the ControlService function.
//
// Parameters:
//   dwCtrl - control code
// 
// Return value:
//   None
//
VOID WINAPI SvcCtrlHandler( DWORD dwCtrl )
{
   // Handle the requested control code. 

   switch(dwCtrl) 
   {  
      case SERVICE_CONTROL_STOP: 
         ReportSvcStatus(SERVICE_STOP_PENDING, NO_ERROR, 0);

         // Signal the service to stop.

         SetEvent(ghSvcStopEvent);
         ReportSvcStatus(gSvcStatus.dwCurrentState, NO_ERROR, 0);
         
         return;
 
      case SERVICE_CONTROL_INTERROGATE: 
         break; 
 
      default: 
         break;
   } 
   
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Función de controlador de control de servicio](service-control-handler-function.md)
</dt> <dt>

[Ejemplo de servicio completo](the-complete-service-sample.md)
</dt> </dl>

 

 



