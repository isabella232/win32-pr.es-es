---
description: Evento por usuario generado por un cliente de mensajería instantánea cuando un usuario deja una conversación en los controles parentales.
ms.assetid: e6bd6bce-9eba-4192-aac8-c9e47d7180a1
title: WPCEVENT_IM_LEAVE evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260833a30f08330da9c622faae06f76b5d79e682
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574672"
---
# <a name="wpcevent_im_leave-event"></a>Evento IM \_ LEAVE de WPCEVENT \_

Evento por usuario generado por un cliente de mensajería instantánea cuando un usuario deja una conversación en los controles parentales.


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

Cadena que contiene la dirección IP del equipo que sale de esta conversación.

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

Recuento de participantes que están en la conversación y que tienen identidades definidas en el campo miembro.

</dd> <dt>

*Miembro* 
</dt> <dd>

Cadena delimitada que contiene cadenas de identidad de cuenta de mensajería instantánea para todos los miembros actuales de esta conversación.

</dd> <dt>

*Marcas* 
</dt> <dd>

Valor de la enumeración [**WPCFLAG \_ IM \_ LEAVE**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_im_leave) que indica información sobre cuándo un participante abandona la interacción de mensajería instantánea.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Encabezado<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Uso de las API de registro para los controles parentales](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




