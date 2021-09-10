---
title: WM_CAP_STOP mensaje (Vfw.h)
description: El mensaje \_ WM CAP STOP detiene la operación de \_ captura. Puede enviar este mensaje explícitamente o mediante la macro capCaptureStop.
ms.assetid: 0fea82f5-f381-485a-82ae-b081b3a5e402
keywords:
- WM_CAP_STOP mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ded89ea8999fa2b29f576a6d047f5147d492bc2
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371540"
---
# <a name="wm_cap_stop-message"></a>Mensaje \_ STOP de WM CAP \_

El **mensaje WM CAP \_ \_ STOP** detiene la operación de captura. Puede enviar este mensaje explícitamente o mediante la [**macro capCaptureStop.**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop)

En la captura de fotogramas paso a paso, los datos de imagen recopilados antes de enviar este mensaje se conservan en el archivo de captura. También se conserva una duración equivalente de los datos de audio en el archivo de captura si se ha habilitado la captura de audio.


```C++
WM_CAP_STOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

## <a name="remarks"></a>Observaciones

La operación de captura debe producir para usar este mensaje. Use el [**mensaje ABORT \_ \_ de WM CAP**](wm-cap-abort.md) para abandonar la operación de captura actual.

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

 

 





