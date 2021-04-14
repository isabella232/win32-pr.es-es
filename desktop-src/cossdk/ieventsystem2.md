---
description: Lo utiliza el servicio de notificación de eventos del sistema (SENS) de Microsoft Internet Explorer para tener acceso al almacén de datos de eventos. Esta interfaz extiende la interfaz IEventSystem.
ms.assetid: ad3c38a6-fa2d-4fcd-8782-1fac7595e829
title: Interfaz IEventSystem2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3a174c9457dc347257677e8111772ad14f0dc9fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496451"
---
# <a name="ieventsystem2-interface"></a><span data-ttu-id="d7f11-104">Interfaz IEventSystem2</span><span class="sxs-lookup"><span data-stu-id="d7f11-104">IEventSystem2 interface</span></span>

<span data-ttu-id="d7f11-105">Lo utiliza el servicio de notificación de eventos del sistema (SENS) de Microsoft Internet Explorer para tener acceso al almacén de datos de eventos.</span><span class="sxs-lookup"><span data-stu-id="d7f11-105">Used by the Microsoft Internet Explorer System Event Notification Service (SENS) to access the event data store.</span></span> <span data-ttu-id="d7f11-106">Esta interfaz extiende la interfaz [**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) .</span><span class="sxs-lookup"><span data-stu-id="d7f11-106">This interface extends the [**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="d7f11-107">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="d7f11-107">When to implement</span></span>

<span data-ttu-id="d7f11-108">No es necesario implementar la interfaz **IEventSystem2** .</span><span class="sxs-lookup"><span data-stu-id="d7f11-108">You do not need to implement the **IEventSystem2** interface.</span></span> <span data-ttu-id="d7f11-109">Un objeto de sistema de eventos proporcionado por el sistema (CLSID \_ CEventSystem) implementa **IEventSystem2**.</span><span class="sxs-lookup"><span data-stu-id="d7f11-109">A system-supplied event system object (CLSID\_CEventSystem) implements **IEventSystem2**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="d7f11-110">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="d7f11-110">When to use</span></span>

<span data-ttu-id="d7f11-111">Si usa SENS, puede llamar a los métodos de **IEventSystem2** para agregar y quitar objetos en el almacén de eventos y para obtener objetos del almacén de eventos.</span><span class="sxs-lookup"><span data-stu-id="d7f11-111">If you use SENS, you can call the methods of **IEventSystem2** to add and remove objects to and from the event store and to obtain objects from the event store.</span></span>

<span data-ttu-id="d7f11-112">Dado que ya no se admiten [**IEventPublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) y el objeto Publisher, no se llama a [**IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) en el método [**ChangedPublisher**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher) .</span><span class="sxs-lookup"><span data-stu-id="d7f11-112">Because [**IEventPublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) and the publisher object are no longer supported, [**IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) is not called on the [**ChangedPublisher**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher) method.</span></span>

## <a name="members"></a><span data-ttu-id="d7f11-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="d7f11-113">Members</span></span>

<span data-ttu-id="d7f11-114">La interfaz **IEventSystem2** hereda de **IEventSystem**.</span><span class="sxs-lookup"><span data-stu-id="d7f11-114">The **IEventSystem2** interface inherits from **IEventSystem**.</span></span> <span data-ttu-id="d7f11-115">**IEventSystem2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d7f11-115">**IEventSystem2** also has these types of members:</span></span>

-   [<span data-ttu-id="d7f11-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="d7f11-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d7f11-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="d7f11-117">Methods</span></span>

<span data-ttu-id="d7f11-118">La interfaz **IEventSystem2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d7f11-118">The **IEventSystem2** interface has these methods.</span></span>



| <span data-ttu-id="d7f11-119">Método</span><span class="sxs-lookup"><span data-stu-id="d7f11-119">Method</span></span>                                                                         | <span data-ttu-id="d7f11-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7f11-120">Description</span></span>                                                                       |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="d7f11-121">**GetVersion**</span><span class="sxs-lookup"><span data-stu-id="d7f11-121">**GetVersion**</span></span>](ieventsystem2-getversion.md)                                 | <span data-ttu-id="d7f11-122">Recupera el número de versión del sistema de eventos.</span><span class="sxs-lookup"><span data-stu-id="d7f11-122">Retrieves the version number of the event system.</span></span><br/>                      |
| [<span data-ttu-id="d7f11-123">**VerifyTransientSubscribers**</span><span class="sxs-lookup"><span data-stu-id="d7f11-123">**VerifyTransientSubscribers**</span></span>](ieventsystem2-verifytransientsubscribers.md) | <span data-ttu-id="d7f11-124">Comprueba la existencia de todos los suscriptores transitorios en el almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="d7f11-124">Verifies the existence of all transient subscribers in the data store.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d7f11-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7f11-125">Requirements</span></span>



| <span data-ttu-id="d7f11-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7f11-126">Requirement</span></span> | <span data-ttu-id="d7f11-127">Value</span><span class="sxs-lookup"><span data-stu-id="d7f11-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d7f11-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7f11-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d7f11-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d7f11-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d7f11-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7f11-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d7f11-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d7f11-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d7f11-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7f11-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f11-133">**IEventSystem**</span><span class="sxs-lookup"><span data-stu-id="d7f11-133">**IEventSystem**</span></span>](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem)
</dt> </dl>

 

