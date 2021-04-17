---
description: Una operación es una acción de equipo de bajo nivel.
ms.assetid: d75bc507-3502-417c-af05-cbff807a5778
title: Operaciones y tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a198d8844a9f34030b8b6a40eba759eed4057119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667920"
---
# <a name="operations-and-tasks"></a>Operaciones y tareas

Una operación es una acción de equipo de bajo nivel. En la API de administrador de autorización, una operación se representa mediante un objeto [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) . En general, las operaciones son demasiado numerosas en número y demasiado bajo para facilitar la administración. Agrupe las operaciones en tareas para simplificar la administración de la Directiva de autorización.

Una tarea se representa mediante un objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) y puede contener uno o más objetos [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) . Un objeto **IAzTask** también puede contener otros objetos **IAzTask** , por lo que las tareas se pueden anidar. Para facilitar la administración, un objeto **IAzTask** debe representar una tarea que un usuario real desea realizar.

El acceso a las operaciones que contiene una tarea se puede calificar en tiempo de ejecución mediante un script de regla de negocios asociado al objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) que representa esa tarea. Para obtener más información sobre los scripts de reglas de negocios, vea [reglas de negocios](business-rules.md).

Un objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) también puede representar una definición de rol estableciendo su propiedad [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) en **true**. A continuación, la interfaz de usuario del complemento MMC de **Administrador de autorización** muestra el objeto **IAzTask** como un rol. Para obtener más información sobre las definiciones de roles, vea [roles](roles.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Definir operaciones en C++](defining-operations-in-c--.md)
</dt> <dt>

[Agrupar operaciones en tareas en C++](grouping-operations-into-tasks-in-c--.md)
</dt> <dt>

[Agrupar tareas en roles en C++](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[Usuarios y grupos](users-and-groups.md)
</dt> </dl>

 

 



