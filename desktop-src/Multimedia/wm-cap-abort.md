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
ms.openlocfilehash: 2843e3c4d59b62f2b58be20cef63ed0dc2e79d4b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371329"
---
# <a name="wm_cap_abort-message"></a>Mensaje \_ DE \_ ANULACIÓN DE WM CAP

El **mensaje ABORT \_ \_ de WM CAP** detiene la operación de captura. En el caso de la captura paso a paso, los datos de imagen recopilados hasta el punto del mensaje **WM \_ CAP \_ ABORT** se conservarán en el archivo de captura, pero no se capturará el audio. Puede enviar este mensaje explícitamente o mediante la [**macro capCaptureAbort.**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort)


```C++
WM_CAP_ABORT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE en **caso** contrario.

## <a name="remarks"></a>Observaciones

La operación de captura debe producir para usar este mensaje.

Use el [**mensaje WM \_ CAP \_ STOP**](wm-cap-stop.md) para detener la captura de pasos en la posición actual y, a continuación, capture el audio.

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

 

 





