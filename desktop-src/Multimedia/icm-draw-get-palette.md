---
title: Mensaje de ICM_DRAW_GET_PALETTE (VFW. h)
description: El mensaje de la \_ paleta de obtención de Draw ICM \_ \_ solicita un controlador de representación para devolver una paleta.
ms.assetid: 02a9df7d-e0b9-4bde-9cda-c36d2a10a23c
keywords:
- Mensaje de ICM_DRAW_GET_PALETTE de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03f3658d2a2653f940e18e9b82b7cc3d7690ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078987"
---
# <a name="icm_draw_get_palette-message"></a>Mensaje de la paleta de obtención de \_ Draw ICM \_ \_

El mensaje de la **\_ paleta de \_ obtención \_ de Draw ICM** solicita un controlador de representación para devolver una paleta.


```C++
ICM_DRAW_GET_PALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

El controlador debe devolver uno de los siguientes: un identificador de la paleta que se está usando, **null** si no tiene un identificador para devolver o ICERR no \_ compatible Si no admite paletas.

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

 

 





