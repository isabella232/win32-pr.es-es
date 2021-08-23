---
title: Mostrar nombres y estados de tareas (scripting)
description: En este ejemplo de scripting se muestra cómo enumerar las tareas de una carpeta de tareas y mostrar los valores de propiedad de cada tarea.
ms.assetid: 2a84a752-fbf3-4041-8b0a-304f89a49354
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6f3ec036b1d9d61c387495b48874bf742a9479ae0608f0e5c728a029df24709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002493"
---
# <a name="displaying-task-names-and-states-scripting"></a>Mostrar nombres y estados de tareas (scripting)

En este ejemplo de scripting se muestra cómo enumerar las tareas de una carpeta de tareas y mostrar los valores de propiedad de cada tarea.

En el procedimiento siguiente se describe cómo mostrar los nombres y estados de las tareas de una carpeta de tareas.

**Para mostrar los nombres y el estado de todas las tareas de una carpeta de tareas**

1.  Cree el [**objeto TaskService.**](taskservice.md)

    Este objeto le permite conectarse al servicio Programador de tareas y acceder a una carpeta de tareas específica.

2.  Obtenga una carpeta de tareas que contiene las tareas de las que desea obtener información.

    Use el [**método TaskService.GetFolder**](taskservice-getfolder.md) para obtener la carpeta.

3.  Obtenga la colección de tareas de la carpeta .

    Use el [**método TaskFolder.GetTasks**](taskfolder-gettasks.md) para obtener la colección de tareas ([**RegisteredTaskCollection**](registeredtaskcollection.md)).

4.  Obtenga el número de tareas de la colección y enumere a través de cada tarea de la colección.

    Use la [**colección RegisteredTaskCollection**](registeredtaskcollection.md) de objetos para obtener una [**instancia de objeto RegisteredTask.**](registeredtask.md) Cada instancia contendrá una tarea en la colección. A continuación, puede mostrar la información (valores de propiedad) de cada tarea registrada.

En el siguiente ejemplo de VBScript se muestra cómo enumerar a través de una colección de tareas registradas en la carpeta de tareas raíz y mostrar el nombre y el estado de cada tarea.


```VB
'---------------------------------------------------------
' This sample enumerates through the tasks on the local computer and
' displays their name and state.
'---------------------------------------------------------


' Create the TaskService object.
Set service = CreateObject("Schedule.Service")
call service.Connect()

' Get the task folder that contains the tasks. 
Dim rootFolder
Set rootFolder = service.GetFolder("\")
 
Dim taskCollection
Set taskCollection = rootFolder.GetTasks(0)

Dim numberOfTasks
numberOfTasks = taskCollection.Count

If numberOfTasks = 0 Then 
    Wscript.Echo "No tasks are registered."
Else
    WScript.Echo "Number of tasks registered: " & numberOfTasks
    
    Dim registeredTask
    For Each registeredTask In taskCollection
        WScript.Echo "Task Name: " & registeredTask.Name
    
        Dim taskState 
        Select Case registeredTask.State 
            Case "0"
                taskState = "Unknown"
            Case "1"
                taskState = "Disabled"
            Case "2"
                taskState = "Queued"
            Case "3"
                taskState = "Ready"
            Case "4"
                taskState = "Running"
        End Select

        WScript.Echo "    Task State: " & taskState
    Next
End If

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




