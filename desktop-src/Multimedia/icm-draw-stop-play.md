---
title: ICM_DRAW_STOP_PLAY mensaje (Vfw.h)
description: El ICM draw stop play notifica a un controlador \_ de representación cuando se completa una operación de \_ \_ reproducción. Puede enviar este mensaje explícitamente o mediante la macro ICDrawStopPlay.
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
ms.openlocfilehash: ea3964b623c93d452ab7bf9a32c6b9d9b1573fec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246320"
---
# <a name="icm_draw_stop_play-message"></a>\_ICM Mensaje DRAW \_ STOP \_ PLAY

El **ICM DRAW STOP \_ \_ \_ PLAY** notifica a un controlador de representación cuando se completa una operación de reproducción. Puede enviar este mensaje explícitamente o mediante la [**macro ICDrawStopPlay.**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay)


```C++
ICM_DRAW_STOP_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

Use este mensaje cuando se complete la operación de reproducción. Use el ICM [**\_ DRAW \_ STOP**](icm-draw-stop.md) para finalizar el tiempo.

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

 

 





