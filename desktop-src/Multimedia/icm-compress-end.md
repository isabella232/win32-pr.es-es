---
title: Mensaje de ICM_COMPRESS_END (VFW. h)
description: El mensaje de finalización de compresión ICM \_ \_ notifica a un controlador de compresión de vídeo que finalice la compresión y libere los recursos asignados para la compresión. Puede enviar este mensaje explícitamente o mediante la macro ICCompressEnd.
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- Mensaje de ICM_COMPRESS_END de Windows multimedia
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
ms.openlocfilehash: 320cc99ed4223b7919b85d2b39e15d4d9b76aa90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489899"
---
# <a name="icm_compress_end-message"></a>\_Mensaje final de compresión ICM \_

El mensaje de **\_ \_ finalización** de compresión ICM notifica a un controlador de compresión de vídeo que finalice la compresión y libere los recursos asignados para la compresión. Puede enviar este mensaje explícitamente o mediante la macro [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) .


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

VCM guarda la configuración del mensaje de [**Inicio de \_ compresión \_ ICM**](icm-compress-begin.md) más reciente. **ICM \_ Los \_** **\_ \_ extremos** de la compresión Begin y ICM no se anidan. Si el controlador recibe la compresión de **ICM \_ \_ comienza** antes de que se detenga la compresión con el **\_ \_ fin de comprimir ICM**, debe reiniciar la compresión con nuevos parámetros.

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

 

 





