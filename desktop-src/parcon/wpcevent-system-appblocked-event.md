---
description: Evento de nivel de sistema generado por las directivas de restricción de software (SRP) cuando una aplicación está bloqueada por reglas más seguras.
ms.assetid: 6772a2c9-35c1-4b75-94e4-baa84af7c0ed
title: Evento WPCEVENT_SYSTEM_APPBLOCKED (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67c3f6255911f59717c1fa594aee4bfc49f6c5a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716035"
---
# <a name="wpcevent_system_appblocked-event"></a>\_Evento APPBLOCKED del sistema WPCEVENT \_

Evento de nivel de sistema generado por las directivas de restricción de software (SRP) cuando una aplicación está bloqueada por reglas más seguras.


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYSTEM_APPBLOCKED = {0x10, 0x0, 0x10, 0x4, 0x16, 0x10, 0x8000000000000010};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Indicaciones* 
</dt> <dd>

La hora a la que se produjo el bloque.

</dd> <dt>

*UserID* 
</dt> <dd>

El identificador de seguridad del usuario que está intentando iniciar la aplicación.

</dd> <dt>

*Ruta de acceso* 
</dt> <dd>

La ruta de acceso a la aplicación que el usuario está intentando iniciar.

</dd> <dt>

*RuleID* 
</dt> <dd>

El identificador de la regla dentro del conjunto de reglas más seguras de control parental que bloquea la ejecución.

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

 

 




