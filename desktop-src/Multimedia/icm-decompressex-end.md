---
title: ICM_DECOMPRESSEX_END mensaje (Vfw.h)
description: El ICM end de DECOMPRESSEX notifica a un controlador de descompresión de vídeo que finalice la descompresión y los recursos gratuitos asignados para \_ \_ la descompresión. Puede enviar este mensaje explícitamente o mediante la macro ICDecompressExEnd.
ms.assetid: 7ed63a4e-bb17-43a3-b593-25c4a51be942
keywords:
- ICM_DECOMPRESSEX_END mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370514"
---
# <a name="icm_decompressex_end-message"></a>\_ICM Mensaje FINAL \_ DECOMPRESSEX

El **ICM end de \_ DECOMPRESSEX \_** notifica a un controlador de descompresión de vídeo que finalice la descompresión y los recursos gratuitos asignados para la descompresión. Puede enviar este mensaje explícitamente o mediante la macro [**ICDecompressExEnd.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend)


```C++
ICM_DECOMPRESSEX_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

El controlador libera los recursos asignados para el [**ICM \_ DECOMPRESSEX \_ BEGIN.**](icm-decompressex-begin.md)

[**ICM \_ DECOMPRESSEX \_ BEGIN y**](icm-decompressex-begin.md) ICM END de **\_ DECOMPRESSEX \_** no anidan. Si el controlador recibe **ICM \_ DECOMPRESSEX \_ BEGIN** antes de detener la descompresión con ICM **\_ DECOMPRESSEX \_ END**, debe reiniciar la descompresión con nuevos parámetros.

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

 

 





