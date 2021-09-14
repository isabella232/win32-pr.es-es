---
title: Ejemplo de desencadenador de registro (scripting)
description: En este ejemplo de scripting se muestra cómo crear una tarea que está programada para ejecutarse Bloc de notas cuando se registra una tarea.
ms.assetid: 956b3a21-7d36-4d06-be84-690884ba653a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bce6271927e74e31f25b3ac86783b35899bbd862
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172933"
---
# <a name="registration-trigger-example-scripting"></a>Ejemplo de desencadenador de registro (scripting)

En este ejemplo de scripting se muestra cómo crear una tarea que está programada para ejecutarse Bloc de notas cuando se registra una tarea. La tarea contiene un desencadenador de registro que especifica un límite inicial y un límite final para la tarea. El límite inicial especifica cuándo se activa el desencadenador. La tarea también contiene una acción que especifica la tarea que se ejecutará Bloc de notas.

> [!Note]  
> Cuando se actualiza una tarea con un desencadenador de registro, la tarea se ejecutará después de que se produzca la actualización.

 

En el procedimiento siguiente se describe cómo programar un ejecutable como Bloc de notas iniciar cuando se registra una tarea.

**Para programar Bloc de notas iniciar cuando se registra una tarea**

1.  Cree un [**objeto TaskService.**](taskservice.md) Este objeto permite crear la tarea en una carpeta especificada.
2.  Obtenga una carpeta de tareas y cree una tarea. Use el [**método TaskService.GetFolder**](taskservice-getfolder.md) para obtener la carpeta donde se almacena la tarea y el método [**TaskService.NewTask**](taskservice-newtask.md) para crear el objeto [**TaskDefinition**](taskdefinition.md) que representa la tarea.
3.  Defina información sobre la tarea mediante el [**objeto TaskDefinition.**](taskdefinition.md) Use la propiedad [**TaskDefinition.Configuración**](taskdefinition-settings.md) para definir la configuración que determina cómo realiza la tarea el servicio Programador de tareas y la propiedad [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) para definir la información que describe la tarea.
4.  Cree un desencadenador de registro mediante [**la propiedad TaskDefinition.Triggers.**](taskdefinition-triggers.md) Esta propiedad proporciona acceso al [**objeto TriggerCollection.**](triggercollection.md) Use el [**método TriggerCollection.Create**](triggercollection-create.md) (especificando el tipo de desencadenador que desea crear) para crear un desencadenador de registro.
5.  Cree una acción para que la tarea se ejecute mediante la [**propiedad TaskDefinition.Actions.**](taskdefinition-actions.md) Esta propiedad proporciona acceso al [**objeto ActionCollection.**](actioncollection.md) Use el [**método ActionCollection.Create**](actioncollection-create.md) para especificar el tipo de acción que desea crear. En este ejemplo se [**usa un objeto ExecAction,**](execaction.md) que representa una acción que inicia un ejecutable.
6.  Registre la tarea mediante el [**método TaskFolder.RegisterTaskDefinition.**](taskfolder-registertaskdefinition.md)

En el siguiente ejemplo de VBScript se muestra cómo crear una tarea que programa Bloc de notas ejecutar cuando se registra la tarea.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




