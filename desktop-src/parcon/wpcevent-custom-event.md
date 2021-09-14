---
description: Evento por usuario que admite hasta tres campos.
ms.assetid: e6cf8008-b896-453b-9946-a6b3d94a991a
title: WPCEVENT_CUSTOM evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d20cb2450cd18bb0c77993622d226cfc06dff6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268431"
---
# <a name="wpcevent_custom-event"></a>Evento WPCEVENT \_ CUSTOM

Evento por usuario que admite hasta tres campos.

Los eventos se muestran en el **Visor de actividad** de la sección **Otros** con la siguiente jerarquía:

1.  Publisher

2.  Application

3.  Evento


```C++
const EVENT_DESCRIPTOR WPCEVENT_CUSTOM = {0xd, 0x0, 0x10, 0x4, 0x17, 0xd, 0x8000000000000030};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Publicador* 
</dt> <dd>

Publicador del evento (por ejemplo, un nombre de empresa).

</dd> <dt>

*AppName* 
</dt> <dd>

Nombre de la aplicación que genera el evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Versión de la aplicación que genera el evento.

</dd> <dt>

*Evento* 
</dt> <dd>

Nombre del evento.

</dd> <dt>

*Valor1* 
</dt> <dd>

Campo personalizado 1.

</dd> <dt>

*Valor2* 
</dt> <dd>

Campo personalizado 2.

</dd> <dt>

*Valor3* 
</dt> <dd>

Campo personalizado 3.

</dd> <dt>

*Bloqueado* 
</dt> <dd>

Valor de la enumeración [**\_ WPCFLAG ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados para su uso y qué controles están en su lugar.

</dd> <dt>

*Motivo* 
</dt> <dd>

Cadena personalizada que proporciona información adicional sobre la razón para bloquear o no bloquear.

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

 

 




