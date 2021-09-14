---
description: Evento por usuario generado por un cliente de correo electrónico que registra cuándo se agrega, cambia o elimina un contacto en los controles parentales.
ms.assetid: 9d1f52ef-ff49-4c0d-a48a-93aeccbe7f2b
title: WPCEVENT_EMAIL_CONTACT evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0974030e53756b44f2be2e8550707161f2d6d461
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268420"
---
# <a name="wpcevent_email_contact-event"></a>Evento WPCEVENT \_ EMAIL \_ CONTACT

Evento por usuario generado por un cliente de correo electrónico que registra cuándo se agrega, cambia o elimina un contacto en los controles parentales.


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_CONTACT = {0xe, 0x0, 0x10, 0x4, 0x16, 0xe, 0x8000000000000030};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AppName* 
</dt> <dd>

Nombre de la aplicación de correo electrónico que genera el evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Versión de la aplicación de correo electrónico que genera el evento.

</dd> <dt>

*OldName* 
</dt> <dd>

El nombre de la cuenta de correo electrónico anterior, si se elimina o cambia.

</dd> <dt>

*Oldid* 
</dt> <dd>

Identificador asociado al nombre de la cuenta de correo electrónico anterior.

</dd> <dt>

*Newname* 
</dt> <dd>

Nombre de la nueva cuenta de correo electrónico, si se ha agregado o cambiado.

</dd> <dt>

*NewID* 
</dt> <dd>

Identificador asociado al nuevo nombre de la cuenta de correo electrónico.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valor de la enumeración [**\_ WPCFLAG ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados para su uso y qué controles están en su lugar.

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
| Encabezado<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Uso de las API de registro para los controles parentales](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




