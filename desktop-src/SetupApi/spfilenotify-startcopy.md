---
description: La notificación de STARTCOPY de SPFILENOTIFY \_ se envía a la función de devolución de llamada cuando la cola inicia una operación de copia de archivos.
ms.assetid: 01a7d9d4-b548-4e72-b1c9-7116e67c023b
title: Mensaje de SPFILENOTIFY_STARTCOPY (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6693938a2f67530e7e3c906c5105d2c98a915a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668173"
---
# <a name="spfilenotify_startcopy-message"></a>SPFILENOTIFY \_ STARTCOPY

La notificación de **\_ STARTCOPY de SPFILENOTIFY** se envía a la función de devolución de llamada cuando la cola inicia una operación de copia de archivos.


```C++
SPFILENOTIFY_STARTCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .

</dd> <dt>

*Param2* 
</dt> <dd>

Siempre tiene el valor FILEOP \_ copiar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada debe devolver uno de los valores siguientes.



| Código devuelto                                                                                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_anulación de FILEOP**</dt> </dl> | Anular el proceso de confirmación de la cola. La rutina de devolución de llamada debe llamar a [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para indicar el motivo de la terminación. La función [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) devuelve **false** y una llamada subsiguiente a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el código de error establecido por la rutina de devolución de llamada durante la llamada a **SetLastError**.<br/> |
| <dl> <dt>**FILEOP \_ Doit**</dt> </dl>  | Realice la operación de copia de archivos.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>  | Omitir la operación de copia actual.<br/>                                                                                                                                                                                                                                                                                                                                                          |



 

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

 

