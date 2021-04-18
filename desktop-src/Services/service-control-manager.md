---
description: El administrador de control de servicios (SCM) se inicia en el arranque del sistema. Es un servidor de llamada a procedimiento remoto (RPC), por lo que los programas de configuración de servicio y de control de servicio pueden manipular servicios en equipos remotos.
ms.assetid: 56ad011d-17c4-4410-b598-6ef47fb3638f
title: Administrador de control de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8a35fd34bd2714d22d40ccf618c89a8b66a6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666447"
---
# <a name="service-control-manager"></a><span data-ttu-id="a3a3e-104">Administrador de control de servicios</span><span class="sxs-lookup"><span data-stu-id="a3a3e-104">Service Control Manager</span></span>

<span data-ttu-id="a3a3e-105">El administrador de control de servicios (SCM) se inicia en el arranque del sistema.</span><span class="sxs-lookup"><span data-stu-id="a3a3e-105">The service control manager (SCM) is started at system boot.</span></span> <span data-ttu-id="a3a3e-106">Es un servidor de llamada a procedimiento remoto (RPC), por lo que los programas de configuración de servicio y de control de servicio pueden manipular servicios en equipos remotos.</span><span class="sxs-lookup"><span data-stu-id="a3a3e-106">It is a remote procedure call (RPC) server, so that service configuration and service control programs can manipulate services on remote machines.</span></span>

<span data-ttu-id="a3a3e-107">Las funciones de servicio proporcionan una interfaz para las siguientes tareas realizadas por el SCM:</span><span class="sxs-lookup"><span data-stu-id="a3a3e-107">The service functions provide an interface for the following tasks performed by the SCM:</span></span>

-   <span data-ttu-id="a3a3e-108">Mantenimiento de la base de datos de servicios instalados.</span><span class="sxs-lookup"><span data-stu-id="a3a3e-108">Maintaining the database of installed services.</span></span>
-   <span data-ttu-id="a3a3e-109">Iniciar servicios y servicios de controladores al iniciar el sistema o a petición.</span><span class="sxs-lookup"><span data-stu-id="a3a3e-109">Starting services and driver services either upon system startup or upon demand.</span></span>
-   <span data-ttu-id="a3a3e-110">Enumerar servicios instalados y servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="a3a3e-110">Enumerating installed services and driver services.</span></span>
-   <span data-ttu-id="a3a3e-111">Mantenimiento de la información de estado para la ejecución de servicios y servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="a3a3e-111">Maintaining status information for running services and driver services.</span></span>
-   <span data-ttu-id="a3a3e-112">Transmisión de solicitudes de control a servicios en ejecución.</span><span class="sxs-lookup"><span data-stu-id="a3a3e-112">Transmitting control requests to running services.</span></span>
-   <span data-ttu-id="a3a3e-113">Bloqueo y desbloqueo de la base de datos de servicio.</span><span class="sxs-lookup"><span data-stu-id="a3a3e-113">Locking and unlocking the service database.</span></span>

<span data-ttu-id="a3a3e-114">En las secciones siguientes se describe con más detalle el SCM:</span><span class="sxs-lookup"><span data-stu-id="a3a3e-114">The following sections describe the SCM in more detail:</span></span>

-   [<span data-ttu-id="a3a3e-115">Base de datos de servicios instalados</span><span class="sxs-lookup"><span data-stu-id="a3a3e-115">Database of Installed Services</span></span>](database-of-installed-services.md)
-   [<span data-ttu-id="a3a3e-116">Inicio automático de servicios</span><span class="sxs-lookup"><span data-stu-id="a3a3e-116">Automatically Starting Services</span></span>](automatically-starting-services.md)
-   [<span data-ttu-id="a3a3e-117">Inicio de servicios a petición</span><span class="sxs-lookup"><span data-stu-id="a3a3e-117">Starting Services on Demand</span></span>](starting-services-on-demand.md)
-   [<span data-ttu-id="a3a3e-118">Lista de registros de servicio</span><span class="sxs-lookup"><span data-stu-id="a3a3e-118">Service Record List</span></span>](service-record-list.md)
-   [<span data-ttu-id="a3a3e-119">Identificadores de SCM</span><span class="sxs-lookup"><span data-stu-id="a3a3e-119">SCM Handles</span></span>](scm-handles.md)

 

 



