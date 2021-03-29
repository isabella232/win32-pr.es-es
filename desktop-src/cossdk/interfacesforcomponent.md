---
description: Contiene un objeto para cada interfaz expuesta por el componente al que está relacionada la colección.
ms.assetid: ee755693-e3ff-4bb1-9fde-a2bfee9c3d29
title: Colección InterfacesForComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InterfacesForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9450c898e694e5459dbb126d7f7bf11b853e33d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153200"
---
# <a name="interfacesforcomponent-collection"></a><span data-ttu-id="aa033-103">Colección InterfacesForComponent</span><span class="sxs-lookup"><span data-stu-id="aa033-103">InterfacesForComponent collection</span></span>

<span data-ttu-id="aa033-104">Contiene un objeto para cada interfaz expuesta por el componente al que está relacionada la colección.</span><span class="sxs-lookup"><span data-stu-id="aa033-104">Contains an object for each interface exposed by the component to which the collection is related.</span></span>

<span data-ttu-id="aa033-105">Esta colección no admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="aa033-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="aa033-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="aa033-106">Members</span></span>

<span data-ttu-id="aa033-107">La colección **InterfacesForComponent** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="aa033-107">The **InterfacesForComponent** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="aa033-108">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="aa033-108">Related Collections</span></span>

<span data-ttu-id="aa033-109">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="aa033-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="aa033-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="aa033-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="aa033-111">**MethodsForInterface**</span><span class="sxs-lookup"><span data-stu-id="aa033-111">**MethodsForInterface**</span></span>](methodsforinterface.md)
-   [<span data-ttu-id="aa033-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="aa033-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="aa033-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="aa033-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="aa033-114">**RolesForInterface**</span><span class="sxs-lookup"><span data-stu-id="aa033-114">**RolesForInterface**</span></span>](rolesforinterface.md)

<span data-ttu-id="aa033-115">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="aa033-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="aa033-116">**Componentes**</span><span class="sxs-lookup"><span data-stu-id="aa033-116">**Components**</span></span>](components.md)

## <a name="properties"></a><span data-ttu-id="aa033-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aa033-117">Properties</span></span>

<span data-ttu-id="aa033-118">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="aa033-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="aa033-119">CLSID</span><span class="sxs-lookup"><span data-stu-id="aa033-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="aa033-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa033-120">Description</span></span>](#description)
-   [<span data-ttu-id="aa033-121">IID</span><span class="sxs-lookup"><span data-stu-id="aa033-121">IID</span></span>](#iid)
-   [<span data-ttu-id="aa033-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="aa033-122">Name</span></span>](#name)
-   [<span data-ttu-id="aa033-123">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="aa033-123">QueuingEnabled</span></span>](#queuingenabled)
-   [<span data-ttu-id="aa033-124">QueueingSupported</span><span class="sxs-lookup"><span data-stu-id="aa033-124">QueueingSupported</span></span>](#queueingsupported)

### <a name="clsid"></a><span data-ttu-id="aa033-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="aa033-125">CLSID</span></span>



| <span data-ttu-id="aa033-126">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa033-126">Entry</span></span> | <span data-ttu-id="aa033-127">Value</span><span class="sxs-lookup"><span data-stu-id="aa033-127">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="aa033-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa033-128">Description</span></span>    | <span data-ttu-id="aa033-129">GUID del componente.</span><span class="sxs-lookup"><span data-stu-id="aa033-129">A GUID for the component.</span></span> |
| <span data-ttu-id="aa033-130">Access</span><span class="sxs-lookup"><span data-stu-id="aa033-130">Access</span></span>         | <span data-ttu-id="aa033-131">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="aa033-131">ReadOnly</span></span>                  |
| <span data-ttu-id="aa033-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa033-132">Type</span></span>           | <span data-ttu-id="aa033-133">String</span><span class="sxs-lookup"><span data-stu-id="aa033-133">String</span></span>                    |
| <span data-ttu-id="aa033-134">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="aa033-134">Default</span></span>        | <span data-ttu-id="aa033-135">N/D</span><span class="sxs-lookup"><span data-stu-id="aa033-135">N/A</span></span>                       |
| <span data-ttu-id="aa033-136">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aa033-136">Minimum system</span></span> | <span data-ttu-id="aa033-137">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aa033-137">Windows 2000</span></span>              |



 

### <a name="description"></a><span data-ttu-id="aa033-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa033-138">Description</span></span>



| <span data-ttu-id="aa033-139">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa033-139">Entry</span></span> | <span data-ttu-id="aa033-140">Value</span><span class="sxs-lookup"><span data-stu-id="aa033-140">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="aa033-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa033-141">Description</span></span>    | <span data-ttu-id="aa033-142">Descripción de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="aa033-142">A description for the interface.</span></span> |
| <span data-ttu-id="aa033-143">Access</span><span class="sxs-lookup"><span data-stu-id="aa033-143">Access</span></span>         | <span data-ttu-id="aa033-144">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aa033-144">ReadWrite</span></span>                        |
| <span data-ttu-id="aa033-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa033-145">Type</span></span>           | <span data-ttu-id="aa033-146">String</span><span class="sxs-lookup"><span data-stu-id="aa033-146">String</span></span>                           |
| <span data-ttu-id="aa033-147">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="aa033-147">Default</span></span>        | <span data-ttu-id="aa033-148">""</span><span class="sxs-lookup"><span data-stu-id="aa033-148">""</span></span>                               |
| <span data-ttu-id="aa033-149">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aa033-149">Minimum system</span></span> | <span data-ttu-id="aa033-150">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aa033-150">Windows 2000</span></span>                     |



 

### <a name="iid"></a><span data-ttu-id="aa033-151">IID</span><span class="sxs-lookup"><span data-stu-id="aa033-151">IID</span></span>



| <span data-ttu-id="aa033-152">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa033-152">Entry</span></span> | <span data-ttu-id="aa033-153">Value</span><span class="sxs-lookup"><span data-stu-id="aa033-153">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa033-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa033-154">Description</span></span>    | <span data-ttu-id="aa033-155">Un GUID para la interfaz.</span><span class="sxs-lookup"><span data-stu-id="aa033-155">A GUID for the interface.</span></span> <span data-ttu-id="aa033-156">Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="aa033-156">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="aa033-157">Access</span><span class="sxs-lookup"><span data-stu-id="aa033-157">Access</span></span>         | <span data-ttu-id="aa033-158">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="aa033-158">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="aa033-159">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa033-159">Type</span></span>           | <span data-ttu-id="aa033-160">String</span><span class="sxs-lookup"><span data-stu-id="aa033-160">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="aa033-161">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="aa033-161">Default</span></span>        | <span data-ttu-id="aa033-162">N/D</span><span class="sxs-lookup"><span data-stu-id="aa033-162">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="aa033-163">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aa033-163">Minimum system</span></span> | <span data-ttu-id="aa033-164">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aa033-164">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="name"></a><span data-ttu-id="aa033-165">Nombre</span><span class="sxs-lookup"><span data-stu-id="aa033-165">Name</span></span>



| <span data-ttu-id="aa033-166">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa033-166">Entry</span></span> | <span data-ttu-id="aa033-167">Value</span><span class="sxs-lookup"><span data-stu-id="aa033-167">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa033-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa033-168">Description</span></span>    | <span data-ttu-id="aa033-169">Nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="aa033-169">A name for the interface.</span></span> <span data-ttu-id="aa033-170">Esta propiedad se devuelve cuando se llama al método de la propiedad [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="aa033-170">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="aa033-171">Access</span><span class="sxs-lookup"><span data-stu-id="aa033-171">Access</span></span>         | <span data-ttu-id="aa033-172">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="aa033-172">ReadOnly</span></span>                                                                                                                                                    |
| <span data-ttu-id="aa033-173">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa033-173">Type</span></span>           | <span data-ttu-id="aa033-174">String</span><span class="sxs-lookup"><span data-stu-id="aa033-174">String</span></span>                                                                                                                                                      |
| <span data-ttu-id="aa033-175">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="aa033-175">Default</span></span>        | <span data-ttu-id="aa033-176">N/D</span><span class="sxs-lookup"><span data-stu-id="aa033-176">N/A</span></span>                                                                                                                                                         |
| <span data-ttu-id="aa033-177">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aa033-177">Minimum system</span></span> | <span data-ttu-id="aa033-178">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aa033-178">Windows 2000</span></span>                                                                                                                                                |



 

### <a name="queuingenabled"></a><span data-ttu-id="aa033-179">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="aa033-179">QueuingEnabled</span></span>



| <span data-ttu-id="aa033-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa033-180">Entry</span></span> | <span data-ttu-id="aa033-181">Value</span><span class="sxs-lookup"><span data-stu-id="aa033-181">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa033-182">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa033-182">Description</span></span>    | <span data-ttu-id="aa033-183">Marca la interfaz como queuable y se puede establecer mediante el SDK de administración o la herramienta administrativa Servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="aa033-183">Marks the interface as queuable and can be set by using the Admin SDK or Component Services administrative tool.</span></span> <span data-ttu-id="aa033-184">Sin embargo, solo se puede establecer la marca de **puesta en cola habilitada** para una interfaz que tenga establecida la marca **compatible con puesta en cola** .</span><span class="sxs-lookup"><span data-stu-id="aa033-184">However, only an interface that has the **Queuing Supported** flag set can have the **Queuing Enabled** flag set.</span></span> |
| <span data-ttu-id="aa033-185">Access</span><span class="sxs-lookup"><span data-stu-id="aa033-185">Access</span></span>         | <span data-ttu-id="aa033-186">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aa033-186">ReadWrite</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="aa033-187">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa033-187">Type</span></span>           | <span data-ttu-id="aa033-188">Bool</span><span class="sxs-lookup"><span data-stu-id="aa033-188">Bool</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="aa033-189">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aa033-189">Default</span></span>        | <span data-ttu-id="aa033-190">False</span><span class="sxs-lookup"><span data-stu-id="aa033-190">False</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="aa033-191">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aa033-191">Minimum system</span></span> | <span data-ttu-id="aa033-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aa033-192">Windows 2000</span></span>                                                                                                                                                                                                                       |



 

### <a name="queueingsupported"></a><span data-ttu-id="aa033-193">QueueingSupported</span><span class="sxs-lookup"><span data-stu-id="aa033-193">QueueingSupported</span></span>



| <span data-ttu-id="aa033-194">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa033-194">Entry</span></span> | <span data-ttu-id="aa033-195">Value</span><span class="sxs-lookup"><span data-stu-id="aa033-195">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa033-196">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa033-196">Description</span></span>    | <span data-ttu-id="aa033-197">La interfaz admite la puesta en cola.</span><span class="sxs-lookup"><span data-stu-id="aa033-197">Interface supports queuing.</span></span> <span data-ttu-id="aa033-198">Para que una interfaz admita la puesta en cola, todos los métodos solo deben tener parámetros in.</span><span class="sxs-lookup"><span data-stu-id="aa033-198">For an interface to support queuing, all methods should have only in parameters.</span></span> <span data-ttu-id="aa033-199">**Queue Supported** se expone como una propiedad de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="aa033-199">**Queuing Supported** is exposed as a read-only property.</span></span> |
| <span data-ttu-id="aa033-200">Access</span><span class="sxs-lookup"><span data-stu-id="aa033-200">Access</span></span>         | <span data-ttu-id="aa033-201">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="aa033-201">ReadOnly</span></span>                                                                                                                                                               |
| <span data-ttu-id="aa033-202">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa033-202">Type</span></span>           | <span data-ttu-id="aa033-203">Bool</span><span class="sxs-lookup"><span data-stu-id="aa033-203">Bool</span></span>                                                                                                                                                                   |
| <span data-ttu-id="aa033-204">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aa033-204">Default</span></span>        | <span data-ttu-id="aa033-205">False</span><span class="sxs-lookup"><span data-stu-id="aa033-205">False</span></span>                                                                                                                                                                  |
| <span data-ttu-id="aa033-206">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aa033-206">Minimum system</span></span> | <span data-ttu-id="aa033-207">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aa033-207">Windows 2000</span></span>                                                                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="aa033-208">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa033-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa033-209">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="aa033-209">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
