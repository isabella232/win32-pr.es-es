---
title: Obtención del servicio y el usuario SDOs
description: Para obtener SDOs para NPS (IAS) o un usuario determinado, llame a los métodos ISdoMachine GetServiceSDO o ISdoMachine GetUserSDO.
ms.assetid: 23e23fb3-0102-4c36-b30f-18604131ee32
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c7562c3b7c6aa1150ba3ce6581441064eb386f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359166"
---
# <a name="obtaining-service-and-user-sdos"></a><span data-ttu-id="3124f-103">Obtención del servicio y el usuario SDOs</span><span class="sxs-lookup"><span data-stu-id="3124f-103">Obtaining Service and User SDOs</span></span>

> [!Note]  
> <span data-ttu-id="3124f-104">Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3124f-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

<span data-ttu-id="3124f-105">Para obtener SDOs para NPS (IAS) o un usuario determinado, llame a los métodos [**ISdoMachine:: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) o [**ISdoMachine:: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) .</span><span class="sxs-lookup"><span data-stu-id="3124f-105">To obtain SDOs for NPS (IAS) or a particular user, call the [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) or [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) methods.</span></span> <span data-ttu-id="3124f-106">Estos métodos devuelven punteros a las interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para estos objetos.</span><span class="sxs-lookup"><span data-stu-id="3124f-106">These methods return pointers to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interfaces for these objects.</span></span> <span data-ttu-id="3124f-107">Para el SDO de usuarios, use el método [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener una interfaz [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) para el objeto.</span><span class="sxs-lookup"><span data-stu-id="3124f-107">For the user SDO, use the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method to obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface for the object.</span></span> <span data-ttu-id="3124f-108">En el caso de los SDO de servicio, use **IUnknown:: QueryInterface** para obtener una interfaz [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) o una interfaz [**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) .</span><span class="sxs-lookup"><span data-stu-id="3124f-108">For the service SDO, use **IUnknown::QueryInterface** to obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface or [**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) interface.</span></span>

<span data-ttu-id="3124f-109">Antes de llamar a [**ISdoMachine:: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) o [**ISdoMachine:: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo), llame a [**ISdoMachine:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) para asociar el objeto de equipo al equipo local.</span><span class="sxs-lookup"><span data-stu-id="3124f-109">Before calling either [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) or [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo), call [**ISdoMachine::Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) to associate the machine object with the local computer.</span></span>

<span data-ttu-id="3124f-110">Vea [recuperar un SDO de servicio](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) y [recuperar un SDO de usuarios](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) para obtener código de ejemplo que muestra cómo obtener estos SDOs.</span><span class="sxs-lookup"><span data-stu-id="3124f-110">See [Retrieving a Service SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) and [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) for sample code that demonstrates how to obtain these SDOs.</span></span>

 

 