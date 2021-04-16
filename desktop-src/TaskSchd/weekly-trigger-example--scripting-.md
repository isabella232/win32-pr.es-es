---
title: Ejemplo de desencadenador semanal (scripting)
description: En este ejemplo de scripting se muestra cómo crear una tarea que ejecute el Bloc de notas a las 8 00 A.M. del lunes de cada semana.
ms.assetid: 68ef73b0-3780-480e-90fe-940b6e8a5340
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4d9cf627591250c341008ba3a5129c4cc10cad6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418524"
---
# <a name="weekly-trigger-example-scripting"></a><span data-ttu-id="a1223-103">Ejemplo de desencadenador semanal (scripting)</span><span class="sxs-lookup"><span data-stu-id="a1223-103">Weekly Trigger Example (Scripting)</span></span>

<span data-ttu-id="a1223-104">En este ejemplo de scripting se muestra cómo crear una tarea que ejecute el Bloc de notas a las 8:00 A.M. del lunes de cada semana.</span><span class="sxs-lookup"><span data-stu-id="a1223-104">This scripting example shows how to create a task that runs Notepad at 8:00 AM on Monday of every week.</span></span> <span data-ttu-id="a1223-105">La tarea contiene un desencadenador diario que especifica cuándo se ejecuta la tarea y una acción ejecutable que ejecuta el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="a1223-105">The task contains a daily trigger that specifies when the task runs and an executable action that runs Notepad.</span></span>

<span data-ttu-id="a1223-106">En el procedimiento siguiente se describe cómo programar una tarea para que inicie un ejecutable a las 8:00 A.M. del lunes de cada semana.</span><span class="sxs-lookup"><span data-stu-id="a1223-106">The following procedure describes how to schedule a task to start an executable at 8:00 AM on Monday of every week.</span></span>

<span data-ttu-id="a1223-107">**Para programar el inicio del Bloc de notas a las 8:00 A.M. del lunes de cada semana**</span><span class="sxs-lookup"><span data-stu-id="a1223-107">**To schedule Notepad to start at 8:00 AM on Monday of every week**</span></span>

1.  <span data-ttu-id="a1223-108">Cree un objeto [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="a1223-108">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="a1223-109">Este objeto permite crear la tarea en una carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="a1223-109">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="a1223-110">Obtener una carpeta de tareas y crear una tarea.</span><span class="sxs-lookup"><span data-stu-id="a1223-110">Get a task folder and create a task.</span></span> <span data-ttu-id="a1223-111">Use el método [**TaskService. GetFolder**](taskservice-getfolder.md) para obtener la carpeta donde se almacena la tarea y el método [**TaskService. newtask**](taskservice-newtask.md) para crear el objeto [**TaskDefinition**](taskdefinition.md) que representa la tarea.</span><span class="sxs-lookup"><span data-stu-id="a1223-111">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="a1223-112">Defina la información sobre la tarea mediante el objeto [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="a1223-112">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="a1223-113">Use la propiedad [**TaskDefinition. Settings**](taskdefinition-settings.md) para definir la configuración que determina cómo el servicio de programador de tareas realiza la tarea y la propiedad [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) para definir la información que describe la tarea.</span><span class="sxs-lookup"><span data-stu-id="a1223-113">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="a1223-114">Cree un desencadenador semanal mediante la propiedad [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="a1223-114">Create a weekly trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="a1223-115">Esta propiedad proporciona acceso al objeto [**TriggerCollection**](triggercollection.md) que se usa para crear el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="a1223-115">This property provides access to the [**TriggerCollection**](triggercollection.md) object that is used to create the trigger.</span></span>

    <span data-ttu-id="a1223-116">Use el método [**TriggerCollection. Create**](triggercollection-create.md) (especificando el tipo de desencadenador que desea crear) para crear un desencadenador semanal.</span><span class="sxs-lookup"><span data-stu-id="a1223-116">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger you want to create) to create a weekly trigger.</span></span>

    <span data-ttu-id="a1223-117">Establezca la propiedad [**WeeklyTrigger. StartBoundary**](trigger-startboundary.md) para especificar Cuándo se activa el desencadenador y la hora del día en que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="a1223-117">Set the [**WeeklyTrigger.StartBoundary**](trigger-startboundary.md) property to specify when the trigger is activated and the time of the day when the task is run.</span></span> <span data-ttu-id="a1223-118">En este ejemplo, el desencadenador se activa el 1 de enero de 2005 y la tarea se ejecuta a las 8:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="a1223-118">In this example the trigger is activated on January 1, 2005 and the task runs at 8:00 AM.</span></span>

    <span data-ttu-id="a1223-119">Establezca la propiedad [**WeeklyTrigger. EndBoundary**](trigger-endboundary.md)para especificar Cuándo se desactiva el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="a1223-119">Set the [**WeeklyTrigger.EndBoundary**](trigger-endboundary.md)property to specify when the trigger is deactivated.</span></span> <span data-ttu-id="a1223-120">En este ejemplo, el desencadenador se desactiva el 1 de enero de 2015.</span><span class="sxs-lookup"><span data-stu-id="a1223-120">In this example the trigger is deactivated on January 1, 2015.</span></span>

    <span data-ttu-id="a1223-121">Establezca la propiedad [**WeeklyTrigger. DaysOfWeek**](weeklytrigger-daysofweek.md) para especificar los días de la semana en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="a1223-121">Set the [**WeeklyTrigger.DaysOfWeek**](weeklytrigger-daysofweek.md) property to specify the days of the week on which the task runs.</span></span> <span data-ttu-id="a1223-122">En este ejemplo, la tarea se ejecuta el lunes.</span><span class="sxs-lookup"><span data-stu-id="a1223-122">In this example the task is run on Monday.</span></span>

    <span data-ttu-id="a1223-123">Establezca la propiedad [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md)para especificar el intervalo entre las semanas de la programación.</span><span class="sxs-lookup"><span data-stu-id="a1223-123">Set the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md)property to specify the interval between the weeks in the schedule.</span></span> <span data-ttu-id="a1223-124">En este ejemplo, la tarea se ejecuta cada semana.</span><span class="sxs-lookup"><span data-stu-id="a1223-124">In this example the task runs every week.</span></span>

5.  <span data-ttu-id="a1223-125">Cree una acción para que la tarea se ejecute mediante la propiedad [**TaskDefinition. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="a1223-125">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="a1223-126">Esta propiedad proporciona acceso al objeto [**ActionCollection**](actioncollection.md) que se usa para crear la acción.</span><span class="sxs-lookup"><span data-stu-id="a1223-126">This property provides access to the [**ActionCollection**](actioncollection.md) object used to create the action.</span></span> <span data-ttu-id="a1223-127">Use el método [**ActionCollection. Create**](actioncollection-create.md) para especificar el tipo de acción que desea crear.</span><span class="sxs-lookup"><span data-stu-id="a1223-127">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action you want to create.</span></span> <span data-ttu-id="a1223-128">En este ejemplo se usa un objeto [**ExecAction**](execaction.md) , que representa una acción que ejecuta una operación de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="a1223-128">This example uses an [**ExecAction**](execaction.md) object, which represents an action that executes a command-line operation.</span></span>
6.  <span data-ttu-id="a1223-129">Registre la tarea mediante el método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="a1223-129">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="a1223-130">En este ejemplo, la tarea iniciará el Bloc de notas a las 8:00 A.M. del lunes de cada semana.</span><span class="sxs-lookup"><span data-stu-id="a1223-130">For this example the task will start Notepad at 8:00 AM on Monday of every week.</span></span>

<span data-ttu-id="a1223-131">En el siguiente ejemplo de VBScript se muestra cómo programar una tarea para ejecutar el Bloc de notas todos los días a las 8:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="a1223-131">The following VBScript example shows how to schedule a task to execute Notepad every day at 8:00 AM.</span></span>


```VB
'------------------------------------------------------------------
' This sample schedules a task to start on a weekly basis.
'------------------------------------------------------------------

' A constant that specifies a weekly trigger.
const TriggerTypeWeekly = 3
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
regInfo.Description = "Start Notepad weekly."
regInfo.Author = "Administrator"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a weekly trigger. Note that the start boundary 
' specifies the time of day that the task starts, the 
' day-of-week specfies on what day of the week the task 
' runs, and the interval specifies what weeks the task runs.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeWeekly)

' Trigger variables that define when the trigger is active 
' and the time of day that the task is run. The format of 
' this tims is YYYY-MM-DDTHH:MM:SS
Dim startTime, endTime

Dim time
startTime = "2006-05-02T08:00:00"  'Task runs at 8:00 AM
endTime = "2015-05-02T08:00:00"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.DaysOfWeek = 1
trigger.WeeksInterval = 1    'Task runs every week.
trigger.Id = "WeeklyTriggerId"
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
    "Test Weekly Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a><span data-ttu-id="a1223-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1223-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1223-133">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="a1223-133">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




