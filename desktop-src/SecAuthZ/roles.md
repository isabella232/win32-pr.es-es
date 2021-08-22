---
description: Los roles sirven para dos propósitos diferentes en el Administrador de autorización.
ms.assetid: 6d045ecb-432e-4ba6-b5d2-37db82ab1884
title: Roles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f884475589bc8ecef945c1fd89d1ffab647258c01d3c83a2c9b96df53300501d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911969"
---
# <a name="roles"></a>Roles

Los roles sirven para dos propósitos diferentes en el Administrador de autorización. Un rol es un conjunto de tareas u operaciones a las que una categoría de usuarios requiere acceso y también es un conjunto de usuarios y grupos que caben en esa categoría.

-   [Roles como conjuntos de tareas](#roles-as-sets-of-tasks)
-   [Roles como conjuntos de usuarios y grupos](#roles-as-sets-of-users-and-groups)
-   [Temas relacionados](#related-topics)

## <a name="roles-as-sets-of-tasks"></a>Roles como conjuntos de tareas

Una directiva de autorización asigna [**objetos IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) a un [**objeto IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) para crear conjuntos de tareas. Todos los usuarios y grupos asignados a ese objeto **IAzRole** tienen permiso para acceder a todas las operaciones contenidas en esos **objetos IAzTask.**

Dado que un objeto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) representa un conjunto de tareas y un conjunto de usuarios y grupos que tienen acceso a esas tareas, el Administrador de autorización proporciona una manera de crear definiciones de roles que se pueden asignar a más de un objeto **IAzRole.** Un [**objeto IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) puede contener otros **objetos IAzTask.** A continuación, puede usar ese **objeto IAzTask** como una definición de rol si lo asigna a uno o varios **objetos IAzRole.** Establezca la [**propiedad IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) del objeto **IAzTask** en **TRUE** para que la interfaz de usuario del complemento **MMC** del Administrador de autorización muestre el objeto **IAzTask** como un rol.

## <a name="roles-as-sets-of-users-and-groups"></a>Roles como conjuntos de usuarios y grupos

Asigne usuarios y grupos a un objeto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) para conceder a esos usuarios y grupos acceso a las tareas asignadas a ese objeto **IAzRole** mediante una llamada al [**método AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) [**o AddMemberName.**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) Asigne grupos de aplicaciones existentes, representados por objetos [**IAzApplicationGroup,**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) a un **objeto IAzRole** mediante una llamada [**al método AddAppMember.**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) Todos los usuarios y grupos asignados al **objeto IAzRole** tienen acceso a las tareas y operaciones asignadas a ese rol. Para obtener más información sobre los grupos de aplicaciones, [vea Usuarios y grupos.](users-and-groups.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Agrupación de tareas en roles en C++](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[Definir grupos de usuarios en C++](defining-groups-of-users-in-c--.md)
</dt> <dt>

[Agregar usuarios a un grupo de aplicaciones en C++](adding-users-to-an-application-group-in-c--.md)
</dt> </dl>

 

 



