---
description: Evento por usuario que admite hasta tres campos.
ms.assetid: e6cf8008-b896-453b-9946-a6b3d94a991a
title: Evento WPCEVENT_CUSTOM (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d20cb2450cd18bb0c77993622d226cfc06dff6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276675"
---
# <a name="wpcevent_custom-event"></a>\_Evento personalizado WPCEVENT

Evento por usuario que admite hasta tres campos.

Los eventos se muestran en el **visor de actividades** de la **otra** sección con la siguiente jerarquía:

1.  Publicador

2.  Application

3.  Evento


```C++
const EVENT_DESCRIPTOR WPCEVENT_CUSTOM = {0xd, 0x0, 0x10, 0x4, 0x17, 0xd, 0x8000000000000030};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Publicador* 
</dt> <dd>

El publicador del evento (por ejemplo, un nombre de empresa).

</dd> <dt>

*AppName* 
</dt> <dd>

El nombre de la aplicación que está generando el evento.

</dd> <dt>

*Versiónaplicación* 
</dt> <dd>

Versión de la aplicación que está generando el evento.

</dd> <dt>

*Evento* 
</dt> <dd>

Nombre del evento.

</dd> <dt>

*Value1* 
</dt> <dd>

Campo personalizado 1.

</dd> <dt>

*Valor2* 
</dt> <dd>

Campo personalizado 2.

</dd> <dt>

*Value3* 
</dt> <dd>

Campo personalizado 3.

</dd> <dt>

*Bloqueado* 
</dt> <dd>

Un valor de la enumeración [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados y qué controles hay en su lugar.

</dd> <dt>

*Motivo* 
</dt> <dd>

Una cadena personalizada que proporciona información adicional sobre el motivo de bloqueo o no bloqueo.

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

 

 




