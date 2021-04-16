---
description: Almacena y recupera información sobre las suscripciones a eventos. Esta interfaz extiende la interfaz IEventSubscription.
ms.assetid: f153afb7-c897-40f8-81ed-50308844cac5
title: Interfaz IEventSubscription2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2
api_type:
- COM
api_location: ''
ms.openlocfilehash: bc7e3e41efc4b44c00c23f0910b8b696940fc1df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686460"
---
# <a name="ieventsubscription2-interface"></a><span data-ttu-id="876b3-104">Interfaz IEventSubscription2</span><span class="sxs-lookup"><span data-stu-id="876b3-104">IEventSubscription2 interface</span></span>

<span data-ttu-id="876b3-105">Almacena y recupera información sobre las suscripciones a eventos.</span><span class="sxs-lookup"><span data-stu-id="876b3-105">Stores and retrieves information about event subscriptions.</span></span> <span data-ttu-id="876b3-106">Esta interfaz extiende la interfaz [**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) .</span><span class="sxs-lookup"><span data-stu-id="876b3-106">This interface extends the [**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="876b3-107">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="876b3-107">When to implement</span></span>

<span data-ttu-id="876b3-108">No es necesario implementar la interfaz **IEventSubscription2** .</span><span class="sxs-lookup"><span data-stu-id="876b3-108">You do not need to implement the **IEventSubscription2** interface.</span></span> <span data-ttu-id="876b3-109">Una clase de objeto de evento proporcionado por el sistema (CLSID \_ CEventSubscription) implementa **IEventSubscription2**.</span><span class="sxs-lookup"><span data-stu-id="876b3-109">A system-supplied event object class (CLSID\_CEventSubscription) implements **IEventSubscription2**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="876b3-110">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="876b3-110">When to use</span></span>

<span data-ttu-id="876b3-111">El sistema de [eventos com+](com--events.md) usa esta interfaz para obtener información acerca de las suscripciones individuales.</span><span class="sxs-lookup"><span data-stu-id="876b3-111">The [COM+ Events](com--events.md) system uses this interface to obtain information about individual subscriptions.</span></span>

## <a name="members"></a><span data-ttu-id="876b3-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="876b3-112">Members</span></span>

<span data-ttu-id="876b3-113">La interfaz **IEventSubscription2** hereda de **IEventSubscription**.</span><span class="sxs-lookup"><span data-stu-id="876b3-113">The **IEventSubscription2** interface inherits from **IEventSubscription**.</span></span> <span data-ttu-id="876b3-114">**IEventSubscription2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="876b3-114">**IEventSubscription2** also has these types of members:</span></span>

-   [<span data-ttu-id="876b3-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="876b3-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="876b3-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="876b3-116">Properties</span></span>

<span data-ttu-id="876b3-117">La interfaz **IEventSubscription2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="876b3-117">The **IEventSubscription2** interface has these properties.</span></span>



| <span data-ttu-id="876b3-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="876b3-118">Property</span></span>                                                                      | <span data-ttu-id="876b3-119">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="876b3-119">Access type</span></span>           | <span data-ttu-id="876b3-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="876b3-120">Description</span></span>                                                |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="876b3-121">**FilterCriteria**</span><span class="sxs-lookup"><span data-stu-id="876b3-121">**FilterCriteria**</span></span>](ieventsubscription2-filtercriteria.md)<br/>       | <span data-ttu-id="876b3-122">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="876b3-122">Read/write</span></span><br/> | <span data-ttu-id="876b3-123">Los criterios de filtro que rigen la suscripción.</span><span class="sxs-lookup"><span data-stu-id="876b3-123">The filter criteria governing the subscription.</span></span><br/> |
| [<span data-ttu-id="876b3-124">**SubscriberMoniker**</span><span class="sxs-lookup"><span data-stu-id="876b3-124">**SubscriberMoniker**</span></span>](ieventsubscription2-subscribermoniker.md)<br/> | <span data-ttu-id="876b3-125">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="876b3-125">Read/write</span></span><br/> | <span data-ttu-id="876b3-126">Moniker del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="876b3-126">The subscriber's moniker.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="876b3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="876b3-127">Requirements</span></span>



| <span data-ttu-id="876b3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="876b3-128">Requirement</span></span> | <span data-ttu-id="876b3-129">Value</span><span class="sxs-lookup"><span data-stu-id="876b3-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="876b3-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="876b3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="876b3-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="876b3-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="876b3-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="876b3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="876b3-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="876b3-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="876b3-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="876b3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="876b3-135">**IEventSubscription**</span><span class="sxs-lookup"><span data-stu-id="876b3-135">**IEventSubscription**</span></span>](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 




