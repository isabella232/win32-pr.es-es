---
title: Elemento SendEmail (actionGroup)
description: Representa una acción que envía un mensaje de correo electrónico.
ms.assetid: 83416b02-8327-47b3-9dfc-1bf5b9365728
keywords:
- Elemento SendEmail Programador de tareas
topic_type:
- apiref
api_name:
- SendEmail
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81f6f3437521dea2c5cf6e157ad7997718632081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996844"
---
# <a name="sendemail-actiongroup-element"></a><span data-ttu-id="9c3f8-104">Elemento SendEmail (actionGroup)</span><span class="sxs-lookup"><span data-stu-id="9c3f8-104">SendEmail (actionGroup) Element</span></span>

<span data-ttu-id="9c3f8-105">Representa una acción que envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9c3f8-105">Represents an action that sends an email message.</span></span>

``` syntax
<xs:element name="SendEmail"
    type="sendEmailType"
 />
```

<span data-ttu-id="9c3f8-106">El elemento **sendEmail** se define mediante [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="9c3f8-106">The **SendEmail** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="9c3f8-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="9c3f8-107">Parent element</span></span>



| <span data-ttu-id="9c3f8-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="9c3f8-108">Element</span></span>                                                         | <span data-ttu-id="9c3f8-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="9c3f8-109">Derived from</span></span>                                                       | <span data-ttu-id="9c3f8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c3f8-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="9c3f8-111">**Acciones**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="9c3f8-112">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="9c3f8-113">Contiene las acciones realizadas por la tarea.</span><span class="sxs-lookup"><span data-stu-id="9c3f8-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="9c3f8-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9c3f8-114">Child elements</span></span>



| <span data-ttu-id="9c3f8-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="9c3f8-115">Element</span></span>                                                                        | <span data-ttu-id="9c3f8-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c3f8-116">Type</span></span>                                                                         | <span data-ttu-id="9c3f8-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c3f8-117">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c3f8-118">**Datos adjuntos**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-118">**Attachments**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md)   | [<span data-ttu-id="9c3f8-119">**attachmentsType**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-119">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md)   | <span data-ttu-id="9c3f8-120">Especifica una lista de datos adjuntos en el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9c3f8-120">Specifies a list of attachments in the email message.</span></span><br/>                                 |
| [<span data-ttu-id="9c3f8-121">**CCO**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-121">**Bcc**</span></span>](taskschedulerschema-bcc-sendemailtype-element.md)                   | <span data-ttu-id="9c3f8-122">**string**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-122">**string**</span></span>                                                                   | <span data-ttu-id="9c3f8-123">Especifica las direcciones de correo electrónico utilizadas en la línea CCO de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9c3f8-123">Specifies the email addresses used on the Bcc line of an email message.</span></span><br/>               |
| [<span data-ttu-id="9c3f8-124">**Cuerpo**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-124">**Body**</span></span>](taskschedulerschema-body-sendemailtype-element.md)                 | <span data-ttu-id="9c3f8-125">**string**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-125">**string**</span></span>                                                                   | <span data-ttu-id="9c3f8-126">Especifica el texto en el cuerpo del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9c3f8-126">Specifies the text in the body of the email message.</span></span><br/>                                  |
| [<span data-ttu-id="9c3f8-127">**Correos**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-127">**Cc**</span></span>](taskschedulerschema-cc-sendemailtype-element.md)                     | <span data-ttu-id="9c3f8-128">**string**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-128">**string**</span></span>                                                                   | <span data-ttu-id="9c3f8-129">Especifica las direcciones de correo electrónico utilizadas en la línea CC de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9c3f8-129">Specifies the email addresses used on the Cc line of an email message.</span></span><br/>                |
| [<span data-ttu-id="9c3f8-130">**From**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-130">**From**</span></span>](taskschedulerschema-from-sendemailtype-element.md)                 | <span data-ttu-id="9c3f8-131">**string**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-131">**string**</span></span>                                                                   | <span data-ttu-id="9c3f8-132">Especifica la dirección de correo electrónico del remitente.</span><span class="sxs-lookup"><span data-stu-id="9c3f8-132">Specifies the email address of the sender.</span></span><br/>                                            |
| [<span data-ttu-id="9c3f8-133">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-133">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="9c3f8-134">**headerFieldsType**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-134">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="9c3f8-135">Especifica los campos de encabezado y sus valores utilizados en el encabezado del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9c3f8-135">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |
| [<span data-ttu-id="9c3f8-136">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-136">**ReplyTo**</span></span>](taskschedulerschema-replyto-sendemailtype-element.md)           | <span data-ttu-id="9c3f8-137">**string**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-137">**string**</span></span>                                                                   | <span data-ttu-id="9c3f8-138">Especifica las direcciones de correo electrónico a las que se responde en el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9c3f8-138">Specifies the email addresses that are replied to in the email message.</span></span><br/>               |
| [<span data-ttu-id="9c3f8-139">**Server**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-139">**Server**</span></span>](taskschedulerschema-server-sendemailtype-element.md)             | [<span data-ttu-id="9c3f8-140">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-140">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)      | <span data-ttu-id="9c3f8-141">Especifica el servidor de correo electrónico que se usa para enviar el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9c3f8-141">Specifies the email server used to send the email message.</span></span> <br/>                           |
| [<span data-ttu-id="9c3f8-142">**Asunto**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-142">**Subject**</span></span>](taskschedulerschema-subject-sendemailtype-element.md)           | <span data-ttu-id="9c3f8-143">**string**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-143">**string**</span></span>                                                                   | <span data-ttu-id="9c3f8-144">Especifica el asunto del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9c3f8-144">Specifies the subject of the email message.</span></span><br/>                                           |
| [<span data-ttu-id="9c3f8-145">**En**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-145">**To**</span></span>](taskschedulerschema-to-sendemailtype-element.md)                     | <span data-ttu-id="9c3f8-146">**string**</span><span class="sxs-lookup"><span data-stu-id="9c3f8-146">**string**</span></span>                                                                   | <span data-ttu-id="9c3f8-147">Especifica las direcciones de correo electrónico a las que se enviará el correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9c3f8-147">Specifies the email addresses to which the email will be sent.</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="9c3f8-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c3f8-148">Remarks</span></span>

<span data-ttu-id="9c3f8-149">Para el desarrollo de C++, vea la interfaz [**IEmailAction**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) .</span><span class="sxs-lookup"><span data-stu-id="9c3f8-149">For C++ development, see the [**IEmailAction**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) interface.</span></span>

<span data-ttu-id="9c3f8-150">Para el desarrollo de scripts, vea el objeto [**EmailAction**](emailaction.md) .</span><span class="sxs-lookup"><span data-stu-id="9c3f8-150">For script development, see the [**EmailAction**](emailaction.md) object.</span></span>

<span data-ttu-id="9c3f8-151">**Windows 8 y Windows Server 2012:** Este elemento se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="9c3f8-151">**Windows 8 and Windows Server 2012:** This element has been removed.</span></span> <span data-ttu-id="9c3f8-152">Use IExecAction con el cmdlet [**send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) de PowerShell como solución alternativa.</span><span class="sxs-lookup"><span data-stu-id="9c3f8-152">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.</span></span>

## <a name="examples"></a><span data-ttu-id="9c3f8-153">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9c3f8-153">Examples</span></span>

<span data-ttu-id="9c3f8-154">Para obtener un ejemplo completo del XML de una tarea que especifica una acción de correo electrónico, vea [ejemplo de desencadenador de eventos (XML)](/previous-versions//aa446889(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9c3f8-154">For a complete example of the XML for a task that specifies an email action, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c3f8-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c3f8-155">Requirements</span></span>



| <span data-ttu-id="9c3f8-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c3f8-156">Requirement</span></span> | <span data-ttu-id="9c3f8-157">Value</span><span class="sxs-lookup"><span data-stu-id="9c3f8-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9c3f8-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c3f8-158">Minimum supported client</span></span><br/> | <span data-ttu-id="9c3f8-159">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9c3f8-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9c3f8-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c3f8-160">Minimum supported server</span></span><br/> | <span data-ttu-id="9c3f8-161">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c3f8-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9c3f8-162">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="9c3f8-162">End of client support</span></span><br/>    | <span data-ttu-id="9c3f8-163">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c3f8-163">Windows 7</span></span><br/>                                 |
| <span data-ttu-id="9c3f8-164">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="9c3f8-164">End of server support</span></span><br/>    | <span data-ttu-id="9c3f8-165">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9c3f8-165">Windows Server 2008 R2</span></span><br/>                    |



 

