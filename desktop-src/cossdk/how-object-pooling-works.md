---
description: Al configurar un componente que se va a agrupar, COM+ mantendrá las instancias del mismo en un grupo, listo para activarse para cualquier cliente que solicite el componente. Cualquier solicitud de creación de objetos se controlará a través del administrador de grupos.
ms.assetid: 34978b50-cd20-42fd-ad46-410190478ef8
title: Cómo funciona la agrupación de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78784fc0e5362c14ceb598b404976c6ca494a19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714833"
---
# <a name="how-object-pooling-works"></a><span data-ttu-id="cf5cb-104">Cómo funciona la agrupación de objetos</span><span class="sxs-lookup"><span data-stu-id="cf5cb-104">How Object Pooling Works</span></span>

<span data-ttu-id="cf5cb-105">Al configurar un componente que se va a agrupar, COM+ mantendrá las instancias del mismo en un grupo, listo para activarse para cualquier cliente que solicite el componente.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-105">When you configure a component to be pooled, COM+ will maintain instances of it in a pool, ready to be activated for any client requesting the component.</span></span> <span data-ttu-id="cf5cb-106">Cualquier solicitud de creación de objetos se controlará a través del administrador de grupos.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-106">Any object creation requests will be handled through the pool manager.</span></span>

<span data-ttu-id="cf5cb-107">Los grupos se configuran y mantienen en cada componente.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-107">Pools are configured and maintained on a per-component basis.</span></span> <span data-ttu-id="cf5cb-108">Un grupo consta de objetos homogéneos que comparten el mismo CLSID.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-108">A pool consists of homogeneous objects that share the same CLSID.</span></span> <span data-ttu-id="cf5cb-109">La única excepción son los objetos transaccionales, para los que se mantienen los subgrupos que contienen objetos que tienen afinidad de transacción mientras hay una transacción pendiente.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-109">The only exception is for transactional objects, for which subpools are maintained containing objects that have transaction affinity while a transaction is pending.</span></span>

<span data-ttu-id="cf5cb-110">Cuando se inicia la aplicación, el grupo se rellenará hasta el nivel mínimo que haya especificado administrativamente, siempre y cuando la creación del objeto se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-110">When the application starts, the pool will be populated up to the minimum level that you have administratively specified, as long as object creation succeeds.</span></span> <span data-ttu-id="cf5cb-111">A medida que las solicitudes de cliente para el componente se encuentran en, se satisfacen en una base de la primera vez que se atiende desde el grupo.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-111">As client requests for the component come in, they are satisfied on a first-come first-served basis from the pool.</span></span> <span data-ttu-id="cf5cb-112">Si no hay ningún objeto agrupado disponible y el grupo aún no tiene el nivel máximo especificado, se creará y activará un nuevo objeto para el cliente.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-112">If no pooled objects are available and the pool is not yet at its specified maximum level, a new object is created and activated for the client.</span></span>

<span data-ttu-id="cf5cb-113">Cuando el grupo alcanza su nivel máximo, las solicitudes de cliente se ponen en cola y recibirán el primer objeto disponible del grupo.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-113">When the pool reaches its maximum level, client requests are queued and will receive the first available object from the pool.</span></span> <span data-ttu-id="cf5cb-114">El número de objetos, incluidos los activados y desactivados, nunca superará el valor máximo del grupo.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-114">The number of objects, including both activated and deactivated, will never exceed the maximum pool value.</span></span> <span data-ttu-id="cf5cb-115">Las solicitudes de creación de objetos agotarán el tiempo de espera después de un período especificado administrativamente para que pueda controlar cuánto tiempo esperarán los clientes para la creación de objetos.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-115">Object creation requests will time out after an administratively specified period so that you can control how long clients will wait for object creation.</span></span> <span data-ttu-id="cf5cb-116">Tras un error de tiempo de espera, el cliente obtendrá el error E \_ tiempo de espera de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="cf5cb-116">Upon a time-out failure, the client will get back the error E\_TIMEOUT from [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="cf5cb-117">Siempre que sea posible, COM+ intentará volver a usar un objeto después de que un cliente lo libere, hasta que el grupo alcance su nivel máximo.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-117">Whenever possible, COM+ will attempt to reuse an object after a client releases it, until the pool reaches its maximum level.</span></span> <span data-ttu-id="cf5cb-118">El objeto es responsable de supervisar su estado para determinar si se puede reutilizar y devolver un valor adecuado para [**IObjectControl:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span><span class="sxs-lookup"><span data-stu-id="cf5cb-118">The object is responsible for monitoring its state to determine whether it can be reused and should return an appropriate value for [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span></span>

<span data-ttu-id="cf5cb-119">Cuando se crea un objeto agrupado, se agrega a un objeto más grande que administrará la duración del objeto.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-119">When a pooled object is created, it is aggregated into a larger object that will manage the object's lifetime.</span></span> <span data-ttu-id="cf5cb-120">El objeto externo llama a los métodos en [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) en los momentos adecuados del ciclo de vida del objeto, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="cf5cb-120">The outer object calls methods on [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) at appropriate times in the object's life cycle, as follows:</span></span>

-   <span data-ttu-id="cf5cb-121">Se llama al método [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) cuando el objeto se devuelve a un cliente, que se activa en un contexto específico.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-121">The [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) method is called whenever the object is returned to a client, activated in a specific context.</span></span>
-   <span data-ttu-id="cf5cb-122">Se llama al método de [**desactivación**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) cada vez que el cliente libera un objeto o, en el caso de un objeto activado en JIT, cuando se desactiva.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-122">The [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) method is called whenever an object is released by the client or, in the case of a JIT-activated object, when it is deactivated.</span></span>
-   <span data-ttu-id="cf5cb-123">Se llama al método [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) cada vez que un objeto se va a devolver al grupo general.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-123">The [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) method is called whenever an object is to be returned to the general pool.</span></span> <span data-ttu-id="cf5cb-124">Si el objeto detecta que algún recurso reutilizable está en mal estado, debería devolver **false** para este método y el administrador del grupo descartará el objeto.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-124">If the object detects that some reusable resource is in a bad state, it should return **FALSE** for this method and the pool manager will discard the object.</span></span>

<span data-ttu-id="cf5cb-125">Un objeto no necesita necesariamente implementar [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span><span class="sxs-lookup"><span data-stu-id="cf5cb-125">An object does not necessarily need to implement [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span></span> <span data-ttu-id="cf5cb-126">Si no es así, las instancias siempre se volverán a usar hasta que se alcance el nivel máximo del grupo.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-126">If it does not, instances will always be reused, until the pool maximum level is reached.</span></span>

<span data-ttu-id="cf5cb-127">Para obtener más información sobre cómo configurar los componentes que se van a agrupar, vea [configurar un componente para agrupar](configuring-a-component-to-be-pooled.md).</span><span class="sxs-lookup"><span data-stu-id="cf5cb-127">For details about how to configure components to be pooled, see [Configuring a Component to Be Pooled](configuring-a-component-to-be-pooled.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf5cb-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cf5cb-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf5cb-129">Cadenas del constructor de objetos COM+</span><span class="sxs-lookup"><span data-stu-id="cf5cb-129">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="cf5cb-130">Controlar la duración y el estado de los objetos</span><span class="sxs-lookup"><span data-stu-id="cf5cb-130">Controlling Object Lifetime and State</span></span>](controlling-object-lifetime-and-state.md)
</dt> <dt>

[<span data-ttu-id="cf5cb-131">Mejorar el rendimiento con la agrupación de objetos</span><span class="sxs-lookup"><span data-stu-id="cf5cb-131">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)
</dt> <dt>

[<span data-ttu-id="cf5cb-132">Agrupar objetos transaccionales</span><span class="sxs-lookup"><span data-stu-id="cf5cb-132">Pooling Transactional Objects</span></span>](pooling-transactional-objects.md)
</dt> <dt>

[<span data-ttu-id="cf5cb-133">Requisitos para objetos agrupables</span><span class="sxs-lookup"><span data-stu-id="cf5cb-133">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)
</dt> </dl>

 

 
