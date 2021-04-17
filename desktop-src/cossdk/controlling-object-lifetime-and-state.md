---
description: Controlar la duración y el estado de los objetos
ms.assetid: 172e07a2-1711-4353-9099-ff9d31a564c6
title: Controlar la duración y el estado de los objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cc1d582d85bc84ef2b1749a427711d1fe26fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705333"
---
# <a name="controlling-object-lifetime-and-state"></a><span data-ttu-id="abd1f-103">Controlar la duración y el estado de los objetos</span><span class="sxs-lookup"><span data-stu-id="abd1f-103">Controlling Object Lifetime and State</span></span>

<span data-ttu-id="abd1f-104">Un objeto agrupado puede participar en el modo en que COM+ administra su actividad en el grupo implementando [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span><span class="sxs-lookup"><span data-stu-id="abd1f-104">A pooled object can participate in how COM+ manages its activity in the pool by implementing [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span></span> <span data-ttu-id="abd1f-105">Cuando se crea un objeto agrupado, se agrega a un objeto más grande que administrará el objeto llamando a los métodos siguientes en **IObjectControl** en los puntos normales del ciclo de vida del objeto:</span><span class="sxs-lookup"><span data-stu-id="abd1f-105">When a pooled object is created, it is aggregated into a larger object that will manage the object by calling the following methods on **IObjectControl** at regular points in the object's lifecycle:</span></span>

-   <span data-ttu-id="abd1f-106">[**Activar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate): se llama siempre que el objeto se devuelve a un cliente, que se activa en un contexto específico.</span><span class="sxs-lookup"><span data-stu-id="abd1f-106">[**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)—Called whenever the object is returned to a client, activated in a specific context.</span></span>
-   <span data-ttu-id="abd1f-107">[**Desactivar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate): se llama cada vez que el cliente libera un objeto o, en el caso de un objeto activado en JIT, cuando se desactiva.</span><span class="sxs-lookup"><span data-stu-id="abd1f-107">[**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)—Called whenever an object is released by the client or, in the case of a JIT-activated object, when it is deactivated.</span></span>
-   <span data-ttu-id="abd1f-108">[**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled): se llama siempre que se va a devolver un objeto al grupo general.</span><span class="sxs-lookup"><span data-stu-id="abd1f-108">[**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)—Called whenever an object is to be returned to the general pool.</span></span>

<span data-ttu-id="abd1f-109">La implementación de [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) es opcional, salvo en el caso de los objetos transaccionales, que siempre deben implementar [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) para supervisar el estado de los recursos que contienen.</span><span class="sxs-lookup"><span data-stu-id="abd1f-109">Implementing [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) is optional, except for transactional objects, which should always implement [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) to monitor the state of the resources they hold.</span></span> <span data-ttu-id="abd1f-110">Sin embargo, es aconsejable implementar **IObjectControl** en la mayoría de los casos, ya que proporciona una manera eficaz de administrar el comportamiento de un objeto agrupado, tal y como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="abd1f-110">However, it is advisable to implement **IObjectControl** in most cases because it provides an efficient way to manage the behavior of a pooled object, as described below.</span></span>

## <a name="performing-context-specific-initialization"></a><span data-ttu-id="abd1f-111">Realización de Context-Specific inicialización</span><span class="sxs-lookup"><span data-stu-id="abd1f-111">Performing Context-Specific Initialization</span></span>

<span data-ttu-id="abd1f-112">Mediante [**Activar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate), puede inicializar el objeto en el contexto en el que se activa para un cliente determinado.</span><span class="sxs-lookup"><span data-stu-id="abd1f-112">Using [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate), you can initialize the object in the context in which it is activated for a given client.</span></span> <span data-ttu-id="abd1f-113">Por ejemplo, para determinar si el objeto tiene afinidad de transacción (es posible que sus recursos ya estén en la lista), podría obtener el ID. de transacción asociado al contexto.</span><span class="sxs-lookup"><span data-stu-id="abd1f-113">For example, to determine whether the object has transaction affinity (its resources may already be enlisted), you might get the transaction ID associated with the context.</span></span>

<span data-ttu-id="abd1f-114">Normalmente se usaría [**Activar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)para realizar la inicialización que sea coherente en todos los métodos expuestos por el objeto, tratando como la parte específica del contexto del constructor del objeto.</span><span class="sxs-lookup"><span data-stu-id="abd1f-114">Typically you would use [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)to perform initialization that is consistent across any methods exposed by the object, treating it as the context-specific portion of the object's constructor.</span></span>

## <a name="cleaning-up-any-client-state"></a><span data-ttu-id="abd1f-115">Limpiar cualquier estado de cliente</span><span class="sxs-lookup"><span data-stu-id="abd1f-115">Cleaning Up Any Client State</span></span>

<span data-ttu-id="abd1f-116">Con [**desactivación**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), puede deshacerse de cualquier estado específico del cliente que pueda existir para que el objeto vuelva al grupo en un estado totalmente genérico y pueda ser utilizado por cualquier cliente sin poner en peligro la seguridad o el aislamiento.</span><span class="sxs-lookup"><span data-stu-id="abd1f-116">Using [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), you can get rid of any client-specific state that might exist so that your object returns to the pool in a completely generic state and can then be used by any client without compromising security or isolation.</span></span>

## <a name="controlling-reuse-of-the-object"></a><span data-ttu-id="abd1f-117">Controlar la reutilización del objeto</span><span class="sxs-lookup"><span data-stu-id="abd1f-117">Controlling Reuse of the Object</span></span>

<span data-ttu-id="abd1f-118">Con [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), puede supervisar el estado interno del objeto e informar sobre si es adecuado para su reutilización.</span><span class="sxs-lookup"><span data-stu-id="abd1f-118">Using [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), you can monitor the internal state of your object and report on whether it is fit for its reuse.</span></span> <span data-ttu-id="abd1f-119">Si **CanBePooled** devuelve true y no se ha alcanzado el máximo del grupo, el objeto se vuelve a colocar en el grupo general.</span><span class="sxs-lookup"><span data-stu-id="abd1f-119">If **CanBePooled** returns True and the pool maximum has not been reached, the object is placed back in the general pool.</span></span> <span data-ttu-id="abd1f-120">Si **CanBePooled** devuelve false, el objeto se descarta.</span><span class="sxs-lookup"><span data-stu-id="abd1f-120">If **CanBePooled** returns False, the object is discarded.</span></span> <span data-ttu-id="abd1f-121">En el caso de los componentes transaccionales, si se devuelve false, se desactivará la transacción actual.</span><span class="sxs-lookup"><span data-stu-id="abd1f-121">In the case of transactional components, returning False will doom the current transaction.</span></span>

<span data-ttu-id="abd1f-122">Normalmente, conserve algunos miembros de datos globales para el objeto y, si detecta que una conexión es incorrecta o que un recurso de algún tipo está en mal estado, establézcalo para reflejar la situación actual y devolverla a través de [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span><span class="sxs-lookup"><span data-stu-id="abd1f-122">Typically, you would keep some global data member for the object, and if you detect a connection to be bad or a resource of some kind to be in a bad state, set this to reflect the current situation and return it through [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span></span>

<span data-ttu-id="abd1f-123">Si un objeto no implementa [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), las instancias se seguirán reutilizando hasta que se alcance el nivel máximo del grupo.</span><span class="sxs-lookup"><span data-stu-id="abd1f-123">If an object does not implement [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), instances will continue to be reused until the pool maximum level is reached.</span></span>

## <a name="related-topics"></a><span data-ttu-id="abd1f-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="abd1f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abd1f-125">Cadenas del constructor de objetos COM+</span><span class="sxs-lookup"><span data-stu-id="abd1f-125">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="abd1f-126">Cómo funciona la agrupación de objetos</span><span class="sxs-lookup"><span data-stu-id="abd1f-126">How Object Pooling Works</span></span>](how-object-pooling-works.md)
</dt> <dt>

[<span data-ttu-id="abd1f-127">Mejorar el rendimiento con la agrupación de objetos</span><span class="sxs-lookup"><span data-stu-id="abd1f-127">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)
</dt> <dt>

[<span data-ttu-id="abd1f-128">Agrupar objetos transaccionales</span><span class="sxs-lookup"><span data-stu-id="abd1f-128">Pooling Transactional Objects</span></span>](pooling-transactional-objects.md)
</dt> <dt>

[<span data-ttu-id="abd1f-129">Requisitos para objetos agrupables</span><span class="sxs-lookup"><span data-stu-id="abd1f-129">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



