---
description: Un programa de servicio contiene código ejecutable para uno o más servicios.
ms.assetid: 697db543-6149-46ac-add3-c8c6ca3aadbe
title: Programas de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5e78574f46549956325bc19ffb6d51f4a114ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912805"
---
# <a name="service-programs"></a><span data-ttu-id="58526-103">Programas de servicio</span><span class="sxs-lookup"><span data-stu-id="58526-103">Service Programs</span></span>

<span data-ttu-id="58526-104">Un *programa de servicio* contiene código ejecutable para uno o más servicios.</span><span class="sxs-lookup"><span data-stu-id="58526-104">A *service program* contains executable code for one or more services.</span></span> <span data-ttu-id="58526-105">Un programa de servicio creado con el \_ \_ propio \_ proceso de Win32 de servicio de tipo contiene el código de un solo servicio.</span><span class="sxs-lookup"><span data-stu-id="58526-105">A service program created with the type SERVICE\_WIN32\_OWN\_PROCESS contains the code for only one service.</span></span> <span data-ttu-id="58526-106">Un programa de servicio creado con el \_ proceso de \_ recurso compartido \_ de Win32 de servicio de tipo contiene código para más de un servicio, lo que les permite compartir código.</span><span class="sxs-lookup"><span data-stu-id="58526-106">A service program created with the type SERVICE\_WIN32\_SHARE\_PROCESS contains code for more than one service, enabling them to share code.</span></span> <span data-ttu-id="58526-107">Un ejemplo de un programa de servicio que hace esto es el proceso de host de servicio genérico, Svchost.exe, que hospeda los servicios internos de Windows.</span><span class="sxs-lookup"><span data-stu-id="58526-107">An example of a service program that does this is the generic service host process, Svchost.exe, which hosts internal Windows services.</span></span> <span data-ttu-id="58526-108">Tenga en cuenta que Svchost.exe está reservado para su uso por parte del sistema operativo y no debe ser utilizado por servicios que no sean de Windows.</span><span class="sxs-lookup"><span data-stu-id="58526-108">Note that Svchost.exe is reserved for use by the operating system and should not be used by non-Windows services.</span></span> <span data-ttu-id="58526-109">En su lugar, los desarrolladores deben implementar sus propios programas de hospedaje de servicios.</span><span class="sxs-lookup"><span data-stu-id="58526-109">Instead, developers should implement their own service hosting programs.</span></span>

<span data-ttu-id="58526-110">Un programa de servicio se puede configurar para que se ejecute en el contexto de una cuenta de usuario desde el dominio integrado (local), principal o de confianza.</span><span class="sxs-lookup"><span data-stu-id="58526-110">A service program can be configured to execute in the context of a user account from either the built-in (local), primary, or trusted domain.</span></span> <span data-ttu-id="58526-111">También se puede configurar para que se ejecute en una [cuenta de usuario de servicio](service-user-accounts.md)especial.</span><span class="sxs-lookup"><span data-stu-id="58526-111">It can also be configured to run in a special [service user account](service-user-accounts.md).</span></span>

<span data-ttu-id="58526-112">En los temas siguientes se describen los requisitos de interfaz del [Administrador de control de servicios](service-control-manager.md) (SCM) que un programa de servicio debe incluir:</span><span class="sxs-lookup"><span data-stu-id="58526-112">The following topics describe the interface requirements of the [service control manager](service-control-manager.md) (SCM) that a service program must include:</span></span>

-   [<span data-ttu-id="58526-113">Punto de entrada de servicio</span><span class="sxs-lookup"><span data-stu-id="58526-113">Service Entry Point</span></span>](service-entry-point.md)
-   [<span data-ttu-id="58526-114">Función ServiceMain del servicio</span><span class="sxs-lookup"><span data-stu-id="58526-114">Service ServiceMain Function</span></span>](service-servicemain-function.md)
-   [<span data-ttu-id="58526-115">Función de controlador de control de servicio</span><span class="sxs-lookup"><span data-stu-id="58526-115">Service Control Handler Function</span></span>](service-control-handler-function.md)

<span data-ttu-id="58526-116">Estos temas no se aplican a los servicios de controlador.</span><span class="sxs-lookup"><span data-stu-id="58526-116">These topics do not apply to driver services.</span></span> <span data-ttu-id="58526-117">Para conocer los requisitos de la interfaz de los servicios de controladores, consulte el kit de controladores de Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="58526-117">For interface requirements of driver services, see the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="58526-118">Un servicio se ejecuta como un proceso en segundo plano que puede afectar al rendimiento del sistema, la capacidad de respuesta, la eficiencia energética y la seguridad.</span><span class="sxs-lookup"><span data-stu-id="58526-118">A service runs as a background process that can affect system performance, responsiveness, energy efficiency, and security.</span></span> <span data-ttu-id="58526-119">Para obtener instrucciones sobre la optimización del servicio, consulte [desarrollo de procesos en segundo plano eficaces para Windows](/windows-hardware/drivers/kernel/implementing-power-management).</span><span class="sxs-lookup"><span data-stu-id="58526-119">For service optimization guidelines, see [Developing Efficient Background Processes for Windows](/windows-hardware/drivers/kernel/implementing-power-management).</span></span> <span data-ttu-id="58526-120">En los temas siguientes se describen consideraciones de programación adicionales:</span><span class="sxs-lookup"><span data-stu-id="58526-120">The following topics describe additional programming considerations:</span></span>

-   [<span data-ttu-id="58526-121">Transiciones de estado del servicio</span><span class="sxs-lookup"><span data-stu-id="58526-121">Service State Transitions</span></span>](service-status-transitions.md)
-   [<span data-ttu-id="58526-122">Recepción de eventos en un servicio</span><span class="sxs-lookup"><span data-stu-id="58526-122">Receiving Events in a Service</span></span>](receiving-events-in-a-service.md)
-   [<span data-ttu-id="58526-123">Servicios multiproceso</span><span class="sxs-lookup"><span data-stu-id="58526-123">Multithreaded Services</span></span>](multithreaded-services.md)
-   [<span data-ttu-id="58526-124">Servicios y el registro</span><span class="sxs-lookup"><span data-stu-id="58526-124">Services and the Registry</span></span>](services-and-the-registry.md)
-   [<span data-ttu-id="58526-125">Servicios y unidades redirigidas</span><span class="sxs-lookup"><span data-stu-id="58526-125">Services and Redirected Drives</span></span>](services-and-redirected-drives.md)
-   [<span data-ttu-id="58526-126">Eventos de desencadenador de servicio</span><span class="sxs-lookup"><span data-stu-id="58526-126">Service Trigger Events</span></span>](service-trigger-events.md)

<span data-ttu-id="58526-127">Tenga en cuenta que si el programa de servicio funciona como un servidor RPC, debe usar puntos de conexión dinámicos y autenticación mutua.</span><span class="sxs-lookup"><span data-stu-id="58526-127">Note that if the service program functions as an RPC server, it should use dynamic endpoints and mutual authentication.</span></span>

 

 
