---
description: La notificación SPFILENOTIFY RENAMEERROR se envía a la rutina de devolución de llamada si se produce un error durante una operación de cambio \_ de nombre de archivo.
ms.assetid: b7016cbe-2987-477f-958b-52b7a31c54c2
title: SPFILENOTIFY_RENAMEERROR mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500fb05328c50ab953c0a5b9477e00ebb9abdf2856621f014382169b4a4d9042
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964375"
---
# <a name="spfilenotify_renameerror-message"></a>Mensaje SPFILENOTIFY \_ RENAMEERROR

La **notificación SPFILENOTIFY \_ RENAMEERROR** se envía a la rutina de devolución de llamada si se produce un error durante una operación de cambio de nombre de archivo.


```C++
SPFILENOTIFY_RENAMEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Param1* 
</dt> <dd>

Puntero a una [**estructura FILEPATHS.**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) El **miembro Win32Error** de la **estructura FILEPATHS** especifica el error que se produjo durante la operación de cambio de nombre.

</dd> <dt>

*Param2* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada debe devolver una de las siguientes opciones.



| Código devuelto                                                                                  | Descripción                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**REINTENTO \_ DE FILEOP**</dt> </dl> | El usuario eligió intentar de nuevo la operación de cambio de nombre.<br/>                                                                                                                                                                                                  |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>  | El usuario eligió omitir la operación de cambio de nombre de archivo.<br/>                                                                                                                                                                                                      |
| <dl> <dt>**FILEOP \_ ABORT**</dt> </dl> | Detenga la confirmación de la cola. [**SetupCommitFileQueue devuelve**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) **FALSE.** [**GetLastError devuelve**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) información de error extendida, como ERROR CANCELLED (si el usuario \_ canceló) o ERROR \_ NOT ENOUGH \_ \_ MEMORY.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

