---
description: La notificación de STARTSUBQUEUE de SPFILENOTIFY \_ se envía a la función de devolución de llamada cuando la cola comienza a procesar las operaciones en la subcola de eliminación, cambio de nombre o copia.
ms.assetid: 4f971549-8f79-4995-9796-1177c3a3c416
title: Mensaje de SPFILENOTIFY_STARTSUBQUEUE (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30e4f20440c12e7fcd1900cd9762a504a26b907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669715"
---
# <a name="spfilenotify_startsubqueue-message"></a>SPFILENOTIFY \_ STARTSUBQUEUE

La notificación de **\_ STARTSUBQUEUE de SPFILENOTIFY** se envía a la función de devolución de llamada cuando la cola comienza a procesar las operaciones en la subcola de eliminación, cambio de nombre o copia.


```C++
SPFILENOTIFY_STARTSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) NumOperations;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Subqueue que se ha iniciado. Este parámetro puede ser cualquiera de los valores FILEOP \_ Delete, FILEOP \_ Rename o FILEOP \_ Copy.

</dd> <dt>

*Param2* 
</dt> <dd>

Número de operaciones de copia, cambio de nombre o eliminación de archivos en la subcola.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se produce un error, la rutina de devolución de llamada debe llamar a [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), especificar el error y, a continuación, devolver cero. La función [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) devolverá **false** y una llamada subsiguiente a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devolverá el código de error establecido por la rutina de devolución de llamada.

Si no se produce ningún error, la rutina de devolución de llamada debe devolver un valor distinto de cero.

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

 

