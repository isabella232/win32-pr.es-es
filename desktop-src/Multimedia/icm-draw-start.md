---
title: ICM_DRAW_START mensaje (Vfw.h)
description: El ICM DRAW START notifica a un controlador de representación que inicie su reloj interno \_ para el tiempo de dibujo de \_ fotogramas. Puede enviar este mensaje explícitamente o mediante la macro ICDrawStart.
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
ms.openlocfilehash: 538659eb9878be819ee6ec1506403fcce314eb0b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370562"
---
# <a name="icm_draw_start-message"></a>\_ICM Draw \_ START message

El **ICM \_ DRAW \_ START** notifica a un controlador de representación que inicie su reloj interno para el tiempo de dibujo de fotogramas. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawStart.**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart)


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este mensaje lo usa el hardware que realiza su propia descompresión asincrónica, control de tiempo y dibujo.

Cuando el controlador recibe este mensaje, debe empezar a representar los datos a la velocidad especificada con [**el ICM \_ DRAW \_ BEGIN.**](icm-draw-begin.md)

Los **ICM \_ DRAW \_ START** [**y ICM DRAW \_ \_ STOP**](icm-draw-stop.md) no anidan. Si el controlador recibe ICM **\_ DRAW \_ START** antes de detener la representación con **ICM DRAW \_ \_ STOP**, debe reiniciar la representación con nuevos parámetros.

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

 

 





