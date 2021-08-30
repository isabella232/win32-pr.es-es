---
title: MCIWNDM_GETINACTIVETIMER mensaje (Vfw.h)
description: El mensaje GETINACTIVETIMER de MCIWNDM recupera el período de actualización utilizado cuando la \_ ventana MCIWnd es la ventana inactiva. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetInactiveTimer.
ms.assetid: 84e00d2f-2cf8-4b6b-a8cb-7eb320754783
keywords:
- MCIWNDM_GETINACTIVETIMER mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ec8de85796139b98e76d631a9386493752dad9942241069a7f1a5ab535fab72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038085"
---
# <a name="mciwndm_getinactivetimer-message"></a>Mensaje GETINACTIVETIMER de MCIWNDM \_

El **mensaje \_ GETINACTIVETIMER de MCIWNDM** recupera el período de actualización utilizado cuando la ventana MCIWnd es la ventana inactiva. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetInactiveTimer.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)


```C++
MCIWNDM_GETINACTIVETIMER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve el período de actualización, en milisegundos. El valor predeterminado es 2000 milisegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
</dt> </dl>

 

 





