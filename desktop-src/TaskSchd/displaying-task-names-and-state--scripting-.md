---
title: Mostrar nombres de tarea y Estados (scripting)
description: Este ejemplo de scripting muestra cómo enumerar las tareas de una carpeta de tareas y mostrar los valores de las propiedades de cada tarea.
ms.assetid: 2a84a752-fbf3-4041-8b0a-304f89a49354
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e7a8f22977f8cfd2d40b3c37a1cc8d7bcb5259e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418859"
---
# <a name="displaying-task-names-and-states-scripting"></a><span data-ttu-id="a3357-103">Mostrar nombres de tarea y Estados (scripting)</span><span class="sxs-lookup"><span data-stu-id="a3357-103">Displaying Task Names and States (Scripting)</span></span>

<span data-ttu-id="a3357-104">Este ejemplo de scripting muestra cómo enumerar las tareas de una carpeta de tareas y mostrar los valores de las propiedades de cada tarea.</span><span class="sxs-lookup"><span data-stu-id="a3357-104">This scripting example shows how to enumerate tasks in a task folder and display property values from each task.</span></span>

<span data-ttu-id="a3357-105">En el procedimiento siguiente se describe cómo mostrar los nombres de tarea y los Estados de todas las tareas de una carpeta de tareas.</span><span class="sxs-lookup"><span data-stu-id="a3357-105">The following procedure describes how to display task names and states for all the tasks in a task folder.</span></span>

<span data-ttu-id="a3357-106">**Para mostrar los nombres de tarea y el estado de todas las tareas de una carpeta de tareas**</span><span class="sxs-lookup"><span data-stu-id="a3357-106">**To display task names and state for all the tasks in a task folder**</span></span>

1.  <span data-ttu-id="a3357-107">Cree el objeto [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="a3357-107">Create the [**TaskService**](taskservice.md) object.</span></span>

    <span data-ttu-id="a3357-108">Este objeto le permite conectarse al servicio Programador de tareas y obtener acceso a una carpeta de tareas específica.</span><span class="sxs-lookup"><span data-stu-id="a3357-108">This object allows you to connect to the Task Scheduler service and access a specific task folder.</span></span>

2.  <span data-ttu-id="a3357-109">Obtenga una carpeta de tareas que contenga las tareas sobre las que desea obtener información.</span><span class="sxs-lookup"><span data-stu-id="a3357-109">Get a task folder that holds the tasks you want information about.</span></span>

    <span data-ttu-id="a3357-110">Use el método [**TaskService. GetFolder**](taskservice-getfolder.md) para obtener la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a3357-110">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder.</span></span>

3.  <span data-ttu-id="a3357-111">Obtiene la colección de tareas de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a3357-111">Get the collection of tasks from the folder.</span></span>

    <span data-ttu-id="a3357-112">Use el método [**TaskFolder. GetTasks**](taskfolder-gettasks.md) para obtener la colección de tareas ([**RegisteredTaskCollection**](registeredtaskcollection.md)).</span><span class="sxs-lookup"><span data-stu-id="a3357-112">Use the [**TaskFolder.GetTasks**](taskfolder-gettasks.md) method to get the collection of tasks ([**RegisteredTaskCollection**](registeredtaskcollection.md)).</span></span>

4.  <span data-ttu-id="a3357-113">Obtiene el número de tareas de la colección y enumera cada tarea de la colección.</span><span class="sxs-lookup"><span data-stu-id="a3357-113">Get the number of tasks in the collection and enumerate through each task in the collection.</span></span>

    <span data-ttu-id="a3357-114">Use la colección [**RegisteredTaskCollection**](registeredtaskcollection.md) de objetos para obtener una instancia de objeto [**RegisteredTask**](registeredtask.md) .</span><span class="sxs-lookup"><span data-stu-id="a3357-114">Use the [**RegisteredTaskCollection**](registeredtaskcollection.md) collection of objects to get a [**RegisteredTask**](registeredtask.md) object instance.</span></span> <span data-ttu-id="a3357-115">Cada instancia contendrá una tarea en la colección.</span><span class="sxs-lookup"><span data-stu-id="a3357-115">Each instance will contain a task in the collection.</span></span> <span data-ttu-id="a3357-116">A continuación, puede mostrar la información (valores de propiedad) de cada tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="a3357-116">You can then display the information (property values) from each registered task.</span></span>

<span data-ttu-id="a3357-117">En el siguiente ejemplo de VBScript se muestra cómo enumerar a través de una colección de tareas registradas en la carpeta de tareas raíz y mostrar el nombre y el estado de cada tarea.</span><span class="sxs-lookup"><span data-stu-id="a3357-117">The following VBScript example shows how to enumerate through a collection of registered tasks in the root task folder and display the name and state for each task.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a3357-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3357-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3357-119">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="a3357-119">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




