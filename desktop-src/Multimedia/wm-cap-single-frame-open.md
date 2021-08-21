---
title: WM_CAP_SINGLE_FRAME_OPEN mensaje (Vfw.h)
description: El mensaje \_ WM CAP SINGLE FRAME OPEN abre el archivo de captura para la captura de fotograma \_ \_ \_ único. Cualquier información anterior del archivo de captura se sobrescribe. Puede enviar este mensaje explícitamente o mediante la macro capCaptureSingleFrameOpen.
ms.assetid: 4814737c-4395-4c01-a68e-fac43dd291fd
keywords:
- WM_CAP_SINGLE_FRAME_OPEN mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a58df70bea8971e10a769efbbc98220c46897ff6979e66ab45ae8f2ba81b971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134840"
---
# <a name="wm_cap_single_frame_open-message"></a>Mensaje \_ WM CAP SINGLE FRAME \_ \_ \_ OPEN

El **mensaje WM CAP SINGLE FRAME \_ \_ \_ \_ OPEN** abre el archivo de captura para la captura de fotograma único. Cualquier información anterior del archivo de captura se sobrescribe. Puede enviar este mensaje explícitamente o mediante la macro [**capCaptureSingleFrameOpen.**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen)


```C++
WM_CAP_SINGLE_FRAME_OPEN 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE en **caso** contrario.

## <a name="remarks"></a>Comentarios

Para obtener información sobre cómo instalar funciones de devolución de llamada, vea los mensajes [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR**](wm-cap-set-callback-error.md) y [**WM CAP SET \_ \_ \_ CALLBACK \_ FRAME.**](wm-cap-set-callback-frame.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





