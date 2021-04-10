---
title: Mensaje de WM_CAP_EDIT_COPY (VFW. h)
description: El \_ \_ mensaje de copia de edición de Cap de WM \_ copia el contenido del búfer de trama de vídeo y la paleta asociada en el portapapeles. Puede enviar este mensaje explícitamente o mediante la macro capEditCopy.
ms.assetid: 16f1dd7d-af4d-4096-add8-eec5f0a0607f
keywords:
- Mensaje de WM_CAP_EDIT_COPY de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_EDIT_COPY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb81c21fc10846adaa113c02b6250bbb35cfff50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150626"
---
# <a name="wm_cap_edit_copy-message"></a>\_Mensaje de \_ copia de edición de Cap de WM \_

El mensaje de copia de edición de Cap de WM copia el contenido del búfer de trama de vídeo y la paleta asociada en el portapapeles. **\_ \_ \_** Puede enviar este mensaje explícitamente o mediante la macro [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) .


```C++
WM_CAP_EDIT_COPY 
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

 

 





