---
title: Ejemplo de desencadenador de tiempo (XML)
description: El XML de este ejemplo define una tarea que inicia el Bloc de notas en un momento determinado.
ms.assetid: dde3627b-e268-45ef-9c26-08877bfe484f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c683c831aa3a07eeb3a41db9cd2768caeb6307a
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/24/2020
ms.locfileid: "104358610"
---
# <a name="time-trigger-example-xml"></a><span data-ttu-id="238e7-103">Ejemplo de desencadenador de tiempo (XML)</span><span class="sxs-lookup"><span data-stu-id="238e7-103">Time Trigger Example (XML)</span></span>

<span data-ttu-id="238e7-104">El XML de este ejemplo define una tarea que inicia el Bloc de notas en un momento determinado.</span><span class="sxs-lookup"><span data-stu-id="238e7-104">The XML in this example defines a task that starts Notepad at a specific time.</span></span>

<span data-ttu-id="238e7-105">Para registrar una tarea que se define en XML, puede usar la función [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripting) o la herramienta de línea de comandos Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="238e7-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="238e7-106">Si usa la herramienta Schtasks.exe (que se encuentra en el directorio C: \\ Windows \\ system32), puede usar el siguiente comando para registrar la tarea: **Schtasks/Create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="238e7-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-at-a-specific-time"></a><span data-ttu-id="238e7-107">Para definir una tarea para iniciar el Bloc de notas en un momento específico</span><span class="sxs-lookup"><span data-stu-id="238e7-107">To define a task to start Notepad at a specific time</span></span>

<span data-ttu-id="238e7-108">En el ejemplo de XML siguiente se muestra cómo definir una tarea con una sola acción de ejecución (iniciando el Bloc de notas), un único desencadenador de tiempo que inicia la tarea a una hora especificada y otras opciones de configuración de tareas que afectan al modo en que el Programador de tareas controla la tarea.</span><span class="sxs-lookup"><span data-stu-id="238e7-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single time trigger that starts the task at a specified time, and several other task settings that affect how the task is handled by the Task Scheduler.</span></span>


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe at a specific time.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after at a specified time.</Description>
    </RegistrationInfo>
    <Triggers>
        <TimeTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <ExecutionTimeLimit>PT5M</ExecutionTimeLimit>
        </TimeTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <UserId>Administrator</UserId>
            <LogonType>InteractiveToken</LogonType>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="238e7-109">Elementos de esquema TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="238e7-109">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="238e7-110">A continuación se muestran algunos elementos importantes que se deben tener en cuenta al usar este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="238e7-110">The following are some important elements to keep in mind when using this example:</span></span>

-   <span data-ttu-id="238e7-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contiene información de registro sobre la tarea.</span><span class="sxs-lookup"><span data-stu-id="238e7-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="238e7-112">[**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md): define el desencadenador que inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="238e7-112">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="238e7-113">[**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md): define el desencadenador de tiempo.</span><span class="sxs-lookup"><span data-stu-id="238e7-113">[**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md): Defines the time trigger.</span></span> <span data-ttu-id="238e7-114">En este caso, se usan tres elementos secundarios: los límites inicial y final que especifican Cuándo se activa y desactiva el desencadenador, y el límite de tiempo de ejecución que especifica la cantidad máxima de tiempo que el desencadenador puede iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="238e7-114">In this case, three child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, and the execution time limit that specifies the maximum amount of time in which the task can be started by the trigger.</span></span> <span data-ttu-id="238e7-115">El elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) es un elemento necesario para los desencadenadores de hora.</span><span class="sxs-lookup"><span data-stu-id="238e7-115">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time triggers.</span></span>
-   <span data-ttu-id="238e7-116">[**Principal**](taskschedulerschema-principal-principaltype-element.md): define el contexto de seguridad en el que se ejecuta una tarea.</span><span class="sxs-lookup"><span data-stu-id="238e7-116">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="238e7-117">[**Configuración**](taskschedulerschema-settings-tasktype-element.md): define la configuración de la tarea que utiliza el programador de tareas para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="238e7-117">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="238e7-118">[**Acciones**](taskschedulerschema-actions-tasktype-element.md): define las acciones que realiza la tarea (en este caso, ejecutar el Bloc de notas).</span><span class="sxs-lookup"><span data-stu-id="238e7-118">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions that the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="238e7-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="238e7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="238e7-120">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="238e7-120">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




