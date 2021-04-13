---
title: Mensaje de ICM_DRAW_STOP (VFW. h)
description: El \_ \_ mensaje detener dibujo de ICM notifica a un controlador de representación que detenga su reloj interno durante el tiempo de dibujo de los marcos. Puede enviar este mensaje explícitamente o mediante la macro ICDrawStop.
ms.assetid: 9ffda595-e3d6-48f0-9487-69f7e95979c2
keywords:
- Mensaje de ICM_DRAW_STOP de Windows multimedia
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
ms.openlocfilehash: b3bde99dfcf483e67aa6a601de2718814cc22439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490138"
---
# <a name="icm_draw_stop-message"></a>Mensaje de detención de \_ Draw ICM \_

El **mensaje \_ \_ detener dibujo de ICM** notifica a un controlador de representación que detenga su reloj interno durante el tiempo de dibujo de los marcos. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) .


```C++
ICM_DRAW_STOP 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este mensaje lo usa el hardware que realiza su propia descompresión asincrónica, temporización y dibujo.

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

 

 





