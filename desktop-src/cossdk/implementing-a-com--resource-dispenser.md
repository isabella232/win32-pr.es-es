---
description: Implementación de un dispensador de recursos COM+
ms.assetid: 083c5962-f55a-435a-964e-fdc868f9bd3d
title: Implementación de un dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81e189f3bfc5025bc949ef6e5bc82bf9408c339
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153462"
---
# <a name="implementing-a-com-resource-dispenser"></a><span data-ttu-id="a426f-103">Implementación de un dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="a426f-103">Implementing a COM+ Resource Dispenser</span></span>

<span data-ttu-id="a426f-104">En los pasos siguientes se describe un procedimiento general para implementar un dispensador de recursos COM+:</span><span class="sxs-lookup"><span data-stu-id="a426f-104">The following steps outline a general procedure for implementing a COM+ resource dispenser:</span></span>

1.  <span data-ttu-id="a426f-105">Decida el formato **RESTYPID** que clasifique el modo en que los recursos difieren entre sí.</span><span class="sxs-lookup"><span data-stu-id="a426f-105">Decide on **RESTYPID** format that categorizes how your resources differ from each other.</span></span>

2.  <span data-ttu-id="a426f-106">Use la biblioteca y el archivo de encabezado Mtxdm. h y Mtxdm. lib, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a426f-106">Use the Mtxdm.h and Mtxdm.lib header file and library, respectively.</span></span>

3.  <span data-ttu-id="a426f-107">Cree un archivo DLL que implemente la interfaz [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) y la API que desee exponer a las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a426f-107">Build a DLL that implements the [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) interface and the API you want to expose to applications.</span></span>

4.  <span data-ttu-id="a426f-108">En Startup ([*DllMain*](/windows/desktop/Dlls/dllmain) o primera llamada a la API Dispensary), llame a la función [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) .</span><span class="sxs-lookup"><span data-stu-id="a426f-108">In the startup ([*DllMain*](/windows/desktop/Dlls/dllmain) or first call to the dispenser API), call the [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) function.</span></span> <span data-ttu-id="a426f-109">Esto devuelve un puntero a la interfaz [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) del administrador del dispensador.</span><span class="sxs-lookup"><span data-stu-id="a426f-109">This returns a pointer to the dispenser manager's [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) interface.</span></span>

5.  <span data-ttu-id="a426f-110">Llame a [**IDispenserManager:: RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser), pasando un puntero a la implementación de [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver).</span><span class="sxs-lookup"><span data-stu-id="a426f-110">Call [**IDispenserManager::RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser), passing a pointer to your implementation of [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver).</span></span> <span data-ttu-id="a426f-111">Esto hace que el administrador del dispensador cree un titular (Administrador de agrupación) para el dispensador de recursos y, a continuación, devuelva el puntero a la interfaz [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) .</span><span class="sxs-lookup"><span data-stu-id="a426f-111">This causes the dispenser manager to create a holder (pooling manager) for your resource dispenser and then return the pointer to your [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) interface.</span></span>

6.  <span data-ttu-id="a426f-112">Almacene este puntero para que pueda llamar a [**IHolder:: AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) y [**IHolder:: FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span><span class="sxs-lookup"><span data-stu-id="a426f-112">Store this pointer so that you can call [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) and [**IHolder::FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span></span>

7.  <span data-ttu-id="a426f-113">Ahora puede realizar llamadas a [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) y [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource)(en respuesta a las llamadas a la API).</span><span class="sxs-lookup"><span data-stu-id="a426f-113">You can now (in response to calls to your API) make calls to [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) and [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span></span> <span data-ttu-id="a426f-114">**AllocResource** responde inicialmente llamando al método [**CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) , pero las llamadas a **AllocResource** posteriores se prestan desde el creciente grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a426f-114">**AllocResource** initially responds by calling back to your [**CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) method, but later **AllocResource** calls are serviced from the growing pool of resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a426f-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a426f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a426f-116">Conceptos del dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="a426f-116">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="a426f-117">Interfaces dispensadoras de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="a426f-117">COM+ Resource Dispenser Interfaces</span></span>](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 
