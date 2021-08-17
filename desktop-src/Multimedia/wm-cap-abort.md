---
title: WM_CAP_ABORT mensaje (Vfw.h)
description: El mensaje ABORT de WM \_ CAP detiene la operación de \_ captura.
ms.assetid: a0479d73-8422-4833-9e8a-c262ec386f58
keywords:
- WM_CAP_ABORT mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_ABORT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904edb47c371ee13ed3492fd9257e3933bf2f001010d7dd2b0177a7729500813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800665"
---
# <a name="wm_cap_abort-message"></a>Mensaje \_ DE \_ ANULACIÓN DE WM CAP

El **mensaje ABORT \_ \_ de WM CAP** detiene la operación de captura. En el caso de la captura de pasos, los datos de imagen recopilados hasta el punto del mensaje **WM \_ CAP \_ ABORT** se conservarán en el archivo de captura, pero no se capturará el audio. Puede enviar este mensaje explícitamente o mediante la [**macro capCaptureAbort.**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort)


```C++
WM_CAP_ABORT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

## <a name="remarks"></a>Comentarios

La operación de captura debe producir para usar este mensaje.

Use el [**mensaje WM \_ CAP \_ STOP**](wm-cap-stop.md) para detener la captura de pasos en la posición actual y, a continuación, capturar audio.

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

 

 





