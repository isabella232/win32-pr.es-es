---
description: Evento por usuario generado por un cliente de mensajería instantánea cuando se agrega, cambia o quita información de contacto en controles parentales.
ms.assetid: 0a016542-306e-48b4-8b0c-b9e4e915513e
title: WPCEVENT_IM_CONTACT evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baac4bf5648b27f2e8d446a79bb2d90d52f0aac416e30d031d3b81d430a6927b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951455"
---
# <a name="wpcevent_im_contact-event"></a>Evento WPCEVENT \_ IM \_ CONTACT

Evento por usuario generado por un cliente de mensajería instantánea cuando se agrega, cambia o quita información de contacto en controles parentales.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_CONTACT = {0xf, 0x0, 0x10, 0x4, 0x16, 0xf, 0x8000000000000030};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AppName* 
</dt> <dd>

Nombre de la aplicación de mensajería instantánea que genera el evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Versión de la aplicación que genera el evento.

</dd> <dt>

*AccountName* 
</dt> <dd>

Nombre de la cuenta de mensajería instantánea para este usuario.

</dd> <dt>

*OldName* 
</dt> <dd>

El nombre de la cuenta de mensajería instantánea anterior, si se elimina o cambia.

</dd> <dt>

*Oldid* 
</dt> <dd>

Identificador asociado al nombre de la cuenta de mensajería instantánea anterior.

</dd> <dt>

*Newname* 
</dt> <dd>

Nombre de la nueva cuenta de mensajería instantánea, si se agrega o cambia.

</dd> <dt>

*NewID* 
</dt> <dd>

Identificador asociado al nuevo nombre de cuenta de mensajería instantánea.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valor de la enumeración [**\_ WPCFLAG ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados para su uso y qué controles están en su lugar.

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

 

 




