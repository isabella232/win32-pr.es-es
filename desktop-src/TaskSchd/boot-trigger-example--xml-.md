---
title: Ejemplo de desencadenador de arranque (XML)
description: En el código XML de este ejemplo se define una tarea que inicia el Bloc de notas al arrancar el sistema.
ms.assetid: 6dd7155c-6163-4408-9cef-c313134beeb0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8f9f5ea10f92979b0798b12a6225f8ba74a38ee
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/24/2020
ms.locfileid: "104358613"
---
# <a name="boot-trigger-example-xml"></a><span data-ttu-id="13da7-103">Ejemplo de desencadenador de arranque (XML)</span><span class="sxs-lookup"><span data-stu-id="13da7-103">Boot Trigger Example (XML)</span></span>

<span data-ttu-id="13da7-104">En el código XML de este ejemplo se define una tarea que inicia el Bloc de notas al arrancar el sistema.</span><span class="sxs-lookup"><span data-stu-id="13da7-104">The XML in this example defines a task that starts Notepad when the system is booted.</span></span>

<span data-ttu-id="13da7-105">Para registrar una tarea que se define en XML, puede usar la función [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripting) o la herramienta de línea de comandos Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="13da7-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="13da7-106">Si usa la herramienta Schtasks.exe (que se encuentra en el directorio C: \\ Windows \\ system32), puede usar el siguiente comando para registrar la tarea: **Schtasks/Create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="13da7-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a><span data-ttu-id="13da7-107">Para definir una tarea para iniciar el Bloc de notas en el arranque del sistema</span><span class="sxs-lookup"><span data-stu-id="13da7-107">To define a task to start Notepad on system boot</span></span>

<span data-ttu-id="13da7-108">En el ejemplo de XML siguiente se muestra cómo definir una tarea con una única acción de ejecución (iniciando el Bloc de notas), un único desencadenador de arranque que inicia la tarea cuando se arranca el sistema y otras opciones de configuración de tareas que afectan al modo en que la tarea la controla el Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="13da7-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single boot trigger that starts the task when the system is booted, and several other task settings that affect how the task is handled by the Task Scheduler.</span></span>


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the system is booted.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad on system boot.</Description>
    </RegistrationInfo>
    <Triggers>
        <BootTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <ExecutionTimeLimit>PT5M</ExecutionTimeLimit>
        </BootTrigger>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="13da7-109">Elementos de esquema TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="13da7-109">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="13da7-110">Estos son algunos elementos importantes que se deben tener en cuenta al usar este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="13da7-110">Here are some important elements to keep in mind when using this example.</span></span>

-   <span data-ttu-id="13da7-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contiene información de registro sobre la tarea.</span><span class="sxs-lookup"><span data-stu-id="13da7-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="13da7-112">[**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md): define el desencadenador que inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="13da7-112">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="13da7-113">[**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md): define el desencadenador de arranque.</span><span class="sxs-lookup"><span data-stu-id="13da7-113">[**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md): Defines the boot trigger.</span></span> <span data-ttu-id="13da7-114">En este caso, solo se usan dos elementos secundarios: los límites inicial y final que especifican Cuándo se activa y desactiva el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="13da7-114">In this case only two child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated.</span></span>
-   <span data-ttu-id="13da7-115">[**Principal**](taskschedulerschema-principal-principaltype-element.md): define el contexto de seguridad en el que se ejecuta una tarea.</span><span class="sxs-lookup"><span data-stu-id="13da7-115">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="13da7-116">[**Configuración**](taskschedulerschema-settings-tasktype-element.md): define la configuración de la tarea que utiliza el programador de tareas para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="13da7-116">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="13da7-117">[**Acciones**](taskschedulerschema-actions-tasktype-element.md): define las acciones que realiza la tarea.</span><span class="sxs-lookup"><span data-stu-id="13da7-117">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions the task performs.</span></span> <span data-ttu-id="13da7-118">En este caso, se ejecuta el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="13da7-118">In this case, running Notepad.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13da7-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="13da7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13da7-120">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="13da7-120">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




