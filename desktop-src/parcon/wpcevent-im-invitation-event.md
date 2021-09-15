---
description: Evento por usuario proporcionado para iniciar el registro de conversaciones por parte de clientes de mensajería instantánea.
ms.assetid: b2cd1d37-9993-4990-83b7-b147a109e4af
title: WPCEVENT_IM_INVITATION evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87c9d7e90eaa901b5e18a072e03e3112ee8c2934
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574676"
---
# <a name="wpcevent_im_invitation-event"></a>Evento DE INVITACIÓN \_ DE MENSAJERÍA DE WPCEVENT \_

Evento por usuario proporcionado para iniciar el registro de conversaciones por parte de clientes de mensajería instantánea.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_INVITATION = {0x7, 0x0, 0x10, 0x4, 0x16, 0x7, 0x8000000000000030};
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

Cadena de identidad de la cuenta de mensajería instantánea.

</dd> <dt>

*ConvID* 
</dt> <dd>

Identificador de la conversación.

</dd> <dt>

*Solicitud deIP* 
</dt> <dd>

Cadena que contiene la dirección IP del equipo que envía la invitación.

</dd> <dt>

*Sender* 
</dt> <dd>

Cadena de identidad de la cuenta de mensajería instantánea para la cuenta que emite la invitación.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valor de la enumeración [**\_ WPCFLAG ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados para su uso y qué controles están en su lugar.

</dd> <dt>

*RecipCount* 
</dt> <dd>

Recuento de destinatarios que reciben la invitación y que tienen identidades definidas en el campo destinatario.

</dd> <dt>

*Recipient* 
</dt> <dd>

Cadena delimitada que contiene cadenas de identidad de cuenta de mensajería instantánea para los destinatarios de la invitación.

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

 

 




