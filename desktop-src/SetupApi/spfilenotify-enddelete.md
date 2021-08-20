---
description: La notificación SPFILENOTIFY ENDDELETE se devuelve a la rutina de devolución de llamada \_ cuando una cola completa una operación de eliminación. Esta notificación se envía incluso si el usuario cancela o si se produce un error.
ms.assetid: 78859854-8411-4c51-9c3c-628315cf1c41
title: SPFILENOTIFY_ENDDELETE mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 638bf333c034ececd5a22536805b2adab970df9f15e70d9f4a9f161229937aa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964608"
---
# <a name="spfilenotify_enddelete-message"></a>Mensaje SPFILENOTIFY \_ ENDDELETE

La **notificación SPFILENOTIFY \_ ENDDELETE** se devuelve a la rutina de devolución de llamada cuando una cola completa una operación de eliminación. Esta notificación se envía incluso si el usuario cancela o si se produce un error.


```C++
SPFILENOTIFY_ENDDELETE
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Param1* 
</dt> <dd>

Puntero a una [**estructura FILEPATHS.**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) El **miembro Win32Error** de la **estructura FILEPATHS** indica el resultado de una operación de copia.

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
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
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

 

 




