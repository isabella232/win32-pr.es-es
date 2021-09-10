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
ms.openlocfilehash: a919036ee38fdcf00f55c3d4044cd3f45bd13c82
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371533"
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

 

 





