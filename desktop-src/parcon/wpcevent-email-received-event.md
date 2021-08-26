---
description: Evento por usuario generado por un cliente de correo electrónico cuando se intenta recibir un mensaje en controles parentales.
ms.assetid: 3b8d9bac-16b0-49e9-b360-b2d6e82f1753
title: WPCEVENT_EMAIL_RECEIVED evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a81a51e79125403504aae2ed6e823c10044ffc35ed36ff139e8333f955338d81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951565"
---
# <a name="wpcevent_email_received-event"></a>Evento WPCEVENT \_ EMAIL \_ RECEIVED

Evento por usuario generado por un cliente de correo electrónico cuando se intenta recibir un mensaje en controles parentales.


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_RECEIVED = {0x4, 0x0, 0x10, 0x4, 0x16, 0x4, 0x8000000000000030};
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

La versión de la aplicación de correo electrónico que genera el evento.

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

 

 




