---
description: La interfaz IUpdateServiceManager define los siguientes métodos.
ms.assetid: b2ae49bc-3fb6-4cb9-82ce-387409096159
title: Métodos IUpdateServiceManager
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464b0b6e48d074dbc43f370f267fe7a526e8269b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540139"
---
# <a name="iupdateservicemanager-methods"></a><span data-ttu-id="19ff7-103">Métodos IUpdateServiceManager</span><span class="sxs-lookup"><span data-stu-id="19ff7-103">IUpdateServiceManager Methods</span></span>

<span data-ttu-id="19ff7-104">La interfaz [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) define los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="19ff7-104">The [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) interface defines the following methods.</span></span>



| <span data-ttu-id="19ff7-105">Método</span><span class="sxs-lookup"><span data-stu-id="19ff7-105">Method</span></span>                                                                           | <span data-ttu-id="19ff7-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="19ff7-106">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19ff7-107">**AddScanPackageService**</span><span class="sxs-lookup"><span data-stu-id="19ff7-107">**AddScanPackageService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice)     | <span data-ttu-id="19ff7-108">Registra un paquete de examen como un servicio con Windows Update Agent (WUA) y, a continuación, devuelve una interfaz [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) .</span><span class="sxs-lookup"><span data-stu-id="19ff7-108">Registers a scan package as a service with Windows Update Agent (WUA) and then returns an [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) interface.</span></span>    |
| [<span data-ttu-id="19ff7-109">**AddService**</span><span class="sxs-lookup"><span data-stu-id="19ff7-109">**AddService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)                           | <span data-ttu-id="19ff7-110">Registra un servicio con WUA.</span><span class="sxs-lookup"><span data-stu-id="19ff7-110">Registers a service with WUA.</span></span>                                                                                                                    |
| [<span data-ttu-id="19ff7-111">**RegisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="19ff7-111">**RegisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)     | <span data-ttu-id="19ff7-112">Registra un servicio con Actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="19ff7-112">Registers a service with Automatic Updates.</span></span>                                                                                                      |
| [<span data-ttu-id="19ff7-113">**RemoveService**</span><span class="sxs-lookup"><span data-stu-id="19ff7-113">**RemoveService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-removeservice)                     | <span data-ttu-id="19ff7-114">Quita un registro de servicio de WUA.</span><span class="sxs-lookup"><span data-stu-id="19ff7-114">Removes a service registration from WUA.</span></span>                                                                                                         |
| [<span data-ttu-id="19ff7-115">**SetOption (**</span><span class="sxs-lookup"><span data-stu-id="19ff7-115">**SetOption**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-setoption)                             | <span data-ttu-id="19ff7-116">Establece las opciones del objeto que especifica el identificador de servicio y si se muestra una advertencia al cambiar el registro de Actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="19ff7-116">Sets options for the object that specifies the service ID, and whether to display a warning when changing the registration of Automatic Updates.</span></span> |
| [<span data-ttu-id="19ff7-117">**UnregisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="19ff7-117">**UnregisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau) | <span data-ttu-id="19ff7-118">Anula el registro de un servicio con Actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="19ff7-118">Unregisters a service with Automatic Updates.</span></span>                                                                                                    |



 

 

 



