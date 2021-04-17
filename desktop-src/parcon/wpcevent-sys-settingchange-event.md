---
description: Evento de nivel de sistema generado en un cambio de configuración de controles parentales.
ms.assetid: 2540c3cc-96d0-4e01-a525-4da4a857cb58
title: Evento WPCEVENT_SYS_SETTINGCHANGE (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea0efb4d68fabcb5f9216c4ccf3bb923ee0ff54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716947"
---
# <a name="wpcevent_sys_settingchange-event"></a>WPCEVENT \_ Sys \_ SETTINGCHANGE

Evento de nivel de sistema generado en un cambio de configuración de controles parentales.


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYS_SETTINGCHANGE = {0x1, 0x0, 0x10, 0x4, 0x15, 0x1, 0x8000000000000010};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clase* 
</dt> <dd>

La clase que está generando el evento.

</dd> <dt>

*Configuración* 
</dt> <dd>

Un valor de la enumeración de **\_ configuración WPC** .

</dd> <dt>

*Propietario* 
</dt> <dd>

El identificador de seguridad del usuario que está generando el evento.

</dd> <dt>

*OldVal* 
</dt> <dd>

Valor anterior de esta configuración, si se elimina o se cambia.

</dd> <dt>

*NewVal* 
</dt> <dd>

Nuevo valor de esta configuración, si se ha agregado o cambiado.

</dd> <dt>

*Motivo* 
</dt> <dd>

Un valor de la enumeración [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados y qué controles hay en su lugar.

</dd> <dt>

*Opcional* 
</dt> <dd>

Un campo opcional.

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

 

 




