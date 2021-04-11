---
description: Evento por usuario generado por un cliente de mensajería instantánea al agregar, cambiar o quitar información de contacto en el control parental.
ms.assetid: 0a016542-306e-48b4-8b0c-b9e4e915513e
title: Evento WPCEVENT_IM_CONTACT (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9747f7ede57f7a1d77af0f0e8e5425401ee32b36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279035"
---
# <a name="wpcevent_im_contact-event"></a>Evento de contacto de \_ im de WPCEVENT \_

Evento por usuario generado por un cliente de mensajería instantánea al agregar, cambiar o quitar información de contacto en el control parental.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_CONTACT = {0xf, 0x0, 0x10, 0x4, 0x16, 0xf, 0x8000000000000030};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AppName* 
</dt> <dd>

El nombre de la aplicación de mensajería instantánea que está generando el evento.

</dd> <dt>

*Versiónaplicación* 
</dt> <dd>

Versión de la aplicación que está generando el evento.

</dd> <dt>

*AccountName* 
</dt> <dd>

El nombre de la cuenta de mensajería instantánea para este usuario.

</dd> <dt>

*OldName* 
</dt> <dd>

El nombre anterior de la cuenta de mensajería instantánea, si se elimina o se cambia.

</dd> <dt>

*OldID* 
</dt> <dd>

IDENTIFICADOR asociado con el nombre de cuenta de mensajería instantánea anterior.

</dd> <dt>

*NewName* 
</dt> <dd>

El nuevo nombre de cuenta de mensajería instantánea, si se ha agregado o cambiado.

</dd> <dt>

*NewID* 
</dt> <dd>

IDENTIFICADOR asociado con el nuevo nombre de cuenta de mensajería instantánea.

</dd> <dt>

*Motivo* 
</dt> <dd>

Un valor de la enumeración [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados y qué controles hay en su lugar.

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

 

 




