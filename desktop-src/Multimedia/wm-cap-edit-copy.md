---
title: WM_CAP_EDIT_COPY mensaje (Vfw.h)
description: El mensaje EDIT COPY de WM CAP copia el contenido del búfer de fotogramas de \_ vídeo y la paleta asociada en el \_ \_ Portapapeles. Puede enviar este mensaje explícitamente o mediante la macro capEditCopy.
ms.assetid: 16f1dd7d-af4d-4096-add8-eec5f0a0607f
keywords:
- WM_CAP_EDIT_COPY mensaje Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473848"
---
# <a name="wm_cap_edit_copy-message"></a>Mensaje \_ EDIT \_ COPY \_ de WM CAP

El **mensaje EDIT COPY \_ \_ \_ de WM CAP** copia el contenido del búfer de fotogramas de vídeo y la paleta asociada en el Portapapeles. Puede enviar este mensaje explícitamente o mediante la [**macro capEditCopy.**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy)


```C++
WM_CAP_EDIT_COPY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

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

 

 





