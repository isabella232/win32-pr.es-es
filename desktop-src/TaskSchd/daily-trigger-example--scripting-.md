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
# <a name="daily-trigger-example-scripting"></a>Ejemplo de desencadenador diario (scripting)

En este ejemplo de scripting se muestra cómo crear una tarea que ejecute el Bloc de notas a las 8:00 AM todos los días. La tarea contiene un desencadenador diario que especifica un límite de inicio para activar el desencadenador y para especificar la hora del día en que se ejecuta la tarea, un intervalo de desencadenador para especificar que la tarea se ejecuta todos los días y un límite de fin para desactivar el desencadenador. En el ejemplo también se muestra cómo establecer un patrón de repetición para que el desencadenador repita la tarea. La tarea también contiene una acción ejecutable que ejecuta el Bloc de notas.

En el procedimiento siguiente se describe cómo programar una tarea para que inicie un ejecutable a las 8:00 AM todos los días. (Estos pasos corresponden a los comentarios de código que se incluyen en el código de ejemplo).

**Para programar el inicio del Bloc de notas a las 8:00 A.M. todos los días**

1.  Cree un objeto [**TaskService**](taskservice.md) . Este objeto permite crear la tarea en una carpeta especificada.
2.  Obtener una carpeta de tareas y crear una tarea. Use el método [**TaskService. GetFolder**](taskservice-getfolder.md) para obtener la carpeta donde se almacena la tarea y el método [**TaskService. newtask**](taskservice-newtask.md) para crear el objeto [**TaskDefinition**](taskdefinition.md) que representa la tarea.
3.  Defina la información sobre la tarea mediante el objeto [**TaskDefinition**](taskdefinition.md) . Use la propiedad [**TaskDefinition. Settings**](taskdefinition-settings.md) para definir la configuración que determina cómo el servicio de programador de tareas realiza la tarea y la propiedad [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) para definir la información que describe la tarea.
4.  Cree un desencadenador diario mediante la propiedad [**TaskDefinition. Triggers**](taskdefinition-triggers.md) . Esta propiedad proporciona acceso al objeto [**TriggerCollection**](triggercollection.md) que se usa para crear el desencadenador. Use el método [**TriggerCollection. Create**](triggercollection-create.md) (especificando el tipo de desencadenador que desea crear) para crear un desencadenador diario. Cuando cree el desencadenador, establezca el límite de inicio para activar el desencadenador y especifique la hora del día en que se ejecuta la tarea, el intervalo entre los días y el límite final para desactivar el desencadenador. En el ejemplo siguiente se muestra cómo establecer un patrón de repetición para que el desencadenador repita la tarea.
5.  Cree una acción para que la tarea se ejecute mediante la propiedad [**TaskDefinition. Actions**](taskdefinition-actions.md) . Esta propiedad proporciona acceso al objeto [**ActionCollection**](actioncollection.md) que se usa para crear la acción. Use el método [**ActionCollection. Create**](actioncollection-create.md) para especificar el tipo de acción que desea crear. En este ejemplo se usa un objeto [**ExecAction**](execaction.md) , que representa una acción que ejecuta una operación de línea de comandos.
6.  Registre la tarea mediante el método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) . En este ejemplo, la tarea iniciará el Bloc de notas a las 8:00 A.M. todos los días.

En el siguiente ejemplo de VBScript se muestra cómo programar una tarea para ejecutar el Bloc de notas todos los días a las 8:00 A.M.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




