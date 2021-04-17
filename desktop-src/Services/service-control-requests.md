---
description: Para enviar solicitudes de control a un servicio en ejecución, un programa de control de servicios utiliza la función ControlService.
ms.assetid: d6cdc876-8b74-460e-ad43-6455ddf428dd
title: Solicitudes de control de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb5edf56137e2c98ea7db440a4db5e55df5e8f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666446"
---
# <a name="service-control-requests"></a><span data-ttu-id="51b88-103">Solicitudes de control de servicio</span><span class="sxs-lookup"><span data-stu-id="51b88-103">Service Control Requests</span></span>

<span data-ttu-id="51b88-104">Para enviar solicitudes de control a un servicio en ejecución, un programa de control de servicios utiliza la función [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) .</span><span class="sxs-lookup"><span data-stu-id="51b88-104">To send control requests to a running service, a service control program uses the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function.</span></span> <span data-ttu-id="51b88-105">Esta función especifica un valor de control que se pasa a la función [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) del servicio especificado.</span><span class="sxs-lookup"><span data-stu-id="51b88-105">This function specifies a control value that is passed to the [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) function of the specified service.</span></span> <span data-ttu-id="51b88-106">Este valor de control puede ser un código definido por el usuario o puede ser uno de los códigos estándar que permiten al programa de llamada realizar las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="51b88-106">This control value can be a user-defined code, or it can be one of the standard codes that enable the calling program to perform the following actions:</span></span>

-   <span data-ttu-id="51b88-107">Detener un servicio ( \_ detención del control de servicio \_ ).</span><span class="sxs-lookup"><span data-stu-id="51b88-107">Stop a service (SERVICE\_CONTROL\_STOP).</span></span>
-   <span data-ttu-id="51b88-108">Pausar un servicio ( \_ pausar el control de servicio \_ ).</span><span class="sxs-lookup"><span data-stu-id="51b88-108">Pause a service (SERVICE\_CONTROL\_PAUSE).</span></span>
-   <span data-ttu-id="51b88-109">Reanuda la ejecución de un servicio en pausa ( \_ continuación de control de servicio \_ ).</span><span class="sxs-lookup"><span data-stu-id="51b88-109">Resume executing a paused service (SERVICE\_CONTROL\_CONTINUE).</span></span>
-   <span data-ttu-id="51b88-110">Recuperar información de estado actualizada de un servicio ( \_ interrogar de control de servicio \_ ).</span><span class="sxs-lookup"><span data-stu-id="51b88-110">Retrieve updated status information from a service (SERVICE\_CONTROL\_INTERROGATE).</span></span>

<span data-ttu-id="51b88-111">Cada servicio especifica los valores de control que aceptará y procesará.</span><span class="sxs-lookup"><span data-stu-id="51b88-111">Each service specifies the control values that it will accept and process.</span></span> <span data-ttu-id="51b88-112">Para determinar cuál de los valores de control estándar es aceptado por un servicio, utilice la función [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) o especifique el \_ \_ valor del control interrogate del control de servicios en una llamada a la función [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) .</span><span class="sxs-lookup"><span data-stu-id="51b88-112">To determine which of the standard control values are accepted by a service, use the [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function or specify the SERVICE\_CONTROL\_INTERROGATE control value in a call to the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function.</span></span> <span data-ttu-id="51b88-113">El miembro **dwControlsAccepted** de la estructura de [**\_ Estado de servicio**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) que devuelven estas funciones indica si el servicio se puede detener, pausar o reanudar.</span><span class="sxs-lookup"><span data-stu-id="51b88-113">The **dwControlsAccepted** member of the [**SERVICE\_STATUS**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) structure returned by these functions indicates whether the service can be stopped, paused, or resumed.</span></span> <span data-ttu-id="51b88-114">Todos los servicios aceptan el \_ \_ valor de control interrogate del control de servicios.</span><span class="sxs-lookup"><span data-stu-id="51b88-114">All services accept the SERVICE\_CONTROL\_INTERROGATE control value.</span></span>

<span data-ttu-id="51b88-115">La función [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) notifica el estado más reciente de un servicio especificado, pero no obtiene un estado actualizado del propio servicio.</span><span class="sxs-lookup"><span data-stu-id="51b88-115">The [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function reports the most recent status for a specified service, but does not get an updated status from the service itself.</span></span> <span data-ttu-id="51b88-116">El uso del \_ \_ valor de control interrogate del control de servicios en una llamada a [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) garantiza que la información de estado devuelta es actual.</span><span class="sxs-lookup"><span data-stu-id="51b88-116">Using the SERVICE\_CONTROL\_INTERROGATE control value in a call to [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) ensures that the status information returned is current.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51b88-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="51b88-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51b88-118">Controlar un servicio mediante SC</span><span class="sxs-lookup"><span data-stu-id="51b88-118">Controlling a Service Using SC</span></span>](controlling-a-service-using-sc.md)
</dt> </dl>

 

 



