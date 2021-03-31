---
title: Mensaje de WM_CAP_SINGLE_FRAME (VFW. h)
description: El mensaje de un \_ \_ solo fotograma Cap de WM \_ anexa un solo fotograma a un archivo de captura que se abrió con el \_ mensaje de apertura de trama único de Cap de WM \_ \_ \_ . Puede enviar este mensaje explícitamente o mediante la macro capCaptureSingleFrame.
ms.assetid: 95466961-0719-4ff7-afc8-f7bf0e0974ac
keywords:
- Mensaje de WM_CAP_SINGLE_FRAME de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151092"
---
# <a name="wm_cap_single_frame-message"></a>\_Mensaje de \_ marco único de Cap de WM \_

El mensaje de un **\_ \_ solo \_ fotograma Cap de WM** anexa un solo fotograma a un archivo de captura que se abrió con el mensaje de [**\_ \_ \_ \_ apertura de trama único de Cap de WM**](wm-cap-single-frame-open.md) . Puede enviar este mensaje explícitamente o mediante la macro [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) .


```C++
WM_CAP_SINGLE_FRAME 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

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

 

 





