---
title: Mensaje de ICM_DRAW_RENDERBUFFER (VFW. h)
description: El mensaje RENDERBUFFER de ICM de \_ Draw \_ notifica a un controlador de representación que dibuje los fotogramas que se le han pasado. Puede enviar este mensaje explícitamente o mediante la macro ICDrawRenderBuffer.
ms.assetid: b21be12c-b8a5-49ea-b6b3-d2eb0077a8e9
keywords:
- Mensaje de ICM_DRAW_RENDERBUFFER de Windows multimedia
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
ms.openlocfilehash: ccb02a1fbe334547b9679970ac7598df23237f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996859"
---
# <a name="icm_draw_renderbuffer-message"></a>\_Mensaje RENDERBUFFER de Draw ICM \_

El **mensaje \_ \_ RENDERBUFFER de ICM de Draw** notifica a un controlador de representación que dibuje los fotogramas que se le han pasado. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) .


```C++
ICM_DRAW_RENDERBUFFER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use este mensaje con hardware que realice su propia descompresión asincrónica, temporización y dibujo.

Este mensaje se usa normalmente para realizar una operación de búsqueda cuando el controlador se debe indicar específicamente para mostrar cada fotograma de vídeo que se le ha pasado en lugar de reproducir una secuencia de fotogramas de vídeo.

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

 

 





