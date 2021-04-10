---
title: Ejemplo de desencadenador Logon (scripting)
description: Este ejemplo de scripting muestra cómo crear una tarea programada para ejecutar el Bloc de notas cuando un usuario inicia sesión.
ms.assetid: f25e105f-9439-4646-bdfd-609ee99a5d55
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72a8c4b5d0d67b59160eb3ed0b13885ee7e0eb51
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268551"
---
# <a name="logon-trigger-example-scripting"></a>Ejemplo de desencadenador Logon (scripting)

Este ejemplo de scripting muestra cómo crear una tarea programada para ejecutar el Bloc de notas cuando un usuario inicia sesión. La tarea contiene un desencadenador Logon que especifica un límite de inicio para que la tarea se inicie y un identificador de usuario que especifica el usuario. La tarea se registra mediante el grupo administradores como contexto de seguridad para ejecutar la tarea.

En el procedimiento siguiente se describe cómo programar un ejecutable, como el Bloc de notas, para que se inicie cuando un usuario especificado inicie sesión.

**Para programar el inicio del Bloc de notas cuando un usuario inicia sesión**

1.  Cree un objeto [**TaskService**](taskservice.md) . Este objeto permite crear la tarea en una carpeta especificada.
2.  Obtener una carpeta de tareas y crear una tarea. Use el método [**TaskService. GetFolder**](taskservice-getfolder.md) para obtener la carpeta donde se almacena la tarea y el método [**TaskService. newtask**](taskservice-newtask.md) para crear el objeto [**TaskDefinition**](taskdefinition.md) que representa la tarea.
3.  Defina la información sobre la tarea mediante el objeto [**TaskDefinition**](taskdefinition.md) . Use la propiedad [**TaskDefinition. Settings**](taskdefinition-settings.md) para definir la configuración que determina cómo el servicio de programador de tareas realiza la tarea y la propiedad [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) para definir la información que describe la tarea.
4.  Cree un desencadenador Logon mediante la propiedad [**TaskDefinition. Triggers**](taskdefinition-triggers.md) . Esta propiedad proporciona acceso al objeto [**TriggerCollection**](triggercollection.md) . Use el método [**TriggerCollection. Create**](triggercollection-create.md) (especificando el tipo de desencadenador que desea crear) para crear un desencadenador Logon. Cuando cree el desencadenador, establezca el límite inicial y el límite final del desencadenador para activar y desactivar el desencadenador. Debe establecer la propiedad [**userid**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) para el desencadenador para que las acciones de la tarea se programen para ejecutarse cuando el usuario especificado inicia sesión después del límite de inicio.
5.  Cree una acción para que la tarea se ejecute mediante la propiedad [**TaskDefinition. Actions**](taskdefinition-actions.md) . Esta propiedad proporciona acceso al objeto [**ActionCollection**](actioncollection.md) . Use el método [**ActionCollection. Create**](actioncollection-create.md) para especificar el tipo de acción que desea crear. En este ejemplo se usa un objeto [**ExecAction**](execaction.md) , que representa una acción que inicia un ejecutable.
6.  Registre la tarea mediante el método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) . En este ejemplo se registra la tarea para que use el grupo administradores como contexto de seguridad para ejecutar la tarea.

En el siguiente ejemplo de VBScript se muestra cómo programar una tarea para ejecutar el Bloc de notas cuando un usuario inicia sesión.


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe when a user logs on.
'---------------------------------------------------------

' A constant that specifies a logon trigger.
const TriggerTypeLogon = 9
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
regInfo.Description = "Task will execute Notepad when a " & _
    "specified user logs on."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a logon trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeLogon)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime
startTime = "2006-05-02T10:49:02"
endTime = "2006-05-02T10:52:02"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    ' Five minutes
trigger.Id = "LogonTriggerId"
trigger.UserId = "DOMAIN\UserName"   ' Must be a valid user account   

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
    "Test Logon Trigger", taskDefinition, createOrUpdateTask, _
    "Builtin\Administrators", , 4)

WScript.Echo "Task submitted."
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




