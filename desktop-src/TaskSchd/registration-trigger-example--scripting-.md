---
title: Ejemplo de desencadenador de registro (scripting)
description: En este ejemplo de scripting se muestra cómo crear una tarea programada para ejecutar el Bloc de notas cuando se registra una tarea.
ms.assetid: 956b3a21-7d36-4d06-be84-690884ba653a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bce6271927e74e31f25b3ac86783b35899bbd862
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357733"
---
# <a name="registration-trigger-example-scripting"></a><span data-ttu-id="57f69-103">Ejemplo de desencadenador de registro (scripting)</span><span class="sxs-lookup"><span data-stu-id="57f69-103">Registration Trigger Example (Scripting)</span></span>

<span data-ttu-id="57f69-104">En este ejemplo de scripting se muestra cómo crear una tarea programada para ejecutar el Bloc de notas cuando se registra una tarea.</span><span class="sxs-lookup"><span data-stu-id="57f69-104">This scripting example shows how to create a task that is scheduled to execute Notepad when a task is registered.</span></span> <span data-ttu-id="57f69-105">La tarea contiene un desencadenador de registro que especifica un límite de inicio y un límite de fin para la tarea.</span><span class="sxs-lookup"><span data-stu-id="57f69-105">The task contains a registration trigger that specifies a start boundary and an end boundary for the task.</span></span> <span data-ttu-id="57f69-106">El límite inicial especifica cuándo se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="57f69-106">The start boundary specifies when the trigger is activated.</span></span> <span data-ttu-id="57f69-107">La tarea también contiene una acción que especifica la tarea para ejecutar el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="57f69-107">The task also contains an action that specifies the task to execute Notepad.</span></span>

> [!Note]  
> <span data-ttu-id="57f69-108">Cuando se actualiza una tarea con un desencadenador de registro, la tarea se ejecutará después de que se produzca la actualización.</span><span class="sxs-lookup"><span data-stu-id="57f69-108">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

<span data-ttu-id="57f69-109">En el procedimiento siguiente se describe cómo programar un ejecutable, como el Bloc de notas, para que se inicie cuando se registre una tarea.</span><span class="sxs-lookup"><span data-stu-id="57f69-109">The following procedure describes how to schedule an executable such as Notepad to start when a task is registered.</span></span>

<span data-ttu-id="57f69-110">**Para programar el inicio del Bloc de notas cuando se registra una tarea**</span><span class="sxs-lookup"><span data-stu-id="57f69-110">**To schedule Notepad to start when a task is registered**</span></span>

1.  <span data-ttu-id="57f69-111">Cree un objeto [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="57f69-111">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="57f69-112">Este objeto permite crear la tarea en una carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="57f69-112">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="57f69-113">Obtener una carpeta de tareas y crear una tarea.</span><span class="sxs-lookup"><span data-stu-id="57f69-113">Get a task folder and create a task.</span></span> <span data-ttu-id="57f69-114">Use el método [**TaskService. GetFolder**](taskservice-getfolder.md) para obtener la carpeta donde se almacena la tarea y el método [**TaskService. newtask**](taskservice-newtask.md) para crear el objeto [**TaskDefinition**](taskdefinition.md) que representa la tarea.</span><span class="sxs-lookup"><span data-stu-id="57f69-114">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="57f69-115">Defina la información sobre la tarea mediante el objeto [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="57f69-115">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="57f69-116">Use la propiedad [**TaskDefinition. Settings**](taskdefinition-settings.md) para definir la configuración que determina cómo el servicio de programador de tareas realiza la tarea y la propiedad [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) para definir la información que describe la tarea.</span><span class="sxs-lookup"><span data-stu-id="57f69-116">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="57f69-117">Cree un desencadenador de registro mediante la propiedad [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="57f69-117">Create a registration trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="57f69-118">Esta propiedad proporciona acceso al objeto [**TriggerCollection**](triggercollection.md) .</span><span class="sxs-lookup"><span data-stu-id="57f69-118">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="57f69-119">Use el método [**TriggerCollection. Create**](triggercollection-create.md) (especificando el tipo de desencadenador que desea crear) para crear un desencadenador de registro.</span><span class="sxs-lookup"><span data-stu-id="57f69-119">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger that you want to create) to create a registration trigger.</span></span>
5.  <span data-ttu-id="57f69-120">Cree una acción para que la tarea se ejecute mediante la propiedad [**TaskDefinition. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="57f69-120">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="57f69-121">Esta propiedad proporciona acceso al objeto [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="57f69-121">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="57f69-122">Use el método [**ActionCollection. Create**](actioncollection-create.md) para especificar el tipo de acción que desea crear.</span><span class="sxs-lookup"><span data-stu-id="57f69-122">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="57f69-123">En este ejemplo se usa un objeto [**ExecAction**](execaction.md) , que representa una acción que inicia un ejecutable.</span><span class="sxs-lookup"><span data-stu-id="57f69-123">This example uses an [**ExecAction**](execaction.md) object, which represents an action that starts an executable.</span></span>
6.  <span data-ttu-id="57f69-124">Registre la tarea mediante el método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="57f69-124">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span>

<span data-ttu-id="57f69-125">En el siguiente ejemplo de VBScript se muestra cómo crear una tarea que programa el Bloc de notas para que se ejecute cuando se registre la tarea.</span><span class="sxs-lookup"><span data-stu-id="57f69-125">The following VBScript example shows how to create a task that schedules Notepad to execute when the task is registered.</span></span>


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe when
' the task is registered.
'---------------------------------------------------------

' A constant that specifies a registration trigger.
const TriggerTypeRegistration = 7
' A constant that specifies an executable action.
const ActionTypeExecutable = 0   


'********************************************************
' Create the TaskService object.
Set service = CreateObject("Schedule.Service")
call service.Connect()

'********************************************************
' Get a folder to create a task definition in. 
Dim rootFolder
Set rootFolder = service.GetFolder("\")

' The taskDefinition variable is the TaskDefinition object.
Dim taskDefinition
' The flags parameter is 0 because it is not supported.
Set taskDefinition = service.NewTask(0) 

'********************************************************
' Define information about the task.

' Set the registration info for the task by 
' creating the RegistrationInfo object.
Dim regInfo
Set regInfo = taskDefinition.RegistrationInfo
regInfo.Description = "Start Notepad when the task is registered."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a registration trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeRegistration)

trigger.ExecutionTimeLimit = "PT5M"    'Five minutes
trigger.Id = "RegistrationTriggerId"   

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task. The action executes Notepad.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExecutable )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.

call rootFolder.RegisterTaskDefinition( _
    "Test Registration Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a><span data-ttu-id="57f69-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="57f69-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57f69-127">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="57f69-127">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




