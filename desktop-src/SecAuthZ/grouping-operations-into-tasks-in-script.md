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
# <a name="grouping-operations-into-tasks-in-script"></a><span data-ttu-id="b30b3-103">Agrupar operaciones en tareas en script</span><span class="sxs-lookup"><span data-stu-id="b30b3-103">Grouping Operations into Tasks in Script</span></span>

<span data-ttu-id="b30b3-104">En Administrador de autorización, una tarea es una acción de alto nivel que los usuarios de una aplicación deben completar.</span><span class="sxs-lookup"><span data-stu-id="b30b3-104">In Authorization Manager, a task is a high-level action that users of an application need to complete.</span></span> <span data-ttu-id="b30b3-105">Las tareas se componen de operaciones, que son funciones de bajo nivel y métodos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b30b3-105">Tasks are made up of operations, which are low-level functions and methods of the application.</span></span> <span data-ttu-id="b30b3-106">A continuación, se asigna una tarea a esos roles que deben realizar esa tarea.</span><span class="sxs-lookup"><span data-stu-id="b30b3-106">A task is then assigned to those roles that must perform that task.</span></span> <span data-ttu-id="b30b3-107">Una tarea se representa mediante un objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) .</span><span class="sxs-lookup"><span data-stu-id="b30b3-107">A task is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object.</span></span> <span data-ttu-id="b30b3-108">Para obtener más información acerca de las operaciones y las tareas, consulte [operaciones y tareas](operations-and-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="b30b3-108">For more information about operations and tasks, see [Operations and Tasks](operations-and-tasks.md).</span></span>

<span data-ttu-id="b30b3-109">En el ejemplo siguiente se muestra cómo agrupar operaciones para crear una tarea.</span><span class="sxs-lookup"><span data-stu-id="b30b3-109">The following example shows how to group operations to create a task.</span></span> <span data-ttu-id="b30b3-110">En el ejemplo se da por supuesto que hay un almacén de directivas XML denominado MyStore.xml en el directorio raíz de la unidad C, que este almacén contiene una aplicación denominada///Expense y que esta aplicación contiene operaciones definidas en el tema [definir operaciones en el script](defining-operations-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="b30b3-110">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains operations defined in the topic [Defining Operations in Script](defining-operations-in-script.md).</span></span>


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



 

 



