---
title: ICM_DECOMPRESS_END mensaje (Vfw.h)
description: El ICM END de DECOMPRESS notifica a un controlador de descompresión de vídeo que finalice la descompresión y los recursos gratuitos asignados para \_ \_ la descompresión. Puede enviar este mensaje explícitamente o mediante la macro ICDecompressEnd.
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- ICM_DECOMPRESS_END mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25155755b6bfbb893905e6facad890dbf98f175
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370501"
---
# <a name="icm_decompress_end-message"></a>\_ICM MENSAJE FINAL DE \_ DECOMPRESS

El **ICM END de \_ DECOMPRESS \_** notifica a un controlador de descompresión de vídeo que finalice la descompresión y los recursos gratuitos asignados para la descompresión. Puede enviar este mensaje explícitamente o mediante la macro [**ICDecompressEnd.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend)


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

El controlador debe liberar todos los recursos asignados para [**el ICM \_ DECOMPRESS \_ BEGIN.**](icm-decompress-begin.md)

[**ICM \_ DECOMPRESS \_ BEGIN y**](icm-decompress-begin.md) ICM END de **\_ DECOMPRESS \_** no anidan. Si el controlador recibe **ICM \_ DECOMPRESS \_ BEGIN** antes de detener la descompresión con ICM **\_ DECOMPRESS \_ END,** debe reiniciar la descompresión con nuevos parámetros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





