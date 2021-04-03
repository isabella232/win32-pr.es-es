---
description: La notificación de ENDSUBQUEUE de SPFILENOTIFY \_ se envía a la función de devolución de llamada cuando la cola completa todas las operaciones de la subcola de eliminación, cambio de nombre o copia.
ms.assetid: 76bd027a-0f00-46e3-b502-0c97827308a8
title: Mensaje de SPFILENOTIFY_ENDSUBQUEUE (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7eadc7546487b308313b7cb31088a22420e27af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083388"
---
# <a name="spfilenotify_endsubqueue-message"></a>SPFILENOTIFY \_ ENDSUBQUEUE

La notificación de **\_ ENDSUBQUEUE de SPFILENOTIFY** se envía a la función de devolución de llamada cuando la cola completa todas las operaciones de la subcola de eliminación, cambio de nombre o copia.


```C++
SPFILENOTIFY_ENDSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Subcola que se ha completado. Este parámetro puede ser uno de los siguientes valores FILEOP \_ Delete, FILEOP \_ Rename o FILEOP \_ Copy.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



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

 

 




