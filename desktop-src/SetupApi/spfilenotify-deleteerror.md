---
description: La notificación de DELETEERROR de SPFILENOTIFY \_ se envía a la rutina de devolución de llamada si se produce un error durante una operación de eliminación de archivo.
ms.assetid: b98b62f0-0b59-430e-966d-c1447026b696
title: Mensaje de SPFILENOTIFY_DELETEERROR (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035b61120bd1343b43c9b6f6d74246eab33cb430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083390"
---
# <a name="spfilenotify_deleteerror-message"></a>SPFILENOTIFY \_ DELETEERROR

La notificación de **\_ DELETEERROR de SPFILENOTIFY** se envía a la rutina de devolución de llamada si se produce un error durante una operación de eliminación de archivo.


```C++
SPFILENOTIFY_DELETEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .

</dd> <dt>

*Param2* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada debe devolver uno de los valores siguientes.



| Código devuelto                                                                                  | Descripción                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_anulación de FILEOP**</dt> </dl> | Se debe cancelar el procesamiento de la cola. [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) devuelve cero y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve información de ERROR extendida como error \_ cancelado (si el usuario canceló) o error \_ no \_ hay suficiente \_ memoria.<br/> |
| <dl> <dt>**FILEOP \_ reintentar**</dt> </dl> | El usuario está intentando de nuevo la operación de eliminación.<br/>                                                                                                                                                                                                                 |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>  | El usuario está omitiendo la operación de eliminación de archivo.<br/>                                                                                                                                                                                                                    |



 

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

 

