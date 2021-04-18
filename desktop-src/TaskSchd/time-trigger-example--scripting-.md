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
# <a name="time-trigger-example-scripting"></a>Ejemplo de desencadenador de tiempo (scripting)

Este ejemplo de scripting muestra cómo crear una tarea que ejecute el Bloc de notas en un momento determinado. La tarea contiene un desencadenador basado en tiempo que especifica un límite de inicio para activar la tarea, una acción ejecutable que ejecuta el Bloc de notas y un límite final que desactiva la tarea.

En el procedimiento siguiente se describe cómo programar una tarea para iniciar un ejecutable en un momento determinado.

**Programar el Bloc de notas para que se inicie a una hora específica**

1.  Cree un objeto [**TaskService**](taskservice.md) . Este objeto permite crear la tarea en una carpeta especificada.
2.  Obtener una carpeta de tareas y crear una tarea. Use el método [**TaskService. GetFolder**](taskservice-getfolder.md) para obtener la carpeta donde se almacena la tarea y el método [**TaskService. newtask**](taskservice-newtask.md) para crear el objeto [**TaskDefinition**](taskdefinition.md) que representa la tarea.
3.  Defina la información sobre la tarea mediante el objeto [**TaskDefinition**](taskdefinition.md) . Use la propiedad [**TaskDefinition. Settings**](taskdefinition-settings.md) para definir la configuración que determina cómo el servicio de programador de tareas realiza la tarea y la propiedad [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) para definir la información que describe la tarea.
4.  Cree un desencadenador basado en el tiempo mediante la propiedad [**TaskDefinition. Triggers**](taskdefinition-triggers.md) . Esta propiedad proporciona acceso al objeto [**TriggerCollection**](triggercollection.md) . Use el método [**TriggerCollection. Create**](triggercollection-create.md) (especificando el tipo de desencadenador que desea crear) para crear un desencadenador basado en tiempo. Cuando cree el desencadenador, establezca el límite inicial y el límite final del desencadenador para activar y desactivar el desencadenador. El límite inicial especifica cuándo se realizará la acción de la tarea.
5.  Cree una acción para que la tarea se ejecute mediante la propiedad [**TaskDefinition. Actions**](taskdefinition-actions.md) . Esta propiedad proporciona acceso al objeto [**ActionCollection**](actioncollection.md) . Use el método [**ActionCollection. Create**](actioncollection-create.md) para especificar el tipo de acción que desea crear. En este ejemplo se usa un objeto [**ExecAction**](execaction.md) , que representa una acción que ejecuta una operación de línea de comandos.
6.  Registre la tarea mediante el método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) . En este ejemplo, la tarea iniciará el Bloc de notas en el momento actual más 30 segundos.

En el siguiente ejemplo de VBScript se muestra cómo programar una tarea para ejecutar el Bloc de notas 30 segundos después de que se haya registrado la tarea.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




