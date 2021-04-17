---
description: Evento por usuario generado por un cliente de mensajería instantánea cuando un usuario deja una conversación en el control parental.
ms.assetid: e6bd6bce-9eba-4192-aac8-c9e47d7180a1
title: Evento WPCEVENT_IM_LEAVE (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260833a30f08330da9c622faae06f76b5d79e682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716948"
---
# <a name="wpcevent_im_leave-event"></a>\_Evento WPCEVENT im \_ leave

Evento por usuario generado por un cliente de mensajería instantánea cuando un usuario deja una conversación en el control parental.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_LEAVE = {0x9, 0x0, 0x10, 0x4, 0x16, 0x9, 0x8000000000000030};
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

*LeavingIP* 
</dt> <dd>

Una cadena que contiene la dirección IP del equipo que sale de esta conversación.

</dd> <dt>

*LeavingUser* 
</dt> <dd>

Cadena de identidad de la cuenta de mensajería instantánea para el usuario que está saliendo.

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

*Marcas* 
</dt> <dd>

Un valor de la enumeración de [**WPCFLAG \_ im \_ leave**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_im_leave) que indica información sobre cuándo un participante abandona la interacción de mensajería instantánea.

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

 

 




