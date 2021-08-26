---
title: ICM_DRAW_STOP mensaje (Vfw.h)
description: El ICM DRAW STOP notifica a un controlador de representación que detenga su reloj interno para el \_ tiempo de dibujo de \_ fotogramas. Puede enviar este mensaje explícitamente o mediante la macro ICDrawStop.
ms.assetid: 9ffda595-e3d6-48f0-9487-69f7e95979c2
keywords:
- ICM_DRAW_STOP mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41bdb8fbc9a0cddf470733fa35b2f25dc62675175cbb40c427d0b160074c5409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038795"
---
# <a name="icm_draw_stop-message"></a>\_ICM Draw \_ STOP message

El **ICM \_ DRAW \_ STOP** notifica a un controlador de representación que detenga su reloj interno para el tiempo de dibujo de fotogramas. Puede enviar este mensaje explícitamente o mediante la [**macro ICDrawStop.**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop)


```C++
ICM_DRAW_STOP 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este mensaje lo usa el hardware que realiza su propia descompresión asincrónica, control de tiempo y dibujo.

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

 

 





