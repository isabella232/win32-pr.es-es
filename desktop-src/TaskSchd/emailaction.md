---
title: Objeto EmailAction
description: Objeto de scripting que representa una acción que envía un mensaje de correo electrónico.
ms.assetid: edc0dc4d-eda0-47e0-981f-8521ac4678eb
keywords:
- Objeto EmailAction Programador de tareas
- Programador de tareas de objeto EmailAction, descrito
topic_type:
- apiref
api_name:
- EmailAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a339a1549b76f61499b7192a48edc7c1b86a6c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905536"
---
# <a name="emailaction-object"></a><span data-ttu-id="81ddd-105">Objeto EmailAction</span><span class="sxs-lookup"><span data-stu-id="81ddd-105">EmailAction object</span></span>

<span data-ttu-id="81ddd-106">\[Este objeto ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="81ddd-106">\[This object is no longer supported.</span></span> <span data-ttu-id="81ddd-107">Use IExecAction con el cmdlet [**send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) de PowerShell como solución alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="81ddd-107">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="81ddd-108">Objeto de scripting que representa una acción que envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="81ddd-108">Scripting object that represents an action that sends an email message.</span></span>

## <a name="members"></a><span data-ttu-id="81ddd-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="81ddd-109">Members</span></span>

<span data-ttu-id="81ddd-110">El objeto **EmailAction** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="81ddd-110">The **EmailAction** object has these types of members:</span></span>

-   [<span data-ttu-id="81ddd-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81ddd-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81ddd-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81ddd-112">Properties</span></span>

<span data-ttu-id="81ddd-113">El objeto **EmailAction** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="81ddd-113">The **EmailAction** object has these properties.</span></span>



| <span data-ttu-id="81ddd-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="81ddd-114">Property</span></span>                                                    | <span data-ttu-id="81ddd-115">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="81ddd-115">Access type</span></span>           | <span data-ttu-id="81ddd-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="81ddd-116">Description</span></span>                                                                                               |
|:------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81ddd-117">**Datos adjuntos**</span><span class="sxs-lookup"><span data-stu-id="81ddd-117">**Attachments**</span></span>](emailaction-attachments.md)<br/>   | <span data-ttu-id="81ddd-118">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="81ddd-118">Read/write</span></span><br/> | <span data-ttu-id="81ddd-119">Obtiene o establece una matriz de datos adjuntos que se envía con el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="81ddd-119">Gets or sets an array of attachments that is sent with the email message.</span></span><br/>                      |
| [<span data-ttu-id="81ddd-120">**CCO**</span><span class="sxs-lookup"><span data-stu-id="81ddd-120">**Bcc**</span></span>](emailaction-bcc.md)<br/>                   | <span data-ttu-id="81ddd-121">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="81ddd-121">Read/write</span></span><br/> | <span data-ttu-id="81ddd-122">Obtiene o establece la dirección o direcciones de correo electrónico que se van a incluir en el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="81ddd-122">Gets or sets the email address or addresses that you want to Bcc in the email message.</span></span><br/>         |
| [<span data-ttu-id="81ddd-123">**Cuerpo**</span><span class="sxs-lookup"><span data-stu-id="81ddd-123">**Body**</span></span>](emailaction-body.md)<br/>                 | <span data-ttu-id="81ddd-124">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="81ddd-124">Read/write</span></span><br/> | <span data-ttu-id="81ddd-125">Obtiene o establece el cuerpo del correo electrónico que contiene el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="81ddd-125">Gets or sets the body of the email that contains the email message.</span></span><br/>                            |
| [<span data-ttu-id="81ddd-126">**Correos**</span><span class="sxs-lookup"><span data-stu-id="81ddd-126">**Cc**</span></span>](emailaction-cc.md)<br/>                     | <span data-ttu-id="81ddd-127">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="81ddd-127">Read/write</span></span><br/> | <span data-ttu-id="81ddd-128">Obtiene o establece la dirección o direcciones de correo electrónico que desea CC en el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="81ddd-128">Gets or sets the email address or addresses that you want to Cc in the email message.</span></span><br/>          |
| [<span data-ttu-id="81ddd-129">**From**</span><span class="sxs-lookup"><span data-stu-id="81ddd-129">**From**</span></span>](emailaction-from.md)<br/>                 | <span data-ttu-id="81ddd-130">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="81ddd-130">Read/write</span></span><br/> | <span data-ttu-id="81ddd-131">Obtiene o establece la dirección de correo electrónico de la que desea enviar el correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="81ddd-131">Gets or sets the email address that you want to send the email from.</span></span><br/>                           |
| [<span data-ttu-id="81ddd-132">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="81ddd-132">**HeaderFields**</span></span>](emailaction-headerfields.md)<br/> | <span data-ttu-id="81ddd-133">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="81ddd-133">Read/write</span></span><br/> | <span data-ttu-id="81ddd-134">Obtiene o establece la información de encabezado del correo electrónico que se desea enviar.</span><span class="sxs-lookup"><span data-stu-id="81ddd-134">Gets or sets the header information in the email that you want to send.</span></span><br/>                        |
| [<span data-ttu-id="81ddd-135">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="81ddd-135">**Id**</span></span>](action-id.md)<br/>                          | <span data-ttu-id="81ddd-136">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="81ddd-136">Read/write</span></span><br/> | <span data-ttu-id="81ddd-137">Heredado del objeto de [**acción**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="81ddd-137">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="81ddd-138">Obtiene o establece el identificador de la acción.</span><span class="sxs-lookup"><span data-stu-id="81ddd-138">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="81ddd-139">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="81ddd-139">**ReplyTo**</span></span>](emailaction-replyto.md)<br/>           | <span data-ttu-id="81ddd-140">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="81ddd-140">Read/write</span></span><br/> | <span data-ttu-id="81ddd-141">Obtiene o establece la dirección de correo electrónico a la que se desea responder.</span><span class="sxs-lookup"><span data-stu-id="81ddd-141">Gets or sets the email address that you want to reply to.</span></span><br/>                                      |
| [<span data-ttu-id="81ddd-142">**Server**</span><span class="sxs-lookup"><span data-stu-id="81ddd-142">**Server**</span></span>](emailaction-server.md)<br/>             | <span data-ttu-id="81ddd-143">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="81ddd-143">Read/write</span></span><br/> | <span data-ttu-id="81ddd-144">Obtiene o establece el nombre del servidor del que se usa para enviar correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="81ddd-144">Gets or sets the name of the server that you use to send email from.</span></span><br/>                           |
| [<span data-ttu-id="81ddd-145">**Asunto**</span><span class="sxs-lookup"><span data-stu-id="81ddd-145">**Subject**</span></span>](emailaction-subject.md)<br/>           | <span data-ttu-id="81ddd-146">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="81ddd-146">Read/write</span></span><br/> | <span data-ttu-id="81ddd-147">Obtiene o establece el asunto del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="81ddd-147">Gets or sets the subject of the email message.</span></span><br/>                                                 |
| [<span data-ttu-id="81ddd-148">**En**</span><span class="sxs-lookup"><span data-stu-id="81ddd-148">**To**</span></span>](emailaction-to.md)<br/>                     | <span data-ttu-id="81ddd-149">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="81ddd-149">Read/write</span></span><br/> | <span data-ttu-id="81ddd-150">Obtiene o establece las direcciones de correo electrónico a las que desea enviar el correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="81ddd-150">Gets or sets the email address or addresses that you want to send the email to.</span></span><br/>                |
| [<span data-ttu-id="81ddd-151">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="81ddd-151">**Type**</span></span>](/windows/win32/api/taskschd/nf-taskschd-iaction-get_type)<br/>                     | <span data-ttu-id="81ddd-152">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="81ddd-152">Read-only</span></span><br/>  | <span data-ttu-id="81ddd-153">Heredado del objeto de [**acción**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="81ddd-153">Inherited from [**Action**](action.md) object.</span></span> <span data-ttu-id="81ddd-154">Obtiene el tipo de la acción.</span><span class="sxs-lookup"><span data-stu-id="81ddd-154">Gets the type of the action.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="81ddd-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81ddd-155">Remarks</span></span>

<span data-ttu-id="81ddd-156">La acción de correo electrónico debe tener un valor válido para las propiedades [**Server**](emailaction-server.md), [**from**](emailaction-from.md)y [**to**](emailaction-to.md) o [**CC**](emailaction-cc.md) para que la tarea se registre y se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="81ddd-156">The email action must have a valid value for the [**Server**](emailaction-server.md), [**From**](emailaction-from.md), and [**To**](emailaction-to.md) or [**Cc**](emailaction-cc.md) properties for the task to register and run correctly.</span></span>

<span data-ttu-id="81ddd-157">Al leer o escribir su propio XML para una tarea, se especifica una acción de correo electrónico mediante el elemento [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="81ddd-157">When reading or writing your own XML for a task, an email action is specified using the [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="81ddd-158">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="81ddd-158">Examples</span></span>

<span data-ttu-id="81ddd-159">Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de eventos (scripting)](/previous-versions//aa446887(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81ddd-159">For more information and example code for this scripting object, see [Event Trigger Example (Scripting)](/previous-versions//aa446887(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="81ddd-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81ddd-160">Requirements</span></span>



| <span data-ttu-id="81ddd-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="81ddd-161">Requirement</span></span> | <span data-ttu-id="81ddd-162">Value</span><span class="sxs-lookup"><span data-stu-id="81ddd-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81ddd-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81ddd-163">Minimum supported client</span></span><br/> | <span data-ttu-id="81ddd-164">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="81ddd-164">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="81ddd-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81ddd-165">Minimum supported server</span></span><br/> | <span data-ttu-id="81ddd-166">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="81ddd-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="81ddd-167">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="81ddd-167">End of client support</span></span><br/>    | <span data-ttu-id="81ddd-168">Windows 7</span><span class="sxs-lookup"><span data-stu-id="81ddd-168">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="81ddd-169">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="81ddd-169">End of server support</span></span><br/>    | <span data-ttu-id="81ddd-170">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="81ddd-170">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="81ddd-171">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="81ddd-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="81ddd-172"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="81ddd-172"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="81ddd-173">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="81ddd-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81ddd-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81ddd-174"><dt>Taskschd.dll</dt></span></span> </dl> |



 

