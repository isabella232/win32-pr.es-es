---
title: Mensaje de WM_CAP_ABORT (VFW. h)
description: El \_ mensaje de anulación de Cap de WM \_ detiene la operación de captura.
ms.assetid: a0479d73-8422-4833-9e8a-c262ec386f58
keywords:
- Mensaje de WM_CAP_ABORT de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534108"
---
# <a name="wm_cap_abort-message"></a>\_Mensaje de anulación de Cap de WM \_

El mensaje de **\_ \_ anulación de Cap de WM** detiene la operación de captura. En el caso de la captura de pasos, los datos de la imagen recopilados hasta el momento del mensaje de **\_ \_ anulación del Cap de WM** se conservarán en el archivo de captura, pero el audio no se capturará. Puede enviar este mensaje explícitamente o mediante la macro [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) .


```C++
WM_CAP_ABORT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

La operación de captura debe proporcionar el uso de este mensaje.

Use el mensaje de [**\_ \_ detención de Cap de WM**](wm-cap-stop.md) para detener la captura de paso en la posición actual y, a continuación, capturar audio.

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

 

 





