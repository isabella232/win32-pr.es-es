---
description: Especifica las aplicaciones contenidas en cada partición.
ms.assetid: 264a35fd-ba71-4ae9-908a-24a72167c26b
title: Colección de particiones
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Partitions
api_type:
- COM
api_location: ''
ms.openlocfilehash: b1016ae932d6841a5db590f2d24496113d3cefc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807958"
---
# <a name="partitions-collection"></a><span data-ttu-id="9bcf5-103">Colección de particiones</span><span class="sxs-lookup"><span data-stu-id="9bcf5-103">Partitions collection</span></span>

<span data-ttu-id="9bcf5-104">Especifica las aplicaciones contenidas en cada partición.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-104">Specifies the applications contained within each partition.</span></span>

<span data-ttu-id="9bcf5-105">Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="9bcf5-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="9bcf5-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="9bcf5-106">Members</span></span>

<span data-ttu-id="9bcf5-107">La colección de **particiones** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-107">The **Partitions** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="9bcf5-108">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="9bcf5-108">Related Collections</span></span>

<span data-ttu-id="9bcf5-109">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="9bcf5-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="9bcf5-110">**APLICACIONES**</span><span class="sxs-lookup"><span data-stu-id="9bcf5-110">**Applications**</span></span>](applications.md)
-   [<span data-ttu-id="9bcf5-111">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="9bcf5-111">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="9bcf5-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="9bcf5-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="9bcf5-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="9bcf5-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="9bcf5-114">**RolesForPartition**</span><span class="sxs-lookup"><span data-stu-id="9bcf5-114">**RolesForPartition**</span></span>](rolesforpartition.md)

<span data-ttu-id="9bcf5-115">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="9bcf5-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="9bcf5-116">**Raíces**</span><span class="sxs-lookup"><span data-stu-id="9bcf5-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="9bcf5-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9bcf5-117">Properties</span></span>

<span data-ttu-id="9bcf5-118">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="9bcf5-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="9bcf5-119">Sustituir</span><span class="sxs-lookup"><span data-stu-id="9bcf5-119">Changeable</span></span>](#changeable)
-   [<span data-ttu-id="9bcf5-120">Eliminable</span><span class="sxs-lookup"><span data-stu-id="9bcf5-120">Deleteable</span></span>](#deleteable)
-   [<span data-ttu-id="9bcf5-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="9bcf5-121">Description</span></span>](#description)
-   [<span data-ttu-id="9bcf5-122">Id</span><span class="sxs-lookup"><span data-stu-id="9bcf5-122">ID</span></span>](#partitions-collection)
-   [<span data-ttu-id="9bcf5-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="9bcf5-123">Name</span></span>](#name)

### <a name="changeable"></a><span data-ttu-id="9bcf5-124">Sustituir</span><span class="sxs-lookup"><span data-stu-id="9bcf5-124">Changeable</span></span>



| <span data-ttu-id="9bcf5-125">Entrada</span><span class="sxs-lookup"><span data-stu-id="9bcf5-125">Entry</span></span> | <span data-ttu-id="9bcf5-126">Value</span><span class="sxs-lookup"><span data-stu-id="9bcf5-126">Value</span></span> |
|----------------|--------------------------------------------------|
| <span data-ttu-id="9bcf5-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="9bcf5-127">Description</span></span>    | <span data-ttu-id="9bcf5-128">Determina si esta partición es modificable.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-128">Determines whether this partition is changeable.</span></span> |
| <span data-ttu-id="9bcf5-129">Access</span><span class="sxs-lookup"><span data-stu-id="9bcf5-129">Access</span></span>         | <span data-ttu-id="9bcf5-130">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9bcf5-130">ReadWrite</span></span>                                        |
| <span data-ttu-id="9bcf5-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9bcf5-131">Type</span></span>           | <span data-ttu-id="9bcf5-132">Bool</span><span class="sxs-lookup"><span data-stu-id="9bcf5-132">Bool</span></span>                                             |
| <span data-ttu-id="9bcf5-133">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="9bcf5-133">Default</span></span>        | <span data-ttu-id="9bcf5-134">True</span><span class="sxs-lookup"><span data-stu-id="9bcf5-134">True</span></span>                                             |
| <span data-ttu-id="9bcf5-135">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="9bcf5-135">Minimum system</span></span> | <span data-ttu-id="9bcf5-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9bcf5-136">Windows Server 2003</span></span>                              |



 

### <a name="deleteable"></a><span data-ttu-id="9bcf5-137">Eliminable</span><span class="sxs-lookup"><span data-stu-id="9bcf5-137">Deleteable</span></span>



| <span data-ttu-id="9bcf5-138">Entrada</span><span class="sxs-lookup"><span data-stu-id="9bcf5-138">Entry</span></span> | <span data-ttu-id="9bcf5-139">Value</span><span class="sxs-lookup"><span data-stu-id="9bcf5-139">Value</span></span> |
|----------------|---------------------------------------------------|
| <span data-ttu-id="9bcf5-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="9bcf5-140">Description</span></span>    | <span data-ttu-id="9bcf5-141">Determina si se puede eliminar esta partición.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-141">Determines whether this partition can be deleted.</span></span> |
| <span data-ttu-id="9bcf5-142">Access</span><span class="sxs-lookup"><span data-stu-id="9bcf5-142">Access</span></span>         | <span data-ttu-id="9bcf5-143">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9bcf5-143">ReadWrite</span></span>                                         |
| <span data-ttu-id="9bcf5-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="9bcf5-144">Type</span></span>           | <span data-ttu-id="9bcf5-145">Bool</span><span class="sxs-lookup"><span data-stu-id="9bcf5-145">Bool</span></span>                                              |
| <span data-ttu-id="9bcf5-146">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="9bcf5-146">Default</span></span>        | <span data-ttu-id="9bcf5-147">True</span><span class="sxs-lookup"><span data-stu-id="9bcf5-147">True</span></span>                                              |
| <span data-ttu-id="9bcf5-148">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="9bcf5-148">Minimum system</span></span> | <span data-ttu-id="9bcf5-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9bcf5-149">Windows Server 2003</span></span>                               |



 

### <a name="description"></a><span data-ttu-id="9bcf5-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="9bcf5-150">Description</span></span>



| <span data-ttu-id="9bcf5-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="9bcf5-151">Entry</span></span> | <span data-ttu-id="9bcf5-152">Value</span><span class="sxs-lookup"><span data-stu-id="9bcf5-152">Value</span></span> |
|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="9bcf5-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="9bcf5-153">Description</span></span>    | <span data-ttu-id="9bcf5-154">Esta propiedad representa la descripción que identifica la partición.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-154">This property represents the description identifying the partition.</span></span> |
| <span data-ttu-id="9bcf5-155">Access</span><span class="sxs-lookup"><span data-stu-id="9bcf5-155">Access</span></span>         | <span data-ttu-id="9bcf5-156">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9bcf5-156">ReadWrite</span></span>                                                           |
| <span data-ttu-id="9bcf5-157">Tipo</span><span class="sxs-lookup"><span data-stu-id="9bcf5-157">Type</span></span>           | <span data-ttu-id="9bcf5-158">String</span><span class="sxs-lookup"><span data-stu-id="9bcf5-158">String</span></span>                                                              |
| <span data-ttu-id="9bcf5-159">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="9bcf5-159">Default</span></span>        | <span data-ttu-id="9bcf5-160">""</span><span class="sxs-lookup"><span data-stu-id="9bcf5-160">""</span></span>                                                                  |
| <span data-ttu-id="9bcf5-161">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="9bcf5-161">Minimum system</span></span> | <span data-ttu-id="9bcf5-162">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9bcf5-162">Windows Server 2003</span></span>                                                 |



 

### <a name="id"></a><span data-ttu-id="9bcf5-163">id</span><span class="sxs-lookup"><span data-stu-id="9bcf5-163">ID</span></span>



| <span data-ttu-id="9bcf5-164">Entrada</span><span class="sxs-lookup"><span data-stu-id="9bcf5-164">Entry</span></span> | <span data-ttu-id="9bcf5-165">Value</span><span class="sxs-lookup"><span data-stu-id="9bcf5-165">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bcf5-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="9bcf5-166">Description</span></span>    | <span data-ttu-id="9bcf5-167">Un GUID que representa la partición.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-167">A GUID representing the partition.</span></span> <span data-ttu-id="9bcf5-168">Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-168">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="9bcf5-169">Access</span><span class="sxs-lookup"><span data-stu-id="9bcf5-169">Access</span></span>         | <span data-ttu-id="9bcf5-170">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="9bcf5-170">WriteOnce</span></span>                                                                                                                                                          |
| <span data-ttu-id="9bcf5-171">Tipo</span><span class="sxs-lookup"><span data-stu-id="9bcf5-171">Type</span></span>           | <span data-ttu-id="9bcf5-172">String</span><span class="sxs-lookup"><span data-stu-id="9bcf5-172">String</span></span>                                                                                                                                                             |
| <span data-ttu-id="9bcf5-173">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="9bcf5-173">Default</span></span>        | <Generated>                                                                                                                                                  |
| <span data-ttu-id="9bcf5-174">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="9bcf5-174">Minimum system</span></span> | <span data-ttu-id="9bcf5-175">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9bcf5-175">Windows Server 2003</span></span>                                                                                                                                                |



 

### <a name="name"></a><span data-ttu-id="9bcf5-176">Nombre</span><span class="sxs-lookup"><span data-stu-id="9bcf5-176">Name</span></span>



| <span data-ttu-id="9bcf5-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="9bcf5-177">Entry</span></span> | <span data-ttu-id="9bcf5-178">Value</span><span class="sxs-lookup"><span data-stu-id="9bcf5-178">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bcf5-179">Descripción</span><span class="sxs-lookup"><span data-stu-id="9bcf5-179">Description</span></span>    | <span data-ttu-id="9bcf5-180">Representa el nombre de la partición.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-180">Represents the partition name.</span></span> <span data-ttu-id="9bcf5-181">Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de la propiedad [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-181">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="9bcf5-182">Access</span><span class="sxs-lookup"><span data-stu-id="9bcf5-182">Access</span></span>         | <span data-ttu-id="9bcf5-183">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9bcf5-183">ReadWrite</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="9bcf5-184">Tipo</span><span class="sxs-lookup"><span data-stu-id="9bcf5-184">Type</span></span>           | <span data-ttu-id="9bcf5-185">String</span><span class="sxs-lookup"><span data-stu-id="9bcf5-185">String</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="9bcf5-186">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="9bcf5-186">Default</span></span>        | <span data-ttu-id="9bcf5-187">"Nueva partición"</span><span class="sxs-lookup"><span data-stu-id="9bcf5-187">"New Partition"</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="9bcf5-188">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="9bcf5-188">Minimum system</span></span> | <span data-ttu-id="9bcf5-189">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9bcf5-189">Windows Server 2003</span></span>                                                                                                                                                                                                                    |



 

## <a name="see-also"></a><span data-ttu-id="9bcf5-190">Vea también</span><span class="sxs-lookup"><span data-stu-id="9bcf5-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bcf5-191">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="9bcf5-191">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
