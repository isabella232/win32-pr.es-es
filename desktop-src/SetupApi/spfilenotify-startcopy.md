---
description: La notificación SPFILENOTIFY STARTCOPY se envía a la función de devolución de llamada \_ cuando la cola inicia una operación de copia de archivos.
ms.assetid: 01a7d9d4-b548-4e72-b1c9-7116e67c023b
title: SPFILENOTIFY_STARTCOPY mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b73be97df5b0241246131ad8dfec1bb67a76c439d8a40eb034446a33b0a9a95e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664784"
---
# <a name="spfilenotify_startcopy-message"></a>Mensaje DE SPFILENOTIFY \_ STARTCOPY

La **notificación SPFILENOTIFY \_ STARTCOPY** se envía a la función de devolución de llamada cuando la cola inicia una operación de copia de archivos.


```C++
SPFILENOTIFY_STARTCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Param1* 
</dt> <dd>

Puntero a una [**estructura FILEPATHS.**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)

</dd> <dt>

*Param2* 
</dt> <dd>

Siempre tiene el valor FILEOP \_ COPY.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada debe devolver uno de los valores siguientes.



| Código devuelto                                                                                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ ABORT**</dt> </dl> | Anule el proceso de confirmación de cola. La rutina de devolución de llamada debe [**llamar a SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para indicar el motivo de la finalización. La [**función SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) devuelve **FALSE** y una llamada posterior a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el código de error establecido por la rutina de devolución de llamada durante la llamada a **SetLastError**.<br/> |
| <dl> <dt>**FILEOP \_ DOIT**</dt> </dl>  | Realice la operación de copia de archivos.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>  | Omita la operación de copia actual.<br/>                                                                                                                                                                                                                                                                                                                                                          |



 

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

 

