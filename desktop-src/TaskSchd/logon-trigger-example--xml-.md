---
title: Ejemplo de desencadenador Logon (XML)
description: El XML de este ejemplo define una tarea que inicia el Bloc de notas cuando un usuario inicia sesión.
ms.assetid: c1cce95f-7558-489e-b092-c82d55b42165
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d66766ce4cae33c3526ac9d30071ff2082ddc1f2
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/24/2020
ms.locfileid: "104420130"
---
# <a name="logon-trigger-example-xml"></a><span data-ttu-id="2569e-103">Ejemplo de desencadenador Logon (XML)</span><span class="sxs-lookup"><span data-stu-id="2569e-103">Logon Trigger Example (XML)</span></span>

<span data-ttu-id="2569e-104">El XML de este ejemplo define una tarea que inicia el Bloc de notas cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="2569e-104">The XML in this example defines a task that starts Notepad when a user logs on.</span></span>

<span data-ttu-id="2569e-105">Para registrar una tarea que se define en XML, puede usar la función [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripting) o la herramienta de línea de comandos Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="2569e-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="2569e-106">Si usa la herramienta Schtasks.exe (que se encuentra en el directorio C: \\ Windows \\ system32), puede usar el siguiente comando para registrar la tarea: **Schtasks/Create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="2569e-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a><span data-ttu-id="2569e-107">Para definir una tarea para iniciar el Bloc de notas en el arranque del sistema</span><span class="sxs-lookup"><span data-stu-id="2569e-107">To define a task to start Notepad on system boot</span></span>

<span data-ttu-id="2569e-108">En el ejemplo de XML siguiente se muestra cómo definir una tarea con una única acción de ejecución (iniciando el Bloc de notas), un único desencadenador de inicio de sesión que inicia la tarea cuando un usuario inicia sesión y otras opciones de configuración de tareas que afectan al modo en que la tarea se controla mediante Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="2569e-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single logon trigger that starts the task when a user logs on, and several other task settings that affect how the task is handled by Task Scheduler.</span></span>

> [!Note]  
> <span data-ttu-id="2569e-109">Establezca el valor del elemento **userid** en un nombre de usuario en el equipo en el que se ha registrado la tarea.</span><span class="sxs-lookup"><span data-stu-id="2569e-109">Set the value of the **UserId** element to a user name on the computer on which the task is registered.</span></span>

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when a user logs on.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad when a specified user logs on.</Description>
    </RegistrationInfo>
    <Triggers>
        <LogonTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <UserId>DOMAIN_NAME\UserName</UserId>
        </LogonTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <GroupId>Builtin\Administrators</GroupId>
        </Principal>
    </Principals>
    <Settings>
        <Enabled>true</Enabled>
        <AllowStartOnDemand>true</AllowStartOnDemand>
        <AllowHardTerminate>true</AllowHardTerminate>
    </Settings>
    <Actions>
        <Exec>
            <Command>notepad.exe</Command>
        </Exec>
    </Actions>
</Task>
```



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="2569e-110">Elementos de esquema TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="2569e-110">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="2569e-111">A continuación se muestran algunos elementos importantes que se deben tener en cuenta al usar este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2569e-111">The following are some important elements to keep in mind when using this example:</span></span>

-   <span data-ttu-id="2569e-112">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contiene información de registro sobre la tarea.</span><span class="sxs-lookup"><span data-stu-id="2569e-112">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="2569e-113">[**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md): define el desencadenador que inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="2569e-113">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="2569e-114">[**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md): define el desencadenador Logon.</span><span class="sxs-lookup"><span data-stu-id="2569e-114">[**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md): Defines the logon trigger.</span></span> <span data-ttu-id="2569e-115">En este caso, se usan tres elementos secundarios: los límites inicial y final que especifican Cuándo se activa y desactiva el desencadenador, y el elemento [**userid**](taskschedulerschema-userid-logontriggertype-element.md) que identifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="2569e-115">In this case, three child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, and the [**UserId**](taskschedulerschema-userid-logontriggertype-element.md) element that identifier of the user.</span></span> <span data-ttu-id="2569e-116">La tarea se inicia cuando este usuario inicia sesión en el equipo.</span><span class="sxs-lookup"><span data-stu-id="2569e-116">The task is started when this user logs on to the computer..</span></span>
-   <span data-ttu-id="2569e-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): define el contexto de seguridad en el que se ejecuta una tarea.</span><span class="sxs-lookup"><span data-stu-id="2569e-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="2569e-118">[**Configuración**](taskschedulerschema-settings-tasktype-element.md): define la configuración de la tarea que utiliza el programador de tareas para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="2569e-118">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="2569e-119">[**Acciones**](taskschedulerschema-actions-tasktype-element.md): define las acciones que realiza la tarea.</span><span class="sxs-lookup"><span data-stu-id="2569e-119">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions the task performs.</span></span> <span data-ttu-id="2569e-120">En este caso, se ejecuta el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="2569e-120">In this case, running Notepad.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2569e-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2569e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2569e-122">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="2569e-122">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




