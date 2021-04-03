---
description: Un programa de control de servicio inicia y controla los servicios de.
ms.assetid: e7ba295f-2937-44ad-89e8-40200c5e58b6
title: Programas de control de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78b34232f5f87d84bdf30acd51f57afbf79a8385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907857"
---
# <a name="service-control-programs"></a><span data-ttu-id="6fe74-103">Programas de control de servicios</span><span class="sxs-lookup"><span data-stu-id="6fe74-103">Service Control Programs</span></span>

<span data-ttu-id="6fe74-104">Un programa de control de servicio inicia y controla los servicios de.</span><span class="sxs-lookup"><span data-stu-id="6fe74-104">A service control program starts and controls services.</span></span> <span data-ttu-id="6fe74-105">Las acciones que realiza son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="6fe74-105">It performs the following actions:</span></span>

-   <span data-ttu-id="6fe74-106">Inicia un servicio o un servicio de controlador, si el tipo de inicio es el inicio de la solicitud de servicio \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6fe74-106">Starts a service or driver service, if the start type is SERVICE\_DEMAND\_START.</span></span>
-   <span data-ttu-id="6fe74-107">Envía solicitudes de control a un servicio en ejecución.</span><span class="sxs-lookup"><span data-stu-id="6fe74-107">Sends control requests to a running service.</span></span>
-   <span data-ttu-id="6fe74-108">Consulta el estado actual de un servicio en ejecución.</span><span class="sxs-lookup"><span data-stu-id="6fe74-108">Queries the current status of a running service.</span></span>

<span data-ttu-id="6fe74-109">Estas acciones requieren un identificador abierto para el objeto de servicio.</span><span class="sxs-lookup"><span data-stu-id="6fe74-109">These actions require an open handle to the service object.</span></span> <span data-ttu-id="6fe74-110">Para obtener el identificador, el programa de control de servicios debe:</span><span class="sxs-lookup"><span data-stu-id="6fe74-110">To obtain the handle, the service control program must:</span></span>

1.  <span data-ttu-id="6fe74-111">Utilice la función [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) para obtener un identificador de la base de datos SCM en un equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="6fe74-111">Use the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to obtain a handle to the SCM database on a specified machine.</span></span>
2.  <span data-ttu-id="6fe74-112">Utilice la función [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) o [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para obtener un identificador para el objeto de servicio.</span><span class="sxs-lookup"><span data-stu-id="6fe74-112">Use the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) or [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to obtain a handle to the service object.</span></span>

<span data-ttu-id="6fe74-113">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="6fe74-113">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="6fe74-114">Inicio del servicio</span><span class="sxs-lookup"><span data-stu-id="6fe74-114">Service Startup</span></span>](service-startup.md)
-   [<span data-ttu-id="6fe74-115">Solicitudes de control de servicio</span><span class="sxs-lookup"><span data-stu-id="6fe74-115">Service Control Requests</span></span>](service-control-requests.md)
-   [<span data-ttu-id="6fe74-116">Controlar un servicio mediante SC</span><span class="sxs-lookup"><span data-stu-id="6fe74-116">Controlling a Service Using SC</span></span>](controlling-a-service-using-sc.md)

 

 



