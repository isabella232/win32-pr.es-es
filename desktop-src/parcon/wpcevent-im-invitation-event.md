---
description: Evento por usuario proporcionado para el inicio de sesión de las conversaciones por parte de clientes de mensajería instantánea.
ms.assetid: b2cd1d37-9993-4990-83b7-b147a109e4af
title: Evento WPCEVENT_IM_INVITATION (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87c9d7e90eaa901b5e18a072e03e3112ee8c2934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716669"
---
# <a name="wpcevent_im_invitation-event"></a>Evento de invitación de WPCEVENT \_ im \_

Evento por usuario proporcionado para el inicio de sesión de las conversaciones por parte de clientes de mensajería instantánea.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_INVITATION = {0x7, 0x0, 0x10, 0x4, 0x16, 0x7, 0x8000000000000030};
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

Cadena de identidad de la cuenta de mensajería instantánea.

</dd> <dt>

*ConvID* 
</dt> <dd>

Identificador de la conversación.

</dd> <dt>

*RequestingIP* 
</dt> <dd>

Cadena que contiene la dirección IP del equipo que envía la invitación.

</dd> <dt>

*Sender* 
</dt> <dd>

La cadena de identidad de la cuenta de mensajería instantánea para la cuenta que emite la invitación.

</dd> <dt>

*Motivo* 
</dt> <dd>

Un valor de la enumeración [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados y qué controles hay en su lugar.

</dd> <dt>

*RecipCount* 
</dt> <dd>

El número de destinatarios que reciben la invitación y que tienen identidades definidas en el campo de destinatario.

</dd> <dt>

*Recipient* 
</dt> <dd>

Una cadena delimitada que contiene cadenas de identidad de la cuenta de mensajería instantánea para los destinatarios de la invitación.

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

 

 




