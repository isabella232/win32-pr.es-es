---
description: Evento por usuario generado por una aplicación de mensajería instantánea cuando una entidad intenta unirse a una conversación en curso en Controles parentales.
ms.assetid: 5251234b-0280-4d5d-80f5-295d720a89d1
title: WPCEVENT_IM_JOIN evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b020eb3d4204f946002f59f472e5c95b715f88f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574673"
---
# <a name="wpcevent_im_join-event"></a>Evento IM \_ JOIN de WPCEVENT \_

Evento por usuario generado por una aplicación de mensajería instantánea cuando una entidad intenta unirse a una conversación en curso en Controles parentales.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_JOIN = {0x8, 0x0, 0x10, 0x4, 0x16, 0x8, 0x8000000000000030};
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

*JoiningIP* 
</dt> <dd>

Cadena que contiene la dirección IP del equipo que se une a esta conversación.

</dd> <dt>

*JoiningUser* 
</dt> <dd>

Cadena de identidad de la cuenta de mensajería instantánea para el usuario que se va a unir.

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

*Sender* 
</dt> <dd>

Cadena de identidad de la cuenta de mensajería instantánea para el usuario que realiza la solicitud para unirse a la conversación.

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

 

 




