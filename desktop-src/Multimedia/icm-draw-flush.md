---
title: ICM_DRAW_FLUSH mensaje (Vfw.h)
description: El ICM DRAW FLUSH notifica a un controlador de representación que represente el contenido de los búferes de imagen que están a la espera \_ \_ de ser dibujados. Puede enviar este mensaje explícitamente o mediante la macro ICDrawFlush.
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
ms.openlocfilehash: 38ec42c51222313f7d3599c3b4f264dbd21a9434
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161403"
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

## <a name="remarks"></a>Observaciones

Este mensaje solo lo usa el hardware que realiza su propia descompresión asincrónica, control de tiempo y dibujo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





