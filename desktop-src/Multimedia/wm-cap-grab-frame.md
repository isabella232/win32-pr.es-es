---
title: Mensaje de WM_CAP_GRAB_FRAME (VFW. h)
description: El \_ mensaje del \_ \_ marco de captación de Cap de WM recupera y muestra un único fotograma del controlador de captura. Después de la captura, la superposición y la vista previa están deshabilitadas. Puede enviar este mensaje explícitamente o mediante la macro capGrabFrame.
ms.assetid: 91d58c1c-53b9-4813-88c2-7a1acf641d96
keywords:
- Mensaje de WM_CAP_GRAB_FRAME de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ffd91ce767ad86ddac002bb216420b604883d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491146"
---
# <a name="wm_cap_grab_frame-message"></a>\_Mensaje de \_ marco de captura de Cap de WM \_

El mensaje del **\_ \_ \_ marco de captación de Cap de WM** recupera y muestra un único fotograma del controlador de captura. Después de la captura, la superposición y la vista previa están deshabilitadas. Puede enviar este mensaje explícitamente o mediante la macro [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) .


```C++
WM_CAP_GRAB_FRAME 
wParam = (WPARAM)0; 
lParam = (LPARAM)0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Para obtener información sobre la instalación de funciones de devolución de llamada, consulte los mensajes de [**\_ error de devolución de \_ \_ llamada \_ set Cap de WM**](wm-cap-set-callback-error.md) y del marco de [**\_ \_ devolución de \_ llamada \_ de WM**](wm-cap-set-callback-frame.md) .

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

 

 





