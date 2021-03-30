---
title: Mensaje de ICM_DECOMPRESS_END (VFW. h)
description: El mensaje final de descompresión de ICM \_ \_ notifica a un controlador de descompresión de vídeo que finalice la descompresión y libere los recursos asignados para la descompresión. Puede enviar este mensaje explícitamente o mediante la macro ICDecompressEnd.
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- Mensaje de ICM_DECOMPRESS_END de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803379"
---
# <a name="icm_decompress_end-message"></a>Descomprime el \_ \_ mensaje final de ICM

El **mensaje \_ \_ final** de descompresión de ICM notifica a un controlador de descompresión de vídeo que finalice la descompresión y libere los recursos asignados para la descompresión. Puede enviar este mensaje explícitamente o mediante la macro [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) .


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

El controlador debe liberar todos los recursos asignados para el mensaje de [**\_ \_ Inicio de descomprimir ICM**](icm-decompress-begin.md) .

[**ICM \_ La instrucción DESCOMPRIMIr \_ Begin**](icm-decompress-begin.md) y **ICM \_ uncompre \_ End** no se anidan. Si el controlador recibe **el \_ \_ Inicio** de la descompresión ICM antes de que se detenga la descompresión con el **\_ \_ fin de descomprimir ICM**, debe reiniciar la descompresión con nuevos parámetros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





