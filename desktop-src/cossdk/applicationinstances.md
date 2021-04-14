---
description: Recupera información relacionada con las aplicaciones en ejecución.
ms.assetid: 148e42aa-e99e-4fa2-8b74-a7ebf82b99d0
title: Colección ApplicationInstances
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationInstances
api_type:
- COM
api_location: ''
ms.openlocfilehash: 56680a81cc564466dc3586bf0381cf4db97f914b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496126"
---
# <a name="applicationinstances-collection"></a><span data-ttu-id="48a5f-103">Colección ApplicationInstances</span><span class="sxs-lookup"><span data-stu-id="48a5f-103">ApplicationInstances collection</span></span>

<span data-ttu-id="48a5f-104">Recupera información relacionada con las aplicaciones en ejecución.</span><span class="sxs-lookup"><span data-stu-id="48a5f-104">Retrieves information regarding running applications.</span></span>

<span data-ttu-id="48a5f-105">Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="48a5f-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="48a5f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="48a5f-106">Members</span></span>

<span data-ttu-id="48a5f-107">La colección **ApplicationInstances** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="48a5f-107">The **ApplicationInstances** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="48a5f-108">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="48a5f-108">Related Collections</span></span>

<span data-ttu-id="48a5f-109">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="48a5f-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="48a5f-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="48a5f-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="48a5f-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="48a5f-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="48a5f-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="48a5f-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="48a5f-113">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="48a5f-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="48a5f-114">**APLICACIONES**</span><span class="sxs-lookup"><span data-stu-id="48a5f-114">**Applications**</span></span>](applications.md)
-   [<span data-ttu-id="48a5f-115">**Raíces**</span><span class="sxs-lookup"><span data-stu-id="48a5f-115">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="48a5f-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="48a5f-116">Properties</span></span>

<span data-ttu-id="48a5f-117">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="48a5f-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="48a5f-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="48a5f-118">Application</span></span>](#applicationinstances-collection)
-   [<span data-ttu-id="48a5f-119">HasRecycled</span><span class="sxs-lookup"><span data-stu-id="48a5f-119">HasRecycled</span></span>](#hasrecycled)
-   [<span data-ttu-id="48a5f-120">InstanceID</span><span class="sxs-lookup"><span data-stu-id="48a5f-120">InstanceID</span></span>](#instanceid)
-   [<span data-ttu-id="48a5f-121">IsPaused</span><span class="sxs-lookup"><span data-stu-id="48a5f-121">IsPaused</span></span>](#ispaused)
-   [<span data-ttu-id="48a5f-122">PartitionID</span><span class="sxs-lookup"><span data-stu-id="48a5f-122">PartitionID</span></span>](#partitionid)
-   [<span data-ttu-id="48a5f-123">ProcessID</span><span class="sxs-lookup"><span data-stu-id="48a5f-123">ProcessID</span></span>](#processid)

### <a name="application"></a><span data-ttu-id="48a5f-124">Application</span><span class="sxs-lookup"><span data-stu-id="48a5f-124">Application</span></span>



| <span data-ttu-id="48a5f-125">Entrada</span><span class="sxs-lookup"><span data-stu-id="48a5f-125">Entry</span></span> | <span data-ttu-id="48a5f-126">Value</span><span class="sxs-lookup"><span data-stu-id="48a5f-126">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="48a5f-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="48a5f-127">Description</span></span>    | <span data-ttu-id="48a5f-128">IDENTIFICADOR de la aplicación en ejecución.</span><span class="sxs-lookup"><span data-stu-id="48a5f-128">The ID for the running application.</span></span> |
| <span data-ttu-id="48a5f-129">Access</span><span class="sxs-lookup"><span data-stu-id="48a5f-129">Access</span></span>         | <span data-ttu-id="48a5f-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="48a5f-130">ReadOnly</span></span>                            |
| <span data-ttu-id="48a5f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="48a5f-131">Type</span></span>           | <span data-ttu-id="48a5f-132">String</span><span class="sxs-lookup"><span data-stu-id="48a5f-132">String</span></span>                              |
| <span data-ttu-id="48a5f-133">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="48a5f-133">Default</span></span>        | <span data-ttu-id="48a5f-134">N/D</span><span class="sxs-lookup"><span data-stu-id="48a5f-134">N/A</span></span>                                 |
| <span data-ttu-id="48a5f-135">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="48a5f-135">Minimum system</span></span> | <span data-ttu-id="48a5f-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="48a5f-136">Windows XP</span></span>                          |



 

### <a name="hasrecycled"></a><span data-ttu-id="48a5f-137">HasRecycled</span><span class="sxs-lookup"><span data-stu-id="48a5f-137">HasRecycled</span></span>



| <span data-ttu-id="48a5f-138">Entrada</span><span class="sxs-lookup"><span data-stu-id="48a5f-138">Entry</span></span> | <span data-ttu-id="48a5f-139">Value</span><span class="sxs-lookup"><span data-stu-id="48a5f-139">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="48a5f-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="48a5f-140">Description</span></span>    | <span data-ttu-id="48a5f-141">Indica si se ha reciclado la instancia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="48a5f-141">Indicates whether the application instance has been recycled.</span></span> |
| <span data-ttu-id="48a5f-142">Access</span><span class="sxs-lookup"><span data-stu-id="48a5f-142">Access</span></span>         | <span data-ttu-id="48a5f-143">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="48a5f-143">ReadOnly</span></span>                                                      |
| <span data-ttu-id="48a5f-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="48a5f-144">Type</span></span>           | <span data-ttu-id="48a5f-145">Bool</span><span class="sxs-lookup"><span data-stu-id="48a5f-145">Bool</span></span>                                                          |
| <span data-ttu-id="48a5f-146">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="48a5f-146">Default</span></span>        | <span data-ttu-id="48a5f-147">False</span><span class="sxs-lookup"><span data-stu-id="48a5f-147">False</span></span>                                                         |
| <span data-ttu-id="48a5f-148">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="48a5f-148">Minimum system</span></span> | <span data-ttu-id="48a5f-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="48a5f-149">Windows XP</span></span>                                                    |



 

### <a name="instanceid"></a><span data-ttu-id="48a5f-150">InstanceID</span><span class="sxs-lookup"><span data-stu-id="48a5f-150">InstanceID</span></span>



| <span data-ttu-id="48a5f-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="48a5f-151">Entry</span></span> | <span data-ttu-id="48a5f-152">Value</span><span class="sxs-lookup"><span data-stu-id="48a5f-152">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48a5f-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="48a5f-153">Description</span></span>    | <span data-ttu-id="48a5f-154">Identificador único global de la instancia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="48a5f-154">The globally unique identifier for the application instance.</span></span> <span data-ttu-id="48a5f-155">Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="48a5f-155">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="48a5f-156">Access</span><span class="sxs-lookup"><span data-stu-id="48a5f-156">Access</span></span>         | <span data-ttu-id="48a5f-157">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="48a5f-157">ReadOnly</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="48a5f-158">Tipo</span><span class="sxs-lookup"><span data-stu-id="48a5f-158">Type</span></span>           | <span data-ttu-id="48a5f-159">String</span><span class="sxs-lookup"><span data-stu-id="48a5f-159">String</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="48a5f-160">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="48a5f-160">Default</span></span>        | <span data-ttu-id="48a5f-161">N/D</span><span class="sxs-lookup"><span data-stu-id="48a5f-161">N/A</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="48a5f-162">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="48a5f-162">Minimum system</span></span> | <span data-ttu-id="48a5f-163">Windows XP</span><span class="sxs-lookup"><span data-stu-id="48a5f-163">Windows XP</span></span>                                                                                                                                                                                                                          |



 

### <a name="ispaused"></a><span data-ttu-id="48a5f-164">IsPaused</span><span class="sxs-lookup"><span data-stu-id="48a5f-164">IsPaused</span></span>



| <span data-ttu-id="48a5f-165">Entrada</span><span class="sxs-lookup"><span data-stu-id="48a5f-165">Entry</span></span> | <span data-ttu-id="48a5f-166">Value</span><span class="sxs-lookup"><span data-stu-id="48a5f-166">Value</span></span> |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="48a5f-167">Descripción</span><span class="sxs-lookup"><span data-stu-id="48a5f-167">Description</span></span>    | <span data-ttu-id="48a5f-168">Indica si la instancia de la aplicación está en pausa actualmente.</span><span class="sxs-lookup"><span data-stu-id="48a5f-168">Indicates whether the application instance is currently paused.</span></span> |
| <span data-ttu-id="48a5f-169">Access</span><span class="sxs-lookup"><span data-stu-id="48a5f-169">Access</span></span>         | <span data-ttu-id="48a5f-170">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="48a5f-170">ReadOnly</span></span>                                                        |
| <span data-ttu-id="48a5f-171">Tipo</span><span class="sxs-lookup"><span data-stu-id="48a5f-171">Type</span></span>           | <span data-ttu-id="48a5f-172">Bool</span><span class="sxs-lookup"><span data-stu-id="48a5f-172">Bool</span></span>                                                            |
| <span data-ttu-id="48a5f-173">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="48a5f-173">Default</span></span>        | <span data-ttu-id="48a5f-174">False</span><span class="sxs-lookup"><span data-stu-id="48a5f-174">False</span></span>                                                           |
| <span data-ttu-id="48a5f-175">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="48a5f-175">Minimum system</span></span> | <span data-ttu-id="48a5f-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="48a5f-176">Windows XP</span></span>                                                      |



 

### <a name="partitionid"></a><span data-ttu-id="48a5f-177">PartitionID</span><span class="sxs-lookup"><span data-stu-id="48a5f-177">PartitionID</span></span>



| <span data-ttu-id="48a5f-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="48a5f-178">Entry</span></span> | <span data-ttu-id="48a5f-179">Value</span><span class="sxs-lookup"><span data-stu-id="48a5f-179">Value</span></span> |
|----------------|-------------------------------------------------|
| <span data-ttu-id="48a5f-180">Descripción</span><span class="sxs-lookup"><span data-stu-id="48a5f-180">Description</span></span>    | <span data-ttu-id="48a5f-181">El identificador de partición que utiliza la aplicación.</span><span class="sxs-lookup"><span data-stu-id="48a5f-181">The partition ID that the application is using.</span></span> |
| <span data-ttu-id="48a5f-182">Access</span><span class="sxs-lookup"><span data-stu-id="48a5f-182">Access</span></span>         | <span data-ttu-id="48a5f-183">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="48a5f-183">ReadOnly</span></span>                                        |
| <span data-ttu-id="48a5f-184">Tipo</span><span class="sxs-lookup"><span data-stu-id="48a5f-184">Type</span></span>           | <span data-ttu-id="48a5f-185">String</span><span class="sxs-lookup"><span data-stu-id="48a5f-185">String</span></span>                                          |
| <span data-ttu-id="48a5f-186">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="48a5f-186">Default</span></span>        | <span data-ttu-id="48a5f-187">N/D</span><span class="sxs-lookup"><span data-stu-id="48a5f-187">N/A</span></span>                                             |
| <span data-ttu-id="48a5f-188">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="48a5f-188">Minimum system</span></span> | <span data-ttu-id="48a5f-189">Windows XP</span><span class="sxs-lookup"><span data-stu-id="48a5f-189">Windows XP</span></span>                                      |



 

### <a name="processid"></a><span data-ttu-id="48a5f-190">ProcessID</span><span class="sxs-lookup"><span data-stu-id="48a5f-190">ProcessID</span></span>



| <span data-ttu-id="48a5f-191">Entrada</span><span class="sxs-lookup"><span data-stu-id="48a5f-191">Entry</span></span> | <span data-ttu-id="48a5f-192">Value</span><span class="sxs-lookup"><span data-stu-id="48a5f-192">Value</span></span> |
|----------------|---------------------------------------------|
| <span data-ttu-id="48a5f-193">Descripción</span><span class="sxs-lookup"><span data-stu-id="48a5f-193">Description</span></span>    | <span data-ttu-id="48a5f-194">Identificador de proceso de la instancia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="48a5f-194">The process ID of the application instance.</span></span> |
| <span data-ttu-id="48a5f-195">Access</span><span class="sxs-lookup"><span data-stu-id="48a5f-195">Access</span></span>         | <span data-ttu-id="48a5f-196">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="48a5f-196">ReadOnly</span></span>                                    |
| <span data-ttu-id="48a5f-197">Tipo</span><span class="sxs-lookup"><span data-stu-id="48a5f-197">Type</span></span>           | <span data-ttu-id="48a5f-198">String</span><span class="sxs-lookup"><span data-stu-id="48a5f-198">String</span></span>                                      |
| <span data-ttu-id="48a5f-199">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="48a5f-199">Default</span></span>        | <span data-ttu-id="48a5f-200">N/D</span><span class="sxs-lookup"><span data-stu-id="48a5f-200">N/A</span></span>                                         |
| <span data-ttu-id="48a5f-201">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="48a5f-201">Minimum system</span></span> | <span data-ttu-id="48a5f-202">Windows XP</span><span class="sxs-lookup"><span data-stu-id="48a5f-202">Windows XP</span></span>                                  |



 

## <a name="see-also"></a><span data-ttu-id="48a5f-203">Vea también</span><span class="sxs-lookup"><span data-stu-id="48a5f-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a5f-204">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="48a5f-204">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
