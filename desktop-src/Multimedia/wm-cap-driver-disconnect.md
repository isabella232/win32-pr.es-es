---
title: WM_CAP_DRIVER_DISCONNECT mensaje (Vfw.h)
description: El mensaje WM \_ CAP DRIVER DISCONNECT desconecta un controlador de captura de una ventana de \_ \_ captura. Puede enviar este mensaje explícitamente o mediante la macro capDriverDisconnect.
ms.assetid: a420f24a-aa7d-4788-9120-2c11e5e2c14c
keywords:
- WM_CAP_DRIVER_DISCONNECT mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_DISCONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6365366c6ea37b36734262d1d7a8412a7729406ff3fcc12e10ae9ba55d9ba84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803865"
---
# <a name="wm_cap_driver_disconnect-message"></a>Mensaje \_ WM CAP DRIVER \_ \_ DISCONNECT

El **mensaje WM CAP DRIVER \_ \_ \_ DISCONNECT** desconecta un controlador de captura de una ventana de captura. Puede enviar este mensaje explícitamente o mediante la [**macro capDriverDisconnect.**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect)


```C++
WM_CAP_DRIVER_DISCONNECT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza **correctamente o FALSE** si la ventana de captura no está conectada a un controlador de captura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





