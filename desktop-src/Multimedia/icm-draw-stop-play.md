---
title: Mensaje de ICM_DRAW_STOP_PLAY (VFW. h)
description: El \_ mensaje ICM Draw \_ Stop \_ Play notifica a un controlador de representación cuando se completa una operación de reproducción. Puede enviar este mensaje explícitamente o mediante la macro ICDrawStopPlay.
ms.assetid: cfe2ee98-80d0-4554-bcbd-9873769da674
keywords:
- Mensaje de ICM_DRAW_STOP_PLAY de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151243"
---
# <a name="icm_draw_stop_play-message"></a>\_ \_ Mostrar mensaje de detención de \_ reproducción de ICM

El mensaje **ICM \_ Draw \_ Stop \_ Play** notifica a un controlador de representación cuando se completa una operación de reproducción. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawStopPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) .


```C++
ICM_DRAW_STOP_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use este mensaje cuando se complete la operación de reproducción. Use el [**mensaje \_ \_ detener dibujo de ICM**](icm-draw-stop.md) para finalizar la temporización.

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

 

 





