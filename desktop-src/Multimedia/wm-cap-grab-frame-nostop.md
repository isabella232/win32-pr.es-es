---
title: Mensaje de WM_CAP_GRAB_FRAME_NOSTOP (VFW. h)
description: El \_ mensaje de \_ \_ \_ punto de interrupción del casquillo de WM rellena el búfer de fotogramas con un solo fotograma sin comprimir del dispositivo de captura y lo muestra.
ms.assetid: 5f6e3ce7-3595-456e-82c8-eeb162ace81a
keywords:
- Mensaje de WM_CAP_GRAB_FRAME_NOSTOP de Windows multimedia
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
ms.openlocfilehash: 5073cf5eae44f564d24cd1ebb67193d8738fd77b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905490"
---
# <a name="wm_cap_grab_frame_nostop-message"></a>\_Mensaje de \_ marco de captación de Cap de \_ WM \_

El mensaje de **\_ punto de \_ \_ \_ interrupción del casquillo de WM** rellena el búfer de fotogramas con un solo fotograma sin comprimir del dispositivo de captura y lo muestra. A diferencia de lo que sucede con el mensaje del [**\_ \_ \_ marco de captación de Cap de WM**](wm-cap-grab-frame.md) , este mensaje no modifica el estado de superposición o vista previa. Puede enviar este mensaje explícitamente o mediante la macro [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) .


```C++
WM_CAP_GRAB_FRAME_NOSTOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
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

 

 





