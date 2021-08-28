---
description: Evento por usuario generado por un cliente de correo electrónico cuando se intenta enviar un mensaje en controles parentales.
ms.assetid: c49919a2-2a03-475d-9cfa-20a960184202
title: WPCEVENT_EMAIL_SENT evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe3d5fb08764aa83677fcca66af7f1e3b868f2b1bdf393741865bf64fd23049
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112735"
---
# <a name="wpcevent_email_sent-event"></a>Evento WPCEVENT \_ EMAIL \_ SENT

Evento por usuario generado por un cliente de correo electrónico cuando se intenta enviar un mensaje en controles parentales.


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_SENT = {0x5, 0x0, 0x10, 0x4, 0x16, 0x5, 0x8000000000000030};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Sender* 
</dt> <dd>

Nombre de la cuenta de correo electrónico de la entidad de envío.

</dd> <dt>

*AppName* 
</dt> <dd>

Nombre de la aplicación de correo electrónico que genera el evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Versión de la aplicación de correo electrónico que genera el evento.

</dd> <dt>

*Subject* 
</dt> <dd>

Línea de asunto del mensaje recibido.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valor de la enumeración [**\_ WPCFLAG ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados para su uso y qué controles están en su lugar.

</dd> <dt>

*RecipCount* 
</dt> <dd>

Recuento de destinatarios de correo electrónico que reciben el mensaje y que tienen identidades definidas en el campo destinatario.

</dd> <dt>

*Recipient* 
</dt> <dd>

Cadena delimitada que contiene los nombres de cuenta de correo electrónico de todos los destinatarios del mensaje.

</dd> <dt>

*AttachCount* 
</dt> <dd>

Recuento de datos adjuntos al mensaje.

</dd> <dt>

*AttachmentName* 
</dt> <dd>

Cadena delimitada que contiene los nombres de todos los datos adjuntos al mensaje.

</dd> <dt>

*ReceivedTime* 
</dt> <dd>

Hora a la que se intentó recibir el mensaje.

</dd> <dt>

*EmailAccount* 
</dt> <dd>

Nombre de la cuenta de correo electrónico de este usuario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Header<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de las API de registro para los controles parentales](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




