---
title: ICM_DRAW_RENDERBUFFER mensaje (Vfw.h)
description: El ICM DRAW RENDERBUFFER notifica a un controlador de representación que dibuje los fotogramas que \_ se le han \_ pasado. Puede enviar este mensaje explícitamente o mediante la macro ICDrawRenderBuffer.
ms.assetid: b21be12c-b8a5-49ea-b6b3-d2eb0077a8e9
keywords:
- ICM_DRAW_RENDERBUFFER mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_RENDERBUFFER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a5066d5aa129ffad98aa82eb8d09ba91c0e42fca4edae501f8a7c1775d4be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526135"
---
# <a name="icm_draw_renderbuffer-message"></a>\_ICM Mensaje DRAW \_ RENDERBUFFER

El **ICM \_ DRAW \_ RENDERBUFFER** notifica a un controlador de representación que dibuje los fotogramas que se le han pasado. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawRenderBuffer.**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer)


```C++
ICM_DRAW_RENDERBUFFER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

Use este mensaje con hardware que realice su propia descompresión asincrónica, control de tiempo y dibujo.

Este mensaje se usa normalmente para realizar una operación de búsqueda cuando se debe indicar específicamente al controlador que muestre cada fotograma de vídeo pasado a él en lugar de reproducir una secuencia de fotogramas de vídeo.

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

 

 





