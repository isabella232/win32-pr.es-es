---
description: El administrador de control de servicios (SCM) controla un servicio mediante el envío de eventos de control de servicio a la rutina del controlador de control de servicios.
ms.assetid: 86e04b43-5f6f-409e-ac18-d7efada4d3d3
title: Servicios multiproceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5795a170f912050d115537407fcb491305a35ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668294"
---
# <a name="multithreaded-services"></a><span data-ttu-id="4760b-103">Servicios multiproceso</span><span class="sxs-lookup"><span data-stu-id="4760b-103">Multithreaded Services</span></span>

<span data-ttu-id="4760b-104">El administrador de control de servicios (SCM) controla un servicio mediante el envío de eventos de control de servicio a la rutina del controlador de control del servicio.</span><span class="sxs-lookup"><span data-stu-id="4760b-104">The service control manager (SCM) controls a service by sending service control events to the service's control handler routine.</span></span> <span data-ttu-id="4760b-105">El servicio debe responder a los eventos de control de forma oportuna para que el SCM pueda realizar un seguimiento del estado del servicio.</span><span class="sxs-lookup"><span data-stu-id="4760b-105">The service must respond to control events in a timely manner so that the SCM can keep track of the state of the service.</span></span> <span data-ttu-id="4760b-106">Además, el estado del servicio debe coincidir con la descripción de su estado que recibe el SCM.</span><span class="sxs-lookup"><span data-stu-id="4760b-106">Also, the state of the service must match the description of its state that the SCM receives.</span></span>

<span data-ttu-id="4760b-107">Debido a este mecanismo de comunicación entre un servicio y el SCM, debe tener cuidado al usar varios subprocesos en un servicio.</span><span class="sxs-lookup"><span data-stu-id="4760b-107">Due to this communication mechanism between a service and the SCM, you must be careful when using multiple threads in a service.</span></span> <span data-ttu-id="4760b-108">Cuando se indica a un servicio que lo detenga el SCM, debe esperar a que finalicen todos los subprocesos antes de informar al SCM de que el servicio se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="4760b-108">When a service is instructed to stop by the SCM, it must wait for all the threads to exit before reporting to the SCM that the service is stopped.</span></span> <span data-ttu-id="4760b-109">De lo contrario, el SCM puede confundirse con respecto al estado del servicio y podría no cerrarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="4760b-109">Otherwise, the SCM can become confused about the state of the service and might fail to shut down correctly.</span></span>

<span data-ttu-id="4760b-110">El SCM debe recibir una notificación de que el servicio responde al evento STOP control y que se está realizando el progreso al detener el servicio.</span><span class="sxs-lookup"><span data-stu-id="4760b-110">The SCM needs to be notified that the service is responding to the stop control event and that progress is being made in stopping the service.</span></span> <span data-ttu-id="4760b-111">El SCM asumirá que el servicio progresa si el servicio responde (a la [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) dentro del tiempo (sugerencia de espera) especificado en la llamada anterior a **SetServiceStatus** y el punto de comprobación se actualiza para que sea mayor que el punto de control especificado en la llamada anterior a **SetServiceStatus**.</span><span class="sxs-lookup"><span data-stu-id="4760b-111">The SCM will assume the service is making progress if the service responds (through [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) within the time (wait hint) specified in the previous call to **SetServiceStatus**, and the check point is updated to be greater than the checkpoint specified in the previous call to **SetServiceStatus**.</span></span>

<span data-ttu-id="4760b-112">Si el servicio informa al SCM de que el servicio se ha detenido antes de que todos los subprocesos se hayan cerrado, es posible que el SCM lo interprete como contradicción.</span><span class="sxs-lookup"><span data-stu-id="4760b-112">If the service reports to the SCM that the service has stopped before all threads have exited, it is possible that the SCM will interpret this as a contradiction.</span></span> <span data-ttu-id="4760b-113">Esto podría dar lugar a un estado en el que el servicio no se puede detener o reiniciar.</span><span class="sxs-lookup"><span data-stu-id="4760b-113">This might result in a state where the service cannot be stopped or restarted.</span></span>

 

 



