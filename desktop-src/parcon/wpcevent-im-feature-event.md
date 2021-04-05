---
description: Evento por usuario generado por un cliente de mensajería instantánea cuando se usan características definidas en controles parentales.
ms.assetid: 45e80314-90b1-4fcf-9c8f-c9840ae1775b
title: Evento WPCEVENT_IM_FEATURE (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee28f004560ed287bc3cb94cbee1bda876355834
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001842"
---
# <a name="wpcevent_im_feature-event"></a>Evento de característica de WPCEVENT \_ im \_

Evento por usuario generado por un cliente de mensajería instantánea cuando se usan características definidas en controles parentales.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_FEATURE = {0xb, 0x0, 0x10, 0x4, 0x16, 0xb, 0x8000000000000030};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AppName* 
</dt> <dd>

El nombre de la aplicación de mensajería instantánea.

</dd> <dt>

*Versiónaplicación* 
</dt> <dd>

La cadena de versión de la aplicación.

</dd> <dt>

*AccountName* 
</dt> <dd>

Nombre de la cuenta de mensajería instantánea de este usuario.

</dd> <dt>

*ConvID* 
</dt> <dd>

IDENTIFICADOR de esta conversación.

</dd> <dt>

*MediaType* 
</dt> <dd>

Un valor de la enumeración de [**\_ \_ características de WPCFLAG im**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_im_feature) que indica información sobre las características a las que se tiene acceso durante una interacción de mensajería instantánea.

</dd> <dt>

*Motivo* 
</dt> <dd>

Un valor de la enumeración [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados y qué controles hay en su lugar.

</dd> <dt>

*RecipCount* 
</dt> <dd>

El recuento de usuarios de mensajería instantánea que reciben la característica y que tienen identidades definidas en el campo de destinatario.

</dd> <dt>

*Recipient* 
</dt> <dd>

Una cadena delimitada que contiene las identidades de la cuenta de mensajería instantánea de todos los usuarios que reciben la característica.

</dd> <dt>

*Sender* 
</dt> <dd>

El nombre de la cuenta de mensajería instantánea para el usuario que ha originado la característica.

</dd> <dt>

*SenderIP* 
</dt> <dd>

Dirección IP del equipo del remitente.

</dd> <dt>

*Data* 
</dt> <dd>

La descripción de los datos de la característica.

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

 

 




