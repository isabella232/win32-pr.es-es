---
title: Mensaje de ICM_DRAW_FLUSH (VFW. h)
description: El \_ \_ mensaje de vaciado de dibujo de ICM notifica a un controlador de representación que represente el contenido de los búferes de imagen que están a la espera de ser dibujados. Puede enviar este mensaje explícitamente o mediante la macro ICDrawFlush.
ms.assetid: c29ed751-c773-4476-98fe-6edef3ff0cf4
keywords:
- Mensaje de ICM_DRAW_FLUSH de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676799"
---
# <a name="icm_draw_flush-message"></a>\_Mensaje de vaciado de dibujo de ICM \_

El mensaje de **\_ \_ vaciado de dibujo de ICM** notifica a un controlador de representación que represente el contenido de los búferes de imagen que están a la espera de ser dibujados. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) .


```C++
ICM_DRAW_FLUSH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje solo lo usa el hardware que realiza su propia descompresión asincrónica, temporización y dibujo.

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

 

 





