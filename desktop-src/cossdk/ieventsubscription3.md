---
description: Almacena y recupera información sobre las suscripciones a eventos. Esta interfaz extiende la interfaz IEventSubscription2.
ms.assetid: fd1c136e-6e4e-42ca-a951-4aa5fcdfaa49
title: Interfaz IEventSubscription3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3
api_type:
- COM
api_location: ''
ms.openlocfilehash: 94225faf957b2eac3388422d74df3cfdb8bf6d90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705373"
---
# <a name="ieventsubscription3-interface"></a><span data-ttu-id="b5b27-104">Interfaz IEventSubscription3</span><span class="sxs-lookup"><span data-stu-id="b5b27-104">IEventSubscription3 interface</span></span>

<span data-ttu-id="b5b27-105">Almacena y recupera información sobre las suscripciones a eventos.</span><span class="sxs-lookup"><span data-stu-id="b5b27-105">Stores and retrieves information about event subscriptions.</span></span> <span data-ttu-id="b5b27-106">Esta interfaz extiende la interfaz [**IEventSubscription2**](ieventsubscription2.md) .</span><span class="sxs-lookup"><span data-stu-id="b5b27-106">This interface extends the [**IEventSubscription2**](ieventsubscription2.md) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="b5b27-107">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="b5b27-107">When to implement</span></span>

<span data-ttu-id="b5b27-108">No es necesario implementar la interfaz **IEventSubscription3** .</span><span class="sxs-lookup"><span data-stu-id="b5b27-108">You do not need to implement the **IEventSubscription3** interface.</span></span> <span data-ttu-id="b5b27-109">Una clase de objeto de evento proporcionado por el sistema (CLSID \_ CEventSubscription) implementa **IEventSubscription3**.</span><span class="sxs-lookup"><span data-stu-id="b5b27-109">A system-supplied event object class (CLSID\_CEventSubscription) implements **IEventSubscription3**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="b5b27-110">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="b5b27-110">When to use</span></span>

<span data-ttu-id="b5b27-111">El sistema de [eventos com+](com--events.md) usa esta interfaz para obtener información acerca de las suscripciones individuales.</span><span class="sxs-lookup"><span data-stu-id="b5b27-111">The [COM+ Events](com--events.md) system uses this interface to obtain information about individual subscriptions.</span></span>

## <a name="members"></a><span data-ttu-id="b5b27-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="b5b27-112">Members</span></span>

<span data-ttu-id="b5b27-113">La interfaz **IEventSubscription3** hereda de **IEventSubscription2**.</span><span class="sxs-lookup"><span data-stu-id="b5b27-113">The **IEventSubscription3** interface inherits from **IEventSubscription2**.</span></span> <span data-ttu-id="b5b27-114">**IEventSubscription3** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b5b27-114">**IEventSubscription3** also has these types of members:</span></span>

-   [<span data-ttu-id="b5b27-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b5b27-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5b27-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b5b27-116">Properties</span></span>

<span data-ttu-id="b5b27-117">La interfaz **IEventSubscription3** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b5b27-117">The **IEventSubscription3** interface has these properties.</span></span>



| <span data-ttu-id="b5b27-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b5b27-118">Property</span></span>                                                                                  | <span data-ttu-id="b5b27-119">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="b5b27-119">Access type</span></span>           | <span data-ttu-id="b5b27-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5b27-120">Description</span></span>                                                |
|:------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="b5b27-121">**EventClassApplicationID**</span><span class="sxs-lookup"><span data-stu-id="b5b27-121">**EventClassApplicationID**</span></span>](ieventsubscription3-eventclassapplicationid.md)<br/> | <span data-ttu-id="b5b27-122">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b5b27-122">Read/write</span></span><br/> | <span data-ttu-id="b5b27-123">GUID de la aplicación del objeto de la clase de evento.</span><span class="sxs-lookup"><span data-stu-id="b5b27-123">The application GUID of the event class object.</span></span><br/> |
| [<span data-ttu-id="b5b27-124">**EventClassPartitionID**</span><span class="sxs-lookup"><span data-stu-id="b5b27-124">**EventClassPartitionID**</span></span>](ieventsubscription3-eventclasspartitionid.md)<br/>     | <span data-ttu-id="b5b27-125">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b5b27-125">Read/write</span></span><br/> | <span data-ttu-id="b5b27-126">GUID de la partición del objeto de la clase de evento.</span><span class="sxs-lookup"><span data-stu-id="b5b27-126">The partition GUID of the event class object.</span></span><br/>   |
| [<span data-ttu-id="b5b27-127">**SubscriberApplicationID**</span><span class="sxs-lookup"><span data-stu-id="b5b27-127">**SubscriberApplicationID**</span></span>](ieventsubscription3-subscriberapplicationid.md)<br/> | <span data-ttu-id="b5b27-128">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b5b27-128">Read/write</span></span><br/> | <span data-ttu-id="b5b27-129">GUID de la aplicación del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="b5b27-129">The application GUID of the subscriber.</span></span><br/>         |
| [<span data-ttu-id="b5b27-130">**SubscriberPartitionID**</span><span class="sxs-lookup"><span data-stu-id="b5b27-130">**SubscriberPartitionID**</span></span>](ieventsubscription3-subscriberpartitionid.md)<br/>     | <span data-ttu-id="b5b27-131">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b5b27-131">Read/write</span></span><br/> | <span data-ttu-id="b5b27-132">GUID de partición del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="b5b27-132">The partition GUID of the subscriber.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="b5b27-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5b27-133">Requirements</span></span>



| <span data-ttu-id="b5b27-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5b27-134">Requirement</span></span> | <span data-ttu-id="b5b27-135">Value</span><span class="sxs-lookup"><span data-stu-id="b5b27-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b5b27-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5b27-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b5b27-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b5b27-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b5b27-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5b27-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b5b27-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b5b27-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b5b27-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5b27-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5b27-141">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="b5b27-141">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




