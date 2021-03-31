---
description: Instrucciones para usar la API de administrador de autorización para crear un almacén de directivas de autorización en el script.
ms.assetid: bd9a995a-4195-4da4-a194-472448a0cb08
title: Creación de un almacén de directivas de autorización en un script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0cb35e8e998f95e99193d1dc5e8a74838b7efc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155501"
---
# <a name="creating-an-authorization-policy-store-in-script"></a><span data-ttu-id="8abf9-103">Creación de un almacén de directivas de autorización en un script</span><span class="sxs-lookup"><span data-stu-id="8abf9-103">Creating an Authorization Policy Store in Script</span></span>

<span data-ttu-id="8abf9-104">Cree una directiva de autorización antes o durante la instalación de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8abf9-104">Create an authorization policy before or during the installation of an application.</span></span>

<span data-ttu-id="8abf9-105">Cuando use la API de administrador de autorización para crear una directiva de autorización, siga las instrucciones que se proporcionan en los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="8abf9-105">When you use the Authorization Manager API to create an authorization policy, follow the instructions provided in the following topics.</span></span>



| <span data-ttu-id="8abf9-106">Tema</span><span class="sxs-lookup"><span data-stu-id="8abf9-106">Topic</span></span>                                                                                                                  | <span data-ttu-id="8abf9-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8abf9-107">Description</span></span>                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8abf9-108">Crear un objeto de almacén de directivas de autorización en el script</span><span class="sxs-lookup"><span data-stu-id="8abf9-108">Creating an Authorization Policy Store Object in Script</span></span>](creating-an-authorization-policy-store-object-in-script.md) | <span data-ttu-id="8abf9-109">Un almacén de directivas de autorización contiene información sobre la Directiva de seguridad de una aplicación o grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8abf9-109">An authorization policy store contains information about the security policy of an application or group of applications.</span></span>                                                                                                                                       |
| [<span data-ttu-id="8abf9-110">Crear un objeto de aplicación en el script</span><span class="sxs-lookup"><span data-stu-id="8abf9-110">Creating an Application Object in Script</span></span>](creating-an-application-object-in-script.md)                               | <span data-ttu-id="8abf9-111">Para cada aplicación que usa un almacén de directivas de autorización, debe crear un objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) y guardarlo en un almacén de directivas.</span><span class="sxs-lookup"><span data-stu-id="8abf9-111">For each application that uses an authorization policy store, you must create an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object and save it to a policy store.</span></span>                                                                                                |
| [<span data-ttu-id="8abf9-112">Definir operaciones en el script</span><span class="sxs-lookup"><span data-stu-id="8abf9-112">Defining Operations in Script</span></span>](defining-operations-in-script.md)                                                     | <span data-ttu-id="8abf9-113">Una operación es una función o un método de bajo nivel de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8abf9-113">An operation is a low-level function or method of an application.</span></span>                                                                                                                                                                                              |
| [<span data-ttu-id="8abf9-114">Agrupar operaciones en tareas en script</span><span class="sxs-lookup"><span data-stu-id="8abf9-114">Grouping Operations into Tasks in Script</span></span>](grouping-operations-into-tasks-in-script.md)                               | <span data-ttu-id="8abf9-115">Una tarea es una acción de alto nivel que los usuarios de una aplicación deben completar.</span><span class="sxs-lookup"><span data-stu-id="8abf9-115">A task is a high-level action that users of an application need to complete.</span></span> <span data-ttu-id="8abf9-116">Las tareas se componen de operaciones, que son funciones de bajo nivel y métodos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8abf9-116">Tasks are made up of operations, which are low-level functions and methods of the application.</span></span>                                                                                    |
| [<span data-ttu-id="8abf9-117">Agrupar tareas en roles en el script</span><span class="sxs-lookup"><span data-stu-id="8abf9-117">Grouping Tasks into Roles in Script</span></span>](grouping-tasks-into-roles-in-script.md)                                         | <span data-ttu-id="8abf9-118">Un rol representa una categoría de usuarios y las tareas que pueden realizar los usuarios.</span><span class="sxs-lookup"><span data-stu-id="8abf9-118">A role represents a category of users and the tasks those users are authorized to perform.</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="8abf9-119">Definir grupos de usuarios en el script</span><span class="sxs-lookup"><span data-stu-id="8abf9-119">Defining Groups of Users in Script</span></span>](defining-groups-of-users-in-script.md)                                           | <span data-ttu-id="8abf9-120">Un objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) representa un grupo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="8abf9-120">An [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="8abf9-121">Los roles se pueden asignar a este grupo de usuarios colectivamente.</span><span class="sxs-lookup"><span data-stu-id="8abf9-121">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="8abf9-122">Un objeto **IAzApplicationGroup** también puede incluir otros objetos **IAzApplicationGroup** como miembros.</span><span class="sxs-lookup"><span data-stu-id="8abf9-122">An **IAzApplicationGroup** object can also include other **IAzApplicationGroup** objects as members.</span></span> |
| [<span data-ttu-id="8abf9-123">Agregar usuarios a un grupo de aplicaciones en el script</span><span class="sxs-lookup"><span data-stu-id="8abf9-123">Adding Users to an Application Group in Script</span></span>](adding-users-to-an-application-group-in-script.md)                   | <span data-ttu-id="8abf9-124">Un grupo de aplicación es un grupo de usuarios y grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="8abf9-124">An application group is a group of users and user groups.</span></span> <span data-ttu-id="8abf9-125">Un grupo de aplicaciones puede contener otros grupos de aplicaciones, por lo que se pueden anidar grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="8abf9-125">An application group can contain other application groups, so groups of users can be nested.</span></span> <span data-ttu-id="8abf9-126">Un grupo de aplicación se representa mediante un objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .</span><span class="sxs-lookup"><span data-stu-id="8abf9-126">An application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span>    |



 

 

 



