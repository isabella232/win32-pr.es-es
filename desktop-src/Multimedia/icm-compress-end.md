---
title: ICM_COMPRESS_END mensaje (Vfw.h)
description: El ICM COMPRESS END notifica a un controlador de compresión de vídeo que finalice la compresión y los recursos gratuitos \_ \_ asignados para la compresión. Puede enviar este mensaje explícitamente o mediante la macro ICCompressEnd.
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- ICM_COMPRESS_END mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c320190da37d286db1c20329a849ea09ac6d915087e9d3bdbb2333d31cec3e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785045"
---
# <a name="icm_compress_end-message"></a>\_ICM Mensaje COMPRESS \_ END

El **ICM \_ COMPRESS \_ END** notifica a un controlador de compresión de vídeo que finalice la compresión y los recursos gratuitos asignados para la compresión. Puede enviar este mensaje explícitamente o mediante la macro [**ICCompressEnd.**](/windows/desktop/api/Vfw/nf-vfw-iccompressend)


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Comentarios

VCM guarda la configuración del mensaje más reciente [**ICM \_ COMPRESS \_ BEGIN.**](icm-compress-begin.md) **ICM \_ COMPRESS \_ BEGIN** y **ICM COMPRESS \_ \_ END** no anidan. Si el controlador recibe ICM **\_ COMPRESS \_ BEGIN** antes de detener la compresión **con ICM COMPRESS \_ \_ END**, debe reiniciar la compresión con nuevos parámetros.

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

 

 





