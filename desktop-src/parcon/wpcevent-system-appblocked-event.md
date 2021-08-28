---
description: Evento de nivel de sistema generado por las directivas de restricciones de software (SRP) cuando una aplicación está bloqueada por reglas más seguras.
ms.assetid: 6772a2c9-35c1-4b75-94e4-baa84af7c0ed
title: WPCEVENT_SYSTEM_APPBLOCKED evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0444cee0a2844ae868923b5cf51923e0024c9de9a2a12ad51e20d8db9fa3b60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112725"
---
# <a name="wpcevent_system_appblocked-event"></a>Evento WPCEVENT \_ SYSTEM \_ APPBLOCKED

Evento de nivel de sistema generado por las directivas de restricciones de software (SRP) cuando una aplicación está bloqueada por reglas más seguras.


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYSTEM_APPBLOCKED = {0x10, 0x0, 0x10, 0x4, 0x16, 0x10, 0x8000000000000010};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Timestamp* 
</dt> <dd>

Hora a la que se produjo el bloque.

</dd> <dt>

*UserID* 
</dt> <dd>

Identificador de seguridad del usuario que está intentando iniciar la aplicación.

</dd> <dt>

*Ruta de acceso* 
</dt> <dd>

Ruta de acceso a la aplicación que el usuario está intentando iniciar.

</dd> <dt>

*RuleID* 
</dt> <dd>

Identificador de la regla dentro del conjunto de reglas más seguras de los controles parentales que bloquean la ejecución.

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

 

 




