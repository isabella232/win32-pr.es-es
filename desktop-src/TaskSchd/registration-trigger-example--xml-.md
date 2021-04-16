---
title: Ejemplo de desencadenador de registro (XML)
description: El XML de este ejemplo define una tarea que inicia el Bloc de notas cuando se registra la tarea.
ms.assetid: 976b9767-635f-42a6-84f5-7e0203478594
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09b9193f3b63f21464811609e8f5f19017539ecd
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/24/2020
ms.locfileid: "105685670"
---
# <a name="registration-trigger-example-xml"></a><span data-ttu-id="8a6ab-103">Ejemplo de desencadenador de registro (XML)</span><span class="sxs-lookup"><span data-stu-id="8a6ab-103">Registration Trigger Example (XML)</span></span>

<span data-ttu-id="8a6ab-104">El XML de este ejemplo define una tarea que inicia el Bloc de notas cuando se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="8a6ab-104">The XML in this example defines a task that starts Notepad when the task is registered.</span></span>

<span data-ttu-id="8a6ab-105">Para registrar una tarea que se define en XML, puede usar la función [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripting) o la herramienta de línea de comandos Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="8a6ab-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="8a6ab-106">Si usa la herramienta Schtasks.exe (que se encuentra en el directorio C: \\ Windows \\ system32), puede usar el siguiente comando para registrar la tarea: **Schtasks/Create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="8a6ab-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

> [!Note]  
> <span data-ttu-id="8a6ab-107">Cuando se actualiza una tarea con un desencadenador de registro, la tarea se ejecutará después de que se produzca la actualización.</span><span class="sxs-lookup"><span data-stu-id="8a6ab-107">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

## <a name="to-define-a-task-to-start-notepad-on-registration"></a><span data-ttu-id="8a6ab-108">Para definir una tarea para iniciar el Bloc de notas en el registro</span><span class="sxs-lookup"><span data-stu-id="8a6ab-108">To define a task to start Notepad on registration</span></span>

<span data-ttu-id="8a6ab-109">En el ejemplo de XML siguiente se muestra cómo definir una tarea con una única acción de ejecución (iniciando el Bloc de notas), un único desencadenador de registro que inicia la tarea cuando se registra y otras opciones de configuración de tareas que afectan al modo en que la tarea la controla el Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="8a6ab-109">The following XML example shows how to define a task with a single execution action (starting Notepad), a single registration trigger that starts the task when it is registered, and several other task settings that affect how the task is handled by the Task Scheduler.</span></span>

> [!Note]  
> <span data-ttu-id="8a6ab-110">Cuando se actualiza una tarea con un desencadenador de registro, la tarea se ejecutará después de que se produzca la actualización.</span><span class="sxs-lookup"><span data-stu-id="8a6ab-110">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the task is registered.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after registration.</Description>
    </RegistrationInfo>
    <Triggers>
        <RegistrationTrigger>
        </RegistrationTrigger>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="8a6ab-111">Elementos de esquema TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="8a6ab-111">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="8a6ab-112">Estos son algunos elementos importantes que se deben tener en cuenta al usar este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8a6ab-112">Here are some important elements to keep in mind when using this example.</span></span>

-   <span data-ttu-id="8a6ab-113">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contiene información de registro sobre la tarea.</span><span class="sxs-lookup"><span data-stu-id="8a6ab-113">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="8a6ab-114">[**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md): define el desencadenador que inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="8a6ab-114">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="8a6ab-115">[**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md): define el desencadenador de registro.</span><span class="sxs-lookup"><span data-stu-id="8a6ab-115">[**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md): Defines the registration trigger.</span></span> <span data-ttu-id="8a6ab-116">En este caso, solo se usan dos elementos secundarios: los límites inicial y final que especifican Cuándo se activa y desactiva el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="8a6ab-116">In this case, only two child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated.</span></span>
-   <span data-ttu-id="8a6ab-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): define el contexto de seguridad en el que se ejecuta una tarea.</span><span class="sxs-lookup"><span data-stu-id="8a6ab-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="8a6ab-118">[**Configuración**](taskschedulerschema-settings-tasktype-element.md): define la configuración de la tarea que utiliza el programador de tareas para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="8a6ab-118">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="8a6ab-119">[**Acciones**](taskschedulerschema-actions-tasktype-element.md): define las acciones que realiza la tarea.</span><span class="sxs-lookup"><span data-stu-id="8a6ab-119">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions the task performs.</span></span> <span data-ttu-id="8a6ab-120">En este caso, se ejecuta el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="8a6ab-120">In this case, running Notepad.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a6ab-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8a6ab-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a6ab-122">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="8a6ab-122">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




