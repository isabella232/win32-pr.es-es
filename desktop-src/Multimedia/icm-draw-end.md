---
title: ICM_DRAW_END mensaje (Vfw.h)
description: El ICM DRAW END notifica a un controlador de representación que descomprima la imagen actual en la pantalla y que libere los recursos asignados para \_ \_ la descompresión y el dibujo. Puede enviar este mensaje explícitamente o mediante la macro ICDrawEnd.
ms.assetid: 03910752-6122-4a5a-84ff-2cecf66cf439
keywords:
- ICM_DRAW_END mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e420ac37791bc6c5aa7f660d71005be65fc87fff
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370520"
---
# <a name="icm_draw_end-message"></a>\_ICM DRAW \_ END message

El **ICM \_ DRAW \_ END** notifica a un controlador de representación que descomprima la imagen actual en la pantalla y que libere los recursos asignados para la descompresión y el dibujo. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawEnd.**](/windows/desktop/api/Vfw/nf-vfw-icdrawend)


```C++
ICM_DRAW_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Los [**ICM \_ DRAW \_ BEGIN**](icm-draw-begin.md) **y ICM \_ DRAW \_ END** no anidan. Si el controlador recibe **ICM \_ DRAW \_ BEGIN** antes de detener la descompresión **con ICM DRAW \_ \_ END**, debe reiniciar la descompresión con nuevos parámetros.

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

 

 





