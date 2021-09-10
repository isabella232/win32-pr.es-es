---
title: ICM_DRAW_GET_PALETTE mensaje (Vfw.h)
description: El ICM \_ DRAW \_ GET PALETTE solicita a un controlador de \_ representación que devuelva una paleta.
ms.assetid: 02a9df7d-e0b9-4bde-9cda-c36d2a10a23c
keywords:
- ICM_DRAW_GET_PALETTE mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370544"
---
# <a name="icm_draw_get_palette-message"></a>\_ICM Draw \_ GET \_ PALETTE message

El **ICM DRAW GET \_ \_ \_ PALETTE** solicita a un controlador de representación que devuelva una paleta.


```C++
ICM_DRAW_GET_PALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

El controlador debe devolver una de las siguientes opciones: un identificador de la paleta que se usa, **NULL** si no tiene un identificador para devolver o ICERR UNSUPPORTED si no admite \_ paletas.

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

 

 





