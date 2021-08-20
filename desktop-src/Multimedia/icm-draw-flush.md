---
title: ICM_DRAW_FLUSH mensaje (Vfw.h)
description: El ICM DRAW FLUSH notifica a un controlador de representación que represente el contenido de los búferes de imagen que están \_ \_ esperando ser dibujados. Puede enviar este mensaje explícitamente o mediante la macro ICDrawFlush.
ms.assetid: c29ed751-c773-4476-98fe-6edef3ff0cf4
keywords:
- ICM_DRAW_FLUSH mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_FLUSH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7f8fe55b0fc5fd514573ff7d3314dbc82bc2217b08e0bf841b68b53b23fde12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987405"
---
# <a name="icm_draw_flush-message"></a>\_ICM Draw \_ FLUSH message

El **ICM \_ DRAW \_ FLUSH** notifica a un controlador de representación que represente el contenido de los búferes de imagen que están esperando ser dibujados. Puede enviar este mensaje explícitamente o mediante la [**macro ICDrawFlush.**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush)


```C++
ICM_DRAW_FLUSH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Comentarios

Este mensaje solo lo usa el hardware que realiza su propia descompresión asincrónica, control de tiempo y dibujo.

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

 

 





