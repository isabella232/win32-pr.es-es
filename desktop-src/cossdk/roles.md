---
description: La colección de roles siempre está relacionada con un objeto de la colección de aplicaciones. Contiene un objeto para cada rol asignado a la aplicación a la que está relacionado.
ms.assetid: 87f39c2a-ad66-4390-9220-06751dcebd95
title: Colección de roles
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Roles
api_type:
- COM
api_location: ''
ms.openlocfilehash: f676a53f5fe54e42ca2a489ad834b9c91e4e0ef5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275068"
---
# <a name="roles-collection"></a><span data-ttu-id="ea43c-104">Colección de roles</span><span class="sxs-lookup"><span data-stu-id="ea43c-104">Roles collection</span></span>

<span data-ttu-id="ea43c-105">La colección de **roles** siempre está relacionada con un objeto de la colección de [**aplicaciones**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="ea43c-105">The **Roles** collection is always related to an object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="ea43c-106">Contiene un objeto para cada rol asignado a la aplicación a la que está relacionado.</span><span class="sxs-lookup"><span data-stu-id="ea43c-106">It holds an object for each role assigned to the application to which it is related.</span></span>

<span data-ttu-id="ea43c-107">Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="ea43c-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="ea43c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ea43c-108">Members</span></span>

<span data-ttu-id="ea43c-109">La colección de **roles** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="ea43c-109">The **Roles** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="ea43c-110">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="ea43c-110">Related Collections</span></span>

<span data-ttu-id="ea43c-111">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="ea43c-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="ea43c-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="ea43c-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="ea43c-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="ea43c-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="ea43c-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="ea43c-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="ea43c-115">**UsersInRole**</span><span class="sxs-lookup"><span data-stu-id="ea43c-115">**UsersInRole**</span></span>](usersinrole.md)

<span data-ttu-id="ea43c-116">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="ea43c-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="ea43c-117">**APLICACIONES**</span><span class="sxs-lookup"><span data-stu-id="ea43c-117">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="ea43c-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ea43c-118">Properties</span></span>

<span data-ttu-id="ea43c-119">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="ea43c-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="ea43c-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea43c-120">Description</span></span>](#description)
-   [<span data-ttu-id="ea43c-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="ea43c-121">Name</span></span>](#name)

### <a name="description"></a><span data-ttu-id="ea43c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea43c-122">Description</span></span>



| <span data-ttu-id="ea43c-123">Entrada</span><span class="sxs-lookup"><span data-stu-id="ea43c-123">Entry</span></span> | <span data-ttu-id="ea43c-124">Value</span><span class="sxs-lookup"><span data-stu-id="ea43c-124">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="ea43c-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea43c-125">Description</span></span>    | <span data-ttu-id="ea43c-126">Descripción del rol.</span><span class="sxs-lookup"><span data-stu-id="ea43c-126">A description of the role.</span></span> |
| <span data-ttu-id="ea43c-127">Access</span><span class="sxs-lookup"><span data-stu-id="ea43c-127">Access</span></span>         | <span data-ttu-id="ea43c-128">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ea43c-128">ReadWrite</span></span>                  |
| <span data-ttu-id="ea43c-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea43c-129">Type</span></span>           | <span data-ttu-id="ea43c-130">String</span><span class="sxs-lookup"><span data-stu-id="ea43c-130">String</span></span>                     |
| <span data-ttu-id="ea43c-131">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="ea43c-131">Default</span></span>        | <span data-ttu-id="ea43c-132">""</span><span class="sxs-lookup"><span data-stu-id="ea43c-132">""</span></span>                         |
| <span data-ttu-id="ea43c-133">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="ea43c-133">Minimum system</span></span> | <span data-ttu-id="ea43c-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ea43c-134">Windows 2000</span></span>               |



 

### <a name="name"></a><span data-ttu-id="ea43c-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="ea43c-135">Name</span></span>



| <span data-ttu-id="ea43c-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="ea43c-136">Entry</span></span> | <span data-ttu-id="ea43c-137">Value</span><span class="sxs-lookup"><span data-stu-id="ea43c-137">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea43c-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea43c-138">Description</span></span>    | <span data-ttu-id="ea43c-139">Nombre del rol.</span><span class="sxs-lookup"><span data-stu-id="ea43c-139">The role name.</span></span> <span data-ttu-id="ea43c-140">Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="ea43c-140">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ea43c-141">Access</span><span class="sxs-lookup"><span data-stu-id="ea43c-141">Access</span></span>         | <span data-ttu-id="ea43c-142">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="ea43c-142">WriteOnce</span></span>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="ea43c-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea43c-143">Type</span></span>           | <span data-ttu-id="ea43c-144">String</span><span class="sxs-lookup"><span data-stu-id="ea43c-144">String</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ea43c-145">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="ea43c-145">Default</span></span>        | <span data-ttu-id="ea43c-146">"Nuevo rol"</span><span class="sxs-lookup"><span data-stu-id="ea43c-146">"New Role"</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ea43c-147">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="ea43c-147">Minimum system</span></span> | <span data-ttu-id="ea43c-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ea43c-148">Windows 2000</span></span>                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a><span data-ttu-id="ea43c-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea43c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea43c-150">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="ea43c-150">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
