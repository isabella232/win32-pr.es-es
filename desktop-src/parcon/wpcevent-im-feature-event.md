---
description: Evento por usuario generado por un cliente de mensajería instantánea cuando se usan características definidas en los controles parentales.
ms.assetid: 45e80314-90b1-4fcf-9c8f-c9840ae1775b
title: WPCEVENT_IM_FEATURE evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee28f004560ed287bc3cb94cbee1bda876355834
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268399"
---
# <a name="wpcevent_im_feature-event"></a>Evento WPCEVENT \_ IM \_ FEATURE

Evento por usuario generado por un cliente de mensajería instantánea cuando se usan características definidas en los controles parentales.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_FEATURE = {0xb, 0x0, 0x10, 0x4, 0x16, 0xb, 0x8000000000000030};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AppName* 
</dt> <dd>

Nombre de la aplicación de mensajería instantánea.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Cadena de versión de la aplicación.

</dd> <dt>

*AccountName* 
</dt> <dd>

Nombre de la cuenta de mensajería instantánea de este usuario.

</dd> <dt>

*ConvID* 
</dt> <dd>

Identificador de esta conversación.

</dd> <dt>

*MediaType* 
</dt> <dd>

Valor de la [**enumeración WPCFLAG \_ IM \_ FEATURE**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_im_feature) que indica información sobre las características a las que se accede durante una interacción de mensajería instantánea.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valor de la enumeración [**\_ WPCFLAG ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados para su uso y qué controles están en su lugar.

</dd> <dt>

*RecipCount* 
</dt> <dd>

Recuento de usuarios de mensajería instantánea que reciben la característica y que tienen identidades definidas en el campo destinatario.

</dd> <dt>

*Recipient* 
</dt> <dd>

Cadena delimitada que contiene identidades de cuenta de mensajería instantánea de todos los usuarios que reciben la característica.

</dd> <dt>

*Sender* 
</dt> <dd>

Nombre de la cuenta de mensajería instantánea para el usuario que está aprovisionamiento de la característica.

</dd> <dt>

*SenderIP* 
</dt> <dd>

Dirección IP del equipo del remitente.

</dd> <dt>

*Data* 
</dt> <dd>

Descripción de los datos de la característica.

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

 

 




