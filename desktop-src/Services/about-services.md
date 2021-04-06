---
description: El administrador de control de servicios (SCM) mantiene una base de datos de servicios instalados y servicios de controladores, y proporciona un medio unificado y seguro para controlarlos.
ms.assetid: a3af8340-d367-417b-9759-7282edf1d694
title: Acerca de los servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87aeec6dfcdc4e2dc0cc0ab3ef084b7927b2c3bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002331"
---
# <a name="about-services"></a><span data-ttu-id="c5eec-103">Acerca de los servicios</span><span class="sxs-lookup"><span data-stu-id="c5eec-103">About Services</span></span>

<span data-ttu-id="c5eec-104">El [Administrador de control de servicios](service-control-manager.md) (SCM) mantiene una base de datos de servicios instalados y servicios de controladores, y proporciona un medio unificado y seguro para controlarlos.</span><span class="sxs-lookup"><span data-stu-id="c5eec-104">The [service control manager](service-control-manager.md) (SCM) maintains a database of installed services and driver services, and provides a unified and secure means of controlling them.</span></span> <span data-ttu-id="c5eec-105">La base de datos incluye información sobre cómo se debe iniciar cada servicio o controlador.</span><span class="sxs-lookup"><span data-stu-id="c5eec-105">The database includes information on how each service or driver service should be started.</span></span> <span data-ttu-id="c5eec-106">También permite a los administradores del sistema personalizar los requisitos de seguridad para cada servicio y, por tanto, controlar el acceso al servicio.</span><span class="sxs-lookup"><span data-stu-id="c5eec-106">It also enables system administrators to customize security requirements for each service and thereby control access to the service.</span></span>

<span data-ttu-id="c5eec-107">Los siguientes tipos de programas usan las funciones proporcionadas por el SCM.</span><span class="sxs-lookup"><span data-stu-id="c5eec-107">The following types of programs use the functions provided by the SCM.</span></span>



| <span data-ttu-id="c5eec-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5eec-108">Type</span></span>                          | <span data-ttu-id="c5eec-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5eec-109">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5eec-110">Programa de servicio</span><span class="sxs-lookup"><span data-stu-id="c5eec-110">Service program</span></span>               | <span data-ttu-id="c5eec-111">Programa que proporciona código ejecutable para uno o más servicios.</span><span class="sxs-lookup"><span data-stu-id="c5eec-111">A program that provides executable code for one or more services.</span></span> <span data-ttu-id="c5eec-112">Los programas de servicio usan funciones que se conectan al SCM y envían información de estado al SCM.</span><span class="sxs-lookup"><span data-stu-id="c5eec-112">Service programs use functions that connect to the SCM and send status information to the SCM.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="c5eec-113">Programa de configuración del servicio</span><span class="sxs-lookup"><span data-stu-id="c5eec-113">Service configuration program</span></span> | <span data-ttu-id="c5eec-114">Programa que consulta o modifica la base de datos de servicios.</span><span class="sxs-lookup"><span data-stu-id="c5eec-114">A program that queries or modifies the services database.</span></span> <span data-ttu-id="c5eec-115">Los programas de configuración de servicio usan funciones que abren la base de datos, instalan o eliminan servicios en la base de datos y consultan o modifican los parámetros de configuración y seguridad para los servicios instalados.</span><span class="sxs-lookup"><span data-stu-id="c5eec-115">Service configuration programs use functions that open the database, install or delete services in the database, and query or modify the configuration and security parameters for installed services.</span></span> <span data-ttu-id="c5eec-116">Los programas de configuración de servicio administran servicios y servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="c5eec-116">Service configuration programs manage both services and driver services.</span></span> |
| <span data-ttu-id="c5eec-117">Programa de control de servicios</span><span class="sxs-lookup"><span data-stu-id="c5eec-117">Service control program</span></span>       | <span data-ttu-id="c5eec-118">Programa que inicia y controla servicios y servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="c5eec-118">A program that starts and controls services and driver services.</span></span> <span data-ttu-id="c5eec-119">Los programas de control de servicios usan funciones que envían solicitudes al SCM, que lleva a cabo la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c5eec-119">Service control programs use functions that send requests to the SCM, which carries out the request.</span></span>                                                                                                                                                                     |



 

<span data-ttu-id="c5eec-120">En esta información general se describen los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="c5eec-120">This overview discusses the following topics:</span></span>

-   [<span data-ttu-id="c5eec-121">Administrador de control de servicios</span><span class="sxs-lookup"><span data-stu-id="c5eec-121">Service Control Manager</span></span>](service-control-manager.md)
-   [<span data-ttu-id="c5eec-122">Programas de servicio</span><span class="sxs-lookup"><span data-stu-id="c5eec-122">Service Programs</span></span>](service-programs.md)
-   [<span data-ttu-id="c5eec-123">Programas de configuración de servicio</span><span class="sxs-lookup"><span data-stu-id="c5eec-123">Service Configuration Programs</span></span>](service-configuration-programs.md)
-   [<span data-ttu-id="c5eec-124">Programas de control de servicios</span><span class="sxs-lookup"><span data-stu-id="c5eec-124">Service Control Programs</span></span>](service-control-programs.md)
-   [<span data-ttu-id="c5eec-125">Cuentas de usuario de servicio</span><span class="sxs-lookup"><span data-stu-id="c5eec-125">Service User Accounts</span></span>](service-user-accounts.md)
-   [<span data-ttu-id="c5eec-126">Servicios interactivos</span><span class="sxs-lookup"><span data-stu-id="c5eec-126">Interactive Services</span></span>](interactive-services.md)
-   [<span data-ttu-id="c5eec-127">Derechos de acceso y seguridad del servicio</span><span class="sxs-lookup"><span data-stu-id="c5eec-127">Service Security and Access Rights</span></span>](service-security-and-access-rights.md)
-   [<span data-ttu-id="c5eec-128">Depuración de un servicio</span><span class="sxs-lookup"><span data-stu-id="c5eec-128">Debugging a Service</span></span>](debugging-a-service.md)
-   [<span data-ttu-id="c5eec-129">Eventos de desencadenador de servicio</span><span class="sxs-lookup"><span data-stu-id="c5eec-129">Service Trigger Events</span></span>](service-trigger-events.md)

 

 



