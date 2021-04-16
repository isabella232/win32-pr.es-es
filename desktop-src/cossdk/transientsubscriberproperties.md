---
description: Contiene un objeto para cada propiedad de suscriptor de la colección TransientSubscriptions primaria. Las suscripciones transitorias se pueden crear sobre la marcha para ejecutar instancias de objeto y desaparecen cuando se destruye el objeto.
ms.assetid: b4f003b0-db9d-45f1-a57d-3e4d321289ca
title: Colección TransientSubscriberProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriberProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 17f89638efe232f2cdf06e1206f74a0df44601b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686456"
---
# <a name="transientsubscriberproperties-collection"></a><span data-ttu-id="a10d7-104">Colección TransientSubscriberProperties</span><span class="sxs-lookup"><span data-stu-id="a10d7-104">TransientSubscriberProperties collection</span></span>

<span data-ttu-id="a10d7-105">Contiene un objeto para cada propiedad de suscriptor de la colección [**TransientSubscriptions**](transientsubscriptions.md) primaria.</span><span class="sxs-lookup"><span data-stu-id="a10d7-105">Contains an object for each subscriber property for the parent [**TransientSubscriptions**](transientsubscriptions.md) collection.</span></span> <span data-ttu-id="a10d7-106">Las suscripciones transitorias se pueden crear sobre la marcha para ejecutar instancias de objeto y desaparecen cuando se destruye el objeto.</span><span class="sxs-lookup"><span data-stu-id="a10d7-106">Transient subscriptions can be created on the fly for running object instances, and they vanish when the object is destroyed.</span></span>

<span data-ttu-id="a10d7-107">Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="a10d7-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="a10d7-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a10d7-108">Members</span></span>

<span data-ttu-id="a10d7-109">La colección **TransientSubscriberProperties** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="a10d7-109">The **TransientSubscriberProperties** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="a10d7-110">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="a10d7-110">Related Collections</span></span>

<span data-ttu-id="a10d7-111">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="a10d7-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="a10d7-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="a10d7-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="a10d7-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="a10d7-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="a10d7-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="a10d7-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="a10d7-115">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="a10d7-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="a10d7-116">**TransientSubscriptions**</span><span class="sxs-lookup"><span data-stu-id="a10d7-116">**TransientSubscriptions**</span></span>](transientsubscriptions.md)

## <a name="properties"></a><span data-ttu-id="a10d7-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a10d7-117">Properties</span></span>

<span data-ttu-id="a10d7-118">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="a10d7-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="a10d7-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="a10d7-119">Name</span></span>](#name)
-   [<span data-ttu-id="a10d7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a10d7-120">Value</span></span>](#value)

### <a name="name"></a><span data-ttu-id="a10d7-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="a10d7-121">Name</span></span>



| <span data-ttu-id="a10d7-122">Entrada</span><span class="sxs-lookup"><span data-stu-id="a10d7-122">Entry</span></span> | <span data-ttu-id="a10d7-123">Value</span><span class="sxs-lookup"><span data-stu-id="a10d7-123">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a10d7-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="a10d7-124">Description</span></span>    | <span data-ttu-id="a10d7-125">Nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="a10d7-125">The name of the property.</span></span> <span data-ttu-id="a10d7-126">Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="a10d7-126">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="a10d7-127">Access</span><span class="sxs-lookup"><span data-stu-id="a10d7-127">Access</span></span>         | <span data-ttu-id="a10d7-128">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="a10d7-128">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="a10d7-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="a10d7-129">Type</span></span>           | <span data-ttu-id="a10d7-130">String</span><span class="sxs-lookup"><span data-stu-id="a10d7-130">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a10d7-131">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="a10d7-131">Default</span></span>        | <span data-ttu-id="a10d7-132">"Nueva propiedad"</span><span class="sxs-lookup"><span data-stu-id="a10d7-132">"New Property"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="a10d7-133">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="a10d7-133">Minimum system</span></span> | <span data-ttu-id="a10d7-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a10d7-134">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="value"></a><span data-ttu-id="a10d7-135">Value</span><span class="sxs-lookup"><span data-stu-id="a10d7-135">Value</span></span>



| <span data-ttu-id="a10d7-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="a10d7-136">Entry</span></span> | <span data-ttu-id="a10d7-137">Value</span><span class="sxs-lookup"><span data-stu-id="a10d7-137">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="a10d7-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="a10d7-138">Description</span></span>    | <span data-ttu-id="a10d7-139">Valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="a10d7-139">A value for the property.</span></span> |
| <span data-ttu-id="a10d7-140">Access</span><span class="sxs-lookup"><span data-stu-id="a10d7-140">Access</span></span>         | <span data-ttu-id="a10d7-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a10d7-141">ReadWrite</span></span>                 |
| <span data-ttu-id="a10d7-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="a10d7-142">Type</span></span>           | <span data-ttu-id="a10d7-143">Variante</span><span class="sxs-lookup"><span data-stu-id="a10d7-143">Variant</span></span>                   |
| <span data-ttu-id="a10d7-144">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="a10d7-144">Default</span></span>        | <span data-ttu-id="a10d7-145">N/D</span><span class="sxs-lookup"><span data-stu-id="a10d7-145">N/A</span></span>                       |
| <span data-ttu-id="a10d7-146">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="a10d7-146">Minimum system</span></span> | <span data-ttu-id="a10d7-147">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a10d7-147">Windows 2000</span></span>              |



 

## <a name="see-also"></a><span data-ttu-id="a10d7-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="a10d7-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a10d7-149">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="a10d7-149">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
