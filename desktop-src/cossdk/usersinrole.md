---
description: Contiene un objeto para cada usuario en el rol con el que está relacionada la colección.
ms.assetid: e7d9e5e8-1927-42b2-bdd5-0c49a562c31f
title: Colección UsersInRole
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: e5bf36937d08efd377b48ef251ffb7219c05504f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275008"
---
# <a name="usersinrole-collection"></a><span data-ttu-id="7db3b-103">Colección UsersInRole</span><span class="sxs-lookup"><span data-stu-id="7db3b-103">UsersInRole collection</span></span>

<span data-ttu-id="7db3b-104">Contiene un objeto para cada usuario en el rol con el que está relacionada la colección.</span><span class="sxs-lookup"><span data-stu-id="7db3b-104">Contains an object for each user in the role to which the collection is related.</span></span>

<span data-ttu-id="7db3b-105">Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="7db3b-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="7db3b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="7db3b-106">Members</span></span>

<span data-ttu-id="7db3b-107">La colección **UsersInRole** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="7db3b-107">The **UsersInRole** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="7db3b-108">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="7db3b-108">Related Collections</span></span>

<span data-ttu-id="7db3b-109">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="7db3b-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="7db3b-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="7db3b-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="7db3b-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="7db3b-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="7db3b-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="7db3b-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="7db3b-113">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="7db3b-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="7db3b-114">**Roles**</span><span class="sxs-lookup"><span data-stu-id="7db3b-114">**Roles**</span></span>](roles.md)

## <a name="properties"></a><span data-ttu-id="7db3b-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7db3b-115">Properties</span></span>

<span data-ttu-id="7db3b-116">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="7db3b-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="7db3b-117">User</span><span class="sxs-lookup"><span data-stu-id="7db3b-117">User</span></span>](#usersinrole-collection)

### <a name="user"></a><span data-ttu-id="7db3b-118">User (Usuario)</span><span class="sxs-lookup"><span data-stu-id="7db3b-118">User</span></span>



| <span data-ttu-id="7db3b-119">Entrada</span><span class="sxs-lookup"><span data-stu-id="7db3b-119">Entry</span></span> | <span data-ttu-id="7db3b-120">Value</span><span class="sxs-lookup"><span data-stu-id="7db3b-120">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7db3b-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="7db3b-121">Description</span></span>    | <span data-ttu-id="7db3b-122">Nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="7db3b-122">The user name.</span></span> <span data-ttu-id="7db3b-123">Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="7db3b-123">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="7db3b-124">Access</span><span class="sxs-lookup"><span data-stu-id="7db3b-124">Access</span></span>         | <span data-ttu-id="7db3b-125">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="7db3b-125">WriteOnce</span></span>                                                                                                                                                                             |
| <span data-ttu-id="7db3b-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="7db3b-126">Type</span></span>           | <span data-ttu-id="7db3b-127">String</span><span class="sxs-lookup"><span data-stu-id="7db3b-127">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="7db3b-128">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="7db3b-128">Default</span></span>        | <span data-ttu-id="7db3b-129">"Nuevo usuario"</span><span class="sxs-lookup"><span data-stu-id="7db3b-129">"New User"</span></span>                                                                                                                                                                            |
| <span data-ttu-id="7db3b-130">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7db3b-130">Minimum system</span></span> | <span data-ttu-id="7db3b-131">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7db3b-131">Windows 2000</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="7db3b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="7db3b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7db3b-133">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="7db3b-133">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
