---
description: Contiene un objeto para cada rol asignado a la interfaz con la que está relacionada la colección. Los roles ya deben estar asignados en el nivel de aplicación.
ms.assetid: f5c1dc9a-13da-4504-a244-4ce8058240b8
title: Colección RolesForInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 60c52e3cb48adc0ed52ef10bd9e0a73e716fabfc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714793"
---
# <a name="rolesforinterface-collection"></a><span data-ttu-id="f22d0-104">Colección RolesForInterface</span><span class="sxs-lookup"><span data-stu-id="f22d0-104">RolesForInterface collection</span></span>

<span data-ttu-id="f22d0-105">Contiene un objeto para cada rol asignado a la interfaz con la que está relacionada la colección.</span><span class="sxs-lookup"><span data-stu-id="f22d0-105">Contains an object for each role assigned to the interface to which the collection is related.</span></span> <span data-ttu-id="f22d0-106">Los roles ya deben estar asignados en el nivel de aplicación.</span><span class="sxs-lookup"><span data-stu-id="f22d0-106">The roles must already be assigned at the application level.</span></span>

<span data-ttu-id="f22d0-107">Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="f22d0-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="f22d0-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f22d0-108">Members</span></span>

<span data-ttu-id="f22d0-109">La colección **RolesForInterface** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="f22d0-109">The **RolesForInterface** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="f22d0-110">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="f22d0-110">Related Collections</span></span>

<span data-ttu-id="f22d0-111">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="f22d0-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="f22d0-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="f22d0-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="f22d0-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="f22d0-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="f22d0-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="f22d0-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="f22d0-115">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="f22d0-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="f22d0-116">**InterfacesForComponent**</span><span class="sxs-lookup"><span data-stu-id="f22d0-116">**InterfacesForComponent**</span></span>](interfacesforcomponent.md)

## <a name="properties"></a><span data-ttu-id="f22d0-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f22d0-117">Properties</span></span>

<span data-ttu-id="f22d0-118">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="f22d0-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="f22d0-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="f22d0-119">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="f22d0-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="f22d0-120">Name</span></span>



| <span data-ttu-id="f22d0-121">Entrada</span><span class="sxs-lookup"><span data-stu-id="f22d0-121">Entry</span></span> | <span data-ttu-id="f22d0-122">Value</span><span class="sxs-lookup"><span data-stu-id="f22d0-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f22d0-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="f22d0-123">Description</span></span>    | <span data-ttu-id="f22d0-124">Nombre del rol.</span><span class="sxs-lookup"><span data-stu-id="f22d0-124">The role name.</span></span> <span data-ttu-id="f22d0-125">Debe ser ya un rol asignado a la aplicación (que aparece en la colección de roles).</span><span class="sxs-lookup"><span data-stu-id="f22d0-125">Must already be a role assigned to the application (appearing in the Roles collection).</span></span> <span data-ttu-id="f22d0-126">Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="f22d0-126">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="f22d0-127">Access</span><span class="sxs-lookup"><span data-stu-id="f22d0-127">Access</span></span>         | <span data-ttu-id="f22d0-128">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="f22d0-128">WriteOnce</span></span>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="f22d0-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="f22d0-129">Type</span></span>           | <span data-ttu-id="f22d0-130">String</span><span class="sxs-lookup"><span data-stu-id="f22d0-130">String</span></span>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="f22d0-131">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="f22d0-131">Default</span></span>        | <span data-ttu-id="f22d0-132">"Nuevo rol"</span><span class="sxs-lookup"><span data-stu-id="f22d0-132">"New Role"</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="f22d0-133">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f22d0-133">Minimum system</span></span> | <span data-ttu-id="f22d0-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f22d0-134">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="see-also"></a><span data-ttu-id="f22d0-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="f22d0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f22d0-136">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="f22d0-136">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
