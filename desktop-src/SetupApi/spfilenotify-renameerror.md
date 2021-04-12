---
description: La notificación de RENAMEERROR de SPFILENOTIFY \_ se envía a la rutina de devolución de llamada si se produce un error durante una operación de cambio de nombre de archivo.
ms.assetid: b7016cbe-2987-477f-958b-52b7a31c54c2
title: Mensaje de SPFILENOTIFY_RENAMEERROR (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a45658153980d7cfd5cb99b76fb344fcdb4bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361048"
---
# <a name="spfilenotify_renameerror-message"></a>SPFILENOTIFY \_ RENAMEERROR

La notificación de **\_ RENAMEERROR de SPFILENOTIFY** se envía a la rutina de devolución de llamada si se produce un error durante una operación de cambio de nombre de archivo.


```C++
SPFILENOTIFY_RENAMEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) . El miembro **Win32Error** de la estructura **FILEPATHS** especifica el error que se produjo durante la operación de cambio de nombre.

</dd> <dt>

*Param2* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada debe devolver uno de los siguientes.



| Código devuelto                                                                                  | Descripción                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ reintentar**</dt> </dl> | El usuario decidió volver a intentar la operación de cambio de nombre.<br/>                                                                                                                                                                                                  |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>  | El usuario decidió omitir la operación de cambio de nombre de archivo.<br/>                                                                                                                                                                                                      |
| <dl> <dt>**\_anulación de FILEOP**</dt> </dl> | Detenga la confirmación de la cola. [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) devuelve **false**. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve información de error extendida, como error \_ cancelado (si el usuario canceló) o error \_ no \_ hay suficiente \_ memoria.<br/> |



 

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

 

