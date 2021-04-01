---
title: Mensaje de MCIWNDM_REALIZE (VFW. h)
description: El mensaje de MCIWNDM de la \_ MCIWnd de la ventana de la ventana de una ventana de. Esta macro se define con el mensaje de MCIWNDM \_ . Puede enviar este mensaje explícitamente o mediante la macro MCIWndRealize.
ms.assetid: fe8803b5-3500-44b4-97f7-784bedf0b362
keywords:
- Mensaje de MCIWNDM_REALIZE de Windows multimedia
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
ms.openlocfilehash: 9ef3a803791a4f8dfe94d128d42ea06a7b28e739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995997"
---
# <a name="mciwndm_realize-message"></a>Mensaje de MCIWNDM \_

El **mensaje \_ de MCIWNDM** de la MCIWnd de la ventana de la ventana de una ventana de. Esta macro se define con el **mensaje \_ de MCIWNDM** . Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) .


```C++
MCIWNDM_REALIZE 
wParam = (WPARAM) (BOOL) fBkgnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*
</dt> <dd>

Marca de fondo. Especifique **true** para este parámetro si la ventana es una aplicación en segundo plano.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

**MCIWNDM \_ En el uso se** usa la paleta del dispositivo MCI y se llama a la función [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) . Si la aplicación controla explícitamente los mensajes de [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) y [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) , debe usar este mensaje en la aplicación en lugar de usar **RealizePalette**. Si el cuerpo de uno de estos controladores de mensajes contiene solo **RealizePalette**, reenvíe el mensaje a la ventana de MCIWnd, que obtendrá automáticamente la paleta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**PALETTECHANGED de WM \_**](/windows/desktop/gdi/wm-palettechanged)
</dt> <dt>

[**QUERYNEWPALETTE de WM \_**](/windows/desktop/gdi/wm-querynewpalette)
</dt> </dl>

 

