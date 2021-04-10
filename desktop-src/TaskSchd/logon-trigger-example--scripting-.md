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
# <a name="logon-trigger-example-scripting"></a><span data-ttu-id="cee51-103">Ejemplo de desencadenador Logon (scripting)</span><span class="sxs-lookup"><span data-stu-id="cee51-103">Logon Trigger Example (Scripting)</span></span>

<span data-ttu-id="cee51-104">Este ejemplo de scripting muestra cómo crear una tarea programada para ejecutar el Bloc de notas cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="cee51-104">This scripting example shows how to create a task that is scheduled to execute Notepad when a user logs on.</span></span> <span data-ttu-id="cee51-105">La tarea contiene un desencadenador Logon que especifica un límite de inicio para que la tarea se inicie y un identificador de usuario que especifica el usuario.</span><span class="sxs-lookup"><span data-stu-id="cee51-105">The task contains a logon trigger that specifies a start boundary for the task to start and a user identifier that specifies the user.</span></span> <span data-ttu-id="cee51-106">La tarea se registra mediante el grupo administradores como contexto de seguridad para ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="cee51-106">The task is registered using the Administrators group as a security context to run the task.</span></span>

<span data-ttu-id="cee51-107">En el procedimiento siguiente se describe cómo programar un ejecutable, como el Bloc de notas, para que se inicie cuando un usuario especificado inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="cee51-107">The following procedure describes how to schedule an executable such as Notepad to start when a specified user logs on.</span></span>

<span data-ttu-id="cee51-108">**Para programar el inicio del Bloc de notas cuando un usuario inicia sesión**</span><span class="sxs-lookup"><span data-stu-id="cee51-108">**To schedule Notepad to start when a user logs on**</span></span>

1.  <span data-ttu-id="cee51-109">Cree un objeto [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="cee51-109">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="cee51-110">Este objeto permite crear la tarea en una carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="cee51-110">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="cee51-111">Obtener una carpeta de tareas y crear una tarea.</span><span class="sxs-lookup"><span data-stu-id="cee51-111">Get a task folder and create a task.</span></span> <span data-ttu-id="cee51-112">Use el método [**TaskService. GetFolder**](taskservice-getfolder.md) para obtener la carpeta donde se almacena la tarea y el método [**TaskService. newtask**](taskservice-newtask.md) para crear el objeto [**TaskDefinition**](taskdefinition.md) que representa la tarea.</span><span class="sxs-lookup"><span data-stu-id="cee51-112">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="cee51-113">Defina la información sobre la tarea mediante el objeto [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="cee51-113">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="cee51-114">Use la propiedad [**TaskDefinition. Settings**](taskdefinition-settings.md) para definir la configuración que determina cómo el servicio de programador de tareas realiza la tarea y la propiedad [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) para definir la información que describe la tarea.</span><span class="sxs-lookup"><span data-stu-id="cee51-114">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="cee51-115">Cree un desencadenador Logon mediante la propiedad [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="cee51-115">Create a logon trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="cee51-116">Esta propiedad proporciona acceso al objeto [**TriggerCollection**](triggercollection.md) .</span><span class="sxs-lookup"><span data-stu-id="cee51-116">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="cee51-117">Use el método [**TriggerCollection. Create**](triggercollection-create.md) (especificando el tipo de desencadenador que desea crear) para crear un desencadenador Logon.</span><span class="sxs-lookup"><span data-stu-id="cee51-117">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger that you want to create) to create a logon trigger.</span></span> <span data-ttu-id="cee51-118">Cuando cree el desencadenador, establezca el límite inicial y el límite final del desencadenador para activar y desactivar el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="cee51-118">As you create the trigger, set the start boundary and end boundary of the trigger to activate and deactivate the trigger.</span></span> <span data-ttu-id="cee51-119">Debe establecer la propiedad [**userid**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) para el desencadenador para que las acciones de la tarea se programen para ejecutarse cuando el usuario especificado inicia sesión después del límite de inicio.</span><span class="sxs-lookup"><span data-stu-id="cee51-119">You must set the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property for the trigger so that the task's actions will be scheduled to execute when the specified user logs on after the start boundary.</span></span>
5.  <span data-ttu-id="cee51-120">Cree una acción para que la tarea se ejecute mediante la propiedad [**TaskDefinition. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="cee51-120">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="cee51-121">Esta propiedad proporciona acceso al objeto [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="cee51-121">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="cee51-122">Use el método [**ActionCollection. Create**](actioncollection-create.md) para especificar el tipo de acción que desea crear.</span><span class="sxs-lookup"><span data-stu-id="cee51-122">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="cee51-123">En este ejemplo se usa un objeto [**ExecAction**](execaction.md) , que representa una acción que inicia un ejecutable.</span><span class="sxs-lookup"><span data-stu-id="cee51-123">This example uses an [**ExecAction**](execaction.md) object, which represents an action that starts an executable.</span></span>
6.  <span data-ttu-id="cee51-124">Registre la tarea mediante el método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="cee51-124">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="cee51-125">En este ejemplo se registra la tarea para que use el grupo administradores como contexto de seguridad para ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="cee51-125">This example registers the task so that it uses the Administrators group as a security context to run the task.</span></span>

<span data-ttu-id="cee51-126">En el siguiente ejemplo de VBScript se muestra cómo programar una tarea para ejecutar el Bloc de notas cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="cee51-126">The following VBScript example shows how to schedule a task to execute Notepad when a user logs on.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="cee51-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cee51-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cee51-128">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="cee51-128">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




