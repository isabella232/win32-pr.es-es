---
description: La notificación SPFILENOTIFY DELETEERROR se envía a la rutina de devolución de llamada si \_ se produce un error durante una operación de eliminación de archivos.
ms.assetid: b98b62f0-0b59-430e-966d-c1447026b696
title: SPFILENOTIFY_DELETEERROR mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0670f2edc116934442204c36513a3f08744aa3f307c7814de55abe2acc7370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964628"
---
# <a name="spfilenotify_deleteerror-message"></a>SpFILENOTIFY \_ DELETEERROR message

La **notificación SPFILENOTIFY \_ DELETEERROR** se envía a la rutina de devolución de llamada si se produce un error durante una operación de eliminación de archivos.


```C++
SPFILENOTIFY_DELETEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Param1* 
</dt> <dd>

Puntero a una [**estructura FILEPATHS.**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)

</dd> <dt>

*Param2* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada debe devolver uno de los valores siguientes.



| Código devuelto                                                                                  | Descripción                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ ABORT**</dt> </dl> | Se debe cancelar el procesamiento de la cola. [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) devuelve cero y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve información de error extendida, como ERROR CANCELLED (si el usuario canceló) o \_ ERROR NOT ENOUGH \_ \_ \_ MEMORY.<br/> |
| <dl> <dt>**REINTENTO \_ DE FILEOP**</dt> </dl> | El usuario está intentando de nuevo la operación de eliminación.<br/>                                                                                                                                                                                                                 |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>  | El usuario omite la operación de eliminación de archivos.<br/>                                                                                                                                                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

