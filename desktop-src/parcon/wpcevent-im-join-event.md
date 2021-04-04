---
description: Evento por usuario generado por una aplicación de mensajería instantánea cuando una entidad intenta unirse a una conversación en curso en el control parental.
ms.assetid: 5251234b-0280-4d5d-80f5-295d720a89d1
title: Evento WPCEVENT_IM_JOIN (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b020eb3d4204f946002f59f472e5c95b715f88f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909386"
---
# <a name="wpcevent_im_join-event"></a>\_Evento WPCEVENT im \_ join

Evento por usuario generado por una aplicación de mensajería instantánea cuando una entidad intenta unirse a una conversación en curso en el control parental.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_JOIN = {0x8, 0x0, 0x10, 0x4, 0x16, 0x8, 0x8000000000000030};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AppName* 
</dt> <dd>

El nombre de la aplicación que está generando el evento.

</dd> <dt>

*Versiónaplicación* 
</dt> <dd>

La cadena de versión de la aplicación que está generando el evento.

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

Cadena de identidad de la cuenta de mensajería instantánea para el usuario que se va a combinar.

</dd> <dt>

*Motivo* 
</dt> <dd>

Un valor de la enumeración [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados y qué controles hay en su lugar.

</dd> <dt>

*MemberCount* 
</dt> <dd>

El recuento de participantes que se encuentran en la conversación y que tienen identidades definidas en el campo de miembro.

</dd> <dt>

*Member* 
</dt> <dd>

Una cadena delimitada que contiene cadenas de identidad de la cuenta de mensajería instantánea para todos los miembros actuales de esta conversación.

</dd> <dt>

*Sender* 
</dt> <dd>

Cadena de identidad de la cuenta de mensajería instantánea para el usuario que está realizando la solicitud para unirse a la conversación.

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

 

 




