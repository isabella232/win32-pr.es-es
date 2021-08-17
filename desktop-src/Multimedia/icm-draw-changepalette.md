---
title: ICM_DRAW_CHANGEPALETTE mensaje (Vfw.h)
description: El ICM \_ DRAW \_ CHANGEPALETTE notifica a un controlador de representación que la paleta de películas está cambiando. Puede enviar este mensaje explícitamente o mediante la macro ICDrawChangePalette.
ms.assetid: 974fc0d8-d0c7-4a82-af84-68b53f753259
keywords:
- ICM_DRAW_CHANGEPALETTE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_CHANGEPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e936c7dce397910ef70a80e2efa7f3e031ab8a61b8f59fece158d5c28e9e1270
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987601"
---
# <a name="icm_draw_changepalette-message"></a>\_ICM Draw \_ CHANGEPALETTE message

El **ICM \_ DRAW \_ CHANGEPALETTE notifica** a un controlador de representación que la paleta de películas está cambiando. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawChangePalette.**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette)


```C++
ICM_DRAW_CHANGEPALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Puntero a una [**estructura BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el nuevo formato y la tabla de colores opcional.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

Este mensaje debe ser compatible con los controladores de representación instalables que dibujan DIB con una estructura interna que incluye una paleta.

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

 

