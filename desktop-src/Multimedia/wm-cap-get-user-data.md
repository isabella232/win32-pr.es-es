---
title: WM_CAP_GET_USER_DATA mensaje (Vfw.h)
description: El mensaje \_ GET USER DATA de WM CAP recupera un valor de datos LONG \_ \_ \_ \_ PTR asociado a una ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro capGetUserData.
ms.assetid: f7c121ba-44a1-4916-b602-c53d8332c2af
keywords:
- WM_CAP_GET_USER_DATA mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a79a513d415d166ab2715a181a6d8fc366b60480caf2982f6bbc53eadf90d96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892035"
---
# <a name="wm_cap_get_user_data-message"></a>Mensaje \_ GET USER DATA \_ \_ \_ de WM CAP

El **mensaje GET USER DATA \_ \_ \_ \_ de WM CAP** recupera un valor de datos LONG **\_ PTR** asociado a una ventana de captura. Puede enviar este mensaje explícitamente o mediante la [**macro capGetUserData.**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata)


```C++
WM_CAP_GET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve un valor guardado previamente mediante el mensaje [**WM CAP SET USER \_ \_ \_ \_ DATA.**](wm-cap-set-user-data.md)

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

 

 





