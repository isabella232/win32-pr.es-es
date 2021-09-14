---
description: Evento por usuario generado por un cliente de mensajería instantánea cuando se agrega, cambia o quita información de contacto en controles parentales.
ms.assetid: 0a016542-306e-48b4-8b0c-b9e4e915513e
title: WPCEVENT_IM_CONTACT evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9747f7ede57f7a1d77af0f0e8e5425401ee32b36
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268404"
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
| Encabezado<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Uso de las API de registro para los controles parentales](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




