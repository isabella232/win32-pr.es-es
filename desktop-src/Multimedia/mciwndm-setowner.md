---
title: MCIWNDM_SETOWNER mensaje (Vfw.h)
description: El mensaje SETOWNER de MCIWNDM \_ establece la ventana para recibir mensajes de notificación asociados a la ventana MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSetOwner.
ms.assetid: c2d0f9d5-bf60-4036-a613-65ba1ed83110
keywords:
- MCIWNDM_SETOWNER mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETOWNER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3989632e83a65cda5e805bd91da3f502ca387d6
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370748"
---
# <a name="mciwndm_setowner-message"></a>Mensaje SETOWNER de MCIWNDM \_

El **mensaje \_ SETOWNER de MCIWNDM** establece la ventana para recibir mensajes de notificación asociados a la ventana MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetOwner.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner)


```C++
MCIWNDM_SETOWNER 
wParam = (WPARAM) hwndP; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hwndP"></span><span id="hwndp"></span><span id="HWNDP"></span>*hwndP*
</dt> <dd>

Identificador en la ventana para recibir los mensajes de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner)
</dt> </dl>

 

 





