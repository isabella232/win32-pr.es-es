---
description: En Administrador de autorización, una tarea es una acción de alto nivel que los usuarios de una aplicación deben completar.
ms.assetid: a266dde7-86f8-4537-99a5-be7142e765c6
title: Agrupar operaciones en tareas en script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fb7fc1d4a84cd42dc0ae48af4fcbf02412b93337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912449"
---
# <a name="grouping-operations-into-tasks-in-script"></a>Agrupar operaciones en tareas en script

En Administrador de autorización, una tarea es una acción de alto nivel que los usuarios de una aplicación deben completar. Las tareas se componen de operaciones, que son funciones de bajo nivel y métodos de la aplicación. A continuación, se asigna una tarea a esos roles que deben realizar esa tarea. Una tarea se representa mediante un objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) . Para obtener más información acerca de las operaciones y las tareas, consulte [operaciones y tareas](operations-and-tasks.md).

En el ejemplo siguiente se muestra cómo agrupar operaciones para crear una tarea. En el ejemplo se da por supuesto que hay un almacén de directivas XML denominado MyStore.xml en el directorio raíz de la unidad C, que este almacén contiene una aplicación denominada///Expense y que esta aplicación contiene operaciones definidas en el tema [definir operaciones en el script](defining-operations-in-script.md).


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create a task object.
Dim Task1
Set Task1 = expenseApp.CreateTask("Submit Expense")

'  Add operations to the task.
Task1.AddOperation CStr("RetrieveForm")
Task1.AddOperation CStr("EnqueRequest")
Task1.AddOperation Cstr("UseFormControl")

'  Save the task to the store.
Task1.Submit
```



 

 



