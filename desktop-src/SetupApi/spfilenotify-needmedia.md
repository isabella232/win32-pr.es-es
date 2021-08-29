---
description: La notificación SPFILENOTIFY NEEDMEDIA se envía a la rutina de devolución de llamada cuando se requieren nuevos medios o \_ un nuevo archivo de archivado.
ms.assetid: 6a7947de-1bb3-46e0-9334-405684e58e98
title: SPFILENOTIFY_NEEDMEDIA mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff4d65ddd4f82e1c401b157b67f39f9cc79e11b1113d502e993abe141b35d8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683115"
---
# <a name="spfilenotify_needmedia-message"></a>SPFILENOTIFY \_ NEEDMEDIA message

La **notificación SPFILENOTIFY \_ NEEDMEDIA** se envía a la rutina de devolución de llamada cuando se requieren nuevos medios o un nuevo archivo de archivado.


```C++
SPFILENOTIFY_NEEDMEDIA
  Param1 = (UINT) SourceMediaInfo;
  Param2 = (UINT) NewPathInfo;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Param1* 
</dt> <dd>

Puntero a una [**estructura SOURCE \_ MEDIA.**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a)

</dd> <dt>

*Param2* 
</dt> <dd>

Puntero a una matriz de caracteres para almacenar la nueva información de ruta de acceso proporcionada por el usuario. El tamaño del búfer es una **matriz TCHAR** de elementos MAX \_ PATH. La información de ruta de acceso devuelta por la aplicación de instalación no debe superar este tamaño.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada debe devolver una de las siguientes opciones.



| Código devuelto                                                                                    | Descripción                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ NEWPATH**</dt> </dl> | El medio está presente y el archivo solicitado está disponible en la ruta de acceso especificada en el búfer al que apunta *Param2*.<br/>                                                                                         |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>    | Omitir el archivo solicitado<br/>                                                                                                                                                                                      |
| <dl> <dt>**FILEOP \_ ABORT**</dt> </dl>   | Anular el procesamiento de la cola. La [**función SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) devuelve **FALSE.** GetLastError devuelve información de error extendida, como ERROR \_ CANCELLED si el usuario canceló.<br/> |
| <dl> <dt>**FILEOP-DOIT**</dt> </dl>     | El medio está disponible.<br/>                                                                                                                                                                                      |



 

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

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[**MEDIOS DE \_ ORIGEN**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a)
</dt> </dl>

 

 




