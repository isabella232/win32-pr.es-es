---
title: MCIWNDM_GETINACTIVETIMER mensaje (Vfw.h)
description: El mensaje MCIWNDM GETFRACCIÓNTIMER recupera el período de actualización utilizado cuando la \_ ventana MCIWnd es la ventana inactiva. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetCiónTimer.
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
ms.openlocfilehash: a270aeffdee59b7749aa87a0e711204960d74d7f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370652"
---
# <a name="mciwndm_getinactivetimer-message"></a>Mensaje GETCIÓNTIMER de MCIWNDM \_

El **mensaje MCIWNDM \_ GETFRACCIÓNTIMER** recupera el período de actualización utilizado cuando la ventana MCIWnd es la ventana inactiva. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetCiónTimer.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)


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

[**MCIWndGetCiónTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
</dt> </dl>

 

 





