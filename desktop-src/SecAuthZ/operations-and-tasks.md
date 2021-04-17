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
# <a name="operations-and-tasks"></a><span data-ttu-id="bd17c-103">Operaciones y tareas</span><span class="sxs-lookup"><span data-stu-id="bd17c-103">Operations and Tasks</span></span>

<span data-ttu-id="bd17c-104">Una operación es una acción de equipo de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="bd17c-104">An operation is a low-level computer action.</span></span> <span data-ttu-id="bd17c-105">En la API de administrador de autorización, una operación se representa mediante un objeto [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) .</span><span class="sxs-lookup"><span data-stu-id="bd17c-105">In the Authorization Manager API, an operation is represented by an [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) object.</span></span> <span data-ttu-id="bd17c-106">En general, las operaciones son demasiado numerosas en número y demasiado bajo para facilitar la administración.</span><span class="sxs-lookup"><span data-stu-id="bd17c-106">In general, operations are too many in number and too low-level to facilitate administration.</span></span> <span data-ttu-id="bd17c-107">Agrupe las operaciones en tareas para simplificar la administración de la Directiva de autorización.</span><span class="sxs-lookup"><span data-stu-id="bd17c-107">Group operations into tasks to simplify administration of authorization policy.</span></span>

<span data-ttu-id="bd17c-108">Una tarea se representa mediante un objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) y puede contener uno o más objetos [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) .</span><span class="sxs-lookup"><span data-stu-id="bd17c-108">A task is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object and can contain one or more [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) objects.</span></span> <span data-ttu-id="bd17c-109">Un objeto **IAzTask** también puede contener otros objetos **IAzTask** , por lo que las tareas se pueden anidar.</span><span class="sxs-lookup"><span data-stu-id="bd17c-109">An **IAzTask** object can also contain other **IAzTask** objects, so that tasks can be nested.</span></span> <span data-ttu-id="bd17c-110">Para facilitar la administración, un objeto **IAzTask** debe representar una tarea que un usuario real desea realizar.</span><span class="sxs-lookup"><span data-stu-id="bd17c-110">To facilitate administration, an **IAzTask** object should represent a task that a real user wants to perform.</span></span>

<span data-ttu-id="bd17c-111">El acceso a las operaciones que contiene una tarea se puede calificar en tiempo de ejecución mediante un script de regla de negocios asociado al objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) que representa esa tarea.</span><span class="sxs-lookup"><span data-stu-id="bd17c-111">Access to the operations contained by a task can be qualified at run time by a business rule script associated with the [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object that represents that task.</span></span> <span data-ttu-id="bd17c-112">Para obtener más información sobre los scripts de reglas de negocios, vea [reglas de negocios](business-rules.md).</span><span class="sxs-lookup"><span data-stu-id="bd17c-112">For more information about business rule scripts, see [Business Rules](business-rules.md).</span></span>

<span data-ttu-id="bd17c-113">Un objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) también puede representar una definición de rol estableciendo su propiedad [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) en **true**.</span><span class="sxs-lookup"><span data-stu-id="bd17c-113">An [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object can also represent a role definition by setting its [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property to **TRUE**.</span></span> <span data-ttu-id="bd17c-114">A continuación, la interfaz de usuario del complemento MMC de **Administrador de autorización** muestra el objeto **IAzTask** como un rol.</span><span class="sxs-lookup"><span data-stu-id="bd17c-114">The **Authorization Manager** MMC snap-in user interface then displays that **IAzTask** object as a role.</span></span> <span data-ttu-id="bd17c-115">Para obtener más información sobre las definiciones de roles, vea [roles](roles.md).</span><span class="sxs-lookup"><span data-stu-id="bd17c-115">For more information about role definitions, see [Roles](roles.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd17c-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bd17c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd17c-117">Definir operaciones en C++</span><span class="sxs-lookup"><span data-stu-id="bd17c-117">Defining Operations in C++</span></span>](defining-operations-in-c--.md)
</dt> <dt>

[<span data-ttu-id="bd17c-118">Agrupar operaciones en tareas en C++</span><span class="sxs-lookup"><span data-stu-id="bd17c-118">Grouping Operations into Tasks in C++</span></span>](grouping-operations-into-tasks-in-c--.md)
</dt> <dt>

[<span data-ttu-id="bd17c-119">Agrupar tareas en roles en C++</span><span class="sxs-lookup"><span data-stu-id="bd17c-119">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[<span data-ttu-id="bd17c-120">Usuarios y grupos</span><span class="sxs-lookup"><span data-stu-id="bd17c-120">Users and Groups</span></span>](users-and-groups.md)
</dt> </dl>

 

 



