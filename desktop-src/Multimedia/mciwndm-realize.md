---
title: MCIWNDM_REALIZE mensaje (Vfw.h)
description: El mensaje MCIWNDM REALIZE se da cuenta de la paleta que usa actualmente el \_ dispositivo MCI en una ventana de MCIWnd. Esta macro se define con el mensaje MCIWNDM \_ REALIZE. Puede enviar este mensaje explícitamente o mediante la macro MCIWndRealize.
ms.assetid: fe8803b5-3500-44b4-97f7-784bedf0b362
keywords:
- MCIWNDM_REALIZE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3fdbee3757e1fd3aada5292b86cc37577ccb718315c5b81140ceb14278c37c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012623"
---
# <a name="mciwndm_realize-message"></a>Mensaje DE MCIWNDM \_ REALIZE

El **mensaje MCIWNDM \_ REALIZE** se da cuenta de la paleta que usa actualmente el dispositivo MCI en una ventana de MCIWnd. Esta macro se define con el **mensaje MCIWNDM \_ REALIZE.** Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndRealize.**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)


```C++
MCIWNDM_REALIZE 
wParam = (WPARAM) (BOOL) fBkgnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBnd*
</dt> <dd>

Marca de fondo. Especifique **TRUE** para este parámetro si la ventana es una aplicación en segundo plano.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Comentarios

**MCIWNDM \_ REALIZE** usa la paleta del dispositivo MCI y llama a la [**función RealizePalette.**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) Si la aplicación controla explícitamente los mensajes [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) y [**WM \_ QUERYNEWPALETTE,**](/windows/desktop/gdi/wm-querynewpalette) debe usar este mensaje en la aplicación en lugar de **usar RealizePalette**. Si el cuerpo de uno de estos controladores de mensajes solo contiene **RealizePalette,** reenvía el mensaje a la ventana MCIWnd, que se dará cuenta automáticamente de la paleta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**PALETA \_ WMCHANGED**](/windows/desktop/gdi/wm-palettechanged)
</dt> <dt>

[**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette)
</dt> </dl>

 

