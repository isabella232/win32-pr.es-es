---
title: Información de registro de tareas
description: La información de registro proporciona una manera de identificar una tarea de varias maneras diferentes. Por ejemplo, una tarea puede identificarla el autor, cómo se creó (denominada origen de la tarea) y la fecha del registro.
ms.assetid: 45c9fa99-2718-4202-8987-4b506bd677e9
keywords:
- Programador de tareas de información de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6c5048e9cbb9b41abcd9052a02371cd575b57c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356680"
---
# <a name="task-registration-information"></a><span data-ttu-id="df166-105">Información de registro de tareas</span><span class="sxs-lookup"><span data-stu-id="df166-105">Task Registration Information</span></span>

<span data-ttu-id="df166-106">La información de registro proporciona una manera de identificar una tarea de varias maneras diferentes.</span><span class="sxs-lookup"><span data-stu-id="df166-106">Registration information provides a way to identify a task in several different ways.</span></span> <span data-ttu-id="df166-107">Por ejemplo, una tarea puede identificarla el autor, cómo se creó (denominada origen de la tarea) y la fecha del registro.</span><span class="sxs-lookup"><span data-stu-id="df166-107">For example, a task can be identified by the author, how it was authored (referred to as the task source), and date of registration.</span></span>

## <a name="using-registration-information"></a><span data-ttu-id="df166-108">Usar información de registro</span><span class="sxs-lookup"><span data-stu-id="df166-108">Using Registration Information</span></span>

<span data-ttu-id="df166-109">Normalmente, la información de registro se especifica cuando se crea la tarea y, a continuación, se usa de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="df166-109">Registration information is typically specified when the task is created and then used in the following ways:</span></span>

-   <span data-ttu-id="df166-110">Lo muestra la interfaz de usuario de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="df166-110">Displayed by the Task Scheduler user interface.</span></span>
-   <span data-ttu-id="df166-111">Obtener o establecer por aplicaciones o scripts de C++.</span><span class="sxs-lookup"><span data-stu-id="df166-111">Get or set by C++ applications or scripts.</span></span>
-   <span data-ttu-id="df166-112">En un entorno empresarial, se usa como criterio de búsqueda al enumerar todas las tareas registradas.</span><span class="sxs-lookup"><span data-stu-id="df166-112">In an enterprise environment, used as a search criteria when enumerating over all registered tasks.</span></span>

## <a name="types-of-registration-information"></a><span data-ttu-id="df166-113">Tipos de información de registro</span><span class="sxs-lookup"><span data-stu-id="df166-113">Types of Registration Information</span></span>

<span data-ttu-id="df166-114">La información de registro de tareas se define mediante las propiedades del objeto [**RegistrationInfo**](registrationinfo.md) para las aplicaciones de scripting, las propiedades de la interfaz [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) para las aplicaciones de C++ y los elementos secundarios del [**elemento RegistrationInfo (taskType)**](taskschedulerschema-registrationinfo-tasktype-element.md) para leer o escribir en XML.</span><span class="sxs-lookup"><span data-stu-id="df166-114">Task registration information is defined by the properties of the [**RegistrationInfo**](registrationinfo.md) object for scripting applications, the properties of the [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) interface for C++ applications, and the child elements of the [**RegistrationInfo (taskType) element**](taskschedulerschema-registrationinfo-tasktype-element.md) for reading or writing XML.</span></span>

<span data-ttu-id="df166-115">Estas propiedades permiten el acceso a los siguientes tipos de información de registro:</span><span class="sxs-lookup"><span data-stu-id="df166-115">These properties allow access to the following types of registration information:</span></span>

-   <span data-ttu-id="df166-116">Autor de la tarea</span><span class="sxs-lookup"><span data-stu-id="df166-116">Task Author</span></span>

    <span data-ttu-id="df166-117">Programador de tareas establece el autor de la tarea cuando se crea.</span><span class="sxs-lookup"><span data-stu-id="df166-117">Task Scheduler sets the author of the task when it is created.</span></span>

-   <span data-ttu-id="df166-118">Fecha de registro de tarea</span><span class="sxs-lookup"><span data-stu-id="df166-118">Task Registration Date</span></span>

    <span data-ttu-id="df166-119">Programador de tareas establece esta fecha cuando se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="df166-119">Task Scheduler sets this date when the task is registered.</span></span>

-   <span data-ttu-id="df166-120">Descripción de la tarea</span><span class="sxs-lookup"><span data-stu-id="df166-120">Task Description</span></span>

    <span data-ttu-id="df166-121">Descripción definida por el usuario que puede incluir los desencadenadores que se usan para iniciar la tarea o las acciones que realiza la tarea.</span><span class="sxs-lookup"><span data-stu-id="df166-121">A user-defined description that may include what triggers are used to start the task or what actions the task performs.</span></span>

-   <span data-ttu-id="df166-122">Documentación de la tarea</span><span class="sxs-lookup"><span data-stu-id="df166-122">Task Documentation</span></span>

    <span data-ttu-id="df166-123">Documentación proporcionada por el usuario que necesita la tarea.</span><span class="sxs-lookup"><span data-stu-id="df166-123">User-supplied documentation that is needed by the task.</span></span>

-   <span data-ttu-id="df166-124">Descriptor de seguridad de tarea</span><span class="sxs-lookup"><span data-stu-id="df166-124">Task Security Descriptor</span></span>

    <span data-ttu-id="df166-125">Un descriptor de seguridad proporcionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="df166-125">A user-supplied security descriptor.</span></span>

-   <span data-ttu-id="df166-126">Origen de la tarea</span><span class="sxs-lookup"><span data-stu-id="df166-126">Task Source</span></span>

    <span data-ttu-id="df166-127">Información proporcionada por el usuario que describe dónde se originó la tarea.</span><span class="sxs-lookup"><span data-stu-id="df166-127">User-supplied information that describes where the task originated from.</span></span> <span data-ttu-id="df166-128">Por ejemplo, una tarea se puede originar a partir de un componente, servicio, aplicación o usuario.</span><span class="sxs-lookup"><span data-stu-id="df166-128">For example, a task may originate from a component, service, application, or user.</span></span>

-   <span data-ttu-id="df166-129">URI de la tarea</span><span class="sxs-lookup"><span data-stu-id="df166-129">Task URI</span></span>

    <span data-ttu-id="df166-130">Identificador uniforme de recursos (URI) para la tarea.</span><span class="sxs-lookup"><span data-stu-id="df166-130">A uniform resource identifier (URI) for the task.</span></span>

-   <span data-ttu-id="df166-131">Versión de la tarea</span><span class="sxs-lookup"><span data-stu-id="df166-131">Task Version</span></span>

    <span data-ttu-id="df166-132">Información proporcionada por el usuario que se utiliza cuando existen varias versiones de una tarea.</span><span class="sxs-lookup"><span data-stu-id="df166-132">User-supplied information that is used when multiple versions of a task exist.</span></span>

-   <span data-ttu-id="df166-133">Texto XML</span><span class="sxs-lookup"><span data-stu-id="df166-133">XML Text</span></span>

    <span data-ttu-id="df166-134">Una versión con formato XML de la información de registro.</span><span class="sxs-lookup"><span data-stu-id="df166-134">An XML-formatted version of the registration information.</span></span> <span data-ttu-id="df166-135">Tenga en cuenta que puede establecer o modificar la información de registro directamente a través de este XML y las propiedades de interfaz y objeto adecuadas se actualizarán en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="df166-135">Note that you can set or modify the registration information directly through this XML and the appropriate object and interface properties will be updated accordingly.</span></span>

## <a name="registering-tasks"></a><span data-ttu-id="df166-136">Registro de tareas</span><span class="sxs-lookup"><span data-stu-id="df166-136">Registering Tasks</span></span>

<span data-ttu-id="df166-137">Una tarea se puede registrar una vez que se han creado las definiciones de tarea y el usuario proporciona la información de registro y los valores de configuración.</span><span class="sxs-lookup"><span data-stu-id="df166-137">A task can be registered after the task definitions are created and registration information and setting values are supplied by the user.</span></span> <span data-ttu-id="df166-138">Una tarea se registra mediante el método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) para las aplicaciones de scripting o el método [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) para las aplicaciones de C++.</span><span class="sxs-lookup"><span data-stu-id="df166-138">A task is registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method for scripting applications or the [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) method for C++ applications.</span></span> <span data-ttu-id="df166-139">Si desea registrar una tarea mediante XML para definir la tarea, use el método [**TaskFolder. RegisterTask**](taskfolder-registertask.md) para las aplicaciones de scripting y el método [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) para las aplicaciones de C++.</span><span class="sxs-lookup"><span data-stu-id="df166-139">If you want to register a task using XML to define the task, you use the [**TaskFolder.RegisterTask**](taskfolder-registertask.md) method for scripting applications and the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) method for C++ applications.</span></span>

<span data-ttu-id="df166-140">En los métodos mencionados anteriormente, puede especificar el contexto de seguridad para ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="df166-140">In the methods mentioned above, you can specify the security context to run the task.</span></span> <span data-ttu-id="df166-141">Debe ser administrador en el sistema para programar trabajos para que se ejecuten en contextos que no sean los suyos propios.</span><span class="sxs-lookup"><span data-stu-id="df166-141">You have to be an administrator on the system to schedule jobs to run under contexts other than your own.</span></span> <span data-ttu-id="df166-142">Para obtener más información sobre los contextos de seguridad para ejecutar tareas, vea [contextos de seguridad para ejecutar tareas](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="df166-142">For more information on the security contexts to run tasks, see [Security Contexts for Running Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="df166-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="df166-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df166-144">Acerca del Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="df166-144">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> <dt>

[<span data-ttu-id="df166-145">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="df166-145">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




