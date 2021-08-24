---
description: La notificación COPYERROR SPFILENOTIFY se envía a la rutina de devolución de llamada si \_ se produce un error durante una operación de copia de archivos.
ms.assetid: d6096954-c6a5-44d4-a358-c1320c50730a
title: SPFILENOTIFY_COPYERROR mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80160af9d8053a90c1848d397da6bbb9bf41f2793756e1d5491fb0d6f5e39abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665155"
---
# <a name="spfilenotify_copyerror-message"></a>SpFILENOTIFY \_ COPYERROR message

La **notificación \_ COPYERROR SPFILENOTIFY** se envía a la rutina de devolución de llamada si se produce un error durante una operación de copia de archivos.


```C++
SPFILENOTIFY_COPYERROR
  Param1 = (UINT_PTR) FilePathInfo;
  Param2 = (UINT_PTR) ReturnBuffer;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Param1* 
</dt> <dd>

Puntero a una [**estructura FILEPATHS.**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)

</dd> <dt>

*Param2* 
</dt> <dd>

Puntero a un búfer, de tamaño MAX PATH, que almacena la nueva información de ruta \_ de acceso especificada por el usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La devolución de llamada debe devolver uno de los valores siguientes.



| Código devuelto                                                                                    | Descripción                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ ABORT**</dt> </dl>   | Se debe cancelar el procesamiento de la cola. [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) devuelve cero y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve información de error extendida, como ERROR CANCELLED (si el usuario canceló) o \_ ERROR NOT ENOUGH \_ \_ \_ MEMORY.<br/> |
| <dl> <dt>**FILEOP \_ NEWPATH**</dt> </dl> | Vuelva a intentar la operación de copia mediante la ruta de acceso a la función de devolución de llamada colocada en el búfer al que apunta *el parámetro Param2.* La rutina de devolución de llamada debe asegurarse de que la ruta de acceso no desborda el tamaño de búfer de una matriz TCHAR de elementos MAX \_ PATH.<br/>                |
| <dl> <dt>**REINTENTO \_ DE FILEOP**</dt> </dl>   | El usuario está intentando de nuevo la operación de copia.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>    | El usuario omite la operación de copia de archivos.<br/>                                                                                                                                                                                                                      |



 

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

 

