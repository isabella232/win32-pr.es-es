---
description: Contiene un objeto para cada suscripción transitoria. Las suscripciones transitorias se pueden crear sobre la marcha para ejecutar instancias de objeto y desaparecen cuando se destruye el objeto.
ms.assetid: beee291c-e03f-4ee0-b1f2-99dcf113c46e
title: Colección TransientSubscriptions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriptions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6421cff326f4c33f0c77ae47d00e17c79c971443
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907308"
---
# <a name="transientsubscriptions-collection"></a><span data-ttu-id="cbb1f-104">Colección TransientSubscriptions</span><span class="sxs-lookup"><span data-stu-id="cbb1f-104">TransientSubscriptions collection</span></span>

<span data-ttu-id="cbb1f-105">Contiene un objeto para cada suscripción transitoria.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-105">Contains an object for each transient subscription.</span></span> <span data-ttu-id="cbb1f-106">Las suscripciones transitorias se pueden crear sobre la marcha para ejecutar instancias de objeto y desaparecen cuando se destruye el objeto.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-106">Transient subscriptions can be created on the fly for running object instances, and they vanish when the object is destroyed.</span></span>

<span data-ttu-id="cbb1f-107">Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="cbb1f-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="cbb1f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="cbb1f-108">Members</span></span>

<span data-ttu-id="cbb1f-109">La colección **TransientSubscriptions** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-109">The **TransientSubscriptions** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="cbb1f-110">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="cbb1f-110">Related Collections</span></span>

<span data-ttu-id="cbb1f-111">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="cbb1f-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="cbb1f-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="cbb1f-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="cbb1f-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="cbb1f-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="cbb1f-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="cbb1f-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="cbb1f-115">**TransientPublisherProperties**</span><span class="sxs-lookup"><span data-stu-id="cbb1f-115">**TransientPublisherProperties**</span></span>](transientpublisherproperties.md)
-   [<span data-ttu-id="cbb1f-116">**TransientSubscriberProperties**</span><span class="sxs-lookup"><span data-stu-id="cbb1f-116">**TransientSubscriberProperties**</span></span>](transientsubscriberproperties.md)

<span data-ttu-id="cbb1f-117">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="cbb1f-117">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="cbb1f-118">**Raíces**</span><span class="sxs-lookup"><span data-stu-id="cbb1f-118">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="cbb1f-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cbb1f-119">Properties</span></span>

<span data-ttu-id="cbb1f-120">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="cbb1f-120">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="cbb1f-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbb1f-121">Description</span></span>](#description)
-   [<span data-ttu-id="cbb1f-122">Enabled</span><span class="sxs-lookup"><span data-stu-id="cbb1f-122">Enabled</span></span>](#enabled)
-   [<span data-ttu-id="cbb1f-123">EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="cbb1f-123">EventClassPartitionID</span></span>](#eventclasspartitionid)
-   [<span data-ttu-id="cbb1f-124">EventCLSID</span><span class="sxs-lookup"><span data-stu-id="cbb1f-124">EventCLSID</span></span>](#eventclsid)
-   [<span data-ttu-id="cbb1f-125">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="cbb1f-125">FilterCriteria</span></span>](#filtercriteria)
-   [<span data-ttu-id="cbb1f-126">Id</span><span class="sxs-lookup"><span data-stu-id="cbb1f-126">ID</span></span>](#transientsubscriptions-collection)
-   [<span data-ttu-id="cbb1f-127">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="cbb1f-127">InterfaceID</span></span>](#interfaceid)
-   [<span data-ttu-id="cbb1f-128">MethodName</span><span class="sxs-lookup"><span data-stu-id="cbb1f-128">MethodName</span></span>](#methodname)
-   [<span data-ttu-id="cbb1f-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="cbb1f-129">Name</span></span>](#methodname)
-   [<span data-ttu-id="cbb1f-130">Perusuario</span><span class="sxs-lookup"><span data-stu-id="cbb1f-130">PerUser</span></span>](#peruser)
-   [<span data-ttu-id="cbb1f-131">PublisherID</span><span class="sxs-lookup"><span data-stu-id="cbb1f-131">PublisherID</span></span>](#publisherid)
-   [<span data-ttu-id="cbb1f-132">SubscriberInterface</span><span class="sxs-lookup"><span data-stu-id="cbb1f-132">SubscriberInterface</span></span>](#subscriberinterface)
-   [<span data-ttu-id="cbb1f-133">SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="cbb1f-133">SubscriberPartitionID</span></span>](#subscriberpartitionid)
-   [<span data-ttu-id="cbb1f-134">UserName</span><span class="sxs-lookup"><span data-stu-id="cbb1f-134">UserName</span></span>](#username)

### <a name="description"></a><span data-ttu-id="cbb1f-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbb1f-135">Description</span></span>



| <span data-ttu-id="cbb1f-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb1f-136">Entry</span></span> | <span data-ttu-id="cbb1f-137">Value</span><span class="sxs-lookup"><span data-stu-id="cbb1f-137">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="cbb1f-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbb1f-138">Description</span></span>    | <span data-ttu-id="cbb1f-139">Una descripción de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-139">A description for the subscription.</span></span> |
| <span data-ttu-id="cbb1f-140">Access</span><span class="sxs-lookup"><span data-stu-id="cbb1f-140">Access</span></span>         | <span data-ttu-id="cbb1f-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cbb1f-141">ReadWrite</span></span>                           |
| <span data-ttu-id="cbb1f-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-142">Type</span></span>           | <span data-ttu-id="cbb1f-143">String</span><span class="sxs-lookup"><span data-stu-id="cbb1f-143">String</span></span>                              |
| <span data-ttu-id="cbb1f-144">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="cbb1f-144">Default</span></span>        | <span data-ttu-id="cbb1f-145">""</span><span class="sxs-lookup"><span data-stu-id="cbb1f-145">""</span></span>                                  |
| <span data-ttu-id="cbb1f-146">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-146">Minimum system</span></span> | <span data-ttu-id="cbb1f-147">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cbb1f-147">Windows 2000</span></span>                        |



 

### <a name="enabled"></a><span data-ttu-id="cbb1f-148">habilitado</span><span class="sxs-lookup"><span data-stu-id="cbb1f-148">Enabled</span></span>



| <span data-ttu-id="cbb1f-149">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb1f-149">Entry</span></span> | <span data-ttu-id="cbb1f-150">Value</span><span class="sxs-lookup"><span data-stu-id="cbb1f-150">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="cbb1f-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbb1f-151">Description</span></span>    | <span data-ttu-id="cbb1f-152">Indica si la suscripción está habilitada actualmente.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-152">Indicates whether the subscription is presently enabled.</span></span> |
| <span data-ttu-id="cbb1f-153">Access</span><span class="sxs-lookup"><span data-stu-id="cbb1f-153">Access</span></span>         | <span data-ttu-id="cbb1f-154">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cbb1f-154">ReadWrite</span></span>                                                |
| <span data-ttu-id="cbb1f-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-155">Type</span></span>           | <span data-ttu-id="cbb1f-156">Bool</span><span class="sxs-lookup"><span data-stu-id="cbb1f-156">Bool</span></span>                                                     |
| <span data-ttu-id="cbb1f-157">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="cbb1f-157">Default</span></span>        | <span data-ttu-id="cbb1f-158">True</span><span class="sxs-lookup"><span data-stu-id="cbb1f-158">True</span></span>                                                     |
| <span data-ttu-id="cbb1f-159">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-159">Minimum system</span></span> | <span data-ttu-id="cbb1f-160">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cbb1f-160">Windows 2000</span></span>                                             |



 

### <a name="eventclasspartitionid"></a><span data-ttu-id="cbb1f-161">EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="cbb1f-161">EventClassPartitionID</span></span>



| <span data-ttu-id="cbb1f-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb1f-162">Entry</span></span> | <span data-ttu-id="cbb1f-163">Value</span><span class="sxs-lookup"><span data-stu-id="cbb1f-163">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb1f-164">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbb1f-164">Description</span></span>    | <span data-ttu-id="cbb1f-165">Al suscribirse a una clase de eventos, se usa para representar el GUID del identificador de la partición que contiene la clase de eventos.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-165">When subscribing to an event class, used to represent the GUID of the partition ID containing the event class.</span></span> <span data-ttu-id="cbb1f-166">Al suscribirse a las clases de eventos, el suscriptor tiene la opción de suscribirse a una clase de eventos en la misma partición o en otra diferente.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-166">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="cbb1f-167">Access</span><span class="sxs-lookup"><span data-stu-id="cbb1f-167">Access</span></span>         | <span data-ttu-id="cbb1f-168">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cbb1f-168">ReadWrite</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="cbb1f-169">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-169">Type</span></span>           | <span data-ttu-id="cbb1f-170">String</span><span class="sxs-lookup"><span data-stu-id="cbb1f-170">String</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="cbb1f-171">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="cbb1f-171">Default</span></span>        | <span data-ttu-id="cbb1f-172">NULL</span><span class="sxs-lookup"><span data-stu-id="cbb1f-172">NULL</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="cbb1f-173">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-173">Minimum system</span></span> | <span data-ttu-id="cbb1f-174">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cbb1f-174">Windows Server 2003</span></span>                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a><span data-ttu-id="cbb1f-175">EventCLSID</span><span class="sxs-lookup"><span data-stu-id="cbb1f-175">EventCLSID</span></span>



| <span data-ttu-id="cbb1f-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb1f-176">Entry</span></span> | <span data-ttu-id="cbb1f-177">Value</span><span class="sxs-lookup"><span data-stu-id="cbb1f-177">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb1f-178">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbb1f-178">Description</span></span>    | <span data-ttu-id="cbb1f-179">El CLSID de la clase de evento.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-179">The CLSID for the event class.</span></span> <span data-ttu-id="cbb1f-180">Puede indicar un EventCLSID o un PublisherID, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-180">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="cbb1f-181">Access</span><span class="sxs-lookup"><span data-stu-id="cbb1f-181">Access</span></span>         | <span data-ttu-id="cbb1f-182">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="cbb1f-182">WriteOnce</span></span>                                                                                    |
| <span data-ttu-id="cbb1f-183">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-183">Type</span></span>           | <span data-ttu-id="cbb1f-184">String</span><span class="sxs-lookup"><span data-stu-id="cbb1f-184">String</span></span>                                                                                       |
| <span data-ttu-id="cbb1f-185">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="cbb1f-185">Default</span></span>        | <span data-ttu-id="cbb1f-186">N/D</span><span class="sxs-lookup"><span data-stu-id="cbb1f-186">N/A</span></span>                                                                                          |
| <span data-ttu-id="cbb1f-187">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-187">Minimum system</span></span> | <span data-ttu-id="cbb1f-188">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cbb1f-188">Windows 2000</span></span>                                                                                 |



 

### <a name="filtercriteria"></a><span data-ttu-id="cbb1f-189">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="cbb1f-189">FilterCriteria</span></span>



| <span data-ttu-id="cbb1f-190">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb1f-190">Entry</span></span> | <span data-ttu-id="cbb1f-191">Value</span><span class="sxs-lookup"><span data-stu-id="cbb1f-191">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb1f-192">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbb1f-192">Description</span></span>    | <span data-ttu-id="cbb1f-193">Cadena que indica los criterios de filtro.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-193">A string that indicates the filter criteria.</span></span> <span data-ttu-id="cbb1f-194">Puede ser un CLSID para una clase [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) .</span><span class="sxs-lookup"><span data-stu-id="cbb1f-194">Can be a CLSID for a [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) class.</span></span> |
| <span data-ttu-id="cbb1f-195">Access</span><span class="sxs-lookup"><span data-stu-id="cbb1f-195">Access</span></span>         | <span data-ttu-id="cbb1f-196">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cbb1f-196">ReadWrite</span></span>                                                                                                            |
| <span data-ttu-id="cbb1f-197">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-197">Type</span></span>           | <span data-ttu-id="cbb1f-198">String</span><span class="sxs-lookup"><span data-stu-id="cbb1f-198">String</span></span>                                                                                                               |
| <span data-ttu-id="cbb1f-199">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="cbb1f-199">Default</span></span>        | <span data-ttu-id="cbb1f-200">N/D</span><span class="sxs-lookup"><span data-stu-id="cbb1f-200">N/A</span></span>                                                                                                                  |
| <span data-ttu-id="cbb1f-201">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-201">Minimum system</span></span> | <span data-ttu-id="cbb1f-202">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cbb1f-202">Windows 2000</span></span>                                                                                                         |



 

### <a name="id"></a><span data-ttu-id="cbb1f-203">id</span><span class="sxs-lookup"><span data-stu-id="cbb1f-203">ID</span></span>



| <span data-ttu-id="cbb1f-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb1f-204">Entry</span></span> | <span data-ttu-id="cbb1f-205">Value</span><span class="sxs-lookup"><span data-stu-id="cbb1f-205">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb1f-206">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbb1f-206">Description</span></span>    | <span data-ttu-id="cbb1f-207">Identificador de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-207">Identifier for the subscription.</span></span> <span data-ttu-id="cbb1f-208">Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-208">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="cbb1f-209">Access</span><span class="sxs-lookup"><span data-stu-id="cbb1f-209">Access</span></span>         | <span data-ttu-id="cbb1f-210">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="cbb1f-210">WriteOnce</span></span>                                                                                                                                                        |
| <span data-ttu-id="cbb1f-211">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-211">Type</span></span>           | <span data-ttu-id="cbb1f-212">String</span><span class="sxs-lookup"><span data-stu-id="cbb1f-212">String</span></span>                                                                                                                                                           |
| <span data-ttu-id="cbb1f-213">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="cbb1f-213">Default</span></span>        | <Generated>                                                                                                                                                |
| <span data-ttu-id="cbb1f-214">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-214">Minimum system</span></span> | <span data-ttu-id="cbb1f-215">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cbb1f-215">Windows 2000</span></span>                                                                                                                                                     |



 

### <a name="interfaceid"></a><span data-ttu-id="cbb1f-216">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="cbb1f-216">InterfaceID</span></span>



| <span data-ttu-id="cbb1f-217">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb1f-217">Entry</span></span> | <span data-ttu-id="cbb1f-218">Value</span><span class="sxs-lookup"><span data-stu-id="cbb1f-218">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="cbb1f-219">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbb1f-219">Description</span></span>    | <span data-ttu-id="cbb1f-220">IID de la interfaz suscrita a.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-220">IID for interface subscribed to.</span></span> |
| <span data-ttu-id="cbb1f-221">Access</span><span class="sxs-lookup"><span data-stu-id="cbb1f-221">Access</span></span>         | <span data-ttu-id="cbb1f-222">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="cbb1f-222">WriteOnce</span></span>                        |
| <span data-ttu-id="cbb1f-223">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-223">Type</span></span>           | <span data-ttu-id="cbb1f-224">String</span><span class="sxs-lookup"><span data-stu-id="cbb1f-224">String</span></span>                           |
| <span data-ttu-id="cbb1f-225">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="cbb1f-225">Default</span></span>        | <span data-ttu-id="cbb1f-226">N/D</span><span class="sxs-lookup"><span data-stu-id="cbb1f-226">N/A</span></span>                              |
| <span data-ttu-id="cbb1f-227">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-227">Minimum system</span></span> | <span data-ttu-id="cbb1f-228">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cbb1f-228">Windows 2000</span></span>                     |



 

### <a name="methodname"></a><span data-ttu-id="cbb1f-229">MethodName</span><span class="sxs-lookup"><span data-stu-id="cbb1f-229">MethodName</span></span>



| <span data-ttu-id="cbb1f-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb1f-230">Entry</span></span> | <span data-ttu-id="cbb1f-231">Value</span><span class="sxs-lookup"><span data-stu-id="cbb1f-231">Value</span></span> |
|----------------|----------------------------------------------|
| <span data-ttu-id="cbb1f-232">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbb1f-232">Description</span></span>    | <span data-ttu-id="cbb1f-233">Método de la interfaz a la que se suscribe.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-233">Method on the interface being subscribed to.</span></span> |
| <span data-ttu-id="cbb1f-234">Access</span><span class="sxs-lookup"><span data-stu-id="cbb1f-234">Access</span></span>         | <span data-ttu-id="cbb1f-235">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cbb1f-235">ReadWrite</span></span>                                    |
| <span data-ttu-id="cbb1f-236">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-236">Type</span></span>           | <span data-ttu-id="cbb1f-237">String</span><span class="sxs-lookup"><span data-stu-id="cbb1f-237">String</span></span>                                       |
| <span data-ttu-id="cbb1f-238">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="cbb1f-238">Default</span></span>        | <span data-ttu-id="cbb1f-239">N/D</span><span class="sxs-lookup"><span data-stu-id="cbb1f-239">N/A</span></span>                                          |
| <span data-ttu-id="cbb1f-240">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-240">Minimum system</span></span> | <span data-ttu-id="cbb1f-241">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cbb1f-241">Windows 2000</span></span>                                 |



 

### <a name="name"></a><span data-ttu-id="cbb1f-242">Nombre</span><span class="sxs-lookup"><span data-stu-id="cbb1f-242">Name</span></span>



| <span data-ttu-id="cbb1f-243">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb1f-243">Entry</span></span> | <span data-ttu-id="cbb1f-244">Value</span><span class="sxs-lookup"><span data-stu-id="cbb1f-244">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb1f-245">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbb1f-245">Description</span></span>    | <span data-ttu-id="cbb1f-246">Nombre de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-246">The name for the subscription.</span></span> <span data-ttu-id="cbb1f-247">Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de la propiedad [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-247">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="cbb1f-248">Access</span><span class="sxs-lookup"><span data-stu-id="cbb1f-248">Access</span></span>         | <span data-ttu-id="cbb1f-249">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cbb1f-249">ReadWrite</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="cbb1f-250">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-250">Type</span></span>           | <span data-ttu-id="cbb1f-251">String</span><span class="sxs-lookup"><span data-stu-id="cbb1f-251">String</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="cbb1f-252">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="cbb1f-252">Default</span></span>        | <span data-ttu-id="cbb1f-253">"Nueva suscripción"</span><span class="sxs-lookup"><span data-stu-id="cbb1f-253">"New Subscription"</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="cbb1f-254">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-254">Minimum system</span></span> | <span data-ttu-id="cbb1f-255">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cbb1f-255">Windows 2000</span></span>                                                                                                                                                                                                                           |



 

### <a name="peruser"></a><span data-ttu-id="cbb1f-256">Perusuario</span><span class="sxs-lookup"><span data-stu-id="cbb1f-256">PerUser</span></span>



| <span data-ttu-id="cbb1f-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb1f-257">Entry</span></span> | <span data-ttu-id="cbb1f-258">Value</span><span class="sxs-lookup"><span data-stu-id="cbb1f-258">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb1f-259">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbb1f-259">Description</span></span>    | <span data-ttu-id="cbb1f-260">Indica si la suscripción se aplica solo a un usuario determinado, representado por la propiedad UserName.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-260">Indicates whether the subscription applies only for a given user, represented by the UserName property.</span></span> |
| <span data-ttu-id="cbb1f-261">Access</span><span class="sxs-lookup"><span data-stu-id="cbb1f-261">Access</span></span>         | <span data-ttu-id="cbb1f-262">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cbb1f-262">ReadWrite</span></span>                                                                                               |
| <span data-ttu-id="cbb1f-263">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-263">Type</span></span>           | <span data-ttu-id="cbb1f-264">Bool</span><span class="sxs-lookup"><span data-stu-id="cbb1f-264">Bool</span></span>                                                                                                    |
| <span data-ttu-id="cbb1f-265">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="cbb1f-265">Default</span></span>        | <span data-ttu-id="cbb1f-266">False</span><span class="sxs-lookup"><span data-stu-id="cbb1f-266">False</span></span>                                                                                                   |
| <span data-ttu-id="cbb1f-267">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-267">Minimum system</span></span> | <span data-ttu-id="cbb1f-268">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cbb1f-268">Windows 2000</span></span>                                                                                            |



 

### <a name="publisherid"></a><span data-ttu-id="cbb1f-269">PublisherID</span><span class="sxs-lookup"><span data-stu-id="cbb1f-269">PublisherID</span></span>



| <span data-ttu-id="cbb1f-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb1f-270">Entry</span></span> | <span data-ttu-id="cbb1f-271">Value</span><span class="sxs-lookup"><span data-stu-id="cbb1f-271">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb1f-272">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbb1f-272">Description</span></span>    | <span data-ttu-id="cbb1f-273">ID. del publicador.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-273">ID for the publisher.</span></span> <span data-ttu-id="cbb1f-274">Puede indicar un EventCLSID o un PublisherID, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-274">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="cbb1f-275">Access</span><span class="sxs-lookup"><span data-stu-id="cbb1f-275">Access</span></span>         | <span data-ttu-id="cbb1f-276">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="cbb1f-276">WriteOnce</span></span>                                                                           |
| <span data-ttu-id="cbb1f-277">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-277">Type</span></span>           | <span data-ttu-id="cbb1f-278">String</span><span class="sxs-lookup"><span data-stu-id="cbb1f-278">String</span></span>                                                                              |
| <span data-ttu-id="cbb1f-279">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="cbb1f-279">Default</span></span>        | <span data-ttu-id="cbb1f-280">""</span><span class="sxs-lookup"><span data-stu-id="cbb1f-280">""</span></span>                                                                                  |
| <span data-ttu-id="cbb1f-281">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-281">Minimum system</span></span> | <span data-ttu-id="cbb1f-282">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cbb1f-282">Windows 2000</span></span>                                                                        |



 

### <a name="subscriberinterface"></a><span data-ttu-id="cbb1f-283">SubscriberInterface</span><span class="sxs-lookup"><span data-stu-id="cbb1f-283">SubscriberInterface</span></span>



| <span data-ttu-id="cbb1f-284">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb1f-284">Entry</span></span> | <span data-ttu-id="cbb1f-285">Value</span><span class="sxs-lookup"><span data-stu-id="cbb1f-285">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="cbb1f-286">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbb1f-286">Description</span></span>    | <span data-ttu-id="cbb1f-287">Puntero a la interfaz del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-287">A pointer to the subscriber's interface.</span></span> |
| <span data-ttu-id="cbb1f-288">Access</span><span class="sxs-lookup"><span data-stu-id="cbb1f-288">Access</span></span>         | <span data-ttu-id="cbb1f-289">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cbb1f-289">ReadWrite</span></span>                                |
| <span data-ttu-id="cbb1f-290">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-290">Type</span></span>           | <span data-ttu-id="cbb1f-291">Variante</span><span class="sxs-lookup"><span data-stu-id="cbb1f-291">Variant</span></span>                                  |
| <span data-ttu-id="cbb1f-292">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="cbb1f-292">Default</span></span>        | <span data-ttu-id="cbb1f-293">N/D</span><span class="sxs-lookup"><span data-stu-id="cbb1f-293">N/A</span></span>                                      |
| <span data-ttu-id="cbb1f-294">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-294">Minimum system</span></span> | <span data-ttu-id="cbb1f-295">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cbb1f-295">Windows 2000</span></span>                             |



 

### <a name="subscriberpartitionid"></a><span data-ttu-id="cbb1f-296">SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="cbb1f-296">SubscriberPartitionID</span></span>



| <span data-ttu-id="cbb1f-297">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb1f-297">Entry</span></span> | <span data-ttu-id="cbb1f-298">Value</span><span class="sxs-lookup"><span data-stu-id="cbb1f-298">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb1f-299">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbb1f-299">Description</span></span>    | <span data-ttu-id="cbb1f-300">Al suscribirse a una clase de eventos en la misma partición, se usa para representar el GUID del ID. de partición del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-300">When subscribing to an event class in the same partition, used to represent the GUID of the partition ID of the subscriber.</span></span> <span data-ttu-id="cbb1f-301">Al suscribirse a las clases de eventos, el suscriptor tiene la opción de suscribirse a una clase de eventos en la misma partición o en otra diferente.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-301">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="cbb1f-302">Access</span><span class="sxs-lookup"><span data-stu-id="cbb1f-302">Access</span></span>         | <span data-ttu-id="cbb1f-303">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="cbb1f-303">WriteOnce</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="cbb1f-304">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-304">Type</span></span>           | <span data-ttu-id="cbb1f-305">String</span><span class="sxs-lookup"><span data-stu-id="cbb1f-305">String</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="cbb1f-306">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="cbb1f-306">Default</span></span>        | <Generated>                                                                                                                                                                                                                                               |
| <span data-ttu-id="cbb1f-307">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-307">Minimum system</span></span> | <span data-ttu-id="cbb1f-308">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cbb1f-308">Windows Server 2003</span></span>                                                                                                                                                                                                                                             |



 

### <a name="username"></a><span data-ttu-id="cbb1f-309">UserName</span><span class="sxs-lookup"><span data-stu-id="cbb1f-309">UserName</span></span>



| <span data-ttu-id="cbb1f-310">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb1f-310">Entry</span></span> | <span data-ttu-id="cbb1f-311">Value</span><span class="sxs-lookup"><span data-stu-id="cbb1f-311">Value</span></span> |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="cbb1f-312">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbb1f-312">Description</span></span>    | <span data-ttu-id="cbb1f-313">Nombre del usuario al que se aplica la suscripción cuando peruser es true.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-313">The name of user that the subscription applies to when PerUser is True.</span></span> |
| <span data-ttu-id="cbb1f-314">Access</span><span class="sxs-lookup"><span data-stu-id="cbb1f-314">Access</span></span>         | <span data-ttu-id="cbb1f-315">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cbb1f-315">ReadWrite</span></span>                                                               |
| <span data-ttu-id="cbb1f-316">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-316">Type</span></span>           | <span data-ttu-id="cbb1f-317">String</span><span class="sxs-lookup"><span data-stu-id="cbb1f-317">String</span></span>                                                                  |
| <span data-ttu-id="cbb1f-318">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="cbb1f-318">Default</span></span>        | <span data-ttu-id="cbb1f-319">N/D</span><span class="sxs-lookup"><span data-stu-id="cbb1f-319">N/A</span></span>                                                                     |
| <span data-ttu-id="cbb1f-320">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="cbb1f-320">Minimum system</span></span> | <span data-ttu-id="cbb1f-321">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cbb1f-321">Windows 2000</span></span>                                                            |



 

## <a name="see-also"></a><span data-ttu-id="cbb1f-322">Vea también</span><span class="sxs-lookup"><span data-stu-id="cbb1f-322">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbb1f-323">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="cbb1f-323">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
