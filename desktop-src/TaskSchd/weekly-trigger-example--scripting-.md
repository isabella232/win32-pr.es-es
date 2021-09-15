---
title: Ejemplo de desencadenador semanal (scripting)
description: En este ejemplo de scripting se muestra cómo crear una tarea que Bloc de notas a las 8:00 a. m. el lunes de cada semana.
ms.assetid: 68ef73b0-3780-480e-90fe-940b6e8a5340
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4d9cf627591250c341008ba3a5129c4cc10cad6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474647"
---
# <a name="weekly-trigger-example-scripting"></a>Ejemplo de desencadenador semanal (scripting)

En este ejemplo de scripting se muestra cómo crear una tarea que Bloc de notas a las 8:00 a. m. el lunes de cada semana. La tarea contiene un desencadenador diario que especifica cuándo se ejecuta la tarea y una acción ejecutable que se ejecuta Bloc de notas.

En el procedimiento siguiente se describe cómo programar una tarea para iniciar un ejecutable a las 8:00 a. m. el lunes de cada semana.

**Para programar Bloc de notas iniciar a las 8:00 a. m. el lunes de cada semana**

1.  Cree un [**objeto TaskService.**](taskservice.md) Este objeto permite crear la tarea en una carpeta especificada.
2.  Obtenga una carpeta de tareas y cree una tarea. Use el [**método TaskService.GetFolder**](taskservice-getfolder.md) para obtener la carpeta donde se almacena la tarea y el método [**TaskService.NewTask**](taskservice-newtask.md) para crear el objeto [**TaskDefinition**](taskdefinition.md) que representa la tarea.
3.  Defina información sobre la tarea mediante el [**objeto TaskDefinition.**](taskdefinition.md) Use la propiedad [**TaskDefinition.Configuración**](taskdefinition-settings.md) para definir la configuración que determina cómo realiza la tarea el servicio Programador de tareas y la propiedad [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) para definir la información que describe la tarea.
4.  Cree un desencadenador semanal mediante la [**propiedad TaskDefinition.Triggers.**](taskdefinition-triggers.md) Esta propiedad proporciona acceso al [**objeto TriggerCollection**](triggercollection.md) que se usa para crear el desencadenador.

    Use el [**método TriggerCollection.Create**](triggercollection-create.md) (especificando el tipo de desencadenador que desea crear) para crear un desencadenador semanal.

    Establezca la [**propiedad WeeklyTrigger.StartBoundary**](trigger-startboundary.md) para especificar cuándo se activa el desencadenador y la hora del día en que se ejecuta la tarea. En este ejemplo, el desencadenador se activa el 1 de enero de 2005 y la tarea se ejecuta a las 8:00 a. m.

    Establezca la [**propiedad WeeklyTrigger.EndBoundary**](trigger-endboundary.md)para especificar cuándo se desactiva el desencadenador. En este ejemplo, el desencadenador se desactiva el 1 de enero de 2015.

    Establezca la [**propiedad WeeklyTrigger.DaysOfWeek**](weeklytrigger-daysofweek.md) para especificar los días de la semana en los que se ejecuta la tarea. En este ejemplo, la tarea se ejecuta el lunes.

    Establezca la [**propiedad WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md)para especificar el intervalo entre las semanas de la programación. En este ejemplo, la tarea se ejecuta cada semana.

5.  Cree una acción para que la tarea se ejecute mediante la [**propiedad TaskDefinition.Actions.**](taskdefinition-actions.md) Esta propiedad proporciona acceso al [**objeto ActionCollection**](actioncollection.md) utilizado para crear la acción. Use el [**método ActionCollection.Create**](actioncollection-create.md) para especificar el tipo de acción que desea crear. En este ejemplo se [**usa un objeto ExecAction,**](execaction.md) que representa una acción que ejecuta una operación de línea de comandos.
6.  Registre la tarea mediante el [**método TaskFolder.RegisterTaskDefinition.**](taskfolder-registertaskdefinition.md) En este ejemplo, la tarea se iniciará Bloc de notas a las 8:00 a. m. el lunes de cada semana.

En el siguiente ejemplo de VBScript se muestra cómo programar una tarea para ejecutar Bloc de notas todos los días a las 8:00 a. m.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




