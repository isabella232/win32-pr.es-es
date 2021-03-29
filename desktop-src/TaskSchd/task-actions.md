---
title: Acciones de tarea
description: Los elementos de trabajo que realiza una tarea se denominan acciones. Una tarea puede tener una sola acción o un máximo de 32 acciones. Tenga en cuenta que cuando se especifican varias acciones, se ejecutan secuencialmente.
ms.assetid: 4cbe739d-4c4e-4469-8289-4be41b93950c
keywords:
- acciones Programador de tareas
- acciones Programador de tareas, descritas
- acciones Programador de tareas, ejecutar acción
- acciones Programador de tareas, acción del controlador COM
- ejecutar Programador de tareas de acción
- Programador de tareas de acción del controlador COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71003e2cea5febfab61617451f3b6ebef4a244a3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "103787599"
---
# <a name="task-actions"></a><span data-ttu-id="a313e-111">Acciones de tarea</span><span class="sxs-lookup"><span data-stu-id="a313e-111">Task Actions</span></span>

<span data-ttu-id="a313e-112">Los elementos de trabajo que realiza una tarea se denominan acciones.</span><span class="sxs-lookup"><span data-stu-id="a313e-112">The work items performed by a task are called actions.</span></span> <span data-ttu-id="a313e-113">Una tarea puede tener una sola acción o un máximo de 32 acciones.</span><span class="sxs-lookup"><span data-stu-id="a313e-113">A task can have a single action or a maximum of 32 actions.</span></span> <span data-ttu-id="a313e-114">Tenga en cuenta que cuando se especifican varias acciones, se ejecutan secuencialmente.</span><span class="sxs-lookup"><span data-stu-id="a313e-114">Be aware that when multiple actions are specified, they are executed sequentially.</span></span>

## <a name="types-of-actions"></a><span data-ttu-id="a313e-115">Tipos de acciones</span><span class="sxs-lookup"><span data-stu-id="a313e-115">Types of Actions</span></span>

<span data-ttu-id="a313e-116">La siguiente tabla de acciones describe el tipo de trabajo o acciones que puede realizar una tarea.</span><span class="sxs-lookup"><span data-stu-id="a313e-116">The following table of actions describes the type of work or actions that can be accomplished by a task.</span></span>

| <span data-ttu-id="a313e-117">Tipo de acción</span><span class="sxs-lookup"><span data-stu-id="a313e-117">Type of Action</span></span>      | <span data-ttu-id="a313e-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a313e-118">Description</span></span>                                                             |
|---------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a313e-119">Acción de comcontrolador</span><span class="sxs-lookup"><span data-stu-id="a313e-119">ComHandler Action</span></span>   | <span data-ttu-id="a313e-120">Esta acción activa un controlador COM.</span><span class="sxs-lookup"><span data-stu-id="a313e-120">This action fires a COM handler.</span></span>                                        |
| <span data-ttu-id="a313e-121">Acción exec</span><span class="sxs-lookup"><span data-stu-id="a313e-121">Exec Action</span></span>         | <span data-ttu-id="a313e-122">Esta acción ejecuta una operación de línea de comandos, como iniciar el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="a313e-122">This action executes a command-line operation such as starting Notepad.</span></span> |
| <span data-ttu-id="a313e-123">Acción de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="a313e-123">E-mail Action</span></span>       | <span data-ttu-id="a313e-124">Esta acción envía un correo electrónico cuando se desencadena una tarea.</span><span class="sxs-lookup"><span data-stu-id="a313e-124">This action sends an email when a task is triggered.</span></span>                    |
| <span data-ttu-id="a313e-125">Mostrar acción de mensaje</span><span class="sxs-lookup"><span data-stu-id="a313e-125">Show Message Action</span></span> | <span data-ttu-id="a313e-126">Esta acción muestra un cuadro de mensaje con un mensaje y título especificados.</span><span class="sxs-lookup"><span data-stu-id="a313e-126">This action shows a message box with a specified message and title.</span></span>     |



 

## <a name="specifying-actions"></a><span data-ttu-id="a313e-127">Especificar acciones</span><span class="sxs-lookup"><span data-stu-id="a313e-127">Specifying Actions</span></span>

<span data-ttu-id="a313e-128">Las acciones de una tarea se especifican cuando la tarea se define y se almacena en una colección de acciones utilizada por el servicio de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="a313e-128">The actions of a task are specified when the task is defined and stored in a collection of actions used by the Task Scheduler service.</span></span> <span data-ttu-id="a313e-129">En la tabla siguiente se incluyen vínculos a temas de referencia para las API y los elementos XML que están asociados a acciones.</span><span class="sxs-lookup"><span data-stu-id="a313e-129">The following table lists links to reference topics for the APIs and XML elements that are associated with actions.</span></span>

<span data-ttu-id="a313e-130">Para obtener más información y ejemplos sobre cómo usar las interfaces de Programador de tareas, los objetos de scripting y XML, vea [usar el programador de tareas](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="a313e-130">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

### <a name="interface-apis-for-c-development"></a><span data-ttu-id="a313e-131">API de interfaz para el desarrollo en C++</span><span class="sxs-lookup"><span data-stu-id="a313e-131">Interface APIs for C++ Development</span></span>



| <span data-ttu-id="a313e-132">API</span><span class="sxs-lookup"><span data-stu-id="a313e-132">API</span></span>                                                                    | <span data-ttu-id="a313e-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="a313e-133">Description</span></span>                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="a313e-134">**Propiedad Actions de ITaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="a313e-134">**Actions Property of ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) | <span data-ttu-id="a313e-135">Obtiene o establece las acciones realizadas por la tarea.</span><span class="sxs-lookup"><span data-stu-id="a313e-135">Gets or sets the actions performed by the task.</span></span>              |
| [<span data-ttu-id="a313e-136">**IActionCollection**</span><span class="sxs-lookup"><span data-stu-id="a313e-136">**IActionCollection**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)                         | <span data-ttu-id="a313e-137">Contiene las acciones realizadas por la tarea.</span><span class="sxs-lookup"><span data-stu-id="a313e-137">Contains the actions performed by the task.</span></span>                  |
| [<span data-ttu-id="a313e-138">**IComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="a313e-138">**IComHandlerAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)                         | <span data-ttu-id="a313e-139">Representa una acción que activa un controlador.</span><span class="sxs-lookup"><span data-stu-id="a313e-139">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="a313e-140">**IExecAction**</span><span class="sxs-lookup"><span data-stu-id="a313e-140">**IExecAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)                                     | <span data-ttu-id="a313e-141">Representa una acción que ejecuta una operación de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="a313e-141">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="a313e-142">**IEmailAction**</span><span class="sxs-lookup"><span data-stu-id="a313e-142">**IEmailAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iemailaction)                                   | <span data-ttu-id="a313e-143">Representa una acción que envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a313e-143">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="a313e-144">**IShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="a313e-144">**IShowMessageAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)                       | <span data-ttu-id="a313e-145">Representa una acción que muestra un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a313e-145">Represents an action that shows a message box.</span></span>               |



 

### <a name="scripting-object-apis-for-scripting-development"></a><span data-ttu-id="a313e-146">Scripting de API de objetos para el desarrollo de scripting</span><span class="sxs-lookup"><span data-stu-id="a313e-146">Scripting Object APIs for Scripting Development</span></span>



| <span data-ttu-id="a313e-147">API</span><span class="sxs-lookup"><span data-stu-id="a313e-147">API</span></span>                                                      | <span data-ttu-id="a313e-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="a313e-148">Description</span></span>                                                  |
|----------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="a313e-149">**TaskDefinition. Actions**</span><span class="sxs-lookup"><span data-stu-id="a313e-149">**TaskDefinition.Actions**</span></span>](taskdefinition-actions.md) | <span data-ttu-id="a313e-150">Obtiene o establece las acciones realizadas por la tarea.</span><span class="sxs-lookup"><span data-stu-id="a313e-150">Gets or sets the actions performed by the task.</span></span>              |
| [<span data-ttu-id="a313e-151">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="a313e-151">**ActionCollection**</span></span>](actioncollection.md)             | <span data-ttu-id="a313e-152">Contiene las acciones realizadas por la tarea.</span><span class="sxs-lookup"><span data-stu-id="a313e-152">Contains the actions performed by the task.</span></span>                  |
| [<span data-ttu-id="a313e-153">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="a313e-153">**ComHandlerAction**</span></span>](comhandleraction.md)             | <span data-ttu-id="a313e-154">Representa una acción que activa un controlador.</span><span class="sxs-lookup"><span data-stu-id="a313e-154">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="a313e-155">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="a313e-155">**ExecAction**</span></span>](execaction.md)                         | <span data-ttu-id="a313e-156">Representa una acción que ejecuta una operación de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="a313e-156">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="a313e-157">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="a313e-157">**EmailAction**</span></span>](emailaction.md)                       | <span data-ttu-id="a313e-158">Representa una acción que envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a313e-158">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="a313e-159">**ShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="a313e-159">**ShowMessageAction**</span></span>](showmessageaction.md)           | <span data-ttu-id="a313e-160">Representa una acción que muestra un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a313e-160">Represents an action that shows a message box.</span></span>               |



 

### <a name="xml-elements"></a><span data-ttu-id="a313e-161">Elementos XML</span><span class="sxs-lookup"><span data-stu-id="a313e-161">XML Elements</span></span>



| <span data-ttu-id="a313e-162">Elemento</span><span class="sxs-lookup"><span data-stu-id="a313e-162">Element</span></span>                                                                    | <span data-ttu-id="a313e-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="a313e-163">Description</span></span>                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="a313e-164">**Acciones**</span><span class="sxs-lookup"><span data-stu-id="a313e-164">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)            | <span data-ttu-id="a313e-165">Define las acciones realizadas por la tarea.</span><span class="sxs-lookup"><span data-stu-id="a313e-165">Defines the actions performed by the task.</span></span>                   |
| [<span data-ttu-id="a313e-166">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="a313e-166">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | <span data-ttu-id="a313e-167">Representa una acción que activa un controlador.</span><span class="sxs-lookup"><span data-stu-id="a313e-167">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="a313e-168">**Ejec**</span><span class="sxs-lookup"><span data-stu-id="a313e-168">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | <span data-ttu-id="a313e-169">Representa una acción que ejecuta una operación de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="a313e-169">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="a313e-170">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="a313e-170">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | <span data-ttu-id="a313e-171">Representa una acción que envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a313e-171">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="a313e-172">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="a313e-172">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | <span data-ttu-id="a313e-173">Representa una acción que muestra un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a313e-173">Represents an action that shows a message box.</span></span>               |



 

## <a name="using-variables-in-action-properties"></a><span data-ttu-id="a313e-174">Usar variables en las propiedades de acción</span><span class="sxs-lookup"><span data-stu-id="a313e-174">Using Variables in Action Properties</span></span>

<span data-ttu-id="a313e-175">Algunas propiedades de acción que son de tipo **BSTR** pueden contener variables $ (Arg0), $ (arg1),..., $ (Arg32) en sus valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="a313e-175">Some action properties that are of type **BSTR** can contain $(Arg0), $(Arg1), ..., $(Arg32) variables in their string values.</span></span> <span data-ttu-id="a313e-176">Estas variables se reemplazan por los valores que se especifican en el parámetro *params* de los métodos [**IRegisteredTask:: Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) y [**IRegisteredTask:: RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) o se encuentran dentro del desencadenador de eventos para la tarea.</span><span class="sxs-lookup"><span data-stu-id="a313e-176">These variables are replaced with the values that are specified in the *params* parameter of the [**IRegisteredTask::Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) and [**IRegisteredTask::RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) methods or are contained within the event trigger for the task.</span></span> <span data-ttu-id="a313e-177">En la tabla siguiente se enumeran las propiedades de acción que pueden usar variables en sus valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="a313e-177">The following table lists the action properties that can use variables in their string values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a313e-178">Acción</span><span class="sxs-lookup"><span data-stu-id="a313e-178">Action</span></span></th>
<th><span data-ttu-id="a313e-179">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a313e-179">Properties</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a313e-180">Acción del controlador COM</span><span class="sxs-lookup"><span data-stu-id="a313e-180">COM Handler Action</span></span></td>
<td><span data-ttu-id="a313e-181">C++:</span><span class="sxs-lookup"><span data-stu-id="a313e-181">C++:</span></span>
<ul>
<li><span data-ttu-id="a313e-182"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>Propiedad ClassId de IComHandlerAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-182"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>ClassId Property of IComHandlerAction</strong></a></span></span></li>
<li><span data-ttu-id="a313e-183"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Propiedad de datos de IComHandlerAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-183"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Data Property of IComHandlerAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="a313e-184">Scripting:</span><span class="sxs-lookup"><span data-stu-id="a313e-184">Scripting:</span></span>
<ul>
<li><span data-ttu-id="a313e-185"><a href="comhandleraction-classid.md"><strong>ComHandlerAction. ClassId</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-185"><a href="comhandleraction-classid.md"><strong>ComHandlerAction.ClassId</strong></a></span></span></li>
<li><span data-ttu-id="a313e-186"><a href="comhandleraction-data.md"><strong>ComHandlerAction. Data</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-186"><a href="comhandleraction-data.md"><strong>ComHandlerAction.Data</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a313e-187">Acción de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="a313e-187">Email Action</span></span></td>
<td><span data-ttu-id="a313e-188">C++:</span><span class="sxs-lookup"><span data-stu-id="a313e-188">C++:</span></span>
<ul>
<li><span data-ttu-id="a313e-189"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Propiedad Body de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-189"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Body Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="a313e-190"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Propiedad Server de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-190"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Server Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="a313e-191"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Propiedad Subject de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-191"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Subject Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="a313e-192"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>Propiedad to de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-192"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>To Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="a313e-193"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Propiedad CC de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-193"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Cc Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="a313e-194"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Propiedad BCC de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-194"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Bcc Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="a313e-195"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>Propiedad ReplyTo de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-195"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>ReplyTo Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="a313e-196"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>Propiedad From de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-196"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>From Property of IEmailAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="a313e-197">Scripting:</span><span class="sxs-lookup"><span data-stu-id="a313e-197">Scripting:</span></span>
<ul>
<li><span data-ttu-id="a313e-198"><a href="emailaction-body.md"><strong>EmailAction. Body</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-198"><a href="emailaction-body.md"><strong>EmailAction.Body</strong></a></span></span></li>
<li><span data-ttu-id="a313e-199"><a href="emailaction-server.md"><strong>EmailAction. Server</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-199"><a href="emailaction-server.md"><strong>EmailAction.Server</strong></a></span></span></li>
<li><span data-ttu-id="a313e-200"><a href="emailaction-subject.md"><strong>EmailAction. Subject</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-200"><a href="emailaction-subject.md"><strong>EmailAction.Subject</strong></a></span></span></li>
<li><span data-ttu-id="a313e-201"><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-201"><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></span></span></li>
<li><span data-ttu-id="a313e-202"><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-202"><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></span></span></li>
<li><span data-ttu-id="a313e-203"><a href="emailaction-bcc.md"><strong>EmailAction. BCC</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-203"><a href="emailaction-bcc.md"><strong>EmailAction.Bcc</strong></a></span></span></li>
<li><span data-ttu-id="a313e-204"><a href="emailaction-replyto.md"><strong>EmailAction. ReplyTo</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-204"><a href="emailaction-replyto.md"><strong>EmailAction.ReplyTo</strong></a></span></span></li>
<li><span data-ttu-id="a313e-205"><a href="emailaction-from.md"><strong>EmailAction. from</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-205"><a href="emailaction-from.md"><strong>EmailAction.From</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a313e-206">Acción exec</span><span class="sxs-lookup"><span data-stu-id="a313e-206">Exec Action</span></span></td>
<td><span data-ttu-id="a313e-207">C++:</span><span class="sxs-lookup"><span data-stu-id="a313e-207">C++:</span></span>
<ul>
<li><span data-ttu-id="a313e-208"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Propiedad arguments de IExecAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-208"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Arguments Property of IExecAction</strong></a></span></span></li>
<li><span data-ttu-id="a313e-209"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>Propiedad WorkingDirectory de IExecAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-209"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>WorkingDirectory Property of IExecAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="a313e-210">Scripting:</span><span class="sxs-lookup"><span data-stu-id="a313e-210">Scripting:</span></span>
<ul>
<li><span data-ttu-id="a313e-211"><a href="execaction-arguments.md"><strong>ExecAction. arguments</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-211"><a href="execaction-arguments.md"><strong>ExecAction.Arguments</strong></a></span></span></li>
<li><span data-ttu-id="a313e-212"><a href="execaction-workingdirectory.md"><strong>ExecAction. WorkingDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-212"><a href="execaction-workingdirectory.md"><strong>ExecAction.WorkingDirectory</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a313e-213">Mostrar acción de mensaje</span><span class="sxs-lookup"><span data-stu-id="a313e-213">Show Message Action</span></span></td>
<td><span data-ttu-id="a313e-214">C++:</span><span class="sxs-lookup"><span data-stu-id="a313e-214">C++:</span></span>
<ul>
<li><span data-ttu-id="a313e-215"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Propiedad title de IShowMessageAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-215"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Title Property of IShowMessageAction</strong></a></span></span></li>
<li><span data-ttu-id="a313e-216"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>Propiedad MessageBody de IShowMessageAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-216"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>MessageBody Property of IShowMessageAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="a313e-217">Scripting:</span><span class="sxs-lookup"><span data-stu-id="a313e-217">Scripting:</span></span>
<ul>
<li><span data-ttu-id="a313e-218"><a href="showmessageaction-title.md"><strong>ShowMessageAction. title</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-218"><a href="showmessageaction-title.md"><strong>ShowMessageAction.Title</strong></a></span></span></li>
<li><span data-ttu-id="a313e-219"><a href="showmessageaction-messagebody.md"><strong>ShowMessageAction. MessageBody</strong></a></span><span class="sxs-lookup"><span data-stu-id="a313e-219"><a href="showmessageaction-messagebody.md"><strong>ShowMessageAction.MessageBody</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="a313e-220">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a313e-220">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a313e-221">Acerca del Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="a313e-221">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 





