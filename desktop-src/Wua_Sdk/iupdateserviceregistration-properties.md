---
description: La interfaz IUpdateServiceRegistration define las siguientes propiedades.
ms.assetid: 2bcde8b4-7bff-4887-8080-89da817afb5f
title: Propiedades de IUpdateServiceRegistration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716c06f2fc8ed9a7ce12542a09440cf0ec0b5c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696244"
---
# <a name="iupdateserviceregistration-properties"></a><span data-ttu-id="a2eb3-103">Propiedades de IUpdateServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="a2eb3-103">IUpdateServiceRegistration Properties</span></span>

<span data-ttu-id="a2eb3-104">La interfaz **IUpdateServiceRegistration** define las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="a2eb3-104">The **IUpdateServiceRegistration** interface defines the following properties.</span></span>



| <span data-ttu-id="a2eb3-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a2eb3-105">Property</span></span>                                                                                      | <span data-ttu-id="a2eb3-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2eb3-106">Description</span></span>                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2eb3-107">**IsPendingRegistrationWithAU**</span><span class="sxs-lookup"><span data-stu-id="a2eb3-107">**IsPendingRegistrationWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_ispendingregistrationwithau) | <span data-ttu-id="a2eb3-108">Obtiene un valor booleano que indica si el servicio también se registrará con Actualizaciones automáticas, cuando se agregue.</span><span class="sxs-lookup"><span data-stu-id="a2eb3-108">Gets a Boolean value that indicates whether the service will also be registered with Automatic Updates, when added.</span></span>                                  |
| [<span data-ttu-id="a2eb3-109">**RegistrationState**</span><span class="sxs-lookup"><span data-stu-id="a2eb3-109">**RegistrationState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_registrationstate)                     | <span data-ttu-id="a2eb3-110">Obtiene un valor [**UpdateServiceRegistrationState**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) que indica el estado actual del registro del servicio.</span><span class="sxs-lookup"><span data-stu-id="a2eb3-110">Gets an [**UpdateServiceRegistrationState**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) value that indicates the current state of the service registration.</span></span> |
| [<span data-ttu-id="a2eb3-111">**Servicio**</span><span class="sxs-lookup"><span data-stu-id="a2eb3-111">**Service**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_service)                                         | <span data-ttu-id="a2eb3-112">Obtiene un puntero a una interfaz [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) .</span><span class="sxs-lookup"><span data-stu-id="a2eb3-112">Gets a pointer to an [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) interface.</span></span> <span data-ttu-id="a2eb3-113">Esta propiedad es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a2eb3-113">This property is the default property.</span></span>                                    |



 

 

 



