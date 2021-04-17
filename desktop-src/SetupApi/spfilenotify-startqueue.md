---
description: La notificación de STARTQUEUE de SPFILENOTIFY \_ se envía a la rutina de devolución de llamada cuando se inicia el proceso de compromiso de cola.
ms.assetid: 682c2ce0-0c82-402c-a487-db5f2c377f3f
title: Mensaje de SPFILENOTIFY_STARTQUEUE (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090e3f97dceb1843d75934dd99cca500e6f93086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668172"
---
# <a name="spfilenotify_startqueue-message"></a>SPFILENOTIFY \_ STARTQUEUE

La notificación de **\_ STARTQUEUE de SPFILENOTIFY** se envía a la rutina de devolución de llamada cuando se inicia el proceso de compromiso de cola.


```C++
SPFILENOTIFY_STARTQUEUE
  Param1 = (UINT) OwnerWindow;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Identificador de la ventana que va a ser propietaria de los cuadros de diálogo generados por la rutina de devolución de llamada.

</dd> <dt>

*Param2* 
</dt> <dd>

Sin usar.

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

 

