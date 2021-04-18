---
description: Contiene un objeto para cada usuario de la partición.
ms.assetid: baec56ae-be8a-42a7-90bc-1db7c5cd7fe2
title: Colección PartitionUsers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PartitionUsers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1521642879037938451decd873a9aa14211ce296
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705361"
---
# <a name="partitionusers-collection"></a><span data-ttu-id="09e98-103">Colección PartitionUsers</span><span class="sxs-lookup"><span data-stu-id="09e98-103">PartitionUsers collection</span></span>

<span data-ttu-id="09e98-104">Contiene un objeto para cada usuario de la partición.</span><span class="sxs-lookup"><span data-stu-id="09e98-104">Contains an object for each partition user.</span></span>

<span data-ttu-id="09e98-105">Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="09e98-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="09e98-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="09e98-106">Members</span></span>

<span data-ttu-id="09e98-107">La colección **PartitionUsers** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="09e98-107">The **PartitionUsers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="09e98-108">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="09e98-108">Related Collections</span></span>

<span data-ttu-id="09e98-109">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="09e98-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="09e98-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="09e98-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="09e98-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="09e98-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="09e98-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="09e98-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="09e98-113">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="09e98-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="09e98-114">**Raíces**</span><span class="sxs-lookup"><span data-stu-id="09e98-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="09e98-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="09e98-115">Properties</span></span>

<span data-ttu-id="09e98-116">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="09e98-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="09e98-117">AccountName</span><span class="sxs-lookup"><span data-stu-id="09e98-117">AccountName</span></span>](#accountname)
-   [<span data-ttu-id="09e98-118">DefaultPartitionID</span><span class="sxs-lookup"><span data-stu-id="09e98-118">DefaultPartitionID</span></span>](#defaultpartitionid)

### <a name="accountname"></a><span data-ttu-id="09e98-119">AccountName</span><span class="sxs-lookup"><span data-stu-id="09e98-119">AccountName</span></span>



| <span data-ttu-id="09e98-120">Entrada</span><span class="sxs-lookup"><span data-stu-id="09e98-120">Entry</span></span> | <span data-ttu-id="09e98-121">Value</span><span class="sxs-lookup"><span data-stu-id="09e98-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09e98-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="09e98-122">Description</span></span>    | <span data-ttu-id="09e98-123">Nombre de la cuenta del usuario de la partición.</span><span class="sxs-lookup"><span data-stu-id="09e98-123">Name of the partition user's account.</span></span> <span data-ttu-id="09e98-124">Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="09e98-124">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="09e98-125">Access</span><span class="sxs-lookup"><span data-stu-id="09e98-125">Access</span></span>         | <span data-ttu-id="09e98-126">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="09e98-126">WriteOnce</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="09e98-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="09e98-127">Type</span></span>           | <span data-ttu-id="09e98-128">String</span><span class="sxs-lookup"><span data-stu-id="09e98-128">String</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="09e98-129">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="09e98-129">Default</span></span>        | <span data-ttu-id="09e98-130">"Nuevo usuario"</span><span class="sxs-lookup"><span data-stu-id="09e98-130">"New User"</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="09e98-131">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="09e98-131">Minimum system</span></span> | <span data-ttu-id="09e98-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="09e98-132">Windows Server 2003</span></span>                                                                                                                                                                                          |



 

### <a name="defaultpartitionid"></a><span data-ttu-id="09e98-133">DefaultPartitionID</span><span class="sxs-lookup"><span data-stu-id="09e98-133">DefaultPartitionID</span></span>



| <span data-ttu-id="09e98-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="09e98-134">Entry</span></span> | <span data-ttu-id="09e98-135">Value</span><span class="sxs-lookup"><span data-stu-id="09e98-135">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="09e98-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="09e98-136">Description</span></span>    | <span data-ttu-id="09e98-137">Identificador único global de la partición de aplicación base.</span><span class="sxs-lookup"><span data-stu-id="09e98-137">The globally unique identifier for the base application partition.</span></span> |
| <span data-ttu-id="09e98-138">Access</span><span class="sxs-lookup"><span data-stu-id="09e98-138">Access</span></span>         | <span data-ttu-id="09e98-139">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="09e98-139">ReadWrite</span></span>                                                          |
| <span data-ttu-id="09e98-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="09e98-140">Type</span></span>           | <span data-ttu-id="09e98-141">String</span><span class="sxs-lookup"><span data-stu-id="09e98-141">String</span></span>                                                             |
| <span data-ttu-id="09e98-142">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="09e98-142">Default</span></span>        | <span data-ttu-id="09e98-143">{41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}</span><span class="sxs-lookup"><span data-stu-id="09e98-143">{41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}</span></span>                             |
| <span data-ttu-id="09e98-144">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="09e98-144">Minimum system</span></span> | <span data-ttu-id="09e98-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="09e98-145">Windows Server 2003</span></span>                                                |



 

## <a name="see-also"></a><span data-ttu-id="09e98-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="09e98-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09e98-147">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="09e98-147">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
