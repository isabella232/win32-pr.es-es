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
# <a name="roles"></a>Roles

Los roles tienen dos propósitos diferentes en el administrador de autorización. Un rol es un conjunto de tareas u operaciones a las que una categoría de usuarios requiere acceso, y también es un conjunto de usuarios y grupos que se ajustan a esa categoría.

-   [Roles como conjuntos de tareas](#roles-as-sets-of-tasks)
-   [Roles como conjuntos de usuarios y grupos](#roles-as-sets-of-users-and-groups)
-   [Temas relacionados](#related-topics)

## <a name="roles-as-sets-of-tasks"></a>Roles como conjuntos de tareas

Una directiva de autorización asigna objetos [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) a un objeto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) para crear conjuntos de tareas. Todos los usuarios y grupos asignados a ese objeto **IAzRole** tienen permiso para tener acceso a todas las operaciones que contienen esos objetos **IAzTask** .

Dado que un objeto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) representa un conjunto de tareas y un conjunto de usuarios y grupos que tienen acceso a esas tareas, el administrador de autorización proporciona una manera de crear definiciones de roles que se pueden asignar a más de un objeto **IAzRole** . Un objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) puede contener otros objetos **IAzTask** . Después, puede usar ese objeto **IAzTask** como una definición de rol asignándole uno o varios objetos **IAzRole** . Establezca la propiedad [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) del objeto **IAzTask** en **true** para que la interfaz de usuario del complemento MMC del **Administrador de autorización** muestre el objeto **IAzTask** como un rol.

## <a name="roles-as-sets-of-users-and-groups"></a>Roles como conjuntos de usuarios y grupos

Asigne usuarios y grupos a un objeto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) para conceder a esos usuarios y grupos acceso a las tareas asignadas a ese objeto **IAzRole** llamando al método [**AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) o [**AddMemberName**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) . Asigne los grupos de aplicaciones existentes, representados por objetos [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) , a un objeto **IAzRole** llamando al método [**AddAppMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) . Todos los usuarios y grupos asignados al objeto **IAzRole** tienen acceso a las tareas y operaciones asignadas a ese rol. Para obtener más información acerca de los grupos de aplicaciones, consulte [usuarios y grupos](users-and-groups.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Agrupar tareas en roles en C++](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[Definir grupos de usuarios en C++](defining-groups-of-users-in-c--.md)
</dt> <dt>

[Agregar usuarios a un grupo de aplicaciones en C++](adding-users-to-an-application-group-in-c--.md)
</dt> </dl>

 

 



