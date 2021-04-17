---
description: Cuando el subproceso de distribuidor llama a una función de controlador, controla el código de control pasado en el parámetro OpCode y, a continuación, llama a la función ReportSvcStatus para actualizar el estado del servicio.
ms.assetid: bf1932bd-496b-46a1-95f4-1581da98299f
title: Escribir una función de controlador de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724a04aa20143d2c4a506da7ac17119388a8c82e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666439"
---
# <a name="writing-a-control-handler-function"></a><span data-ttu-id="0d140-103">Escribir una función de controlador de control</span><span class="sxs-lookup"><span data-stu-id="0d140-103">Writing a Control Handler Function</span></span>

<span data-ttu-id="0d140-104">Cuando el subproceso de distribuidor llama a una función de [**controlador**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) , controla el código de control pasado en el parámetro *OpCode* y, a continuación, llama a la función ReportSvcStatus para actualizar el estado del servicio.</span><span class="sxs-lookup"><span data-stu-id="0d140-104">When a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function is called by the dispatcher thread, it handles the control code passed in the *Opcode* parameter and then calls the ReportSvcStatus function to update the service status.</span></span> <span data-ttu-id="0d140-105">Cuando una función de [**controlador**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) recibe un código de control, debe notificar el estado del servicio solo si el control del código de control hace que el estado del servicio cambie.</span><span class="sxs-lookup"><span data-stu-id="0d140-105">When a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function receives a control code, it should report the service status only if handling the control code causes the service status to change.</span></span> <span data-ttu-id="0d140-106">Si el servicio no actúa sobre el control, no debe notificar el estado al administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="0d140-106">If the service does not act on the control, it should not report status to the service control manager.</span></span> <span data-ttu-id="0d140-107">Para el código fuente de ReportSvcStatus, consulte [escribir una función ServiceMain](writing-a-servicemain-function.md).</span><span class="sxs-lookup"><span data-stu-id="0d140-107">For the source code for ReportSvcStatus, see [Writing a ServiceMain Function](writing-a-servicemain-function.md).</span></span>

<span data-ttu-id="0d140-108">En el ejemplo siguiente, la función SvcCtrlHandler es un ejemplo de una función de [**controlador**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) .</span><span class="sxs-lookup"><span data-stu-id="0d140-108">In the following example, the SvcCtrlHandler function is an example of a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function.</span></span> <span data-ttu-id="0d140-109">Tenga en cuenta que la variable ghSvcStopEvent es una variable global que se debe inicializar y usar como se muestra en [escribir una función ServiceMain](writing-a-servicemain-function.md).</span><span class="sxs-lookup"><span data-stu-id="0d140-109">Note that the ghSvcStopEvent variable is a global variable that should be initialized and used as demonstrated in [Writing a ServiceMain function](writing-a-servicemain-function.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0d140-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0d140-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d140-111">Función de controlador de control de servicio</span><span class="sxs-lookup"><span data-stu-id="0d140-111">Service Control Handler Function</span></span>](service-control-handler-function.md)
</dt> <dt>

[<span data-ttu-id="0d140-112">El ejemplo de servicio completo</span><span class="sxs-lookup"><span data-stu-id="0d140-112">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



