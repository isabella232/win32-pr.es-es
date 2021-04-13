---
title: Ejemplo de desencadenador semanal (XML)
description: El XML de este ejemplo define una tarea que inicia el Bloc de notas semanalmente.
ms.assetid: 1911e8b1-2583-440c-a6ed-d71080b60987
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf8c2683311aecc427e9570a0452c746375eca01
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/24/2020
ms.locfileid: "104420124"
---
# <a name="weekly-trigger-example-xml"></a><span data-ttu-id="73645-103">Ejemplo de desencadenador semanal (XML)</span><span class="sxs-lookup"><span data-stu-id="73645-103">Weekly Trigger Example (XML)</span></span>

<span data-ttu-id="73645-104">El XML de este ejemplo define una tarea que inicia el Bloc de notas semanalmente.</span><span class="sxs-lookup"><span data-stu-id="73645-104">The XML in this example defines a task that starts Notepad on a bi-weekly basis.</span></span>

<span data-ttu-id="73645-105">Para registrar una tarea que se define en XML, puede usar la función [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripting) o la herramienta de línea de comandos Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="73645-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="73645-106">Si usa la herramienta Schtasks.exe (que se encuentra en el directorio C: \\ Windows \\ system32), puede usar el siguiente comando para registrar la tarea: **Schtasks/Create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="73645-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-every-other-week-on-monday-at-800-am"></a><span data-ttu-id="73645-107">Para definir una tarea para iniciar el Bloc de notas cada dos semanas el lunes a las 8:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="73645-107">To define a task to start Notepad every other week on Monday at 8:00 AM</span></span>

<span data-ttu-id="73645-108">En el ejemplo de XML siguiente se muestra cómo definir una tarea con una sola acción de ejecución (iniciando el Bloc de notas), un único desencadenador de calendario (inicia la tarea cada dos semanas el lunes a las 8:00 A.M.) y otras opciones de configuración de tareas que afectan al modo en que la tarea se controla mediante Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="73645-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single calendar trigger (starts the task every other week on Monday at 8:00 AM), and several other task settings that affect how the task is handled by Task Scheduler.</span></span>


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a bi-weekly basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-05-01T09:00:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every other week on Monday at 8:00am.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-05-02T08:00:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00</EndBoundary>
            <ScheduleByWeek>
                <WeeksInterval>2</WeeksInterval>
                <DaysOfWeek>
                    <Monday/>
                </DaysOfWeek>
            </ScheduleByWeek>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="73645-109">Elementos de esquema TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="73645-109">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="73645-110">Estos son algunos elementos importantes que se deben tener en cuenta al usar este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="73645-110">Here are some important elements to keep in mind when using this example.</span></span>

-   [<span data-ttu-id="73645-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="73645-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md)

    <span data-ttu-id="73645-112">Contiene información de registro sobre la tarea.</span><span class="sxs-lookup"><span data-stu-id="73645-112">Contains registration information about the task.</span></span>

-   [<span data-ttu-id="73645-113">**Desencadenadores**</span><span class="sxs-lookup"><span data-stu-id="73645-113">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)

    <span data-ttu-id="73645-114">Define el desencadenador que inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="73645-114">Defines the trigger that starts the task.</span></span>

-   [<span data-ttu-id="73645-115">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="73645-115">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)

    <span data-ttu-id="73645-116">Define el desencadenador de calendario semanal.</span><span class="sxs-lookup"><span data-stu-id="73645-116">Defines the weekly calendar trigger.</span></span> <span data-ttu-id="73645-117">En este caso, solo se usan cuatro elementos secundarios: los límites inicial y final que especifican Cuándo se activa y desactiva el desencadenador, la programación semanal y los días de la semana en los que se ejecutará la tarea.</span><span class="sxs-lookup"><span data-stu-id="73645-117">In this case, only four child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, the weekly schedule, and the days of the week that the task will run on.</span></span> <span data-ttu-id="73645-118">El elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) es un elemento necesario para los desencadenadores de calendario.</span><span class="sxs-lookup"><span data-stu-id="73645-118">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for calendar triggers.</span></span>

-   [<span data-ttu-id="73645-119">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="73645-119">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)

    <span data-ttu-id="73645-120">Define la programación semanal.</span><span class="sxs-lookup"><span data-stu-id="73645-120">Defines the weekly schedule.</span></span> <span data-ttu-id="73645-121">En este caso, el intervalo se establece para realizar la tarea cada dos semanas el lunes.</span><span class="sxs-lookup"><span data-stu-id="73645-121">In this case, the interval is set to perform the task every other week on a Monday.</span></span>

-   [<span data-ttu-id="73645-122">**Principal**</span><span class="sxs-lookup"><span data-stu-id="73645-122">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md)

    <span data-ttu-id="73645-123">Define el contexto de seguridad en el que se ejecuta una tarea.</span><span class="sxs-lookup"><span data-stu-id="73645-123">Defines the security context that a task runs under.</span></span>

-   [<span data-ttu-id="73645-124">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="73645-124">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)

    <span data-ttu-id="73645-125">Define la configuración de la tarea que Programador de tareas usa para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="73645-125">Defines the task settings that Task Scheduler uses to perform the task.</span></span>

-   [<span data-ttu-id="73645-126">**Acciones**</span><span class="sxs-lookup"><span data-stu-id="73645-126">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)

    <span data-ttu-id="73645-127">Define las acciones que realiza la tarea (en este caso, ejecutar el Bloc de notas).</span><span class="sxs-lookup"><span data-stu-id="73645-127">Defines the actions the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="73645-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="73645-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73645-129">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="73645-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




