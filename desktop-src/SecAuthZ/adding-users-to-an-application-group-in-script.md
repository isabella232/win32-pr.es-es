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
# <a name="adding-users-to-an-application-group-in-script"></a>Agregar usuarios a un grupo de aplicaciones en el script

En el administrador de autorización, un grupo de aplicaciones es un grupo de usuarios y grupos de usuarios. Un grupo de aplicaciones puede contener otros grupos de aplicaciones, por lo que se pueden anidar grupos de usuarios. Un grupo de aplicación se representa mediante un objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .

**Para permitir que los miembros de un grupo de aplicaciones realicen una tarea o un conjunto de tareas**

-   Asigne ese grupo de aplicaciones a un rol que contenga esas tareas.

    Los roles se representan mediante objetos [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) .

En el ejemplo siguiente se muestra cómo crear un grupo de aplicaciones, agregar un usuario como miembro del grupo de aplicaciones y asignar el grupo de aplicaciones a un rol existente. En el ejemplo se da por supuesto que hay un almacén de directivas XML denominado MyStore.xml en el directorio raíz de la unidad C, que este almacén contiene una aplicación denominada///Expense y que esta aplicación contiene un rol denominado administrador de gastos.


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



 

 



