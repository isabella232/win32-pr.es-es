---
title: ICM_DRAW_STOP_PLAY mensaje (Vfw.h)
description: El ICM \_ DRAW \_ STOP PLAY notifica a un controlador de \_ representación cuando se completa una operación de reproducción. Puede enviar este mensaje explícitamente o mediante la macro ICDrawStopPlay.
ms.assetid: cfe2ee98-80d0-4554-bcbd-9873769da674
keywords:
- ICM_DRAW_STOP_PLAY mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb5ed2d437a3abc0d24972ee739905a72d2333509e7213973bab9459c7c947a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784985"
---
# <a name="icm_draw_stop_play-message"></a>\_ICM Draw STOP PLAY message (DRAW \_ STOP \_ PLAY)

El **ICM DRAW STOP \_ \_ \_ PLAY** notifica a un controlador de representación cuando se completa una operación de reproducción. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawStopPlay.**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay)


```C++
ICM_DRAW_STOP_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

Use este mensaje cuando se complete la operación de reproducción. Use el ICM [**\_ DRAW STOP \_ para**](icm-draw-stop.md) finalizar el tiempo.

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

 

 





