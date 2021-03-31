---
title: TaskFolder. RegisterTask, método
description: Para el scripting, registra (crea) una nueva tarea en la carpeta utilizando XML para definir la tarea.
ms.assetid: 9bf5c59b-5aa1-42b3-a307-f583cdf59a39
keywords:
- Método RegisterTask Programador de tareas
- Método RegisterTask Programador de tareas, objeto TaskFolder
- Programador de tareas de objeto TaskFolder, método RegisterTask
topic_type:
- apiref
api_name:
- TaskFolder.RegisterTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc0ed00ec736a90f716d895199812899d972930
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996849"
---
# <a name="taskfolderregistertask-method"></a><span data-ttu-id="6f567-106">TaskFolder. RegisterTask, método</span><span class="sxs-lookup"><span data-stu-id="6f567-106">TaskFolder.RegisterTask method</span></span>

<span data-ttu-id="6f567-107">Para el scripting, registra (crea) una nueva tarea en la carpeta utilizando XML para definir la tarea.</span><span class="sxs-lookup"><span data-stu-id="6f567-107">For scripting, registers (creates) a new task in the folder using XML to define the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f567-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f567-108">Syntax</span></span>


```VB
TaskFolder.RegisterTask( _
  ByVal path, _
  ByVal xmlText, _
  ByVal flags, _
  ByVal userId, _
  ByVal password, _
  ByVal logonType, _
  [ ByVal sddl ], _
  ByRef pTask _
)
```



## <a name="parameters"></a><span data-ttu-id="6f567-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f567-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f567-110">*ruta de acceso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f567-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f567-111">Nombre de la tarea.</span><span class="sxs-lookup"><span data-stu-id="6f567-111">The name of the task.</span></span> <span data-ttu-id="6f567-112">Si este valor es **Nothing**, la tarea se registrará en la carpeta de tareas raíz y el nombre de la tarea será un valor GUID creado por el servicio Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="6f567-112">If this value is **Nothing**, the task will be registered in the root task folder and the task name will be a GUID value that is created by the Task Scheduler service.</span></span>

<span data-ttu-id="6f567-113">Un nombre de tarea no puede comenzar ni terminar con un carácter de espacio.</span><span class="sxs-lookup"><span data-stu-id="6f567-113">A task name cannot begin or end with a space character.</span></span> <span data-ttu-id="6f567-114">No se puede usar el carácter '. ' para especificar la carpeta de tareas actual y '.. '</span><span class="sxs-lookup"><span data-stu-id="6f567-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="6f567-115">no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="6f567-115">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="6f567-116">*XmlText* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f567-116">*xmlText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f567-117">Una descripción con formato XML de la tarea.</span><span class="sxs-lookup"><span data-stu-id="6f567-117">An XML-formatted description of the task.</span></span>

<span data-ttu-id="6f567-118">Los temas siguientes contienen tareas definidas mediante XML.</span><span class="sxs-lookup"><span data-stu-id="6f567-118">The following topics contain tasks defined using XML.</span></span>

-   [<span data-ttu-id="6f567-119">Ejemplo de desencadenador de tiempo (XML)</span><span class="sxs-lookup"><span data-stu-id="6f567-119">Time Trigger Example (XML)</span></span>](time-trigger-example--xml-.md)
-   <span data-ttu-id="6f567-120">[Ejemplo de desencadenador de eventos (XML)](/previous-versions//aa446889(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6f567-120">[Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85))</span></span>
-   [<span data-ttu-id="6f567-121">Ejemplo de desencadenador diario (XML)</span><span class="sxs-lookup"><span data-stu-id="6f567-121">Daily Trigger Example (XML)</span></span>](daily-trigger-example--xml-.md)
-   [<span data-ttu-id="6f567-122">Ejemplo de desencadenador de registro (XML)</span><span class="sxs-lookup"><span data-stu-id="6f567-122">Registration Trigger Example (XML)</span></span>](registration-trigger-example--xml-.md)
-   [<span data-ttu-id="6f567-123">Ejemplo de desencadenador semanal (XML)</span><span class="sxs-lookup"><span data-stu-id="6f567-123">Weekly Trigger Example (XML)</span></span>](weekly-trigger-example--xml-.md)
-   [<span data-ttu-id="6f567-124">Ejemplo de desencadenador Logon (XML)</span><span class="sxs-lookup"><span data-stu-id="6f567-124">Logon Trigger Example (XML)</span></span>](logon-trigger-example--xml-.md)
-   [<span data-ttu-id="6f567-125">Ejemplo de desencadenador de arranque (XML)</span><span class="sxs-lookup"><span data-stu-id="6f567-125">Boot Trigger Example (XML)</span></span>](boot-trigger-example--xml-.md)

</dd> <dt>

<span data-ttu-id="6f567-126">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6f567-126">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f567-127">Constante [**de \_ creación de tareas**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) .</span><span class="sxs-lookup"><span data-stu-id="6f567-127">A [**TASK\_CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) constant.</span></span>



| <span data-ttu-id="6f567-128">Value</span><span class="sxs-lookup"><span data-stu-id="6f567-128">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="6f567-129">Significado</span><span class="sxs-lookup"><span data-stu-id="6f567-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <span data-ttu-id="6f567-130"><dt>**Tarea \_ de VALIDAR \_ solo**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="6f567-130"><dt>**TASK\_VALIDATE\_ONLY**</dt> <dt>0x1</dt></span></span> </dl>                                                | <span data-ttu-id="6f567-131">El Programador de tareas comprueba la sintaxis del XML que describe la tarea, pero no registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="6f567-131">The Task Scheduler checks the syntax of the XML that describes the task but does not register the task.</span></span> <span data-ttu-id="6f567-132">Esta constante no se puede combinar con la **tarea \_ crear**, **\_ Actualizar tarea** o **\_ crear \_ o \_ Actualizar** valores.</span><span class="sxs-lookup"><span data-stu-id="6f567-132">This constant cannot be combined with the **TASK\_CREATE**, **TASK\_UPDATE**, or **TASK\_CREATE\_OR\_UPDATE** values.</span></span><br/>                                                                                                                  |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <span data-ttu-id="6f567-133"><dt>**Tarea \_ de CREAR**</dt> <dt>0X2</dt></span><span class="sxs-lookup"><span data-stu-id="6f567-133"><dt>**TASK\_CREATE**</dt> <dt>0x2</dt></span></span> </dl>                                                                      | <span data-ttu-id="6f567-134">El Programador de tareas registra la tarea como una nueva tarea.</span><span class="sxs-lookup"><span data-stu-id="6f567-134">The Task Scheduler registers the task as a new task.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <span data-ttu-id="6f567-135"><dt>**Tarea \_ de ACTUALIZAR**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="6f567-135"><dt>**TASK\_UPDATE**</dt> <dt>0x4</dt></span></span> </dl>                                                                      | <span data-ttu-id="6f567-136">El Programador de tareas registra la tarea como una versión actualizada de una tarea existente.</span><span class="sxs-lookup"><span data-stu-id="6f567-136">The Task Scheduler registers the task as an updated version of an existing task.</span></span> <span data-ttu-id="6f567-137">Cuando se actualiza una tarea con un desencadenador de registro, la tarea se ejecutará después de que se produzca la actualización.</span><span class="sxs-lookup"><span data-stu-id="6f567-137">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span><br/>                                                                                                                                                            |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <span data-ttu-id="6f567-138"><dt>**Tarea \_ de CREAR \_ o \_ Actualizar**</dt> <dt>0x6</dt></span><span class="sxs-lookup"><span data-stu-id="6f567-138"><dt>**TASK\_CREATE\_OR\_UPDATE**</dt> <dt>0x6</dt></span></span> </dl>                                      | <span data-ttu-id="6f567-139">El Programador de tareas registra la tarea como una nueva tarea o como una versión actualizada si la tarea ya existe.</span><span class="sxs-lookup"><span data-stu-id="6f567-139">The Task Scheduler either registers the task as a new task or as an updated version if the task already exists.</span></span> <span data-ttu-id="6f567-140">Equivalente a TASK \_ Create \| Task \_ Update.</span><span class="sxs-lookup"><span data-stu-id="6f567-140">Equivalent to TASK\_CREATE \| TASK\_UPDATE.</span></span><br/>                                                                                                                                                                                    |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <span data-ttu-id="6f567-141"><dt>**Tarea \_ de Deshabilitar**</dt> <dt>0x8</dt></span><span class="sxs-lookup"><span data-stu-id="6f567-141"><dt>**TASK\_DISABLE**</dt> <dt>0x8</dt></span></span> </dl>                                                                   | <span data-ttu-id="6f567-142">El Programador de tareas deshabilita la tarea existente.</span><span class="sxs-lookup"><span data-stu-id="6f567-142">The Task Scheduler disables the existing task.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <span data-ttu-id="6f567-143"><dt>**Tarea \_ de No \_ agregar \_ entidad \_**</dt> de seguridad principal <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="6f567-143"><dt>**TASK\_DONT\_ADD\_PRINCIPAL\_ACE**</dt> <dt>0x10</dt></span></span> </dl>                  | <span data-ttu-id="6f567-144">El Programador de tareas no puede Agregar la entrada de permiso de control de acceso (ACE) para la entidad de seguridad del contexto.</span><span class="sxs-lookup"><span data-stu-id="6f567-144">The Task Scheduler is prevented from adding the allow access-control entry (ACE) for the context principal.</span></span> <span data-ttu-id="6f567-145">Cuando se llama a la función **TaskFolder. RegisterTask** con esta marca para actualizar una tarea, el servicio Programador de tareas no agrega la ACE para la nueva entidad de seguridad de contexto y no quita la ACE de la entidad de seguridad de contexto anterior.</span><span class="sxs-lookup"><span data-stu-id="6f567-145">When the **TaskFolder.RegisterTask** function is called with this flag to update a task, the Task Scheduler service does not add the ACE for the new context principal and does not remove the ACE from the old context principal.</span></span><br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <span data-ttu-id="6f567-146"><dt>**Tarea \_ de OMITIr \_ \_ desencadenadores de registro**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="6f567-146"><dt>**TASK\_IGNORE\_REGISTRATION\_TRIGGERS**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="6f567-147">El Programador de tareas crea la tarea, pero omite los desencadenadores de registro de la tarea.</span><span class="sxs-lookup"><span data-stu-id="6f567-147">The Task Scheduler creates the task, but ignores the registration triggers in the task.</span></span> <span data-ttu-id="6f567-148">Al omitir los desencadenadores de registro, la tarea no se ejecutará cuando se registre a menos que un desencadenador basado en el tiempo haga que se ejecute en el registro.</span><span class="sxs-lookup"><span data-stu-id="6f567-148">By ignoring the registration triggers, the task will not execute when it is registered unless a time-based trigger causes it to execute on registration.</span></span><br/>                                                                                               |



 

</dd> <dt>

<span data-ttu-id="6f567-149">*userId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f567-149">*userId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f567-150">Las credenciales de usuario que se usan para registrar la tarea.</span><span class="sxs-lookup"><span data-stu-id="6f567-150">The user credentials that are used to register the task.</span></span>

> [!Note]  
> <span data-ttu-id="6f567-151">Si la tarea se define como una tarea Programador de tareas 1,0, no use un nombre de grupo (en lugar de un nombre de usuario específico) en este parámetro userId.</span><span class="sxs-lookup"><span data-stu-id="6f567-151">If the task is defined as a Task Scheduler 1.0 task, then do not use a group name (rather than a specific user name) in this userId parameter.</span></span> <span data-ttu-id="6f567-152">Una tarea se define como una tarea Programador de tareas 1,0 cuando el atributo version del elemento Task del XML de la tarea se establece en 1,1.</span><span class="sxs-lookup"><span data-stu-id="6f567-152">A task is defined as a Task Scheduler 1.0 task when the version attribute of the Task element in the task's XML is set to 1.1.</span></span>

 

</dd> <dt>

<span data-ttu-id="6f567-153">*contraseña* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6f567-153">*password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f567-154">La contraseña de userId que se usa para registrar la tarea.</span><span class="sxs-lookup"><span data-stu-id="6f567-154">The password for the userId that is used to register the task.</span></span> <span data-ttu-id="6f567-155">Cuando se usa el tipo de inicio de sesión de la cuenta del servicio de inicio de sesión de tareas \_ \_ \_ , la contraseña debe ser un valor **Variant** vacío como **VT \_ null** o **VT \_ Empty**.</span><span class="sxs-lookup"><span data-stu-id="6f567-155">When the TASK\_LOGON\_SERVICE\_ACCOUNT logon type is used, the password must be an empty **VARIANT** value such as **VT\_NULL** or **VT\_EMPTY**.</span></span>

</dd> <dt>

<span data-ttu-id="6f567-156">*logonType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f567-156">*logonType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f567-157">Define la técnica de inicio de sesión que se utiliza para ejecutar la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="6f567-157">Defines what logon technique is used to run the registered task.</span></span>



| <span data-ttu-id="6f567-158">Value</span><span class="sxs-lookup"><span data-stu-id="6f567-158">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="6f567-159">Significado</span><span class="sxs-lookup"><span data-stu-id="6f567-159">Meaning</span></span>                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <span data-ttu-id="6f567-160"><dt>**Tarea \_ de LOGON \_ ninguno**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6f567-160"><dt>**TASK\_LOGON\_NONE**</dt> <dt>0</dt></span></span> </dl>                                                                               | <span data-ttu-id="6f567-161">No se ha especificado el método Logon.</span><span class="sxs-lookup"><span data-stu-id="6f567-161">The logon method is not specified.</span></span> <span data-ttu-id="6f567-162">Se usa para las credenciales que no son NT.</span><span class="sxs-lookup"><span data-stu-id="6f567-162">Used for non-NT credentials.</span></span> <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <span data-ttu-id="6f567-163"><dt>**Tarea \_ de \_Contraseña de inicio de sesión**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6f567-163"><dt>**TASK\_LOGON\_PASSWORD**</dt> <dt>1</dt></span></span> </dl>                                                                   | <span data-ttu-id="6f567-164">Use una contraseña para iniciar sesión en el usuario.</span><span class="sxs-lookup"><span data-stu-id="6f567-164">Use a password for logging on the user.</span></span> <span data-ttu-id="6f567-165">La contraseña debe proporcionarse en el momento del registro.</span><span class="sxs-lookup"><span data-stu-id="6f567-165">The password must be supplied at registration time.</span></span><br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <span data-ttu-id="6f567-166"><dt>**Tarea \_ de Inicio de sesión \_ S4U**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6f567-166"><dt>**TASK\_LOGON\_S4U**</dt> <dt>2</dt></span></span> </dl>                                                                                  | <span data-ttu-id="6f567-167">Use un token interactivo existente para ejecutar una tarea.</span><span class="sxs-lookup"><span data-stu-id="6f567-167">Use an existing interactive token to run a task.</span></span> <span data-ttu-id="6f567-168">El usuario debe iniciar sesión con un inicio de sesión de servicio para el usuario (S4U).</span><span class="sxs-lookup"><span data-stu-id="6f567-168">The user must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="6f567-169">Cuando se usa un inicio de sesión de S4U, el sistema no almacena ninguna contraseña y no hay acceso a la red ni a los archivos cifrados.</span><span class="sxs-lookup"><span data-stu-id="6f567-169">When an S4U logon is used, no password is stored by the system and there is no access to either the network or to encrypted files.</span></span><br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <span data-ttu-id="6f567-170"><dt>**Tarea \_ de \_ \_ Token interactivo de inicio de sesión**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6f567-170"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="6f567-171">El usuario ya debe haber iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="6f567-171">User must already be logged on.</span></span> <span data-ttu-id="6f567-172">La tarea se ejecutará solo en una sesión interactiva existente.</span><span class="sxs-lookup"><span data-stu-id="6f567-172">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <span data-ttu-id="6f567-173"><dt>**Tarea \_ de \_Grupo de inicio de sesión**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6f567-173"><dt>**TASK\_LOGON\_GROUP**</dt> <dt>4</dt></span></span> </dl>                                                                            | <span data-ttu-id="6f567-174">Activación de grupos.</span><span class="sxs-lookup"><span data-stu-id="6f567-174">Group activation.</span></span> <span data-ttu-id="6f567-175">El campo **GROUPID** especifica el grupo.</span><span class="sxs-lookup"><span data-stu-id="6f567-175">The **groupId** field specifies the group.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <span data-ttu-id="6f567-176"><dt>**Tarea \_ de \_ \_ Cuenta de servicio de inicio de sesión**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="6f567-176"><dt>**TASK\_LOGON\_SERVICE\_ACCOUNT**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="6f567-177">Indica que se utiliza un sistema local, servicio local o cuenta de servicio de red como contexto de seguridad para ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="6f567-177">Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.</span></span><br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <span data-ttu-id="6f567-178"><dt>**Tarea \_ de \_Token interactivo \_ de inicio \_ de sesión o \_ contraseña**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="6f567-178"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="6f567-179">En primer lugar, use el token interactivo.</span><span class="sxs-lookup"><span data-stu-id="6f567-179">First use the interactive token.</span></span> <span data-ttu-id="6f567-180">Si el usuario no ha iniciado sesión (no hay ningún token interactivo disponible), se usa la contraseña.</span><span class="sxs-lookup"><span data-stu-id="6f567-180">If the user is not logged on (no interactive token is available), then the password is used.</span></span> <span data-ttu-id="6f567-181">La contraseña debe especificarse cuando se registra una tarea.</span><span class="sxs-lookup"><span data-stu-id="6f567-181">The password must be specified when a task is registered.</span></span> <span data-ttu-id="6f567-182">Esta marca no se recomienda para las nuevas tareas porque es menos confiable que la contraseña de inicio de sesión de la tarea \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6f567-182">This flag is not recommended for new tasks because it is less reliable than TASK\_LOGON\_PASSWORD.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6f567-183">*SDDL* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6f567-183">*sddl* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f567-184">Descriptor de seguridad asociado a la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="6f567-184">The security descriptor that is associated with the registered task.</span></span> <span data-ttu-id="6f567-185">Puede especificar la lista de control de acceso (ACL) en el descriptor de seguridad de una tarea con el fin de permitir o denegar el acceso de determinados usuarios y grupos a una tarea.</span><span class="sxs-lookup"><span data-stu-id="6f567-185">You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.</span></span>

> [!Note]  
> <span data-ttu-id="6f567-186">Si se deniega el acceso a la cuenta de sistema local a una tarea, el servicio de Programador de tareas puede generar resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="6f567-186">If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</span></span>

 

</dd> <dt>

<span data-ttu-id="6f567-187">*pTask* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6f567-187">*pTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f567-188">Objeto [**RegisteredTask**](registeredtask.md) que representa la nueva tarea.</span><span class="sxs-lookup"><span data-stu-id="6f567-188">A [**RegisteredTask**](registeredtask.md) object that represents the new task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f567-189">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f567-189">Return value</span></span>

<span data-ttu-id="6f567-190">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6f567-190">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f567-191">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f567-191">Remarks</span></span>

<span data-ttu-id="6f567-192">En el caso de una tarea que contenga una acción de cuadro de mensaje, se mostrará el cuadro de mensaje si la tarea está activada y la tarea tiene un tipo de inicio de sesión interactivo.</span><span class="sxs-lookup"><span data-stu-id="6f567-192">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="6f567-193">Para establecer el tipo de inicio de sesión de tarea en interactivo, especifique 3 (**\_ \_ \_ token interactivo de inicio de sesión de tarea**) o 4 (**\_ \_ grupo de inicio de sesión de tareas**) en la propiedad [**LogonType**](principal-logontype.md) de la entidad de seguridad de la tarea, o en el parámetro *LogonType* de **TaskFolder. RegisterTask** o [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="6f567-193">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the [**LogonType**](principal-logontype.md) property of the task principal, or in the *logonType* parameter of **TaskFolder.RegisterTask** or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

<span data-ttu-id="6f567-194">Solo un miembro del grupo administradores puede crear una tarea con un desencadenador de arranque.</span><span class="sxs-lookup"><span data-stu-id="6f567-194">Only a member of the Administrators group can create a task with a boot trigger.</span></span>

<span data-ttu-id="6f567-195">Puede registrar correctamente una tarea con un grupo especificado en el parámetro *userId* y 3 (**\_ \_ \_ símbolo interactivo de inicio de sesión de tarea**) especificado en el parámetro *LogonType* de **TaskFolder. RegisterTask** o [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md), pero la tarea no se ejecutará.</span><span class="sxs-lookup"><span data-stu-id="6f567-195">You can successfully register a task with a group specified in the *userId* parameter and 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) specified in the *logonType* parameter of **TaskFolder.RegisterTask** or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md), but the task will not run.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f567-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f567-196">Requirements</span></span>



| <span data-ttu-id="6f567-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f567-197">Requirement</span></span> | <span data-ttu-id="6f567-198">Value</span><span class="sxs-lookup"><span data-stu-id="6f567-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f567-199">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f567-199">Minimum supported client</span></span><br/> | <span data-ttu-id="6f567-200">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6f567-200">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6f567-201">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f567-201">Minimum supported server</span></span><br/> | <span data-ttu-id="6f567-202">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f567-202">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6f567-203">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6f567-203">Type library</span></span><br/>             | <dl> <span data-ttu-id="6f567-204"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6f567-204"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6f567-205">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f567-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f567-206"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f567-206"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f567-207">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f567-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f567-208">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="6f567-208">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="6f567-209">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="6f567-209">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="6f567-210">**TaskFolder**</span><span class="sxs-lookup"><span data-stu-id="6f567-210">**TaskFolder**</span></span>](taskfolder.md)
</dt> </dl>

 

