---
description: Un grupo de aplicación es un grupo de usuarios y grupos de usuarios. Un grupo de aplicaciones puede contener otros grupos de aplicaciones, por lo que se pueden anidar grupos de usuarios. Un grupo de aplicación se representa mediante un objeto IAzApplicationGroup.
ms.assetid: 9ec5b55e-3d66-44f6-9b59-a5e66192d8ac
title: Agregar usuarios a un grupo de aplicaciones en el script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6fd92a69a236e6b4d04d5bb0a1a8b961c699d434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652903"
---
# <a name="adding-users-to-an-application-group-in-script"></a><span data-ttu-id="a7b75-105">Agregar usuarios a un grupo de aplicaciones en el script</span><span class="sxs-lookup"><span data-stu-id="a7b75-105">Adding Users to an Application Group in Script</span></span>

<span data-ttu-id="a7b75-106">En el administrador de autorización, un grupo de aplicaciones es un grupo de usuarios y grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="a7b75-106">In Authorization Manager, an application group is a group of users and user groups.</span></span> <span data-ttu-id="a7b75-107">Un grupo de aplicaciones puede contener otros grupos de aplicaciones, por lo que se pueden anidar grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="a7b75-107">An application group can contain other application groups, so groups of users can be nested.</span></span> <span data-ttu-id="a7b75-108">Un grupo de aplicación se representa mediante un objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .</span><span class="sxs-lookup"><span data-stu-id="a7b75-108">An application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span>

<span data-ttu-id="a7b75-109">**Para permitir que los miembros de un grupo de aplicaciones realicen una tarea o un conjunto de tareas**</span><span class="sxs-lookup"><span data-stu-id="a7b75-109">**To allow members of an application group to perform a task or set of tasks**</span></span>

-   <span data-ttu-id="a7b75-110">Asigne ese grupo de aplicaciones a un rol que contenga esas tareas.</span><span class="sxs-lookup"><span data-stu-id="a7b75-110">Assign that application group to a role that contains those tasks.</span></span>

    <span data-ttu-id="a7b75-111">Los roles se representan mediante objetos [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) .</span><span class="sxs-lookup"><span data-stu-id="a7b75-111">Roles are represented by [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) objects.</span></span>

<span data-ttu-id="a7b75-112">En el ejemplo siguiente se muestra cómo crear un grupo de aplicaciones, agregar un usuario como miembro del grupo de aplicaciones y asignar el grupo de aplicaciones a un rol existente.</span><span class="sxs-lookup"><span data-stu-id="a7b75-112">The following example shows how to create an application group, add a user as a member of the application group, and assign the application group to an existing role.</span></span> <span data-ttu-id="a7b75-113">En el ejemplo se da por supuesto que hay un almacén de directivas XML denominado MyStore.xml en el directorio raíz de la unidad C, que este almacén contiene una aplicación denominada///Expense y que esta aplicación contiene un rol denominado administrador de gastos.</span><span class="sxs-lookup"><span data-stu-id="a7b75-113">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains a role named Expense Administrator.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("Approvers")

'  Add a member to the group.
'  Replace with valid domain and user name.
appGroup.AddMemberName("domain\\username")

'  Save information to the store.
appGroup.Submit

'  Open a role object.
Dim adminRole
Set adminRole = expenseApp.OpenRole("Expense Administrator")

'  Add the group to the role.
adminRole.AddAppMember("Approvers")

'  Save the information to the store.
adminRole.Submit
```



 

 



