---
description: La notificación SPFILENOTIFY ENDCOPY se pasa a la función de devolución \_ de llamada cuando la cola completa una operación de copia. Esta notificación se envía incluso si el usuario cancela o si se produce un error.
ms.assetid: d58dc397-8803-466c-9069-728faf2c2030
title: SPFILENOTIFY_ENDCOPY mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87b4a53e1dc88f8cdb7d2ec790cab82b66d8698c6f45abf97e2b5ac5b8511ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665135"
---
# <a name="spfilenotify_endcopy-message"></a>SPFILENOTIFY \_ ENDCOPY message

La **notificación SPFILENOTIFY \_ ENDCOPY** se pasa a la función de devolución de llamada cuando la cola completa una operación de copia. Esta notificación se envía incluso si el usuario cancela o si se produce un error.


```C++
SPFILENOTIFY_ENDCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Param1* 
</dt> <dd>

Puntero a una [**estructura FILEPATHS.**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) El **miembro Win32Error** de la **estructura FILEPATHS** indica el resultado de la operación de copia.

</dd> <dt>

*Param2* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el código de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general](overview.md)
</dt> <dt>

[Notificaciones](notifications.md)
</dt> <dt>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




