---
description: Evento por usuario generado por un cliente de correo electrónico que registra Cuándo se agrega, cambia o elimina un contacto en el control parental.
ms.assetid: 9d1f52ef-ff49-4c0d-a48a-93aeccbe7f2b
title: Evento WPCEVENT_EMAIL_CONTACT (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0974030e53756b44f2be2e8550707161f2d6d461
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279036"
---
# <a name="wpcevent_email_contact-event"></a>\_Evento de contacto de correo electrónico de WPCEVENT \_

Evento por usuario generado por un cliente de correo electrónico que registra Cuándo se agrega, cambia o elimina un contacto en el control parental.


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_CONTACT = {0xe, 0x0, 0x10, 0x4, 0x16, 0xe, 0x8000000000000030};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AppName* 
</dt> <dd>

El nombre de la aplicación de correo electrónico que está generando el evento.

</dd> <dt>

*Versiónaplicación* 
</dt> <dd>

La versión de la aplicación de correo electrónico que está generando el evento.

</dd> <dt>

*OldName* 
</dt> <dd>

Nombre de la cuenta de correo electrónico anterior, si se ha eliminado o cambiado.

</dd> <dt>

*OldID* 
</dt> <dd>

IDENTIFICADOR asociado al nombre anterior de la cuenta de correo electrónico.

</dd> <dt>

*NewName* 
</dt> <dd>

Nombre de la nueva cuenta de correo electrónico, si se ha agregado o cambiado.

</dd> <dt>

*NewID* 
</dt> <dd>

IDENTIFICADOR asociado con el nombre de la nueva cuenta de correo electrónico.

</dd> <dt>

*Motivo* 
</dt> <dd>

Un valor de la enumeración [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados y qué controles hay en su lugar.

</dd> <dt>

*EmailAccount* 
</dt> <dd>

Nombre de la cuenta de correo electrónico para este usuario.

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

 

 




