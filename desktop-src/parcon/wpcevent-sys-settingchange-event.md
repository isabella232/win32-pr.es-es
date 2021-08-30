---
description: Evento de nivel de sistema generado en un cambio de configuración de controles parentales.
ms.assetid: 2540c3cc-96d0-4e01-a525-4da4a857cb58
title: WPCEVENT_SYS_SETTINGCHANGE evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7771560de0424b3a03c937e8ad2a08fdb2f23cec77fd02b6c04b29aacf16b434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951144"
---
# <a name="wpcevent_sys_settingchange-event"></a>Evento WPCEVENT \_ SYS \_ SETTINGCHANGE

Evento de nivel de sistema generado en un cambio de configuración de controles parentales.


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYS_SETTINGCHANGE = {0x1, 0x0, 0x10, 0x4, 0x15, 0x1, 0x8000000000000010};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clase* 
</dt> <dd>

Clase que genera el evento.

</dd> <dt>

*Configuración* 
</dt> <dd>

Valor de la **enumeración WPC \_ SETTINGS.**

</dd> <dt>

*Propietario* 
</dt> <dd>

Identificador de seguridad del usuario que genera el evento.

</dd> <dt>

*OldVal* 
</dt> <dd>

Valor anterior de esta configuración, si se elimina o cambia.

</dd> <dt>

*NewVal* 
</dt> <dd>

Nuevo valor de esta configuración, si se agrega o cambia.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valor de la enumeración [**\_ WPCFLAG ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados para su uso y qué controles están en su lugar.

</dd> <dt>

*Opcional* 
</dt> <dd>

Campo opcional.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Header<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de las API de registro para los controles parentales](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




