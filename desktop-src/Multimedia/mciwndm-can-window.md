---
title: MCIWNDM_CAN_WINDOW mensaje (Vfw.h)
description: El mensaje MCIWNDM CAN WINDOW determina si un dispositivo MCI admite comandos \_ \_ MCI orientados a ventanas. Puede enviar este mensaje explícitamente o mediante la macro MCIWndCanWindow.
ms.assetid: bf89c096-1272-441e-9334-2b4215dbc979
keywords:
- MCIWNDM_CAN_WINDOW mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d638b61093483b6e834b57af1d5c892d77d0f1d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476815"
---
# <a name="mciwndm_can_window-message"></a>Mensaje DE VENTANA \_ DE LA VENTANA DE MCIWNDM \_

El **mensaje MCIWNDM \_ CAN \_ WINDOW** determina si un dispositivo MCI admite comandos MCI orientados a ventanas. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndCanWindow.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow)


```C++
MCIWNDM_CAN_WINDOW 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** el dispositivo admite comandos MCI orientados a ventanas o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow)
</dt> </dl>

 

 





