---
description: Contiene un objeto para cada propiedad de publicador para la colección SubscriptionsForComponent primaria.
ms.assetid: 7699c258-ca11-4652-b2f7-b2f2307c01fc
title: Colección PublisherProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublisherProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: bdab3e8143ea3d35d07adb5caa73639fcb568cd1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153195"
---
# <a name="publisherproperties-collection"></a><span data-ttu-id="70e60-103">Colección PublisherProperties</span><span class="sxs-lookup"><span data-stu-id="70e60-103">PublisherProperties collection</span></span>

<span data-ttu-id="70e60-104">Contiene un objeto para cada propiedad de publicador para la colección [**SubscriptionsForComponent**](subscriptionsforcomponent.md) primaria.</span><span class="sxs-lookup"><span data-stu-id="70e60-104">Contains an object for each publisher property for the parent [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection.</span></span>

<span data-ttu-id="70e60-105">Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="70e60-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="70e60-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="70e60-106">Members</span></span>

<span data-ttu-id="70e60-107">La colección **PublisherProperties** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="70e60-107">The **PublisherProperties** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="70e60-108">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="70e60-108">Related Collections</span></span>

<span data-ttu-id="70e60-109">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="70e60-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="70e60-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="70e60-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="70e60-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="70e60-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="70e60-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="70e60-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="70e60-113">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="70e60-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="70e60-114">**SubscriptionsForComponent**</span><span class="sxs-lookup"><span data-stu-id="70e60-114">**SubscriptionsForComponent**</span></span>](subscriptionsforcomponent.md)

## <a name="properties"></a><span data-ttu-id="70e60-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="70e60-115">Properties</span></span>

<span data-ttu-id="70e60-116">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="70e60-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="70e60-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="70e60-117">Name</span></span>](#name)
-   [<span data-ttu-id="70e60-118">Valor</span><span class="sxs-lookup"><span data-stu-id="70e60-118">Value</span></span>](#value)

### <a name="name"></a><span data-ttu-id="70e60-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="70e60-119">Name</span></span>



| <span data-ttu-id="70e60-120">Entrada</span><span class="sxs-lookup"><span data-stu-id="70e60-120">Entry</span></span> | <span data-ttu-id="70e60-121">Value</span><span class="sxs-lookup"><span data-stu-id="70e60-121">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70e60-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="70e60-122">Description</span></span>    | <span data-ttu-id="70e60-123">Nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="70e60-123">The name of the property.</span></span> <span data-ttu-id="70e60-124">Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="70e60-124">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="70e60-125">Access</span><span class="sxs-lookup"><span data-stu-id="70e60-125">Access</span></span>         | <span data-ttu-id="70e60-126">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="70e60-126">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="70e60-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="70e60-127">Type</span></span>           | <span data-ttu-id="70e60-128">String</span><span class="sxs-lookup"><span data-stu-id="70e60-128">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="70e60-129">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="70e60-129">Default</span></span>        | <span data-ttu-id="70e60-130">"Nueva propiedad"</span><span class="sxs-lookup"><span data-stu-id="70e60-130">"New Property"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="70e60-131">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="70e60-131">Minimum system</span></span> | <span data-ttu-id="70e60-132">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="70e60-132">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="value"></a><span data-ttu-id="70e60-133">Value</span><span class="sxs-lookup"><span data-stu-id="70e60-133">Value</span></span>



| <span data-ttu-id="70e60-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="70e60-134">Entry</span></span> | <span data-ttu-id="70e60-135">Value</span><span class="sxs-lookup"><span data-stu-id="70e60-135">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="70e60-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="70e60-136">Description</span></span>    | <span data-ttu-id="70e60-137">Valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="70e60-137">A value for the property.</span></span> |
| <span data-ttu-id="70e60-138">Access</span><span class="sxs-lookup"><span data-stu-id="70e60-138">Access</span></span>         | <span data-ttu-id="70e60-139">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="70e60-139">ReadWrite</span></span>                 |
| <span data-ttu-id="70e60-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="70e60-140">Type</span></span>           | <span data-ttu-id="70e60-141">Variante</span><span class="sxs-lookup"><span data-stu-id="70e60-141">Variant</span></span>                   |
| <span data-ttu-id="70e60-142">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="70e60-142">Default</span></span>        | <span data-ttu-id="70e60-143">N/D</span><span class="sxs-lookup"><span data-stu-id="70e60-143">N/A</span></span>                       |
| <span data-ttu-id="70e60-144">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="70e60-144">Minimum system</span></span> | <span data-ttu-id="70e60-145">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="70e60-145">Windows 2000</span></span>              |



 

## <a name="see-also"></a><span data-ttu-id="70e60-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="70e60-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70e60-147">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="70e60-147">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
