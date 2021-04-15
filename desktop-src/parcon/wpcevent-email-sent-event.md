---
description: Evento por usuario generado por un cliente de correo electrónico cuando se intenta enviar un mensaje en el control parental.
ms.assetid: c49919a2-2a03-475d-9cfa-20a960184202
title: Evento WPCEVENT_EMAIL_SENT (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd222e946f0b7c78116ace9d8d01de2e2709a7ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649255"
---
# <a name="wpcevent_email_sent-event"></a>\_Evento de envío de correo electrónico WPCEVENT \_

Evento por usuario generado por un cliente de correo electrónico cuando se intenta enviar un mensaje en el control parental.


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_SENT = {0x5, 0x0, 0x10, 0x4, 0x16, 0x5, 0x8000000000000030};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Sender* 
</dt> <dd>

Nombre de la cuenta de correo electrónico de la entidad emisora.

</dd> <dt>

*AppName* 
</dt> <dd>

El nombre de la aplicación de correo electrónico que está generando el evento.

</dd> <dt>

*Versiónaplicación* 
</dt> <dd>

La versión de la aplicación de correo electrónico que está generando el evento.

</dd> <dt>

*Subject* 
</dt> <dd>

La línea de asunto del mensaje recibido.

</dd> <dt>

*Motivo* 
</dt> <dd>

Un valor de la enumeración [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados y qué controles hay en su lugar.

</dd> <dt>

*RecipCount* 
</dt> <dd>

El número de destinatarios de correo electrónico que reciben el mensaje y que tienen identidades definidas en el campo de destinatario.

</dd> <dt>

*Recipient* 
</dt> <dd>

Una cadena delimitada que contiene los nombres de las cuentas de correo electrónico de todos los destinatarios del mensaje.

</dd> <dt>

*AttachCount* 
</dt> <dd>

El número de datos adjuntos al mensaje.

</dd> <dt>

*AttachmentName* 
</dt> <dd>

Una cadena delimitada que contiene los nombres de todos los datos adjuntos del mensaje.

</dd> <dt>

*ReceivedTime* 
</dt> <dd>

La hora a la que se intentó recibir el mensaje.

</dd> <dt>

*EmailAccount* 
</dt> <dd>

Nombre de la cuenta de correo electrónico para este usuario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Encabezado<br/>                   | <dl> <dt>Wpcevent. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de las API de registro para controles parentales](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ args \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




