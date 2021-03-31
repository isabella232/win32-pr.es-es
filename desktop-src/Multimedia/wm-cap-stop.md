---
title: Mensaje de WM_CAP_STOP (VFW. h)
description: El mensaje de detención del Cap de WM \_ \_ detiene la operación de captura. Puede enviar este mensaje explícitamente o mediante la macro capCaptureStop.
ms.assetid: 0fea82f5-f381-485a-82ae-b081b3a5e402
keywords:
- Mensaje de WM_CAP_STOP de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803805"
---
# <a name="wm_cap_stop-message"></a>Mensaje de detención de \_ Cap de WM \_

El mensaje de **\_ \_ detención del Cap de WM** detiene la operación de captura. Puede enviar este mensaje explícitamente o mediante la macro [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) .

En la captura de fotogramas del paso, los datos de la imagen que se recopilaron antes de que se enviara este mensaje se conservan en el archivo de captura. También se conserva una duración equivalente de los datos de audio en el archivo de captura si se ha habilitado la captura de audio.


```C++
WM_CAP_STOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

La operación de captura debe proporcionar el uso de este mensaje. Use el mensaje de [**\_ \_ anulación de Cap de WM**](wm-cap-abort.md) para abandonar la operación de captura actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





