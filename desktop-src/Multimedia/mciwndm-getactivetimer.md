---
title: Mensaje de MCIWNDM_GETACTIVETIMER (VFW. h)
description: El \_ mensaje MCIWNDM GETACTIVETIMER recupera el período de actualización que se usa cuando la ventana de MCIWnd es la ventana activa. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetActiveTimer.
ms.assetid: f9e6f9ed-75fd-4e45-ad92-79a82d8d572c
keywords:
- Mensaje de MCIWNDM_GETACTIVETIMER de Windows multimedia
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
ms.openlocfilehash: 4cb86fc2940c8bd5d82c004754b81e5389ada892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151236"
---
# <a name="mciwndm_getactivetimer-message"></a>MCIWNDM \_ GETACTIVETIMER

El mensaje **MCIWNDM \_ GETACTIVETIMER** recupera el período de actualización que se usa cuando la ventana de MCIWnd es la ventana activa. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) .


```C++
MCIWNDM_GETACTIVETIMER 
wParam = 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve el período de actualización en milisegundos. El valor predeterminado es 500 milisegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)
</dt> </dl>

 

 





