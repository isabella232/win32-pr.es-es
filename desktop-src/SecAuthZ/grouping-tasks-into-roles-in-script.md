---
description: En el Administrador de autorización, un rol representa una categoría de usuarios y las tareas que dichos usuarios están autorizados a realizar.
ms.assetid: a4981774-0f5c-4032-8a7d-d9ef44c76abe
title: Agrupación de tareas en roles en script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c84ec45bba8da9d76e2a4fe0b31324429374a74b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361845"
---
# <a name="grouping-tasks-into-roles-in-script"></a>Agrupación de tareas en roles en script

En el Administrador de autorización, un rol representa una categoría de usuarios y las tareas que dichos usuarios están autorizados a realizar. Las tareas se agrupan y se asignan a una definición de rol, que se representa mediante un objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) con su [**propiedad IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) establecida en **True.** A continuación, la definición de rol se puede asignar a un objeto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) y, a continuación, los usuarios o grupos de usuarios se asignan a ese objeto. Para obtener más información sobre tareas y roles, vea [Roles](roles.md).

En el ejemplo siguiente se muestra cómo asignar tareas a una definición de rol, crear un objeto de rol y asignar la definición de rol al objeto de rol. En el ejemplo se supone que hay un almacén de directivas XML existente denominado MyStore.xml en el directorio raíz de la unidad C, que este almacén contiene una aplicación denominada Expense y que esta aplicación contiene tareas denominadas Submit Expense y Approve Expense.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp = AzManStore.OpenApplication("Expense")

'  Create a task object to act as a role definition.
Dim roleTask
Set roleTask = expenseApp.CreateTask("Expense Admin")

'  Set the IsRoleDefinition property of roleTask to True.
roleTask.IsRoleDefinition = True

'  Add two tasks to the role definition.
roleTask.AddTask CStr("Submit Expense")
roleTask.AddTask CStr("Approve Expense")

'  Save the role definition to the store.
roleTask.Submit

'  Create a role object.
Dim role1
Set role1 = expenseApp.CreateRole("Expense Administrator")

'  Add the role definition to the role object.
role1.AddTask(roleTask.Name)

'  Save the role object to the store.
role1.Submit
```



 

 



