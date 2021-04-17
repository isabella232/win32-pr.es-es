---
title: Tipo complejo de sendEmailType
description: Define el tipo de acción que se usa para especificar que se enviará un correo electrónico cuando se ejecute una tarea. Este tipo define todos los elementos que se usan para modelar el mensaje de correo electrónico.
ms.assetid: e384971f-e7e4-4206-9d15-9555dfcbac2f
keywords:
- tipo complejo de sendEmailType Programador de tareas
topic_type:
- apiref
api_name:
- sendEmailType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 959e0b8f03223eb23b7a7bec69ba9b2aeea66447
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676994"
---
# <a name="sendemailtype-complex-type"></a><span data-ttu-id="ad5f1-105">Tipo complejo de sendEmailType</span><span class="sxs-lookup"><span data-stu-id="ad5f1-105">sendEmailType Complex Type</span></span>

<span data-ttu-id="ad5f1-106">Define el tipo de acción que se usa para especificar que se enviará un correo electrónico cuando se ejecute una tarea.</span><span class="sxs-lookup"><span data-stu-id="ad5f1-106">Defines the action type used to specify that an email will be sent when a task executes.</span></span> <span data-ttu-id="ad5f1-107">Este tipo define todos los elementos que se usan para modelar el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ad5f1-107">This type defines all the elements used to model the email message.</span></span>

``` syntax
<xs:complexType name="sendEmailType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Server"
                    type="nonEmptyString"
                 />
                <xs:element name="Subject"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="To"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Cc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Bcc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="ReplyTo"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="From"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="HeaderFields"
                    type="headerFieldsType"
                    minOccurs="0"
                 />
                <xs:element name="Body"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Attachments"
                    type="attachmentsType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ad5f1-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ad5f1-108">Child elements</span></span>



| <span data-ttu-id="ad5f1-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="ad5f1-109">Element</span></span>                                                                        | <span data-ttu-id="ad5f1-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad5f1-110">Type</span></span>                                                                         | <span data-ttu-id="ad5f1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad5f1-111">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad5f1-112">**Datos adjuntos**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-112">**Attachments**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md)   | [<span data-ttu-id="ad5f1-113">**attachmentsType**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-113">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md)   | <span data-ttu-id="ad5f1-114">Especifica una lista de datos adjuntos en el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ad5f1-114">Specifies a list of attachments in the email message.</span></span><br/>                                 |
| [<span data-ttu-id="ad5f1-115">**CCO**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-115">**Bcc**</span></span>](taskschedulerschema-bcc-sendemailtype-element.md)                   | <span data-ttu-id="ad5f1-116">**string**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-116">**string**</span></span>                                                                   | <span data-ttu-id="ad5f1-117">Especifica las direcciones de correo electrónico utilizadas en la línea CCO de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ad5f1-117">Specifies the email addresses used on the Bcc line of an email message.</span></span><br/>               |
| [<span data-ttu-id="ad5f1-118">**Cuerpo**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-118">**Body**</span></span>](taskschedulerschema-body-sendemailtype-element.md)                 | <span data-ttu-id="ad5f1-119">**string**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-119">**string**</span></span>                                                                   | <span data-ttu-id="ad5f1-120">Especifica el texto en el cuerpo del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ad5f1-120">Specifies the text in the body of the email message.</span></span><br/>                                  |
| [<span data-ttu-id="ad5f1-121">**Correos**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-121">**Cc**</span></span>](taskschedulerschema-cc-sendemailtype-element.md)                     | <span data-ttu-id="ad5f1-122">**string**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-122">**string**</span></span>                                                                   | <span data-ttu-id="ad5f1-123">Especifica las direcciones de correo electrónico utilizadas en la línea CC de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ad5f1-123">Specifies the email addresses used on the Cc line of an email message.</span></span><br/>                |
| [<span data-ttu-id="ad5f1-124">**From**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-124">**From**</span></span>](taskschedulerschema-from-sendemailtype-element.md)                 | <span data-ttu-id="ad5f1-125">**string**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-125">**string**</span></span>                                                                   | <span data-ttu-id="ad5f1-126">Especifica la dirección de correo electrónico del remitente.</span><span class="sxs-lookup"><span data-stu-id="ad5f1-126">Specifies the email address of the sender.</span></span><br/>                                            |
| [<span data-ttu-id="ad5f1-127">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-127">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="ad5f1-128">**headerFieldsType**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-128">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="ad5f1-129">Especifica los campos de encabezado y sus valores utilizados en el encabezado del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ad5f1-129">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |
| [<span data-ttu-id="ad5f1-130">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-130">**ReplyTo**</span></span>](taskschedulerschema-replyto-sendemailtype-element.md)           | <span data-ttu-id="ad5f1-131">**string**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-131">**string**</span></span>                                                                   | <span data-ttu-id="ad5f1-132">Especifica las direcciones de correo electrónico a las que se responde en el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ad5f1-132">Specifies the email addresses that are replied to in the email message.</span></span><br/>               |
| [<span data-ttu-id="ad5f1-133">**Server**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-133">**Server**</span></span>](taskschedulerschema-server-sendemailtype-element.md)             | [<span data-ttu-id="ad5f1-134">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-134">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)      | <span data-ttu-id="ad5f1-135">Especifica el servidor de correo electrónico que se usa para enviar el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ad5f1-135">Specifies the email server used to send the email message.</span></span> <br/>                           |
| [<span data-ttu-id="ad5f1-136">**Asunto**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-136">**Subject**</span></span>](taskschedulerschema-subject-sendemailtype-element.md)           | <span data-ttu-id="ad5f1-137">**string**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-137">**string**</span></span>                                                                   | <span data-ttu-id="ad5f1-138">Especifica el asunto del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ad5f1-138">Specifies the subject of the email message.</span></span><br/>                                           |
| [<span data-ttu-id="ad5f1-139">**En**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-139">**To**</span></span>](taskschedulerschema-to-sendemailtype-element.md)                     | <span data-ttu-id="ad5f1-140">**string**</span><span class="sxs-lookup"><span data-stu-id="ad5f1-140">**string**</span></span>                                                                   | <span data-ttu-id="ad5f1-141">Especifica las direcciones de correo electrónico a las que se enviará el correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ad5f1-141">Specifies the email addresses to which the email will be sent.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="ad5f1-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad5f1-142">Requirements</span></span>



| <span data-ttu-id="ad5f1-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad5f1-143">Requirement</span></span> | <span data-ttu-id="ad5f1-144">Value</span><span class="sxs-lookup"><span data-stu-id="ad5f1-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ad5f1-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad5f1-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ad5f1-146">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ad5f1-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ad5f1-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad5f1-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ad5f1-148">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ad5f1-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





