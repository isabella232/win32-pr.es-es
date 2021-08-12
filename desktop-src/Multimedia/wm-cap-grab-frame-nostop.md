---
title: WM_CAP_GRAB_FRAME_NOSTOP mensaje (Vfw.h)
description: El mensaje WM CAP GRAB FRAME NOSTOP rellena el búfer de fotogramas con un único fotograma sin comprimir del dispositivo de captura \_ \_ y lo \_ \_ muestra.
ms.assetid: 5f6e3ce7-3595-456e-82c8-eeb162ace81a
keywords:
- WM_CAP_GRAB_FRAME_NOSTOP mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME_NOSTOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b81c581ad7e3913640271b32b18791ebf7b48ed09cd365af82ed263449f05471
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622604"
---
# <a name="wm_cap_grab_frame_nostop-message"></a>Mensaje \_ WM CAP GRAB FRAME \_ \_ \_ NOSTOP

El **mensaje WM CAP GRAB FRAME \_ \_ \_ \_ NOSTOP** rellena el búfer de fotogramas con un único fotograma sin comprimir del dispositivo de captura y lo muestra. A diferencia del [**mensaje WM CAP GRAB \_ \_ \_ FRAME,**](wm-cap-grab-frame.md) este mensaje no modifica el estado de superposición o vista previa. Puede enviar este mensaje explícitamente o mediante la [**macro capGrabFrameNoStop.**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop)


```C++
WM_CAP_GRAB_FRAME_NOSTOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE en **caso** contrario.

## <a name="remarks"></a>Observaciones

Para obtener información sobre cómo instalar funciones de devolución de llamada, vea los mensajes [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR**](wm-cap-set-callback-error.md) y [**WM CAP SET \_ \_ \_ CALLBACK \_ FRAME.**](wm-cap-set-callback-frame.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





