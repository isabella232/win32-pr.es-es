---
title: Mensaje de ICM_DECOMPRESSEX_END (VFW. h)
description: El \_ mensaje de \_ finalización DECOMPRESSEX de ICM notifica a un controlador de descompresión de vídeo que finalice la descompresión y libere los recursos asignados para la descompresión. Puede enviar este mensaje explícitamente o mediante la macro ICDecompressExEnd.
ms.assetid: 7ed63a4e-bb17-43a3-b593-25c4a51be942
keywords:
- Mensaje de ICM_DECOMPRESSEX_END de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e96f6a069e9ed2c9c52dc2f07f1ab4c5210ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535026"
---
# <a name="icm_decompressex_end-message"></a>\_Mensaje final de DECOMPRESSEX ICM \_

El mensaje de **\_ \_ finalización DECOMPRESSEX de ICM** notifica a un controlador de descompresión de vídeo que finalice la descompresión y libere los recursos asignados para la descompresión. Puede enviar este mensaje explícitamente o mediante la macro [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) .


```C++
ICM_DECOMPRESSEX_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

El controlador libera todos los recursos asignados para el mensaje de [**\_ \_ Inicio DECOMPRESSEX de ICM**](icm-decompressex-begin.md) .

[**ICM \_ DECOMPRESSEX \_ Begin**](icm-decompressex-begin.md) y **ICM \_ DECOMPRESSEX \_ End** no se anidan. Si el controlador recibe **el \_ \_ Inicio de DECOMPRESSEX ICM** antes de que se detenga la descompresión con **ICM \_ DECOMPRESSEX \_ End**, debe reiniciar la descompresión con nuevos parámetros.

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

 

 





