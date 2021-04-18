---
title: Propiedad principal. LogonType
description: En el caso de scripting, obtiene o establece el método de inicio de sesión de seguridad necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.
ms.assetid: ac6fd7a1-00ef-4478-920f-de391a5a2c8c
keywords:
- Programador de tareas de la propiedad LogonType
- Propiedad LogonType Programador de tareas, objeto principal
- Programador de tareas de objeto principal, propiedad LogonType
topic_type:
- apiref
api_name:
- Principal.LogonType
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4455fd273144b2d6abd81c78be31a1b037cd889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491092"
---
# <a name="principallogontype-property"></a><span data-ttu-id="2e668-106">Propiedad principal. LogonType</span><span class="sxs-lookup"><span data-stu-id="2e668-106">Principal.LogonType property</span></span>

<span data-ttu-id="2e668-107">En el caso de scripting, obtiene o establece el método de inicio de sesión de seguridad necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2e668-107">For scripting, gets or sets the security logon method that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e668-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e668-108">Syntax</span></span>


```VB
Principal.LogonType As Integer
```



## <a name="property-value"></a><span data-ttu-id="2e668-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2e668-109">Property value</span></span>

<span data-ttu-id="2e668-110">Establezca en una de las siguientes constantes de enumeración de [**\_ tipo de inicio de sesión de tarea**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) .</span><span class="sxs-lookup"><span data-stu-id="2e668-110">Set to one of the following [**TASK\_LOGON TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) enumeration constants.</span></span>



| <span data-ttu-id="2e668-111">Value</span><span class="sxs-lookup"><span data-stu-id="2e668-111">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="2e668-112">Significado</span><span class="sxs-lookup"><span data-stu-id="2e668-112">Meaning</span></span>                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <span data-ttu-id="2e668-113"><dt>**Tarea \_ de LOGON \_ ninguno**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2e668-113"><dt>**TASK\_LOGON\_NONE**</dt> <dt>0</dt></span></span> </dl>                                                                               | <span data-ttu-id="2e668-114">No se ha especificado el método Logon.</span><span class="sxs-lookup"><span data-stu-id="2e668-114">The logon method is not specified.</span></span> <span data-ttu-id="2e668-115">Se usa para las credenciales que no son NT.</span><span class="sxs-lookup"><span data-stu-id="2e668-115">Used for non-NT credentials.</span></span> <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <span data-ttu-id="2e668-116"><dt>**Tarea \_ de \_Contraseña de inicio de sesión**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2e668-116"><dt>**TASK\_LOGON\_PASSWORD**</dt> <dt>1</dt></span></span> </dl>                                                                   | <span data-ttu-id="2e668-117">Use una contraseña para iniciar sesión en el usuario.</span><span class="sxs-lookup"><span data-stu-id="2e668-117">Use a password for logging on the user.</span></span> <span data-ttu-id="2e668-118">La contraseña debe proporcionarse en el momento del registro.</span><span class="sxs-lookup"><span data-stu-id="2e668-118">The password must be supplied at registration time.</span></span><br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <span data-ttu-id="2e668-119"><dt>**Tarea \_ de Inicio de sesión \_ S4U**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2e668-119"><dt>**TASK\_LOGON\_S4U**</dt> <dt>2</dt></span></span> </dl>                                                                                  | <span data-ttu-id="2e668-120">Use un token interactivo existente para ejecutar una tarea.</span><span class="sxs-lookup"><span data-stu-id="2e668-120">Use an existing interactive token to run a task.</span></span> <span data-ttu-id="2e668-121">El usuario debe iniciar sesión con un inicio de sesión de servicio para el usuario (S4U).</span><span class="sxs-lookup"><span data-stu-id="2e668-121">The user must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="2e668-122">Cuando se usa un inicio de sesión de S4U, el sistema no almacena ninguna contraseña y no se tiene acceso a la red ni a los archivos cifrados.</span><span class="sxs-lookup"><span data-stu-id="2e668-122">When an S4U logon is used, no password is stored by the system and there is no access to either the network or encrypted files.</span></span><br/>                                                |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <span data-ttu-id="2e668-123"><dt>**Tarea \_ de \_ \_ Token interactivo de inicio de sesión**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2e668-123"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="2e668-124">El usuario ya debe haber iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="2e668-124">User must already be logged on.</span></span> <span data-ttu-id="2e668-125">La tarea se ejecutará solo en una sesión interactiva existente.</span><span class="sxs-lookup"><span data-stu-id="2e668-125">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <span data-ttu-id="2e668-126"><dt>**Tarea \_ de \_Grupo de inicio de sesión**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2e668-126"><dt>**TASK\_LOGON\_GROUP**</dt> <dt>4</dt></span></span> </dl>                                                                            | <span data-ttu-id="2e668-127">Activación de grupos.</span><span class="sxs-lookup"><span data-stu-id="2e668-127">Group activation.</span></span> <span data-ttu-id="2e668-128">El campo userId especifica el grupo.</span><span class="sxs-lookup"><span data-stu-id="2e668-128">The userId field specifies the group.</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <span data-ttu-id="2e668-129"><dt>**Tarea \_ de \_ \_ Cuenta de servicio de inicio de sesión**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2e668-129"><dt>**TASK\_LOGON\_SERVICE\_ACCOUNT**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="2e668-130">Indica que se utiliza un sistema local, servicio local o cuenta de servicio de red como contexto de seguridad para ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="2e668-130">Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.</span></span><br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <span data-ttu-id="2e668-131"><dt>**Tarea \_ de \_Token interactivo \_ de inicio \_ de sesión o \_ contraseña**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2e668-131"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="2e668-132">En primer lugar, use el token interactivo.</span><span class="sxs-lookup"><span data-stu-id="2e668-132">First use the interactive token.</span></span> <span data-ttu-id="2e668-133">Si el usuario no ha iniciado sesión (no hay ningún token interactivo disponible), se usa la contraseña.</span><span class="sxs-lookup"><span data-stu-id="2e668-133">If the user is not logged on (no interactive token is available), then the password is used.</span></span> <span data-ttu-id="2e668-134">La contraseña debe especificarse cuando se registra una tarea.</span><span class="sxs-lookup"><span data-stu-id="2e668-134">The password must be specified when a task is registered.</span></span> <span data-ttu-id="2e668-135">Esta marca no se recomienda para las nuevas tareas porque es menos confiable que la contraseña de inicio de sesión de la tarea \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2e668-135">This flag is not recommended for new tasks because it is less reliable than TASK\_LOGON\_PASSWORD.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2e668-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e668-136">Remarks</span></span>

<span data-ttu-id="2e668-137">Esta propiedad solo es válida cuando la propiedad [**userid**](principal-userid.md) especifica un identificador de usuario.</span><span class="sxs-lookup"><span data-stu-id="2e668-137">This property is valid only when a user identifier is specified by the [**UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="2e668-138">Al leer o escribir XML para una tarea, el tipo de inicio de sesión se especifica en el [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) elemento del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="2e668-138">When reading or writing XML for a task, the logon type is specified in the [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="2e668-139">En el caso de una tarea que contenga una acción de cuadro de mensaje, se mostrará el cuadro de mensaje si la tarea está activada y la tarea tiene un tipo de inicio de sesión interactivo.</span><span class="sxs-lookup"><span data-stu-id="2e668-139">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="2e668-140">Para establecer el tipo de inicio de sesión de tarea en interactivo, especifique 3 (**\_ \_ \_ token interactivo de inicio de sesión de tarea**) o 4 (**\_ \_ grupo de inicio de sesión de tareas**) en la propiedad **LogonType** de la entidad de seguridad de la tarea, o en el parámetro *LogonType* de [**TaskFolder. RegisterTask**](taskfolder-registertask.md) o [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="2e668-140">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the **LogonType** property of the task principal, or in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e668-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e668-141">Requirements</span></span>



| <span data-ttu-id="2e668-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e668-142">Requirement</span></span> | <span data-ttu-id="2e668-143">Value</span><span class="sxs-lookup"><span data-stu-id="2e668-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e668-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e668-144">Minimum supported client</span></span><br/> | <span data-ttu-id="2e668-145">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2e668-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2e668-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e668-146">Minimum supported server</span></span><br/> | <span data-ttu-id="2e668-147">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e668-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2e668-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2e668-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="2e668-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2e668-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2e668-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2e668-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e668-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e668-151"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e668-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e668-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e668-153">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="2e668-153">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="2e668-154">**Principal**</span><span class="sxs-lookup"><span data-stu-id="2e668-154">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 





