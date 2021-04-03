---
title: Mensaje de WM_CAP_SINGLE_FRAME_OPEN (VFW. h)
description: El \_ \_ \_ \_ mensaje de apertura de marco único de Cap de WM abre el archivo de captura para la captura de un solo fotograma. Se sobrescribe cualquier información anterior del archivo de captura. Puede enviar este mensaje explícitamente o mediante la macro capCaptureSingleFrameOpen.
ms.assetid: 4814737c-4395-4c01-a68e-fac43dd291fd
keywords:
- Mensaje de WM_CAP_SINGLE_FRAME_OPEN de Windows multimedia
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
ms.openlocfilehash: ac38186e4b5a34bbc11563b7e37a1aefc3de18c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905599"
---
# <a name="wm_cap_single_frame_open-message"></a>\_ \_ \_ Mensaje abierto de marco \_ único de Cap de WM

El mensaje de **\_ \_ \_ \_ apertura de marco único de Cap de WM** abre el archivo de captura para la captura de un solo fotograma. Se sobrescribe cualquier información anterior del archivo de captura. Puede enviar este mensaje explícitamente o mediante la macro [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) .


```C++
WM_CAP_SINGLE_FRAME_OPEN 
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

 

 





