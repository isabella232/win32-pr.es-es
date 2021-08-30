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
ms.openlocfilehash: 26db92a07437f10295c2670e035950be5a56813aa6bb4c6252cfe35ef502f77c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038155"
---
# <a name="mciwndm_can_window-message"></a>Mensaje CAN WINDOW de MCIWNDM \_ \_

El **mensaje MCIWNDM \_ CAN \_ WINDOW** determina si un dispositivo MCI admite comandos MCI orientados a ventanas. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndCanWindow.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow)


```C++
MCIWNDM_CAN_WINDOW 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si el dispositivo admite comandos MCI orientados a ventanas o **FALSE** en caso contrario.

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

 

 





