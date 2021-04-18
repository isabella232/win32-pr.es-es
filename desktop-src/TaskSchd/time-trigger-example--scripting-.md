---
title: Ejemplo de desencadenador de tiempo (scripting)
description: Este ejemplo de scripting muestra cómo crear una tarea que ejecute el Bloc de notas en un momento determinado.
ms.assetid: 8511ffcd-166f-4c63-9cd2-ead53dde9ed8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77cbf9eab12f5ca027fbb6c48ade37a9f57d9beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685494"
---
# <a name="time-trigger-example-scripting"></a><span data-ttu-id="fcb1a-103">Ejemplo de desencadenador de tiempo (scripting)</span><span class="sxs-lookup"><span data-stu-id="fcb1a-103">Time Trigger Example (Scripting)</span></span>

<span data-ttu-id="fcb1a-104">Este ejemplo de scripting muestra cómo crear una tarea que ejecute el Bloc de notas en un momento determinado.</span><span class="sxs-lookup"><span data-stu-id="fcb1a-104">This scripting example shows how to create a task that runs Notepad at a specific time.</span></span> <span data-ttu-id="fcb1a-105">La tarea contiene un desencadenador basado en tiempo que especifica un límite de inicio para activar la tarea, una acción ejecutable que ejecuta el Bloc de notas y un límite final que desactiva la tarea.</span><span class="sxs-lookup"><span data-stu-id="fcb1a-105">The task contains a time-based trigger that specifies a start boundary to activate the task, an executable action that runs Notepad, and an end boundary that deactivates the task.</span></span>

<span data-ttu-id="fcb1a-106">En el procedimiento siguiente se describe cómo programar una tarea para iniciar un ejecutable en un momento determinado.</span><span class="sxs-lookup"><span data-stu-id="fcb1a-106">The following procedure describes how to schedule a task to start an executable at a specific time.</span></span>

<span data-ttu-id="fcb1a-107">**Programar el Bloc de notas para que se inicie a una hora específica**</span><span class="sxs-lookup"><span data-stu-id="fcb1a-107">**To Schedule Notepad to start at a Specific Time**</span></span>

1.  <span data-ttu-id="fcb1a-108">Cree un objeto [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="fcb1a-108">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="fcb1a-109">Este objeto permite crear la tarea en una carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="fcb1a-109">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="fcb1a-110">Obtener una carpeta de tareas y crear una tarea.</span><span class="sxs-lookup"><span data-stu-id="fcb1a-110">Get a task folder and create a task.</span></span> <span data-ttu-id="fcb1a-111">Use el método [**TaskService. GetFolder**](taskservice-getfolder.md) para obtener la carpeta donde se almacena la tarea y el método [**TaskService. newtask**](taskservice-newtask.md) para crear el objeto [**TaskDefinition**](taskdefinition.md) que representa la tarea.</span><span class="sxs-lookup"><span data-stu-id="fcb1a-111">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="fcb1a-112">Defina la información sobre la tarea mediante el objeto [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="fcb1a-112">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="fcb1a-113">Use la propiedad [**TaskDefinition. Settings**](taskdefinition-settings.md) para definir la configuración que determina cómo el servicio de programador de tareas realiza la tarea y la propiedad [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) para definir la información que describe la tarea.</span><span class="sxs-lookup"><span data-stu-id="fcb1a-113">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="fcb1a-114">Cree un desencadenador basado en el tiempo mediante la propiedad [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="fcb1a-114">Create a time-based trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="fcb1a-115">Esta propiedad proporciona acceso al objeto [**TriggerCollection**](triggercollection.md) .</span><span class="sxs-lookup"><span data-stu-id="fcb1a-115">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="fcb1a-116">Use el método [**TriggerCollection. Create**](triggercollection-create.md) (especificando el tipo de desencadenador que desea crear) para crear un desencadenador basado en tiempo.</span><span class="sxs-lookup"><span data-stu-id="fcb1a-116">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger you want to create) to create a time-based trigger.</span></span> <span data-ttu-id="fcb1a-117">Cuando cree el desencadenador, establezca el límite inicial y el límite final del desencadenador para activar y desactivar el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="fcb1a-117">As you create the trigger, set the start boundary and end boundary of the trigger to activate and deactivate the trigger.</span></span> <span data-ttu-id="fcb1a-118">El límite inicial especifica cuándo se realizará la acción de la tarea.</span><span class="sxs-lookup"><span data-stu-id="fcb1a-118">The start boundary specifies when the task's action will be performed.</span></span>
5.  <span data-ttu-id="fcb1a-119">Cree una acción para que la tarea se ejecute mediante la propiedad [**TaskDefinition. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="fcb1a-119">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="fcb1a-120">Esta propiedad proporciona acceso al objeto [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="fcb1a-120">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="fcb1a-121">Use el método [**ActionCollection. Create**](actioncollection-create.md) para especificar el tipo de acción que desea crear.</span><span class="sxs-lookup"><span data-stu-id="fcb1a-121">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action you want to create.</span></span> <span data-ttu-id="fcb1a-122">En este ejemplo se usa un objeto [**ExecAction**](execaction.md) , que representa una acción que ejecuta una operación de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="fcb1a-122">This example uses an [**ExecAction**](execaction.md) object, which represents an action that executes a command-line operation.</span></span>
6.  <span data-ttu-id="fcb1a-123">Registre la tarea mediante el método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="fcb1a-123">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="fcb1a-124">En este ejemplo, la tarea iniciará el Bloc de notas en el momento actual más 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="fcb1a-124">For this example the task will start Notepad at the current time plus 30 seconds.</span></span>

<span data-ttu-id="fcb1a-125">En el siguiente ejemplo de VBScript se muestra cómo programar una tarea para ejecutar el Bloc de notas 30 segundos después de que se haya registrado la tarea.</span><span class="sxs-lookup"><span data-stu-id="fcb1a-125">The following VBScript example shows how to schedule a task to execute Notepad 30 seconds after the task is registered.</span></span>


```VB
'------------------------------------------------------------------
' This sample schedules a task to start notepad.exe 30 seconds
' from the time the task is registered.
'------------------------------------------------------------------

' A constant that specifies a time-based trigger.
const TriggerTypeTime = 1
' A constant that specifies an executable action.
const ActionTypeExec = 0   


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
regInfo.Description = "Start notepad at a certain time"
regInfo.Author = "Author Name"

'********************************************************
' Set the principal for the task
Dim principal
Set principal = taskDefinition.Principal

' Set the logon type to interactive logon
principal.LogonType = 3


' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a time-based trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeTime)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime

Dim time
time = DateAdd("s", 30, Now)  'start time = 30 seconds from now
startTime = XmlTime(time)

time = DateAdd("n", 5, Now) 'end time = 5 minutes from now
endTime = XmlTime(time)

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    'Five minutes
trigger.Id = "TimeTriggerId"
trigger.Enabled = True

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task to run notepad.exe.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExec )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.

call rootFolder.RegisterTaskDefinition( _
    "Test TimeTrigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."



'------------------------------------------------------------------
' Used to get the time for the trigger 
' startBoundary and endBoundary.
' Return the time in the correct format: 
' YYYY-MM-DDTHH:MM:SS. 
'------------------------------------------------------------------
Function XmlTime(t)
    Dim cSecond, cMinute, CHour, cDay, cMonth, cYear
    Dim tTime, tDate

    cSecond = "0" & Second(t)
    cMinute = "0" & Minute(t)
    cHour = "0" & Hour(t)
    cDay = "0" & Day(t)
    cMonth = "0" & Month(t)
    cYear = Year(t)

    tTime = Right(cHour, 2) & ":" & Right(cMinute, 2) & _
        ":" & Right(cSecond, 2)
    tDate = cYear & "-" & Right(cMonth, 2) & "-" & Right(cDay, 2)
    XmlTime = tDate & "T" & tTime 
End Function

```



## <a name="related-topics"></a><span data-ttu-id="fcb1a-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fcb1a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcb1a-127">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="fcb1a-127">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




