---
description: La \_ notificación SPFILENOTIFY ENDCOPY se pasa a la función de devolución de llamada cuando la cola completa una operación de copia. Esta notificación se envía incluso si el usuario cancela o si se produce un error.
ms.assetid: d58dc397-8803-466c-9069-728faf2c2030
title: Mensaje de SPFILENOTIFY_ENDCOPY (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75dba56c4a38ac87003a3b59b594135e55a462f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669985"
---
# <a name="spfilenotify_endcopy-message"></a>SPFILENOTIFY \_ ENDCOPY

La notificación **SPFILENOTIFY \_ ENDCOPY** se pasa a la función de devolución de llamada cuando la cola completa una operación de copia. Esta notificación se envía incluso si el usuario cancela o si se produce un error.


```C++
SPFILENOTIFY_ENDCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) . El miembro **Win32Error** de la estructura **FILEPATHS** indica el resultado de la operación de copia.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



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

 

 




