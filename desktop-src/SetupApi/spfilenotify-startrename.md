---
description: La notificación SPFILENOTIFY STARTRENAME se envía a la función de devolución de llamada cuando la cola inicia una operación de cambio \_ de nombre de archivo.
ms.assetid: 005c1840-6aa9-4e94-bfe7-6a9d53735fd9
title: SPFILENOTIFY_STARTRENAME mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ec75c84841adf5cb8a187e8d8431f031af74b31f33af7a87e46225b1e9a3464
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739425"
---
# <a name="spfilenotify_startrename-message"></a>Mensaje SPFILENOTIFY \_ STARTRENAME

La **notificación SPFILENOTIFY \_ STARTRENAME** se envía a la función de devolución de llamada cuando la cola inicia una operación de cambio de nombre de archivo.


```C++
SPFILENOTIFY_STARTRENAME
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

Siempre tiene el valor FILEOP \_ RENAME.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada debe devolver uno de los valores siguientes.



| Código devuelto                                                                                  | Descripción                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ ABORT**</dt> </dl> | Anule la confirmación de la cola. La rutina de devolución de llamada debe [**llamar a SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para indicar el motivo de la finalización. [**SetupCommitFileQueue devuelve**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) **FALSE** y una llamada posterior a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el código de error establecido por la rutina de devolución de llamada durante la llamada a **SetLastError**.<br/> |
| <dl> <dt>**FILEOP \_ DOIT**</dt> </dl>  | Realice la operación de copia de archivos.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>  | Omita la operación de copia actual.<br/>                                                                                                                                                                                                                                                                                                                                     |



 

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

 

