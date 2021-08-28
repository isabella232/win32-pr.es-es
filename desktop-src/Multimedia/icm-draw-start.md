---
title: ICM_DRAW_START mensaje (Vfw.h)
description: El ICM DRAW START notifica a un controlador de representación que inicie su reloj interno \_ para el tiempo de dibujar \_ fotogramas. Puede enviar este mensaje explícitamente o mediante la macro ICDrawStart.
ms.assetid: d49e0d97-5a29-46f7-82d7-e3d4b4f7666f
keywords:
- ICM_DRAW_START mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_START
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 720d8c2f919d2b00955892a42ba8fca95b2b426c3cbb396aa4ac71a5cf912307
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690955"
---
# <a name="icm_draw_start-message"></a>\_ICM Draw START message (Draw \_ start)

El **ICM \_ DRAW \_ START** notifica a un controlador de representación que inicie su reloj interno para el tiempo de dibujar fotogramas. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawStart.**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart)


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este mensaje lo usa el hardware que realiza su propia descompresión asincrónica, control de tiempo y dibujo.

Cuando el controlador recibe este mensaje, debería empezar a representar los datos a la velocidad especificada con el [**ICM \_ DRAW \_ BEGIN.**](icm-draw-begin.md)

Los **ICM \_ DRAW \_ START** [**y ICM DRAW \_ \_ STOP**](icm-draw-stop.md) no anidan. Si el controlador recibe **ICM \_ DRAW \_ START** antes de detener la **representación con ICM DRAW \_ \_ STOP**, debe reiniciar la representación con nuevos parámetros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





