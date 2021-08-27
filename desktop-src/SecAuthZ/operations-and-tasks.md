---
description: Una operación es una acción de equipo de bajo nivel.
ms.assetid: d75bc507-3502-417c-af05-cbff807a5778
title: Operaciones y tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8e60923e9631e37087a28a6a19747dc63249ff2f1ae8224c20e859e1f13c25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912416"
---
# <a name="operations-and-tasks"></a>Operaciones y tareas

Una operación es una acción de equipo de bajo nivel. En la API de Authorization Manager, una operación se representa mediante un [**objeto IAzOperation.**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) En general, las operaciones son demasiadas en número y de nivel demasiado bajo para facilitar la administración. Agrupa las operaciones en tareas para simplificar la administración de la directiva de autorización.

Una tarea se representa mediante un [**objeto IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) y puede contener uno o varios [**objetos IAzOperation.**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) Un **objeto IAzTask** también puede contener otros **objetos IAzTask,** por lo que las tareas se pueden anidar. Para facilitar la administración, un **objeto IAzTask** debe representar una tarea que un usuario real desea realizar.

El acceso a las operaciones contenidas en una tarea se puede calificar en tiempo de ejecución mediante un script de regla de negocios asociado al objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) que representa esa tarea. Para obtener más información sobre los scripts de reglas de negocios, [vea Business Rules](business-rules.md).

Un [**objeto IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) también puede representar una definición de rol estableciendo su [**propiedad IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) en **TRUE.** A **continuación,** la interfaz de usuario del complemento MMC del Administrador de autorización muestra ese **objeto IAzTask** como un rol. Para obtener más información sobre las definiciones de roles, vea [Roles](roles.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Definir operaciones en C++](defining-operations-in-c--.md)
</dt> <dt>

[Agrupación de operaciones en tareas en C++](grouping-operations-into-tasks-in-c--.md)
</dt> <dt>

[Agrupación de tareas en roles en C++](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[Usuarios y grupos](users-and-groups.md)
</dt> </dl>

 

 



