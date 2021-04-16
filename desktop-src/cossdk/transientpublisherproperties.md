---
description: Contiene un objeto para cada propiedad de publicador transitorio de la colección TransientSubscriptions primaria. Las suscripciones transitorias se pueden crear sobre la marcha para ejecutar instancias de objeto y desaparecen cuando se destruye el objeto.
ms.assetid: 63921caa-5c22-4203-b1a3-f143928f4742
title: Colección TransientPublisherProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientPublisherProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 707cb974dce632c6eb5f65bc38f1fff8b779e54d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696124"
---
# <a name="transientpublisherproperties-collection"></a><span data-ttu-id="076b9-104">Colección TransientPublisherProperties</span><span class="sxs-lookup"><span data-stu-id="076b9-104">TransientPublisherProperties collection</span></span>

<span data-ttu-id="076b9-105">Contiene un objeto para cada propiedad de publicador transitorio de la colección [**TransientSubscriptions**](transientsubscriptions.md) primaria.</span><span class="sxs-lookup"><span data-stu-id="076b9-105">Contains an object for each transient publisher property for the parent [**TransientSubscriptions**](transientsubscriptions.md) collection.</span></span> <span data-ttu-id="076b9-106">Las suscripciones transitorias se pueden crear sobre la marcha para ejecutar instancias de objeto y desaparecen cuando se destruye el objeto.</span><span class="sxs-lookup"><span data-stu-id="076b9-106">Transient subscriptions can be created on the fly for running object instances, and they vanish when the object is destroyed.</span></span>

<span data-ttu-id="076b9-107">Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="076b9-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="076b9-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="076b9-108">Members</span></span>

<span data-ttu-id="076b9-109">La colección **TransientPublisherProperties** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="076b9-109">The **TransientPublisherProperties** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="076b9-110">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="076b9-110">Related Collections</span></span>

<span data-ttu-id="076b9-111">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="076b9-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="076b9-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="076b9-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="076b9-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="076b9-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="076b9-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="076b9-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="076b9-115">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="076b9-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="076b9-116">**TransientSubscriptions**</span><span class="sxs-lookup"><span data-stu-id="076b9-116">**TransientSubscriptions**</span></span>](transientsubscriptions.md)

## <a name="properties"></a><span data-ttu-id="076b9-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="076b9-117">Properties</span></span>

<span data-ttu-id="076b9-118">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="076b9-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="076b9-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="076b9-119">Name</span></span>](#name)
-   [<span data-ttu-id="076b9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="076b9-120">Value</span></span>](#value)

### <a name="name"></a><span data-ttu-id="076b9-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="076b9-121">Name</span></span>



| <span data-ttu-id="076b9-122">Entrada</span><span class="sxs-lookup"><span data-stu-id="076b9-122">Entry</span></span> | <span data-ttu-id="076b9-123">Value</span><span class="sxs-lookup"><span data-stu-id="076b9-123">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="076b9-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="076b9-124">Description</span></span>    | <span data-ttu-id="076b9-125">Nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="076b9-125">The name of the property.</span></span> <span data-ttu-id="076b9-126">Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="076b9-126">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="076b9-127">Access</span><span class="sxs-lookup"><span data-stu-id="076b9-127">Access</span></span>         | <span data-ttu-id="076b9-128">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="076b9-128">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="076b9-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="076b9-129">Type</span></span>           | <span data-ttu-id="076b9-130">String</span><span class="sxs-lookup"><span data-stu-id="076b9-130">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="076b9-131">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="076b9-131">Default</span></span>        | <span data-ttu-id="076b9-132">"Nueva propiedad"</span><span class="sxs-lookup"><span data-stu-id="076b9-132">"New Property"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="076b9-133">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="076b9-133">Minimum system</span></span> | <span data-ttu-id="076b9-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="076b9-134">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="value"></a><span data-ttu-id="076b9-135">Value</span><span class="sxs-lookup"><span data-stu-id="076b9-135">Value</span></span>



| <span data-ttu-id="076b9-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="076b9-136">Entry</span></span> | <span data-ttu-id="076b9-137">Value</span><span class="sxs-lookup"><span data-stu-id="076b9-137">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="076b9-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="076b9-138">Description</span></span>    | <span data-ttu-id="076b9-139">Valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="076b9-139">A value for the property.</span></span> |
| <span data-ttu-id="076b9-140">Access</span><span class="sxs-lookup"><span data-stu-id="076b9-140">Access</span></span>         | <span data-ttu-id="076b9-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="076b9-141">ReadWrite</span></span>                 |
| <span data-ttu-id="076b9-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="076b9-142">Type</span></span>           | <span data-ttu-id="076b9-143">Variante</span><span class="sxs-lookup"><span data-stu-id="076b9-143">Variant</span></span>                   |
| <span data-ttu-id="076b9-144">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="076b9-144">Default</span></span>        | <span data-ttu-id="076b9-145">N/D</span><span class="sxs-lookup"><span data-stu-id="076b9-145">N/A</span></span>                       |
| <span data-ttu-id="076b9-146">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="076b9-146">Minimum system</span></span> | <span data-ttu-id="076b9-147">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="076b9-147">Windows 2000</span></span>              |



 

## <a name="see-also"></a><span data-ttu-id="076b9-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="076b9-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="076b9-149">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="076b9-149">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
