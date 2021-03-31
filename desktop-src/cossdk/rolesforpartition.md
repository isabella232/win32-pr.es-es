---
description: La colección RolesForPartition siempre está relacionada con un objeto de la colección partitions. Contiene un objeto para cada rol asignado a la partición con la que está relacionada.
ms.assetid: 56985f55-d6e8-4066-b6d5-21c62d4278ce
title: Colección RolesForPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForPartition
api_type:
- COM
api_location: ''
ms.openlocfilehash: c97d524e3fc516086db3a815396d6d59f9369b31
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152940"
---
# <a name="rolesforpartition-collection"></a><span data-ttu-id="ce2c8-104">Colección RolesForPartition</span><span class="sxs-lookup"><span data-stu-id="ce2c8-104">RolesForPartition collection</span></span>

<span data-ttu-id="ce2c8-105">La colección **RolesForPartition** siempre está relacionada con un objeto de la colección [**partitions**](partitions.md) .</span><span class="sxs-lookup"><span data-stu-id="ce2c8-105">The **RolesForPartition** collection is always related to an object in the [**Partitions**](partitions.md) collection.</span></span> <span data-ttu-id="ce2c8-106">Contiene un objeto para cada rol asignado a la partición con la que está relacionada.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-106">It holds an object for each role assigned to the partition to which it is related.</span></span>

<span data-ttu-id="ce2c8-107">Esta colección no admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="ce2c8-107">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="ce2c8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ce2c8-108">Members</span></span>

<span data-ttu-id="ce2c8-109">La colección **RolesForPartition** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-109">The **RolesForPartition** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="ce2c8-110">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="ce2c8-110">Related Collections</span></span>

<span data-ttu-id="ce2c8-111">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="ce2c8-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="ce2c8-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="ce2c8-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="ce2c8-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="ce2c8-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="ce2c8-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="ce2c8-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="ce2c8-115">**UsersInPartitionRole**</span><span class="sxs-lookup"><span data-stu-id="ce2c8-115">**UsersInPartitionRole**</span></span>](usersinpartitionrole.md)

<span data-ttu-id="ce2c8-116">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="ce2c8-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="ce2c8-117">**Particiones**</span><span class="sxs-lookup"><span data-stu-id="ce2c8-117">**Partitions**</span></span>](partitions.md)

## <a name="properties"></a><span data-ttu-id="ce2c8-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ce2c8-118">Properties</span></span>

<span data-ttu-id="ce2c8-119">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="ce2c8-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="ce2c8-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce2c8-120">Description</span></span>](#description)
-   [<span data-ttu-id="ce2c8-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="ce2c8-121">Name</span></span>](#name)

### <a name="description"></a><span data-ttu-id="ce2c8-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce2c8-122">Description</span></span>



| <span data-ttu-id="ce2c8-123">Entrada</span><span class="sxs-lookup"><span data-stu-id="ce2c8-123">Entry</span></span> | <span data-ttu-id="ce2c8-124">Value</span><span class="sxs-lookup"><span data-stu-id="ce2c8-124">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="ce2c8-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce2c8-125">Description</span></span>    | <span data-ttu-id="ce2c8-126">Descripción del rol.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-126">A description of the role.</span></span> |
| <span data-ttu-id="ce2c8-127">Access</span><span class="sxs-lookup"><span data-stu-id="ce2c8-127">Access</span></span>         | <span data-ttu-id="ce2c8-128">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ce2c8-128">ReadOnly</span></span>                   |
| <span data-ttu-id="ce2c8-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="ce2c8-129">Type</span></span>           | <span data-ttu-id="ce2c8-130">String</span><span class="sxs-lookup"><span data-stu-id="ce2c8-130">String</span></span>                     |
| <span data-ttu-id="ce2c8-131">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="ce2c8-131">Default</span></span>        | <span data-ttu-id="ce2c8-132">""</span><span class="sxs-lookup"><span data-stu-id="ce2c8-132">""</span></span>                         |
| <span data-ttu-id="ce2c8-133">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="ce2c8-133">Minimum system</span></span> | <span data-ttu-id="ce2c8-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ce2c8-134">Windows Server 2003</span></span>        |



 

### <a name="name"></a><span data-ttu-id="ce2c8-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="ce2c8-135">Name</span></span>



| <span data-ttu-id="ce2c8-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="ce2c8-136">Entry</span></span> | <span data-ttu-id="ce2c8-137">Value</span><span class="sxs-lookup"><span data-stu-id="ce2c8-137">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce2c8-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce2c8-138">Description</span></span>    | <span data-ttu-id="ce2c8-139">Nombre del rol.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-139">The role name.</span></span> <span data-ttu-id="ce2c8-140">Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-140">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ce2c8-141">Access</span><span class="sxs-lookup"><span data-stu-id="ce2c8-141">Access</span></span>         | <span data-ttu-id="ce2c8-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ce2c8-142">ReadOnly</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ce2c8-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="ce2c8-143">Type</span></span>           | <span data-ttu-id="ce2c8-144">String</span><span class="sxs-lookup"><span data-stu-id="ce2c8-144">String</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ce2c8-145">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="ce2c8-145">Default</span></span>        | <span data-ttu-id="ce2c8-146">""</span><span class="sxs-lookup"><span data-stu-id="ce2c8-146">""</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="ce2c8-147">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="ce2c8-147">Minimum system</span></span> | <span data-ttu-id="ce2c8-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ce2c8-148">Windows Server 2003</span></span>                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="ce2c8-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce2c8-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce2c8-150">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="ce2c8-150">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
