---
title: Tareas
description: Una tarea es el trabajo programado que realiza el servicio Programador de tareas.
ms.assetid: 24c43834-5731-4b14-9409-7d7cf20b1a71
keywords:
- Programador de tareas de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbb4ef41915ec70c98b59c9a7ba74c00f283ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676229"
---
# <a name="tasks"></a><span data-ttu-id="7f39d-104">Tareas</span><span class="sxs-lookup"><span data-stu-id="7f39d-104">Tasks</span></span>

<span data-ttu-id="7f39d-105">Una tarea es el trabajo programado que realiza el servicio Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="7f39d-105">A task is the scheduled work that the Task Scheduler service performs.</span></span> <span data-ttu-id="7f39d-106">Una tarea se compone de distintos componentes, pero una tarea debe contener un desencadenador que el Programador de tareas utiliza para iniciar la tarea y una acción que describe el trabajo que realizará el Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="7f39d-106">A task is composed of different components, but a task must contain a trigger that the Task Scheduler uses to start the task and an action that describes what work the Task Scheduler will perform.</span></span>

<span data-ttu-id="7f39d-107">Cuando se crea una tarea, se almacena en una carpeta de tareas.</span><span class="sxs-lookup"><span data-stu-id="7f39d-107">When a task is created, it is stored in a task folder.</span></span> <span data-ttu-id="7f39d-108">Se puede tener acceso a las carpetas de tareas a través de la interfaz [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) ([**TaskFolder**](taskfolder.md) para scripting) y se puede tener acceso a las tareas a través de la interfaz [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) ([**RegisteredTask**](registeredtask.md) para scripting) cuando se crean.</span><span class="sxs-lookup"><span data-stu-id="7f39d-108">Task folders can be accessed through the [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) interface ([**TaskFolder**](taskfolder.md) for scripting), and tasks can be accessed through the [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) interface ([**RegisteredTask**](registeredtask.md) for scripting) when they are created.</span></span> <span data-ttu-id="7f39d-109">Puede cambiar las listas de control de acceso (ACL) para tareas y carpetas de tareas con el fin de conceder o denegar el acceso de determinados usuarios y grupos a una carpeta de tareas o tareas.</span><span class="sxs-lookup"><span data-stu-id="7f39d-109">You can change access control lists (ACLs) for tasks and task folders in order to grant or deny certain users and groups access to a task or task folder.</span></span> <span data-ttu-id="7f39d-110">Esto se puede hacer mediante el método [**IRegisteredTask:: SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) , el método [**ITaskFolder:: SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) o especificando un descriptor de seguridad cuando una tarea se registra mediante el método [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) o [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) .</span><span class="sxs-lookup"><span data-stu-id="7f39d-110">This can be done by using the [**IRegisteredTask::SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) method, the [**ITaskFolder::SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) method, or by specifying a security descriptor when a task is registered by using the [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) or [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) method.</span></span>

> [!Note]  
> <span data-ttu-id="7f39d-111">Si se deniega el acceso a la cuenta de sistema local a un archivo de tarea o a una carpeta de tareas, el servicio Programador de tareas puede generar resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="7f39d-111">If the Local System account is denied access to a task file or task folder, then the Task Scheduler service can produce unexpected results.</span></span>

 

## <a name="components-of-a-task"></a><span data-ttu-id="7f39d-112">Componentes de una tarea</span><span class="sxs-lookup"><span data-stu-id="7f39d-112">Components of a Task</span></span>

<span data-ttu-id="7f39d-113">En la ilustración siguiente se muestran los componentes de la tarea.</span><span class="sxs-lookup"><span data-stu-id="7f39d-113">The following illustration shows the task components.</span></span>

![componentes de tarea](images/taskcomponents.png)

<span data-ttu-id="7f39d-115">La lista siguiente contiene una breve descripción de cada componente de tarea:</span><span class="sxs-lookup"><span data-stu-id="7f39d-115">The following list contains a brief description of each task component:</span></span>

-   <span data-ttu-id="7f39d-116">Desencadenadores: Programador de tareas usa desencadenadores basados en eventos o temporales para saber cuándo se debe iniciar una tarea.</span><span class="sxs-lookup"><span data-stu-id="7f39d-116">Triggers: Task Scheduler uses event or time-based triggers to know when to start a task.</span></span> <span data-ttu-id="7f39d-117">Cada tarea puede especificar uno o varios desencadenadores para iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="7f39d-117">Every task can specify one or more triggers to start the task.</span></span>

    <span data-ttu-id="7f39d-118">Para obtener más información acerca de los desencadenadores, vea [desencadenadores de tareas](task-triggers.md).</span><span class="sxs-lookup"><span data-stu-id="7f39d-118">For more information about triggers, see [Task Triggers](task-triggers.md).</span></span>

-   <span data-ttu-id="7f39d-119">Acciones: estas son las acciones, el trabajo real, que realiza la tarea.</span><span class="sxs-lookup"><span data-stu-id="7f39d-119">Actions: These are the actions, the actual work, that is performed by the task.</span></span> <span data-ttu-id="7f39d-120">Cada tarea puede especificar una o varias acciones para completar su trabajo.</span><span class="sxs-lookup"><span data-stu-id="7f39d-120">Every task can specify one or more actions to complete its work.</span></span>

    <span data-ttu-id="7f39d-121">Para obtener más información sobre las acciones, vea [acciones de tarea](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="7f39d-121">For more information about actions, see [Task Actions](task-actions.md).</span></span>

-   <span data-ttu-id="7f39d-122">Entidades de seguridad: las entidades de seguridad definen el contexto de seguridad en el que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="7f39d-122">Principals: Principals define the security context in which the task is run.</span></span> <span data-ttu-id="7f39d-123">Por ejemplo, una entidad de seguridad podría definir un usuario o un grupo de usuarios específico que pueda ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="7f39d-123">For example, a principal might define a specific user or user group that can run the task.</span></span>

    <span data-ttu-id="7f39d-124">Para obtener más información sobre las entidades de [seguridad, vea contextos de seguridad para tareas](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="7f39d-124">For more information about principals, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

-   <span data-ttu-id="7f39d-125">Configuración: Estos son los valores que el Programador de tareas usa para ejecutar la tarea con respecto a las condiciones que son externas a la propia tarea.</span><span class="sxs-lookup"><span data-stu-id="7f39d-125">Settings: These are the settings that the Task Scheduler uses to run the task with respect to conditions that are external to the task itself.</span></span> <span data-ttu-id="7f39d-126">Por ejemplo, esta configuración puede especificar la prioridad de la tarea con respecto a otras tareas, si se pueden ejecutar varias instancias de la tarea, cómo se administra la tarea cuando el equipo está en una condición de inactividad y otras condiciones.</span><span class="sxs-lookup"><span data-stu-id="7f39d-126">For example, these settings can specify the priority of the task with respect to other tasks, whether multiple instances of the task can be run, how the task is handled when the computer is in an idle condition, and other conditions.</span></span>

    <span data-ttu-id="7f39d-127">Para obtener más información sobre la configuración de tareas, vea [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) for scripting).</span><span class="sxs-lookup"><span data-stu-id="7f39d-127">For more information about task settings, see [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) for scripting).</span></span>

    > [!Note]  
    > <span data-ttu-id="7f39d-128">De forma predeterminada, se detendrá una tarea 72 horas después de que empiece a ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="7f39d-128">By default, a task will be stopped 72 hours after it starts to run.</span></span> <span data-ttu-id="7f39d-129">Puede cambiar esto cambiando el valor de [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) .</span><span class="sxs-lookup"><span data-stu-id="7f39d-129">You can change this by changing the [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) setting.</span></span>

     

-   <span data-ttu-id="7f39d-130">Información de registro: se trata de información administrativa que se recopila cuando se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="7f39d-130">Registration Information: This is administrative information that is gathered when the task is registered.</span></span> <span data-ttu-id="7f39d-131">Por ejemplo, esta información describe el autor de la tarea, la fecha en la que se registró la tarea, una descripción XML de la tarea y otra información.</span><span class="sxs-lookup"><span data-stu-id="7f39d-131">For example, this information describes the author of the task, the date when the task was registered, an XML description of the task, and other information.</span></span>

    <span data-ttu-id="7f39d-132">Para obtener más información sobre la información de registro de tareas, vea [información de registro de tareas](task-registration-information.md).</span><span class="sxs-lookup"><span data-stu-id="7f39d-132">For more information about task registration information, see [Task Registration Information](task-registration-information.md).</span></span>

-   <span data-ttu-id="7f39d-133">Datos: se trata de documentación adicional acerca de la tarea proporcionada por el autor de la tarea.</span><span class="sxs-lookup"><span data-stu-id="7f39d-133">Data: This is additional documentation about the task that is supplied by the author of the task.</span></span> <span data-ttu-id="7f39d-134">Por ejemplo, estos datos pueden contener ayuda XML que pueden usar los usuarios cuando ejecutan la tarea.</span><span class="sxs-lookup"><span data-stu-id="7f39d-134">For example, this data may contain XML Help that can be used by users when they run the task.</span></span>

## <a name="task-apis"></a><span data-ttu-id="7f39d-135">API de tareas</span><span class="sxs-lookup"><span data-stu-id="7f39d-135">Task APIs</span></span>

<span data-ttu-id="7f39d-136">Programador de tareas 2,0 proporciona dos conjuntos de API: un conjunto de interfaces y objetos de scripting para Programador de tareas 2,0.</span><span class="sxs-lookup"><span data-stu-id="7f39d-136">Task Scheduler 2.0 provides two sets of APIs: a set of scripting objects and interfaces for Task Scheduler 2.0.</span></span> <span data-ttu-id="7f39d-137">Para obtener más información, vea [referencia de programador de tareas](task-scheduler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="7f39d-137">For more information, see [Task Scheduler Reference](task-scheduler-reference.md).</span></span>

<span data-ttu-id="7f39d-138">La compatibilidad de tareas, que se establece a través de la propiedad de [**compatibilidad**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) , solo se debe establecer en compatibilidad de tareas \_ \_ v1 si se debe tener acceso a una tarea o modificarla desde un equipo con Windows XP, Windows Server 2003 o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7f39d-138">Task compatibility, which is set through the [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) property, should only be set to TASK\_COMPATIBILITY\_V1 if a task must be accessed or modified from a Windows XP, Windows Server 2003, or Windows 2000 computer.</span></span> <span data-ttu-id="7f39d-139">De lo contrario, se recomienda usar la compatibilidad con Programador de tareas 2,0 porque tiene más características.</span><span class="sxs-lookup"><span data-stu-id="7f39d-139">Otherwise, it is recommended that you use Task Scheduler 2.0 compatibility because it has more features.</span></span>

<span data-ttu-id="7f39d-140">A partir de Programador de tareas 2,0, la interfaz [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) ([**TaskService**](taskservice.md) para scripting) se usa como punto de partida para crear tareas en las carpetas especificadas.</span><span class="sxs-lookup"><span data-stu-id="7f39d-140">Starting with Task Scheduler 2.0, the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) interface ([**TaskService**](taskservice.md) for scripting) is used as a starting point to create tasks in specified folders.</span></span> <span data-ttu-id="7f39d-141">La interfaz [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) ([**TaskDefinition**](taskdefinition.md) para scripting) se usa para contener todos los componentes de una tarea, como la configuración, las acciones y los desencadenadores.</span><span class="sxs-lookup"><span data-stu-id="7f39d-141">The [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface ([**TaskDefinition**](taskdefinition.md) for scripting) is used to hold all the components of a task, such as the settings, actions, and triggers.</span></span> <span data-ttu-id="7f39d-142">Las API [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger), [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction)y [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) proporcionan propiedades que se usan para definir los demás componentes de la tarea.</span><span class="sxs-lookup"><span data-stu-id="7f39d-142">The [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger), [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction), and [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) APIs provide properties that are then used to define the other components of the task.</span></span> <span data-ttu-id="7f39d-143">Programador de tareas 1,0 proporciona la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) , que solo se admite para la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="7f39d-143">Task Scheduler 1.0 provides the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface, which is supported only for backward compatibility.</span></span>

<span data-ttu-id="7f39d-144">En el caso de scripting, las interfaces de Programador de tareas se asignan a objetos de scripting que tienen nombres, propiedades y métodos similares.</span><span class="sxs-lookup"><span data-stu-id="7f39d-144">For scripting, the Task Scheduler interfaces map to scripting objects that have the similar names, properties, and methods.</span></span> <span data-ttu-id="7f39d-145">Por ejemplo, el objeto de scripting [**TaskService**](taskservice.md) tiene las mismas propiedades y métodos que la interfaz [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .</span><span class="sxs-lookup"><span data-stu-id="7f39d-145">For example, the [**TaskService**](taskservice.md) scripting object has the same properties and methods as the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) interface.</span></span>

<span data-ttu-id="7f39d-146">Para obtener más información y ejemplos sobre cómo usar las interfaces de Programador de tareas, los objetos de scripting y XML, vea [usar el programador de tareas](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="7f39d-146">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

### <a name="task-scheduler-10-tasks"></a><span data-ttu-id="7f39d-147">Programador de tareas 1,0 tareas</span><span class="sxs-lookup"><span data-stu-id="7f39d-147">Task Scheduler 1.0 Tasks</span></span>

<span data-ttu-id="7f39d-148">Una tarea Programador de tareas 1,0 es cualquier tipo de aplicación o archivo que pueda ejecutar el Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="7f39d-148">A Task Scheduler 1.0 task is any application or file type that the Task Scheduler can execute.</span></span> <span data-ttu-id="7f39d-149">Estos pueden incluir cualquiera de los siguientes elementos (tal y como lo admite el sistema operativo en el que se ejecutará la tarea): aplicaciones Win32, aplicaciones de Win16, sistema operativo/2, aplicaciones MS-DOS, archivos por lotes ( \* . bat), archivos de comandos ( \* . cmd) o cualquier tipo de archivo registrado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7f39d-149">These may include any of the following (as supported by the operating system on which the task will execute): Win32 applications, Win16 applications, OS/2 applications, MS-DOS applications, batch files (\*.bat), command files (\*.cmd), or any properly registered file type.</span></span>

<span data-ttu-id="7f39d-150">Los datos que describen una tarea se guardan en un archivo de tareas que se almacena en la carpeta tareas programadas.</span><span class="sxs-lookup"><span data-stu-id="7f39d-150">Data that describes a task is kept in a task file that is stored in the Scheduled Tasks folder.</span></span> <span data-ttu-id="7f39d-151">Para obtener más información, vea [*tareas programadas (carpeta*](s.md)).</span><span class="sxs-lookup"><span data-stu-id="7f39d-151">For more information, see [*Scheduled Tasks folder*](s.md).</span></span> <span data-ttu-id="7f39d-152">El nombre de estos archivos de tarea incluye el nombre de la tarea, seguido de una extensión de nombre de archivo. Job.</span><span class="sxs-lookup"><span data-stu-id="7f39d-152">The name of these task files include the name of the task, followed by a .job file name extension.</span></span>

<span data-ttu-id="7f39d-153">Para obtener más información sobre cómo agregar Programador de tareas tareas de 1,0, vea [Agregar elementos de trabajo](adding-work-items.md).</span><span class="sxs-lookup"><span data-stu-id="7f39d-153">For more information about adding Task Scheduler 1.0 tasks, see [Adding Work Items](adding-work-items.md).</span></span>

<span data-ttu-id="7f39d-154">Para obtener más información sobre la enumeración a través de Programador de tareas tareas 1,0, consulte [enumeración de tareas](enumerating-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="7f39d-154">For more information about enumerating through Task Scheduler 1.0 tasks, see [Enumerating Tasks](enumerating-tasks.md).</span></span>

<span data-ttu-id="7f39d-155">En el caso de un equipo con Windows Server 2003, Windows XP o Windows 2000 para crear, supervisar o controlar tareas en un equipo con Windows Vista, se deben completar las siguientes operaciones en el equipo con Windows Vista y el usuario que llama al método [**ITaskScheduler:: SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) debe ser miembro del grupo administradores en el equipo remoto de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7f39d-155">For a Windows Server 2003, Windows XP, or Windows 2000 computer to create, monitor, or control tasks on a Windows Vista computer, the following operations should be completed on the Windows Vista computer, and the user who is calling the [**ITaskScheduler::SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) method must be a member of the Administrators group on the remote Windows Vista computer.</span></span>

<span data-ttu-id="7f39d-156">**Para habilitar la excepción "compartir archivos e impresoras" en firewall de Windows**</span><span class="sxs-lookup"><span data-stu-id="7f39d-156">**To enable the "Share File and Printers" exception in Windows Firewall**</span></span>

1.  <span data-ttu-id="7f39d-157">Haga clic en **Inicio** y, a continuación, en **Panel de control**.</span><span class="sxs-lookup"><span data-stu-id="7f39d-157">Click **Start**, and then click **Control Panel**.</span></span>
2.  <span data-ttu-id="7f39d-158">En el **Panel de control**, haga clic en **vista clásica** y, a continuación, haga doble clic en el icono **firewall de Windows** .</span><span class="sxs-lookup"><span data-stu-id="7f39d-158">In **Control Panel**, click **Classic View** and then double-click the **Windows Firewall** icon.</span></span>
3.  <span data-ttu-id="7f39d-159">En la ventana **firewall de Windows** , haga clic en la pestaña **excepciones** y seleccione la casilla **excepción de uso compartido de archivos e impresoras** .</span><span class="sxs-lookup"><span data-stu-id="7f39d-159">In the **Windows Firewall** window, click the **Exceptions** tab and select **File and Printer Sharing exception** check box.</span></span>

<span data-ttu-id="7f39d-160">**Para habilitar el servicio "registro remoto"**</span><span class="sxs-lookup"><span data-stu-id="7f39d-160">**To enable the "Remote Registry" service**</span></span>

-   <span data-ttu-id="7f39d-161">Abra una ventana del símbolo del sistema y escriba el siguiente comando: **net start "Remote Registry"**.</span><span class="sxs-lookup"><span data-stu-id="7f39d-161">Open a Command Prompt window and enter the following command: **net start "Remote Registry"**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f39d-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7f39d-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f39d-163">Acerca del Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="7f39d-163">About the Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> <dt>

[<span data-ttu-id="7f39d-164">Desencadenadores de tareas</span><span class="sxs-lookup"><span data-stu-id="7f39d-164">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="7f39d-165">Acciones de tarea</span><span class="sxs-lookup"><span data-stu-id="7f39d-165">Task Actions</span></span>](task-actions.md)
</dt> <dt>

[<span data-ttu-id="7f39d-166">**ITaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="7f39d-166">**ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
</dt> <dt>

[<span data-ttu-id="7f39d-167">**TaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="7f39d-167">**TaskDefinition**</span></span>](taskdefinition.md)
</dt> <dt>

[<span data-ttu-id="7f39d-168">**ITaskService**</span><span class="sxs-lookup"><span data-stu-id="7f39d-168">**ITaskService**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)
</dt> <dt>

[<span data-ttu-id="7f39d-169">**TaskService**</span><span class="sxs-lookup"><span data-stu-id="7f39d-169">**TaskService**</span></span>](taskservice.md)
</dt> </dl>

 

 




