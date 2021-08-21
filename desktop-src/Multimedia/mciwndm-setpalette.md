---
title: MCIWNDM_SETPALETTE mensaje (Vfw.h)
description: El mensaje MCIWNDM SETPALETTE envía un identificador de paleta al dispositivo MCI asociado \_ a la ventana MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSetPalette.
ms.assetid: d2399cb7-d83c-465c-b02f-e6a016c28ae3
keywords:
- MCIWNDM_SETPALETTE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b4986224fd23898ef33f8fdda4c12d17880a8bc42441b29cd1865fb7fdfa687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525235"
---
# <a name="mciwndm_setpalette-message"></a>Mensaje SETPALETTE de MCIWNDM \_

El **mensaje MCIWNDM \_ SETPALETTE** envía un identificador de paleta al dispositivo MCI asociado a la ventana MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetPalette.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)


```C++
MCIWNDM_SETPALETTE 
wParam = (WPARAM) (HPALETTE) hpal; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hpal"></span><span id="HPAL"></span>*hpal*
</dt> <dd>

Controlador de paleta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)
</dt> </dl>

 

 





