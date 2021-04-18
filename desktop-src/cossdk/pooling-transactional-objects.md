---
description: Los componentes transaccionales que se van a agrupar tienen requisitos especiales.
ms.assetid: 32e2f830-c30a-4dbc-8e69-dd2038851998
title: Agrupar objetos transaccionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 006ba32ad2ac550be4fa4418dde322ded26c64c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705324"
---
# <a name="pooling-transactional-objects"></a><span data-ttu-id="9eeb1-103">Agrupar objetos transaccionales</span><span class="sxs-lookup"><span data-stu-id="9eeb1-103">Pooling Transactional Objects</span></span>

<span data-ttu-id="9eeb1-104">Los componentes transaccionales que se van a agrupar tienen requisitos especiales.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-104">Transactional components that are to be pooled have special requirements.</span></span>

## <a name="manually-enlisting-resources"></a><span data-ttu-id="9eeb1-105">Inscripción manual de recursos</span><span class="sxs-lookup"><span data-stu-id="9eeb1-105">Manually Enlisting Resources</span></span>

<span data-ttu-id="9eeb1-106">Los objetos agrupables que participan en transacciones deben dar de alta manualmente los recursos administrados.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-106">Poolable objects that participate in transactions must manually enlist managed resources.</span></span> <span data-ttu-id="9eeb1-107">Si un objeto contiene recursos administrados entre clientes, no habrá forma de que el administrador de recursos dé de alta automáticamente en una transacción cuando el objeto se activa en un contexto determinado.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-107">If an object holds managed resources between clients, there will be no way for the resource manager to automatically enlist in a transaction when the object is activated in a given context.</span></span>

<span data-ttu-id="9eeb1-108">El propio objeto debe controlar la lógica de detección de la transacción, la desactivación de la inscripción automática del administrador de recursos y la inscripción manual de los recursos que contiene.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-108">The object itself must handle the logic of detecting the transaction, turning off the resource manager's auto-enlistment, and manually enlisting any resources that it holds.</span></span> <span data-ttu-id="9eeb1-109">Los pasos para hacerlo son específicos del administrador de recursos que está usando.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-109">The steps for doing this are specific to the resource manager that you are using.</span></span> <span data-ttu-id="9eeb1-110">Si necesita realizar una inscripción manual, consulte la documentación del administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-110">If you need to do manual enlistment, consult the documentation for your resource manager.</span></span>

<span data-ttu-id="9eeb1-111">Tal y como se describe a continuación, los objetos se pueden agrupar con afinidad de transacciones mientras una transacción está activa y se puede activar con la afinidad de transacciones si la llama un cliente asociado a esa transacción.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-111">As described below, objects can be pooled with transaction affinity while a transaction is active and can be activated with transaction affinity if called by a client associated with that transaction.</span></span> <span data-ttu-id="9eeb1-112">Antes de dar de alta los recursos, primero debe comprobar la afinidad de la transacción.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-112">Before enlisting resources, you should first check for transaction affinity.</span></span> <span data-ttu-id="9eeb1-113">Si el objeto se ha tomado del grupo específico de esa transacción, ya ha hecho trabajo en esa transacción y dado de alta sus recursos.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-113">If the object has been taken from the pool specific to that transaction, it has already done work in that transaction and enlisted its resources.</span></span>

## <a name="turning-off-automatic-enlistment"></a><span data-ttu-id="9eeb1-114">Desactivación de la inscripción automática</span><span class="sxs-lookup"><span data-stu-id="9eeb1-114">Turning Off Automatic Enlistment</span></span>

<span data-ttu-id="9eeb1-115">La inscripción automática debe desactivarse después de adquirir el recurso, normalmente en el constructor del objeto.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-115">Automatic enlistment should be turned off after the resource is acquired, usually in the object's constructor.</span></span> <span data-ttu-id="9eeb1-116">Es decir, deshabilite la inscripción automática y, a continuación, conéctese.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-116">That is, you disable automatic enlistment and then connect.</span></span>

<span data-ttu-id="9eeb1-117">La deshabilitación de la inscripción automática a veces puede ser un procedimiento sutil, especialmente en el caso de los proveedores de acceso a datos por capas.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-117">Disabling auto-enlistment can sometimes be a subtle procedure, particularly in the case of layered data access providers.</span></span> <span data-ttu-id="9eeb1-118">La inscripción automática a veces se acopla con la agrupación de conexiones, como con ODBC y, a veces, no, como con OLE DB.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-118">Auto-enlistment is sometimes coupled with connection pooling, as with ODBC, and sometimes not, as with OLE DB.</span></span> <span data-ttu-id="9eeb1-119">Es posible que deba asegurarse de que la inscripción automática está desactivada en varios niveles de proveedores.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-119">You might need to ensure that auto-enlistment is off at several levels of providers.</span></span>

## <a name="implementing-iobjectcontrol"></a><span data-ttu-id="9eeb1-120">Implementar IObjectControl</span><span class="sxs-lookup"><span data-stu-id="9eeb1-120">Implementing IObjectControl</span></span>

<span data-ttu-id="9eeb1-121">Los objetos agrupables que participan en transacciones deben supervisar el estado actual de los recursos que contienen.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-121">Poolable objects that participate in transactions must monitor the current state of resources they are holding.</span></span> <span data-ttu-id="9eeb1-122">Si el objeto detecta que se encuentra en un estado no reutilizable (por ejemplo, si una conexión es incorrecta), debe devolver false para [**IObjectControl:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span><span class="sxs-lookup"><span data-stu-id="9eeb1-122">If the object detects that it is in a non-reusable state—for example, if a connection is bad—it should return False for [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span></span> <span data-ttu-id="9eeb1-123">Esto tendrá el efecto de descartar la instancia de objeto y desechar la transacción actual.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-123">This will have the effect of both discarding the object instance and dooming the current transaction.</span></span>

## <a name="transaction-specific-pools"></a><span data-ttu-id="9eeb1-124">Grupos de Transaction-Specific</span><span class="sxs-lookup"><span data-stu-id="9eeb1-124">Transaction-Specific Pools</span></span>

<span data-ttu-id="9eeb1-125">Un grupo de objetos es generalmente homogéneo y cualquier objeto agrupado que no esté en uso actualmente es adecuado para volver a cualquier cliente.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-125">A pool of objects is generally homogenous, and any pooled object not currently in use is good to return to any client.</span></span> <span data-ttu-id="9eeb1-126">La única excepción a esta regla es en el caso de los objetos transaccionales, para los que se optimiza la agrupación de objetos.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-126">The only exception to this rule is in the case of transactional objects, for which object pooling is optimized.</span></span> <span data-ttu-id="9eeb1-127">Cuando el cliente que solicita un objeto tiene una transacción asociada, COM+ examinará el grupo en busca de un objeto disponible que ya esté asociado a esa transacción.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-127">When the client requesting an object has an associated transaction, COM+ will scan the pool for an available object that is already associated with that transaction.</span></span> <span data-ttu-id="9eeb1-128">Si se encuentra un objeto con afinidad de transacciones, se devuelve al cliente; de lo contrario, se devuelve un objeto del grupo general.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-128">If an object with transaction affinity is found, it is returned to the client; otherwise, an object from the general pool is returned.</span></span>

<span data-ttu-id="9eeb1-129">De esta manera, se mantienen subgrupos especiales que contienen objetos con afinidad para una transacción determinada.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-129">In this manner, special subpools are maintained containing objects with affinity for a particular transaction.</span></span> <span data-ttu-id="9eeb1-130">Cuando la transacción se confirma o se anula, estos objetos se devuelven al grupo general sin afinidad de transacciones, ya que se puede usar en cualquier cliente.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-130">When the transaction commits or aborts, these objects are returned to the general pool with no transaction affinity, ready to be used by any client.</span></span>

<span data-ttu-id="9eeb1-131">Por esta razón, cuando el componente da de alta manualmente sus recursos administrados en una transacción, debe comprobar primero si ya están inscritos.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-131">For this reason, when your component manually enlists its managed resources in a transaction, it should first check to see whether they are already enlisted.</span></span> <span data-ttu-id="9eeb1-132">Si es así, no es necesario dar de alta.</span><span class="sxs-lookup"><span data-stu-id="9eeb1-132">If so, there is no need to enlist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9eeb1-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9eeb1-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9eeb1-134">Cadenas del constructor de objetos COM+</span><span class="sxs-lookup"><span data-stu-id="9eeb1-134">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="9eeb1-135">Controlar la duración y el estado de los objetos</span><span class="sxs-lookup"><span data-stu-id="9eeb1-135">Controlling Object Lifetime and State</span></span>](controlling-object-lifetime-and-state.md)
</dt> <dt>

[<span data-ttu-id="9eeb1-136">Cómo funciona la agrupación de objetos</span><span class="sxs-lookup"><span data-stu-id="9eeb1-136">How Object Pooling Works</span></span>](how-object-pooling-works.md)
</dt> <dt>

[<span data-ttu-id="9eeb1-137">Mejorar el rendimiento con la agrupación de objetos</span><span class="sxs-lookup"><span data-stu-id="9eeb1-137">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)
</dt> <dt>

[<span data-ttu-id="9eeb1-138">Requisitos para objetos agrupables</span><span class="sxs-lookup"><span data-stu-id="9eeb1-138">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



