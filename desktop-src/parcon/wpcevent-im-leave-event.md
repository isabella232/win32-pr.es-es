---
description: Evento por usuario generado por un cliente de mensajería instantánea cuando un usuario deja una conversación en controles parentales.
ms.assetid: e6bd6bce-9eba-4192-aac8-c9e47d7180a1
title: WPCEVENT_IM_LEAVE evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d814f6c9d4e3ec5acd3ee3cf3a6eb6e67d315148304f2766baf45fc633fa22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951215"
---
# <a name="wpcevent_im_leave-event"></a>Evento WPCEVENT \_ IM \_ LEAVE

Evento por usuario generado por un cliente de mensajería instantánea cuando un usuario deja una conversación en controles parentales.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_LEAVE = {0x9, 0x0, 0x10, 0x4, 0x16, 0x9, 0x8000000000000030};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AppName* 
</dt> <dd>

Nombre de la aplicación que genera el evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Cadena de versión de la aplicación que genera el evento.

</dd> <dt>

*AccountName* 
</dt> <dd>

Cadena de identidad de la cuenta de mensajería instantánea para este usuario.

</dd> <dt>

*ConvID* 
</dt> <dd>

Identificador de esta conversación.

</dd> <dt>

*LeavingIP* 
</dt> <dd>

Cadena que contiene la dirección IP del equipo que abandona esta conversación.

</dd> <dt>

*LeavingUser* 
</dt> <dd>

Cadena de identidad de la cuenta de mensajería instantánea para el usuario que se va.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valor de la enumeración [**\_ WPCFLAG ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados para su uso y qué controles están en su lugar.

</dd> <dt>

*MemberCount* 
</dt> <dd>

Recuento de participantes que están en la conversación y que tienen identidades definidas en el campo de miembro.

</dd> <dt>

*Miembro* 
</dt> <dd>

Cadena delimitada que contiene cadenas de identidad de cuenta de mensajería instantánea para todos los miembros actuales de esta conversación.

</dd> <dt>

*Marcas* 
</dt> <dd>

Valor de la [**enumeración WPCFLAG \_ IM \_ LEAVE**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_im_leave) que indica información sobre cuándo un participante abandona la interacción de mensajería instantánea.

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

 

 




