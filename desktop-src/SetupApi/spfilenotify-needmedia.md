---
description: La notificación de NEEDMEDIA de SPFILENOTIFY \_ se envía a la rutina de devolución de llamada cuando se requieren nuevos medios o un nuevo archivo. cab.
ms.assetid: 6a7947de-1bb3-46e0-9334-405684e58e98
title: Mensaje de SPFILENOTIFY_NEEDMEDIA (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b856a95f3c2e200d1d81cfa00c05ef592c1759
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670073"
---
# <a name="spfilenotify_needmedia-message"></a>SPFILENOTIFY \_ NEEDMEDIA

La notificación de **\_ NEEDMEDIA de SPFILENOTIFY** se envía a la rutina de devolución de llamada cuando se requieren nuevos medios o un nuevo archivo. cab.


```C++
SPFILENOTIFY_NEEDMEDIA
  Param1 = (UINT) SourceMediaInfo;
  Param2 = (UINT) NewPathInfo;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Puntero a una estructura de [**\_ medios de origen**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) .

</dd> <dt>

*Param2* 
</dt> <dd>

Puntero a una matriz de caracteres para almacenar la nueva información de la ruta de acceso proporcionada por el usuario. El tamaño del búfer es una matriz **TCHAR** de \_ elementos de ruta de acceso Max. La información de ruta de acceso devuelta por la aplicación de instalación no debe superar este tamaño.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada debe devolver uno de los siguientes.



| Código devuelto                                                                                    | Descripción                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ NEWPATH**</dt> </dl> | El medio está presente y el archivo solicitado está disponible en la ruta de acceso especificada en el búfer señalado por *parám2*.<br/>                                                                                         |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>    | Omitir el archivo solicitado<br/>                                                                                                                                                                                      |
| <dl> <dt>**\_anulación de FILEOP**</dt> </dl>   | Anula el procesamiento de la cola. La función [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) devuelve **false**. GetLastError devuelve información de error extendida, como \_ el error cancelado si el usuario canceló la misma.<br/> |
| <dl> <dt>**FILEOP-DOIT**</dt> </dl>     | El medio está disponible.<br/>                                                                                                                                                                                      |



 

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
</dt> <dt>

[**medios de origen \_**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a)
</dt> </dl>

 

 




