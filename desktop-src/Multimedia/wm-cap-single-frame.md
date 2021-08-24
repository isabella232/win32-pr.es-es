---
title: WM_CAP_SINGLE_FRAME mensaje (Vfw.h)
description: El mensaje WM CAP SINGLE FRAME anexa un único marco a un archivo de captura que se abrió con el mensaje \_ WM CAP SINGLE FRAME \_ \_ \_ \_ \_ \_ OPEN. Puede enviar este mensaje explícitamente o mediante la macro capCaptureSingleFrame.
ms.assetid: 95466961-0719-4ff7-afc8-f7bf0e0974ac
keywords:
- WM_CAP_SINGLE_FRAME mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2080c8471849d42c2260c1f4133c996ef31e65e8a20591df531fbd24c19bc85c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891795"
---
# <a name="wm_cap_single_frame-message"></a>Mensaje \_ WM CAP SINGLE \_ \_ FRAME

El **mensaje WM CAP SINGLE \_ \_ \_ FRAME** anexa un único marco a un archivo de captura que se abrió con el mensaje [**WM CAP SINGLE FRAME \_ \_ \_ \_ OPEN.**](wm-cap-single-frame-open.md) Puede enviar este mensaje explícitamente o mediante la macro [**capCaptureSingleFrame.**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe)


```C++
WM_CAP_SINGLE_FRAME 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE en **caso** contrario.

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

 

 





