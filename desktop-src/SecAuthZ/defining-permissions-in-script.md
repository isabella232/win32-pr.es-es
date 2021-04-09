---
description: Instrucciones para usar la API de administrador de autorización para definir permisos en el script mediante la creación de un almacén de directivas de autorización.
ms.assetid: 114426e8-03a7-41e2-96c9-e2da91aa7d84
title: Definir permisos en el script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e16f377ffa669da0b686ac28783e9a370efec94d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002542"
---
# <a name="defining-permissions-in-script"></a><span data-ttu-id="08a65-103">Definir permisos en el script</span><span class="sxs-lookup"><span data-stu-id="08a65-103">Defining Permissions in Script</span></span>

<span data-ttu-id="08a65-104">En Administrador de autorización, puede definir qué usuarios tienen acceso a los recursos de la aplicación mediante la creación de un almacén de directivas de autorización.</span><span class="sxs-lookup"><span data-stu-id="08a65-104">In Authorization Manager, you define which users have access to which application resources by creating an authorization policy store.</span></span>

<span data-ttu-id="08a65-105">**Para definir los permisos de acceso**</span><span class="sxs-lookup"><span data-stu-id="08a65-105">**To define access permissions**</span></span>

1.  <span data-ttu-id="08a65-106">Cree el almacén en el que se define la Directiva de autorización:</span><span class="sxs-lookup"><span data-stu-id="08a65-106">Create the store where the authorization policy is defined:</span></span><dl>

[<span data-ttu-id="08a65-107">Creación de un almacén de directivas de autorización en un script</span><span class="sxs-lookup"><span data-stu-id="08a65-107">Creating an Authorization Policy Store in Script</span></span>](creating-an-authorization-policy-store-object-in-script.md)  
    </dl>
2.  <span data-ttu-id="08a65-108">Cree una sección en el almacén de directivas de autorización para una aplicación específica:</span><span class="sxs-lookup"><span data-stu-id="08a65-108">Create a section in the authorization policy store for a specific application:</span></span><dl>

[<span data-ttu-id="08a65-109">Crear un objeto de aplicación en el script</span><span class="sxs-lookup"><span data-stu-id="08a65-109">Creating an Application Object in Script</span></span>](creating-an-application-object-in-script.md)  
    </dl>
3.  <span data-ttu-id="08a65-110">Defina las operaciones que implementa la aplicación para obtener acceso a los recursos y modificarlos:</span><span class="sxs-lookup"><span data-stu-id="08a65-110">Define operations that the application implements to access and modify resources:</span></span><dl>

[<span data-ttu-id="08a65-111">Definir operaciones en el script</span><span class="sxs-lookup"><span data-stu-id="08a65-111">Defining Operations in Script</span></span>](defining-operations-in-script.md)  
    </dl>
4.  <span data-ttu-id="08a65-112">Agrupe las operaciones en tareas de alto nivel que los usuarios quieran realizar:</span><span class="sxs-lookup"><span data-stu-id="08a65-112">Group operations into high-level tasks that users want to perform:</span></span><dl>

[<span data-ttu-id="08a65-113">Agrupar operaciones en tareas en script</span><span class="sxs-lookup"><span data-stu-id="08a65-113">Grouping Operations into Tasks in Script</span></span>](grouping-operations-into-tasks-in-script.md)  
    </dl>
5.  <span data-ttu-id="08a65-114">Definir roles que se componen de grupos de tareas:</span><span class="sxs-lookup"><span data-stu-id="08a65-114">Define roles that consist of groups of tasks:</span></span><dl>

[<span data-ttu-id="08a65-115">Agrupar tareas en roles en el script</span><span class="sxs-lookup"><span data-stu-id="08a65-115">Grouping Tasks into Roles in Script</span></span>](grouping-tasks-into-roles-in-script.md)  
    </dl><span data-ttu-id="08a65-116">Un usuario que se asigna a un rol tiene permiso para realizar cualquier tarea asignada a ese rol.</span><span class="sxs-lookup"><span data-stu-id="08a65-116">A user that is assigned to a role has permission to perform any task assigned to that role.</span></span>
6.  <span data-ttu-id="08a65-117">Cree scripts para calificar el acceso a las tareas en tiempo de ejecución:</span><span class="sxs-lookup"><span data-stu-id="08a65-117">Create scripts to qualify access to tasks at run time:</span></span><dl>

[<span data-ttu-id="08a65-118">Acceso de calificación con lógica de negocios en script</span><span class="sxs-lookup"><span data-stu-id="08a65-118">Qualifying Access with Business Logic in Script</span></span>](qualifying-access-with-business-logic-in-script.md)  
    </dl><span data-ttu-id="08a65-119">Este paso es opcional.</span><span class="sxs-lookup"><span data-stu-id="08a65-119">This step is optional.</span></span>
7.  <span data-ttu-id="08a65-120">Definir grupos de usuarios:</span><span class="sxs-lookup"><span data-stu-id="08a65-120">Define groups of users:</span></span><dl>

[<span data-ttu-id="08a65-121">Definir grupos de usuarios en el script</span><span class="sxs-lookup"><span data-stu-id="08a65-121">Defining Groups of Users in Script</span></span>](defining-groups-of-users-in-script.md)  
    </dl><span data-ttu-id="08a65-122">Estos grupos se pueden asignar a los roles para determinar qué tareas pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="08a65-122">These groups can then be assigned to roles to determine which tasks they can perform.</span></span>
8.  <span data-ttu-id="08a65-123">Agregar usuarios a grupos de usuarios:</span><span class="sxs-lookup"><span data-stu-id="08a65-123">Add users to user groups:</span></span><dl>

[<span data-ttu-id="08a65-124">Agregar usuarios a un grupo de aplicaciones en el script</span><span class="sxs-lookup"><span data-stu-id="08a65-124">Adding Users to an Application Group in Script</span></span>](adding-users-to-an-application-group-in-script.md)  
    </dl>

 

 



