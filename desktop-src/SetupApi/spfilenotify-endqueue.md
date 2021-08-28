---
description: La notificación SPFILENOTIFY ENDQUEUE se envía a la rutina de devolución de llamada cuando se han completado todas las operaciones \_ en cola.
ms.assetid: f4540ab6-edea-4f84-b7eb-4ab3f774068b
title: SPFILENOTIFY_ENDQUEUE mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6192ac867b47b3e5cf9d06806bfb6eb42743aee4d97a935035fd7b44ea0e79b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665145"
---
# <a name="spfilenotify_endqueue-message"></a>Mensaje SPFILENOTIFY \_ ENDQUEUE

La **notificación SPFILENOTIFY \_ ENDQUEUE** se envía a la rutina de devolución de llamada cuando se han completado todas las operaciones en cola.


```C++
SPFILENOTIFY_ENDQUEUE
  Param1 = (UINT) Result;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Param1* 
</dt> <dd>

**TRUE** si la cola se procesó correctamente; **en caso contrario, FALSE.**

</dd> <dt>

*Param2* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general](overview.md)
</dt> <dt>

[Notificaciones](notifications.md)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




