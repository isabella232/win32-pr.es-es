---
title: Ejemplo de desencadenador diario (XML)
description: En el código XML de este ejemplo se define una tarea que inicia el Bloc de notas a las 8 00 A.M. todos los días.
ms.assetid: b7818071-12b6-41df-85b9-282c08cf6e31
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe673a764e6e7e4e3ae5089022da2232821d9184
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/24/2020
ms.locfileid: "103785524"
---
# <a name="daily-trigger-example-xml"></a><span data-ttu-id="80ac9-103">Ejemplo de desencadenador diario (XML)</span><span class="sxs-lookup"><span data-stu-id="80ac9-103">Daily Trigger Example (XML)</span></span>

<span data-ttu-id="80ac9-104">En el código XML de este ejemplo se define una tarea que inicia el Bloc de notas a las 8:00 A.M. todos los días.</span><span class="sxs-lookup"><span data-stu-id="80ac9-104">The XML in this example defines a task that starts Notepad at 8:00 AM every day.</span></span> <span data-ttu-id="80ac9-105">En el ejemplo también se muestra cómo establecer un patrón de repetición para que el desencadenador repita la tarea.</span><span class="sxs-lookup"><span data-stu-id="80ac9-105">The example also shows how to set a repetition pattern for the trigger to repeat the task.</span></span>

<span data-ttu-id="80ac9-106">Para registrar una tarea que se define en XML, puede usar la función [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripting) o la herramienta de línea de comandos Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="80ac9-106">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="80ac9-107">Si usa la herramienta Schtasks.exe (que se encuentra en el directorio C: \\ Windows \\ system32), puede usar el siguiente comando para registrar la tarea: **Schtasks/Create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="80ac9-107">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-every-day-at-800-am"></a><span data-ttu-id="80ac9-108">Para definir una tarea para iniciar el Bloc de notas todos los días a las 8:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="80ac9-108">To define a task to start Notepad every day at 8:00 AM</span></span>

<span data-ttu-id="80ac9-109">En el ejemplo de XML siguiente se muestra cómo definir una tarea con una sola acción de ejecución (iniciando el Bloc de notas), un único desencadenador de calendario (inicia la tarea todos los días a las 8:00 AM) y otras opciones de configuración de tareas que afectan al modo en que la tarea se controla mediante Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="80ac9-109">The following XML example shows how to define a task with a single execution action (starting Notepad), a single calendar trigger (starts the task every day at 8:00 AM), and several other task settings that affect how the task is handled by Task Scheduler.</span></span>


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a daily basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every day.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Repetition>
                <Interval>PT1M</Interval>
                <Duration>PT4M</Duration>
            </Repetition>
            <ScheduleByDay>
                <DaysInterval>1</DaysInterval>
            </ScheduleByDay>
        </CalendarTrigger>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="80ac9-110">Elementos de esquema TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="80ac9-110">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="80ac9-111">Estos son algunos elementos importantes que se deben tener en cuenta al usar este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="80ac9-111">Here are some important elements to keep in mind when using this example.</span></span>

-   [<span data-ttu-id="80ac9-112">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="80ac9-112">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md)

    <span data-ttu-id="80ac9-113">Contiene información de registro sobre la tarea.</span><span class="sxs-lookup"><span data-stu-id="80ac9-113">Contains registration information about the task.</span></span>

-   [<span data-ttu-id="80ac9-114">**Desencadenadores**</span><span class="sxs-lookup"><span data-stu-id="80ac9-114">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)

    <span data-ttu-id="80ac9-115">Define el desencadenador que inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="80ac9-115">Defines the trigger that starts the task.</span></span>

-   [<span data-ttu-id="80ac9-116">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="80ac9-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)

    <span data-ttu-id="80ac9-117">Define el desencadenador de calendario diario.</span><span class="sxs-lookup"><span data-stu-id="80ac9-117">Defines the daily calendar trigger.</span></span> <span data-ttu-id="80ac9-118">En este caso, se usan cuatro elementos secundarios: los límites inicial y final que especifican Cuándo se activa y desactiva el desencadenador, la programación diaria y el patrón de repetición de la tarea.</span><span class="sxs-lookup"><span data-stu-id="80ac9-118">In this case, four child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, the daily schedule, and the repetition pattern for the task.</span></span> <span data-ttu-id="80ac9-119">El elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) es un elemento necesario para los desencadenadores de calendario.</span><span class="sxs-lookup"><span data-stu-id="80ac9-119">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for calendar triggers.</span></span>

-   [<span data-ttu-id="80ac9-120">**ScheduleByDay**</span><span class="sxs-lookup"><span data-stu-id="80ac9-120">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)

    <span data-ttu-id="80ac9-121">Define la programación diaria.</span><span class="sxs-lookup"><span data-stu-id="80ac9-121">Defines the daily schedule.</span></span> <span data-ttu-id="80ac9-122">En este caso, el intervalo se establece para realizar la tarea cada día.</span><span class="sxs-lookup"><span data-stu-id="80ac9-122">In this case, the interval is set to perform the task every day.</span></span>

-   <span data-ttu-id="80ac9-123">[**Principal**](taskschedulerschema-principal-principaltype-element.md): define el contexto de seguridad en el que se ejecuta una tarea.</span><span class="sxs-lookup"><span data-stu-id="80ac9-123">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   [<span data-ttu-id="80ac9-124">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="80ac9-124">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)

    <span data-ttu-id="80ac9-125">Define la configuración de la tarea que Programador de tareas usa para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="80ac9-125">Defines the task settings that Task Scheduler uses to perform the task.</span></span>

-   [<span data-ttu-id="80ac9-126">**Acciones**</span><span class="sxs-lookup"><span data-stu-id="80ac9-126">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)

    <span data-ttu-id="80ac9-127">Define las acciones que realiza la tarea (en este caso, ejecutar el Bloc de notas).</span><span class="sxs-lookup"><span data-stu-id="80ac9-127">Defines the actions the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="80ac9-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80ac9-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80ac9-129">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="80ac9-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




