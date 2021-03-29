---
title: Ejemplo de desencadenador diario (scripting)
description: En este ejemplo de scripting se muestra cómo crear una tarea que ejecute el Bloc de notas a las 8 00 AM todos los días.
ms.assetid: a13bd54d-b45a-46e5-8281-d080f50f6bef
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3399934786e1cd0f95ca020c92027ccafafa5272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903383"
---
# <a name="daily-trigger-example-scripting"></a><span data-ttu-id="aedc4-103">Ejemplo de desencadenador diario (scripting)</span><span class="sxs-lookup"><span data-stu-id="aedc4-103">Daily Trigger Example (Scripting)</span></span>

<span data-ttu-id="aedc4-104">En este ejemplo de scripting se muestra cómo crear una tarea que ejecute el Bloc de notas a las 8:00 AM todos los días.</span><span class="sxs-lookup"><span data-stu-id="aedc4-104">This scripting example shows how to create a task that runs Notepad at 8:00 AM every day.</span></span> <span data-ttu-id="aedc4-105">La tarea contiene un desencadenador diario que especifica un límite de inicio para activar el desencadenador y para especificar la hora del día en que se ejecuta la tarea, un intervalo de desencadenador para especificar que la tarea se ejecuta todos los días y un límite de fin para desactivar el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="aedc4-105">The task contains a daily trigger that specifies a start boundary to activate the trigger and to specify the time of day that the task runs, a trigger interval to specify that the task runs every day, and an end boundary to deactivates the trigger.</span></span> <span data-ttu-id="aedc4-106">En el ejemplo también se muestra cómo establecer un patrón de repetición para que el desencadenador repita la tarea.</span><span class="sxs-lookup"><span data-stu-id="aedc4-106">The example also shows how to set a repetition pattern for the trigger to repeat the task.</span></span> <span data-ttu-id="aedc4-107">La tarea también contiene una acción ejecutable que ejecuta el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="aedc4-107">The task also contains an executable action that runs Notepad.</span></span>

<span data-ttu-id="aedc4-108">En el procedimiento siguiente se describe cómo programar una tarea para que inicie un ejecutable a las 8:00 AM todos los días.</span><span class="sxs-lookup"><span data-stu-id="aedc4-108">The following procedure describes how to schedule a task to start an executable at 8:00 AM every day.</span></span> <span data-ttu-id="aedc4-109">(Estos pasos corresponden a los comentarios de código que se incluyen en el código de ejemplo).</span><span class="sxs-lookup"><span data-stu-id="aedc4-109">(These steps correspond to the code comments included in the example code.)</span></span>

<span data-ttu-id="aedc4-110">**Para programar el inicio del Bloc de notas a las 8:00 A.M. todos los días**</span><span class="sxs-lookup"><span data-stu-id="aedc4-110">**To schedule Notepad to start at 8:00 AM every day**</span></span>

1.  <span data-ttu-id="aedc4-111">Cree un objeto [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="aedc4-111">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="aedc4-112">Este objeto permite crear la tarea en una carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="aedc4-112">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="aedc4-113">Obtener una carpeta de tareas y crear una tarea.</span><span class="sxs-lookup"><span data-stu-id="aedc4-113">Get a task folder and create a task.</span></span> <span data-ttu-id="aedc4-114">Use el método [**TaskService. GetFolder**](taskservice-getfolder.md) para obtener la carpeta donde se almacena la tarea y el método [**TaskService. newtask**](taskservice-newtask.md) para crear el objeto [**TaskDefinition**](taskdefinition.md) que representa la tarea.</span><span class="sxs-lookup"><span data-stu-id="aedc4-114">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="aedc4-115">Defina la información sobre la tarea mediante el objeto [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="aedc4-115">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="aedc4-116">Use la propiedad [**TaskDefinition. Settings**](taskdefinition-settings.md) para definir la configuración que determina cómo el servicio de programador de tareas realiza la tarea y la propiedad [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) para definir la información que describe la tarea.</span><span class="sxs-lookup"><span data-stu-id="aedc4-116">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="aedc4-117">Cree un desencadenador diario mediante la propiedad [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="aedc4-117">Create a daily trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="aedc4-118">Esta propiedad proporciona acceso al objeto [**TriggerCollection**](triggercollection.md) que se usa para crear el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="aedc4-118">This property provides access to the [**TriggerCollection**](triggercollection.md) object that is used to create the trigger.</span></span> <span data-ttu-id="aedc4-119">Use el método [**TriggerCollection. Create**](triggercollection-create.md) (especificando el tipo de desencadenador que desea crear) para crear un desencadenador diario.</span><span class="sxs-lookup"><span data-stu-id="aedc4-119">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger you want to create) to create a daily trigger.</span></span> <span data-ttu-id="aedc4-120">Cuando cree el desencadenador, establezca el límite de inicio para activar el desencadenador y especifique la hora del día en que se ejecuta la tarea, el intervalo entre los días y el límite final para desactivar el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="aedc4-120">As you create the trigger, set the start boundary to activate the trigger and specify the time of day that the task runs, the interval between the days, and the end boundary to deactivate the trigger.</span></span> <span data-ttu-id="aedc4-121">En el ejemplo siguiente se muestra cómo establecer un patrón de repetición para que el desencadenador repita la tarea.</span><span class="sxs-lookup"><span data-stu-id="aedc4-121">The example below shows how to set a repetition pattern for the trigger to repeat the task.</span></span>
5.  <span data-ttu-id="aedc4-122">Cree una acción para que la tarea se ejecute mediante la propiedad [**TaskDefinition. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="aedc4-122">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="aedc4-123">Esta propiedad proporciona acceso al objeto [**ActionCollection**](actioncollection.md) que se usa para crear la acción.</span><span class="sxs-lookup"><span data-stu-id="aedc4-123">This property provides access to the [**ActionCollection**](actioncollection.md) object used to create the action.</span></span> <span data-ttu-id="aedc4-124">Use el método [**ActionCollection. Create**](actioncollection-create.md) para especificar el tipo de acción que desea crear.</span><span class="sxs-lookup"><span data-stu-id="aedc4-124">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action you want to create.</span></span> <span data-ttu-id="aedc4-125">En este ejemplo se usa un objeto [**ExecAction**](execaction.md) , que representa una acción que ejecuta una operación de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="aedc4-125">This example uses an [**ExecAction**](execaction.md) object, which represents an action that executes a command-line operation.</span></span>
6.  <span data-ttu-id="aedc4-126">Registre la tarea mediante el método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="aedc4-126">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="aedc4-127">En este ejemplo, la tarea iniciará el Bloc de notas a las 8:00 A.M. todos los días.</span><span class="sxs-lookup"><span data-stu-id="aedc4-127">For this example the task will start Notepad at 8:00 AM every day.</span></span>

<span data-ttu-id="aedc4-128">En el siguiente ejemplo de VBScript se muestra cómo programar una tarea para ejecutar el Bloc de notas todos los días a las 8:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="aedc4-128">The following VBScript example shows how to schedule a task to execute Notepad every day at 8:00 AM.</span></span>


```VB
'------------------------------------------------------------------
' This sample schedules a task to start on a daily basis.
'------------------------------------------------------------------

' A constant that specifies a daily trigger.
const TriggerTypeDaily = 2
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
regInfo.Description = "Start notepad at 8:00AM daily"
regInfo.Author = "Administrator"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a daily trigger. Note that the start boundary 
' specifies the time of day that the task starts and the 
' interval specifies what days the task is run.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeDaily)

' Trigger variables that define when the trigger is active 
' and the time of day that the task is run. The format of 
' this time is YYYY-MM-DDTHH:MM:SS
Dim startTime, endTime

Dim time
startTime = "2006-05-02T08:00:00"  'Task runs at 8:00 AM
endTime = "2015-05-02T08:00:00"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.DaysInterval = 1    'Task runs every day.
trigger.Id = "DailyTriggerId"
trigger.Enabled = True

' Set the task repetition pattern for the task.
' This will repeat the task 5 times.
Dim repetitionPattern
Set repetitionPattern = trigger.Repetition
repetitionPattern.Duration = "PT4M"
repetitionPattern.Interval = "PT1M"

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
    "Test Daily Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a><span data-ttu-id="aedc4-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aedc4-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aedc4-130">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="aedc4-130">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




