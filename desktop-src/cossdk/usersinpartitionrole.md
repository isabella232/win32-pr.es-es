---
description: Contiene un objeto para cada usuario en el rol con el que está relacionada la colección.
ms.assetid: c6aebf7a-04d1-4c7c-a015-bc6fb4841c4a
title: Colección UsersInPartitionRole
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInPartitionRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: fce1577636a7b2e678bdade9c32f706c7ccbf158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153191"
---
# <a name="usersinpartitionrole-collection"></a><span data-ttu-id="8a8cf-103">Colección UsersInPartitionRole</span><span class="sxs-lookup"><span data-stu-id="8a8cf-103">UsersInPartitionRole collection</span></span>

<span data-ttu-id="8a8cf-104">Contiene un objeto para cada usuario en el rol con el que está relacionada la colección.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-104">Contains an object for each user in the role to which the collection is related.</span></span>

<span data-ttu-id="8a8cf-105">Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="8a8cf-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="8a8cf-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="8a8cf-106">Members</span></span>

<span data-ttu-id="8a8cf-107">La colección **UsersInPartitionRole** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-107">The **UsersInPartitionRole** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="8a8cf-108">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="8a8cf-108">Related Collections</span></span>

<span data-ttu-id="8a8cf-109">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="8a8cf-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="8a8cf-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="8a8cf-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="8a8cf-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="8a8cf-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="8a8cf-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="8a8cf-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="8a8cf-113">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="8a8cf-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="8a8cf-114">**RolesForPartition**</span><span class="sxs-lookup"><span data-stu-id="8a8cf-114">**RolesForPartition**</span></span>](rolesforpartition.md)

## <a name="properties"></a><span data-ttu-id="8a8cf-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8a8cf-115">Properties</span></span>

<span data-ttu-id="8a8cf-116">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="8a8cf-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="8a8cf-117">User</span><span class="sxs-lookup"><span data-stu-id="8a8cf-117">User</span></span>](#usersinpartitionrole-collection)

### <a name="user"></a><span data-ttu-id="8a8cf-118">User (Usuario)</span><span class="sxs-lookup"><span data-stu-id="8a8cf-118">User</span></span>



| <span data-ttu-id="8a8cf-119">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a8cf-119">Entry</span></span> | <span data-ttu-id="8a8cf-120">Value</span><span class="sxs-lookup"><span data-stu-id="8a8cf-120">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a8cf-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a8cf-121">Description</span></span>    | <span data-ttu-id="8a8cf-122">Nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-122">The user name.</span></span> <span data-ttu-id="8a8cf-123">Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-123">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="8a8cf-124">Access</span><span class="sxs-lookup"><span data-stu-id="8a8cf-124">Access</span></span>         | <span data-ttu-id="8a8cf-125">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="8a8cf-125">WriteOnce</span></span>                                                                                                                                                                             |
| <span data-ttu-id="8a8cf-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="8a8cf-126">Type</span></span>           | <span data-ttu-id="8a8cf-127">String</span><span class="sxs-lookup"><span data-stu-id="8a8cf-127">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="8a8cf-128">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="8a8cf-128">Default</span></span>        | <span data-ttu-id="8a8cf-129">"Nuevo usuario"</span><span class="sxs-lookup"><span data-stu-id="8a8cf-129">"New User"</span></span>                                                                                                                                                                            |
| <span data-ttu-id="8a8cf-130">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="8a8cf-130">Minimum system</span></span> | <span data-ttu-id="8a8cf-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8a8cf-131">Windows Server 2003</span></span>                                                                                                                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="8a8cf-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a8cf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a8cf-133">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="8a8cf-133">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
