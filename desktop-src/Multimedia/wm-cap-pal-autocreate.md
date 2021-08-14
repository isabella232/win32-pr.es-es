---
title: WM_CAP_PAL_AUTOCREATE mensaje (Vfw.h)
description: El mensaje WM CAP PAL AUTOCREATE solicita que el controlador de captura muestree fotogramas de vídeo y \_ cree automáticamente una nueva \_ \_ paleta. Puede enviar este mensaje explícitamente o mediante la macro capPaletteAuto.
ms.assetid: b94d245d-adf4-4fe0-b053-87109ef5fd2f
keywords:
- WM_CAP_PAL_AUTOCREATE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_AUTOCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a18d805ef394388de2265845f4e21bebb98d94391b851a60ed38d46e9872fecc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800645"
---
# <a name="wm_cap_pal_autocreate-message"></a>Mensaje \_ WM CAP PAL \_ \_ AUTOCREATE

El **mensaje WM CAP PAL \_ \_ \_ AUTOCREATE** solicita que el controlador de captura muestree fotogramas de vídeo y cree automáticamente una nueva paleta. Puede enviar este mensaje explícitamente o mediante la [**macro capPaletteAuto.**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto)


```C++
WM_CAP_PAL_AUTOCREATE 
wParam = (WPARAM) (iFrames); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*Iframes*
</dt> <dd>

Número de fotogramas para muestrear.

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*
</dt> <dd>

Número de colores de la paleta. El valor máximo de este parámetro es 256.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

Si se produce un error y se establece una función de devolución de llamada de error mediante el mensaje [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR,**](wm-cap-set-callback-error.md) se llama a la función de devolución de llamada de error.

## <a name="remarks"></a>Comentarios

La secuencia de vídeo muestreada debe incluir todos los colores que desee en la paleta. Para obtener la mejor paleta, es posible que tenga que muestrear toda la secuencia en lugar de una parte de ella.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





