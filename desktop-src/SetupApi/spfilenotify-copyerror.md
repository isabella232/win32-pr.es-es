---
description: La notificación de COPYERROR de SPFILENOTIFY \_ se envía a la rutina de devolución de llamada si se produce un error durante una operación de copia de archivos.
ms.assetid: d6096954-c6a5-44d4-a358-c1320c50730a
title: Mensaje de SPFILENOTIFY_COPYERROR (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cd44daabd6a4aed5e61a716bab3df44f35fc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910333"
---
# <a name="spfilenotify_copyerror-message"></a>SPFILENOTIFY \_ COPYERROR

La notificación de **\_ COPYERROR de SPFILENOTIFY** se envía a la rutina de devolución de llamada si se produce un error durante una operación de copia de archivos.


```C++
SPFILENOTIFY_COPYERROR
  Param1 = (UINT_PTR) FilePathInfo;
  Param2 = (UINT_PTR) ReturnBuffer;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .

</dd> <dt>

*Param2* 
</dt> <dd>

Puntero a un búfer, de tamaño máximo de \_ caracteres de ruta de acceso, que almacena la nueva información de ruta de acceso especificada por el usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La devolución de llamada debe devolver uno de los valores siguientes.



| Código devuelto                                                                                    | Descripción                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_anulación de FILEOP**</dt> </dl>   | Se debe cancelar el procesamiento de la cola. [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) devuelve cero y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve información de ERROR extendida como error \_ cancelado (si el usuario canceló) o error \_ no \_ hay suficiente \_ memoria.<br/> |
| <dl> <dt>**FILEOP \_ NEWPATH**</dt> </dl> | Vuelva a intentar la operación de copia mediante la ruta de acceso de la función de devolución de llamada colocada en el búfer al que apunta el parámetro *parám2* . La rutina de devolución de llamada debe asegurarse de que la ruta de acceso no desborda el tamaño de búfer de una matriz TCHAR de \_ elementos de ruta de acceso máxima.<br/>                |
| <dl> <dt>**FILEOP \_ reintentar**</dt> </dl>   | El usuario está intentando volver a realizar la operación de copia.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>    | El usuario está omitiendo la operación de copia de archivos.<br/>                                                                                                                                                                                                                      |



 

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

 

