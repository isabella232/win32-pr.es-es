---
title: Mensaje de ICM_DRAW_START (VFW. h)
description: El mensaje de inicio de Draw de ICM \_ \_ notifica a un controlador de representación que inicie su reloj interno durante el tiempo de dibujo de los marcos. Puede enviar este mensaje explícitamente o mediante la macro ICDrawStart.
ms.assetid: d49e0d97-5a29-46f7-82d7-e3d4b4f7666f
keywords:
- Mensaje de ICM_DRAW_START de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422225"
---
# <a name="icm_draw_start-message"></a>Mensaje de inicio de \_ Draw de ICM \_

El mensaje de **\_ \_ Inicio de Draw de ICM** notifica a un controlador de representación que inicie su reloj interno durante el tiempo de dibujo de los marcos. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) .


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este mensaje lo usa el hardware que realiza su propia descompresión asincrónica, temporización y dibujo.

Cuando el controlador recibe este mensaje, debe empezar a representar los datos a la velocidad especificada con el mensaje de [**\_ \_ Inicio de Draw de ICM**](icm-draw-begin.md) .

Los mensajes de [**\_ \_ detención**](icm-draw-stop.md) de **\_ \_ Inicio** y de dibujo de ICM de ICM no se anidan. Si el controlador recibe **el \_ \_ Inicio de Draw de ICM** antes de que se detenga la representación con la **\_ \_ detención de Draw ICM**, debe reiniciar la representación con nuevos parámetros.

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

 

 





