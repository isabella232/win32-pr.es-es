---
title: Ejemplo de desencadenador de arranque (scripting)
description: En este ejemplo de scripting se muestra cómo crear una tarea que está programada para ejecutarse Bloc de notas cuando se inicia el sistema.
ms.assetid: 73ae9cc4-ef89-4390-ac05-8a773f45fa46
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ff02bef70b4003c4e7b6e9aff03e2d615f24d7e15707cddcae3a4637ff2b11f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002523"
---
# <a name="boot-trigger-example-scripting"></a>Ejemplo de desencadenador de arranque (scripting)

En este ejemplo de scripting se muestra cómo crear una tarea que está programada para ejecutarse Bloc de notas cuando se inicia el sistema. La tarea contiene un desencadenador de arranque que especifica un límite de inicio y un tiempo de retraso para que la tarea se inicie después de arrancar el sistema. La tarea también contiene una acción que especifica la tarea que se ejecutará Bloc de notas. La tarea se registra mediante la cuenta de servicio local como contexto de seguridad para ejecutar la tarea.

En el procedimiento siguiente se describe cómo programar un ejecutable como Bloc de notas iniciarse cuando se inicia el sistema.

**Para programar Bloc de notas que se inicie cuando se arranque el sistema**

1.  Cree un [**objeto TaskService.**](taskservice.md) Este objeto permite crear la tarea en una carpeta especificada.
2.  Obtenga una carpeta de tareas y cree una tarea. Use el [**método TaskService.GetFolder**](taskservice-getfolder.md) para obtener la carpeta donde se almacena la tarea y el método [**TaskService.NewTask**](taskservice-newtask.md) para crear el objeto [**TaskDefinition**](taskdefinition.md) que representa la tarea.
3.  Defina información sobre la tarea mediante el [**objeto TaskDefinition.**](taskdefinition.md) Use la propiedad [**TaskDefinition.Configuración**](taskdefinition-settings.md) para definir la configuración que determina cómo realiza la tarea el servicio Programador de tareas y la propiedad [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) para definir la información que describe la tarea.
4.  Cree un desencadenador de inicio de sesión mediante [**la propiedad TaskDefinition.Triggers.**](taskdefinition-triggers.md) Esta propiedad proporciona acceso al [**objeto TriggerCollection.**](triggercollection.md) Use el [**método TriggerCollection.Create**](triggercollection-create.md) (especificando el tipo de desencadenador que desea crear) para crear un desencadenador de arranque. Cuando cree el desencadenador, establezca las propiedades [**StartBoundary**](trigger-startboundary.md) y [**EndBoundary**](trigger-endboundary.md) del desencadenador para activarlo y desactivarlo. También puede especificar un valor para la propiedad [**Delay**](boottrigger-delay.md) del desencadenador de arranque.
5.  Cree una acción para que la tarea se ejecute mediante la [**propiedad TaskDefinition.Actions.**](taskdefinition-actions.md) Esta propiedad proporciona acceso al [**objeto ActionCollection.**](actioncollection.md) Use el [**método ActionCollection.Create**](actioncollection-create.md) para especificar el tipo de acción que desea crear. En este ejemplo se [**usa un objeto ExecAction,**](execaction.md) que representa una acción que inicia un ejecutable.
6.  Registre la tarea mediante el [**método TaskFolder.RegisterTaskDefinition.**](taskfolder-registertaskdefinition.md) La tarea se registra mediante la cuenta de servicio local como contexto de seguridad para ejecutar la tarea.

En el siguiente ejemplo de VBScript se muestra cómo programar una tarea para que se ejecute Bloc de notas 30 segundos después de arrancar el sistema.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




