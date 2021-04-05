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
# <a name="sendemail-actiongroup-element"></a>Elemento SendEmail (actionGroup)

Representa una acción que envía un mensaje de correo electrónico.

``` syntax
<xs:element name="SendEmail"
    type="sendEmailType"
 />
```

El elemento **sendEmail** se define mediante [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                         | Derivado de                                                       | Descripción                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Acciones**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Contiene las acciones realizadas por la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                        | Tipo                                                                         | Descripción                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Datos adjuntos**](taskschedulerschema-attachments-sendemailtype-element.md)   | [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md)   | Especifica una lista de datos adjuntos en el mensaje de correo electrónico.<br/>                                 |
| [**CCO**](taskschedulerschema-bcc-sendemailtype-element.md)                   | **string**                                                                   | Especifica las direcciones de correo electrónico utilizadas en la línea CCO de un mensaje de correo electrónico.<br/>               |
| [**Cuerpo**](taskschedulerschema-body-sendemailtype-element.md)                 | **string**                                                                   | Especifica el texto en el cuerpo del mensaje de correo electrónico.<br/>                                  |
| [**Correos**](taskschedulerschema-cc-sendemailtype-element.md)                     | **string**                                                                   | Especifica las direcciones de correo electrónico utilizadas en la línea CC de un mensaje de correo electrónico.<br/>                |
| [**From**](taskschedulerschema-from-sendemailtype-element.md)                 | **string**                                                                   | Especifica la dirección de correo electrónico del remitente.<br/>                                            |
| [**HeaderFields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) | Especifica los campos de encabezado y sus valores utilizados en el encabezado del mensaje de correo electrónico.<br/> |
| [**ReplyTo**](taskschedulerschema-replyto-sendemailtype-element.md)           | **string**                                                                   | Especifica las direcciones de correo electrónico a las que se responde en el mensaje de correo electrónico.<br/>               |
| [**Server**](taskschedulerschema-server-sendemailtype-element.md)             | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)      | Especifica el servidor de correo electrónico que se usa para enviar el mensaje de correo electrónico. <br/>                           |
| [**Asunto**](taskschedulerschema-subject-sendemailtype-element.md)           | **string**                                                                   | Especifica el asunto del mensaje de correo electrónico.<br/>                                           |
| [**En**](taskschedulerschema-to-sendemailtype-element.md)                     | **string**                                                                   | Especifica las direcciones de correo electrónico a las que se enviará el correo electrónico.<br/>                        |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea la interfaz [**IEmailAction**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) .

Para el desarrollo de scripts, vea el objeto [**EmailAction**](emailaction.md) .

**Windows 8 y Windows Server 2012:** Este elemento se ha quitado. Use IExecAction con el cmdlet [**send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) de PowerShell como solución alternativa.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que especifica una acción de correo electrónico, vea [ejemplo de desencadenador de eventos (XML)](/previous-versions//aa446889(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                 |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008 R2<br/>                    |



 

