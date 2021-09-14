---
title: WM_CAP_SINGLE_FRAME_CLOSE mensaje (Vfw.h)
description: El mensaje WM \_ CAP SINGLE FRAME CLOSE cierra el archivo de captura abierto por el mensaje WM CAP \_ SINGLE FRAME \_ \_ \_ \_ \_ \_ OPEN. Puede enviar este mensaje explícitamente o mediante la macro capCaptureSingleFrameClose.
ms.assetid: fde5f34b-0781-49a2-a509-64192a1d9ec0
keywords:
- WM_CAP_SINGLE_FRAME_CLOSE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_CLOSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e35523476dde1c74c4a20447d7c46d5eafc5e529
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171509"
---
# <a name="wm_cap_single_frame_close-message"></a>Mensaje \_ WM CAP SINGLE FRAME \_ \_ \_ CLOSE

El **mensaje WM CAP SINGLE FRAME \_ \_ \_ \_ CLOSE** cierra el archivo de captura abierto por el [**mensaje WM CAP SINGLE FRAME \_ \_ \_ \_ OPEN.**](wm-cap-single-frame-open.md) Puede enviar este mensaje explícitamente o mediante la macro [**capCaptureSingleFrameClose.**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose)


```C++
WM_CAP_SINGLE_FRAME_CLOSE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

## <a name="remarks"></a>Observaciones

Para obtener información sobre cómo instalar funciones de devolución de llamada, vea los mensajes [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR**](wm-cap-set-callback-error.md) y [**WM CAP SET \_ \_ \_ CALLBACK \_ FRAME.**](wm-cap-set-callback-frame.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





