---
description: Instrucciones para usar la API de administrador de autorización para definir permisos en C++ mediante la creación de un almacén de directivas de autorización.
ms.assetid: 8a3bf625-7973-4905-a63c-e42e6682b7c2
title: Definir permisos en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc398d811f44b69dbde8d30f135fd4f30a552bbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653095"
---
# <a name="defining-permissions-in-c"></a><span data-ttu-id="4091d-103">Definir permisos en C++</span><span class="sxs-lookup"><span data-stu-id="4091d-103">Defining Permissions in C++</span></span>

<span data-ttu-id="4091d-104">En Administrador de autorización, puede definir qué usuarios tienen acceso a los recursos de la aplicación mediante la creación de un almacén de directivas de autorización.</span><span class="sxs-lookup"><span data-stu-id="4091d-104">In Authorization Manager, you define which users have access to which application resources by creating an authorization policy store.</span></span>

<span data-ttu-id="4091d-105">Para obtener información sobre cómo definir permisos con ACL, vea [definir permisos con ACL en C++](defining-permissions-with-acls-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="4091d-105">For information about defining permissions with ACLs, see [Defining Permissions with ACLs in C++](defining-permissions-with-acls-in-c--.md).</span></span>

<span data-ttu-id="4091d-106">**Para definir los permisos de acceso**</span><span class="sxs-lookup"><span data-stu-id="4091d-106">**To define access permissions**</span></span>

1.  <span data-ttu-id="4091d-107">Cree el almacén en el que se define la Directiva de autorización:</span><span class="sxs-lookup"><span data-stu-id="4091d-107">Create the store where the authorization policy is defined:</span></span><dl>

[<span data-ttu-id="4091d-108">Crear un objeto de almacén de directivas de autorización en C++</span><span class="sxs-lookup"><span data-stu-id="4091d-108">Creating an Authorization Policy Store Object in C++</span></span>](creating-an-authorization-policy-store-object-in-c--.md)  
    </dl>
2.  <span data-ttu-id="4091d-109">Cree una sección en el almacén de directivas de autorización para una aplicación específica:</span><span class="sxs-lookup"><span data-stu-id="4091d-109">Create a section in the authorization policy store for a specific application:</span></span><dl>

[<span data-ttu-id="4091d-110">Crear un objeto de aplicación en C++</span><span class="sxs-lookup"><span data-stu-id="4091d-110">Creating an Application Object in C++</span></span>](creating-an-application-object-in-c--.md)  
    </dl>
3.  <span data-ttu-id="4091d-111">Defina las operaciones que implementa la aplicación para obtener acceso a los recursos y modificarlos:</span><span class="sxs-lookup"><span data-stu-id="4091d-111">Define operations that the application implements to access and modify resources:</span></span><dl>

[<span data-ttu-id="4091d-112">Definir operaciones en C++</span><span class="sxs-lookup"><span data-stu-id="4091d-112">Defining Operations in C++</span></span>](defining-operations-in-c--.md)  
    </dl>
4.  <span data-ttu-id="4091d-113">Agrupe las operaciones en tareas de alto nivel que los usuarios quieran realizar:</span><span class="sxs-lookup"><span data-stu-id="4091d-113">Group operations into high-level tasks that users want to perform:</span></span><dl>

[<span data-ttu-id="4091d-114">Agrupar operaciones en tareas en C++</span><span class="sxs-lookup"><span data-stu-id="4091d-114">Grouping Operations into Tasks in C++</span></span>](grouping-operations-into-tasks-in-c--.md)  
    </dl>
5.  <span data-ttu-id="4091d-115">Definir roles que se componen de grupos de tareas:</span><span class="sxs-lookup"><span data-stu-id="4091d-115">Define roles that consist of groups of tasks:</span></span><dl>

[<span data-ttu-id="4091d-116">Agrupar tareas en roles en C++</span><span class="sxs-lookup"><span data-stu-id="4091d-116">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)  
    </dl><span data-ttu-id="4091d-117">Un usuario que se asigna a un rol tiene permiso para realizar cualquier tarea asignada a ese rol.</span><span class="sxs-lookup"><span data-stu-id="4091d-117">A user that is assigned to a role has permission to perform any task assigned to that role.</span></span>
6.  <span data-ttu-id="4091d-118">Cree scripts para calificar el acceso a las tareas en tiempo de ejecución:</span><span class="sxs-lookup"><span data-stu-id="4091d-118">Create scripts to qualify access to tasks at run time:</span></span><dl>

[<span data-ttu-id="4091d-119">Calificar el acceso con la lógica de negocios en C++</span><span class="sxs-lookup"><span data-stu-id="4091d-119">Qualifying Access with Business Logic in C++</span></span>](qualifying-access-with-business-logic-in-c--.md)  
    </dl><span data-ttu-id="4091d-120">Este paso es opcional.</span><span class="sxs-lookup"><span data-stu-id="4091d-120">This step is optional.</span></span>
7.  <span data-ttu-id="4091d-121">Definir grupos de usuarios:</span><span class="sxs-lookup"><span data-stu-id="4091d-121">Define groups of users:</span></span><dl>

[<span data-ttu-id="4091d-122">Definir grupos de usuarios en C++</span><span class="sxs-lookup"><span data-stu-id="4091d-122">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)  
    </dl><span data-ttu-id="4091d-123">Estos grupos se pueden asignar a los roles para determinar qué tareas pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="4091d-123">These groups can then be assigned to roles to determine which tasks they can perform.</span></span>
8.  <span data-ttu-id="4091d-124">Agregar usuarios a grupos de usuarios:</span><span class="sxs-lookup"><span data-stu-id="4091d-124">Add users to user groups:</span></span><dl>

[<span data-ttu-id="4091d-125">Agregar usuarios a un grupo de aplicaciones en C++</span><span class="sxs-lookup"><span data-stu-id="4091d-125">Adding Users to an Application Group in C++</span></span>](adding-users-to-an-application-group-in-c--.md)  
    </dl>

 

 



