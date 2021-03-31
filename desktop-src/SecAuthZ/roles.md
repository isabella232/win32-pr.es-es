---
description: Los roles tienen dos propósitos diferentes en el administrador de autorización.
ms.assetid: 6d045ecb-432e-4ba6-b5d2-37db82ab1884
title: Roles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65d140faa22c72d098c7a4ba2f13e952b2713f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908175"
---
# <a name="roles"></a><span data-ttu-id="8c4b5-103">Roles</span><span class="sxs-lookup"><span data-stu-id="8c4b5-103">Roles</span></span>

<span data-ttu-id="8c4b5-104">Los roles tienen dos propósitos diferentes en el administrador de autorización.</span><span class="sxs-lookup"><span data-stu-id="8c4b5-104">Roles serve two different purposes in Authorization Manager.</span></span> <span data-ttu-id="8c4b5-105">Un rol es un conjunto de tareas u operaciones a las que una categoría de usuarios requiere acceso, y también es un conjunto de usuarios y grupos que se ajustan a esa categoría.</span><span class="sxs-lookup"><span data-stu-id="8c4b5-105">A role is a set of tasks or operations to which a category of users requires access, and it is also a set of users and groups that fit into that category.</span></span>

-   [<span data-ttu-id="8c4b5-106">Roles como conjuntos de tareas</span><span class="sxs-lookup"><span data-stu-id="8c4b5-106">Roles as Sets of Tasks</span></span>](#roles-as-sets-of-tasks)
-   [<span data-ttu-id="8c4b5-107">Roles como conjuntos de usuarios y grupos</span><span class="sxs-lookup"><span data-stu-id="8c4b5-107">Roles as Sets of Users and Groups</span></span>](#roles-as-sets-of-users-and-groups)
-   [<span data-ttu-id="8c4b5-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c4b5-108">Related topics</span></span>](#related-topics)

## <a name="roles-as-sets-of-tasks"></a><span data-ttu-id="8c4b5-109">Roles como conjuntos de tareas</span><span class="sxs-lookup"><span data-stu-id="8c4b5-109">Roles as Sets of Tasks</span></span>

<span data-ttu-id="8c4b5-110">Una directiva de autorización asigna objetos [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) a un objeto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) para crear conjuntos de tareas.</span><span class="sxs-lookup"><span data-stu-id="8c4b5-110">An authorization policy assigns [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) objects to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object to create sets of tasks.</span></span> <span data-ttu-id="8c4b5-111">Todos los usuarios y grupos asignados a ese objeto **IAzRole** tienen permiso para tener acceso a todas las operaciones que contienen esos objetos **IAzTask** .</span><span class="sxs-lookup"><span data-stu-id="8c4b5-111">All users and groups assigned to that **IAzRole** object then have permission to access all operations contained by those **IAzTask** objects.</span></span>

<span data-ttu-id="8c4b5-112">Dado que un objeto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) representa un conjunto de tareas y un conjunto de usuarios y grupos que tienen acceso a esas tareas, el administrador de autorización proporciona una manera de crear definiciones de roles que se pueden asignar a más de un objeto **IAzRole** .</span><span class="sxs-lookup"><span data-stu-id="8c4b5-112">Because an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object represents both a set of tasks and a set of users and groups that have access to those tasks, Authorization Manager provides a way to create role definitions that can be assigned to more than one **IAzRole** object.</span></span> <span data-ttu-id="8c4b5-113">Un objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) puede contener otros objetos **IAzTask** .</span><span class="sxs-lookup"><span data-stu-id="8c4b5-113">An [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object can contain other **IAzTask** objects.</span></span> <span data-ttu-id="8c4b5-114">Después, puede usar ese objeto **IAzTask** como una definición de rol asignándole uno o varios objetos **IAzRole** .</span><span class="sxs-lookup"><span data-stu-id="8c4b5-114">You can then use that **IAzTask** object as a role definition by assigning it to one or more **IAzRole** objects.</span></span> <span data-ttu-id="8c4b5-115">Establezca la propiedad [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) del objeto **IAzTask** en **true** para que la interfaz de usuario del complemento MMC del **Administrador de autorización** muestre el objeto **IAzTask** como un rol.</span><span class="sxs-lookup"><span data-stu-id="8c4b5-115">Set the [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property of the **IAzTask** object to **TRUE** to cause the **Authorization Manager** MMC snap-in user interface to display the **IAzTask** object as a role.</span></span>

## <a name="roles-as-sets-of-users-and-groups"></a><span data-ttu-id="8c4b5-116">Roles como conjuntos de usuarios y grupos</span><span class="sxs-lookup"><span data-stu-id="8c4b5-116">Roles as Sets of Users and Groups</span></span>

<span data-ttu-id="8c4b5-117">Asigne usuarios y grupos a un objeto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) para conceder a esos usuarios y grupos acceso a las tareas asignadas a ese objeto **IAzRole** llamando al método [**AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) o [**AddMemberName**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) .</span><span class="sxs-lookup"><span data-stu-id="8c4b5-117">Assign users and groups to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object to grant those users and groups access to the tasks assigned to that **IAzRole** object by calling the [**AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) or [**AddMemberName**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) method.</span></span> <span data-ttu-id="8c4b5-118">Asigne los grupos de aplicaciones existentes, representados por objetos [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) , a un objeto **IAzRole** llamando al método [**AddAppMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) .</span><span class="sxs-lookup"><span data-stu-id="8c4b5-118">Assign existing application groups, represented by [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) objects, to an **IAzRole** object by calling the [**AddAppMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) method.</span></span> <span data-ttu-id="8c4b5-119">Todos los usuarios y grupos asignados al objeto **IAzRole** tienen acceso a las tareas y operaciones asignadas a ese rol.</span><span class="sxs-lookup"><span data-stu-id="8c4b5-119">All users and groups assigned to the **IAzRole** object have access to the tasks and operations assigned to that role.</span></span> <span data-ttu-id="8c4b5-120">Para obtener más información acerca de los grupos de aplicaciones, consulte [usuarios y grupos](users-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="8c4b5-120">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c4b5-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c4b5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c4b5-122">Agrupar tareas en roles en C++</span><span class="sxs-lookup"><span data-stu-id="8c4b5-122">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[<span data-ttu-id="8c4b5-123">Definir grupos de usuarios en C++</span><span class="sxs-lookup"><span data-stu-id="8c4b5-123">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)
</dt> <dt>

[<span data-ttu-id="8c4b5-124">Agregar usuarios a un grupo de aplicaciones en C++</span><span class="sxs-lookup"><span data-stu-id="8c4b5-124">Adding Users to an Application Group in C++</span></span>](adding-users-to-an-application-group-in-c--.md)
</dt> </dl>

 

 



