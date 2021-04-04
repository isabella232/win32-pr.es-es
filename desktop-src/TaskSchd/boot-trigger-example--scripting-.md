---
title: Ejemplo de desencadenador de arranque (scripting)
description: En este ejemplo de scripting se muestra cómo crear una tarea programada para ejecutar el Bloc de notas al arrancar el sistema.
ms.assetid: 73ae9cc4-ef89-4390-ac05-8a773f45fa46
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72b7735c607dfc39b848532a70e4d24b1a14d346
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075735"
---
# <a name="boot-trigger-example-scripting"></a><span data-ttu-id="24eff-103">Ejemplo de desencadenador de arranque (scripting)</span><span class="sxs-lookup"><span data-stu-id="24eff-103">Boot Trigger Example (Scripting)</span></span>

<span data-ttu-id="24eff-104">En este ejemplo de scripting se muestra cómo crear una tarea programada para ejecutar el Bloc de notas al arrancar el sistema.</span><span class="sxs-lookup"><span data-stu-id="24eff-104">This scripting example shows how to create a task that is scheduled to execute Notepad when the system is booted.</span></span> <span data-ttu-id="24eff-105">La tarea contiene un desencadenador de arranque que especifica un límite de inicio y un tiempo de retraso para que la tarea se inicie después de arrancar el sistema.</span><span class="sxs-lookup"><span data-stu-id="24eff-105">The task contains a boot trigger that specifies a start boundary and delay time for the task to start after the system is booted.</span></span> <span data-ttu-id="24eff-106">La tarea también contiene una acción que especifica la tarea para ejecutar el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="24eff-106">The task also contains an action that specifies the task to execute Notepad.</span></span> <span data-ttu-id="24eff-107">La tarea se registra mediante la cuenta de servicio local como contexto de seguridad para ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="24eff-107">The task is registered using the Local Service account as a security context to run the task.</span></span>

<span data-ttu-id="24eff-108">En el procedimiento siguiente se describe cómo programar un archivo ejecutable, como el Bloc de notas, para que se inicie cuando se arranque el sistema.</span><span class="sxs-lookup"><span data-stu-id="24eff-108">The following procedure describes how to schedule an executable such as Notepad to start when the system is booted.</span></span>

<span data-ttu-id="24eff-109">**Para programar el inicio del Bloc de notas al arrancar el sistema**</span><span class="sxs-lookup"><span data-stu-id="24eff-109">**To schedule Notepad to start when the system is booted**</span></span>

1.  <span data-ttu-id="24eff-110">Cree un objeto [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="24eff-110">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="24eff-111">Este objeto permite crear la tarea en una carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="24eff-111">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="24eff-112">Obtener una carpeta de tareas y crear una tarea.</span><span class="sxs-lookup"><span data-stu-id="24eff-112">Get a task folder and create a task.</span></span> <span data-ttu-id="24eff-113">Use el método [**TaskService. GetFolder**](taskservice-getfolder.md) para obtener la carpeta donde se almacena la tarea y el método [**TaskService. newtask**](taskservice-newtask.md) para crear el objeto [**TaskDefinition**](taskdefinition.md) que representa la tarea.</span><span class="sxs-lookup"><span data-stu-id="24eff-113">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="24eff-114">Defina la información sobre la tarea mediante el objeto [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="24eff-114">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="24eff-115">Use la propiedad [**TaskDefinition. Settings**](taskdefinition-settings.md) para definir la configuración que determina cómo el servicio de programador de tareas realiza la tarea y la propiedad [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) para definir la información que describe la tarea.</span><span class="sxs-lookup"><span data-stu-id="24eff-115">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="24eff-116">Cree un desencadenador Logon mediante la propiedad [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="24eff-116">Create a logon trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="24eff-117">Esta propiedad proporciona acceso al objeto [**TriggerCollection**](triggercollection.md) .</span><span class="sxs-lookup"><span data-stu-id="24eff-117">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="24eff-118">Use el método [**TriggerCollection. Create**](triggercollection-create.md) (especificando el tipo de desencadenador que desea crear) para crear un desencadenador de arranque.</span><span class="sxs-lookup"><span data-stu-id="24eff-118">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger that you want to create) to create a boot trigger.</span></span> <span data-ttu-id="24eff-119">Cuando cree el desencadenador, establezca las propiedades [**StartBoundary**](trigger-startboundary.md) y [**EndBoundary**](trigger-endboundary.md) del desencadenador para activar y desactivar el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="24eff-119">As you create the trigger, set the [**StartBoundary**](trigger-startboundary.md) and [**EndBoundary**](trigger-endboundary.md) properties of the trigger to activate and deactivate the trigger.</span></span> <span data-ttu-id="24eff-120">También puede especificar un valor para la propiedad [**Delay**](boottrigger-delay.md) del desencadenador de arranque.</span><span class="sxs-lookup"><span data-stu-id="24eff-120">You can also specify a value for the [**Delay**](boottrigger-delay.md) property of the boot trigger.</span></span>
5.  <span data-ttu-id="24eff-121">Cree una acción para que la tarea se ejecute mediante la propiedad [**TaskDefinition. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="24eff-121">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="24eff-122">Esta propiedad proporciona acceso al objeto [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="24eff-122">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="24eff-123">Use el método [**ActionCollection. Create**](actioncollection-create.md) para especificar el tipo de acción que desea crear.</span><span class="sxs-lookup"><span data-stu-id="24eff-123">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="24eff-124">En este ejemplo se usa un objeto [**ExecAction**](execaction.md) , que representa una acción que inicia un ejecutable.</span><span class="sxs-lookup"><span data-stu-id="24eff-124">This example uses an [**ExecAction**](execaction.md) object, which represents an action that starts an executable.</span></span>
6.  <span data-ttu-id="24eff-125">Registre la tarea mediante el método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="24eff-125">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="24eff-126">La tarea se registra mediante la cuenta de servicio local como contexto de seguridad para ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="24eff-126">The task is registered using the Local Service account as a security context to run the task.</span></span>

<span data-ttu-id="24eff-127">En el siguiente ejemplo de VBScript se muestra cómo programar una tarea para ejecutar el Bloc de notas 30 segundos después de que se arranque el sistema.</span><span class="sxs-lookup"><span data-stu-id="24eff-127">The following VBScript example shows how to schedule a task to execute Notepad 30 seconds after the system is booted.</span></span>


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe 30 seconds after
' the system is booted.
'---------------------------------------------------------

' A constant that specifies a boot trigger.
const TriggerTypeBoot = 8
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
regInfo.Description = "Task will execute Notepad when " & _
    "the computer is booted."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a boot trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeBoot)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime
startTime = "2006-05-02T10:49:02"
endTime = "2006-05-02T10:52:02"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    ' Five minutes
trigger.Id = "BootTriggerId"
trigger.Delay = "PT30S"                ' 30 Seconds   

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task. The action executes notepad.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExecutable )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.
const createOrUpdateTask = 6
call rootFolder.RegisterTaskDefinition( _
    "Test Boot Trigger", taskDefinition, createOrUpdateTask, _
    "Local Service", , 5)

WScript.Echo "Task submitted."
```



## <a name="related-topics"></a><span data-ttu-id="24eff-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="24eff-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24eff-129">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="24eff-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




