---
title: MCIWNDM_GETACTIVETIMER mensaje (Vfw.h)
description: El mensaje GETACTIVETIMER de MCIWNDM recupera el período de actualización utilizado cuando la \_ ventana MCIWnd es la ventana activa. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetActiveTimer.
ms.assetid: f9e6f9ed-75fd-4e45-ad92-79a82d8d572c
keywords:
- MCIWNDM_GETACTIVETIMER mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc542e5a4b43b974eb7f28bc59d8e2fab7547834f28b5bccb6ea46f978e2158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525525"
---
# <a name="mciwndm_getactivetimer-message"></a>Mensaje GETACTIVETIMER de MCIWNDM \_

El **mensaje \_ GETACTIVETIMER de MCIWNDM** recupera el período de actualización utilizado cuando la ventana MCIWnd es la ventana activa. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetActiveTimer.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)


```C++
MCIWNDM_GETACTIVETIMER 
wParam = 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve el período de actualización en milisegundos. El valor predeterminado es 500 milisegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)
</dt> </dl>

 

 





