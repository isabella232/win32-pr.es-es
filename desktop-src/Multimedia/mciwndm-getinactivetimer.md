---
title: Mensaje de MCIWNDM_GETINACTIVETIMER (VFW. h)
description: El \_ mensaje MCIWNDM GETINACTIVETIMER recupera el período de actualización que se usa cuando la ventana de MCIWnd es la ventana inactiva. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetInactiveTimer.
ms.assetid: 84e00d2f-2cf8-4b6b-a8cb-7eb320754783
keywords:
- Mensaje de MCIWNDM_GETINACTIVETIMER de Windows multimedia
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
ms.openlocfilehash: a270aeffdee59b7749aa87a0e711204960d74d7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676591"
---
# <a name="mciwndm_getinactivetimer-message"></a>MCIWNDM \_ GETINACTIVETIMER

El mensaje **MCIWNDM \_ GETINACTIVETIMER** recupera el período de actualización que se usa cuando la ventana de MCIWnd es la ventana inactiva. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) .


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
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
</dt> </dl>

 

 





