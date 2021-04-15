---
title: Mensaje de MCIWNDM_SETINACTIVETIMER (VFW. h)
description: El \_ mensaje MCIWNDM SETINACTIVETIMER establece el período de actualización que usa MCIWnd para actualizar la barra de control en la ventana MCIWnd, actualizar la información de la posición que se muestra en la barra de título de la ventana y enviar mensajes de notificación a la ventana primaria cuando la ventana de MCIWnd está inactiva. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSetInactiveTimer.
ms.assetid: 8900c372-0493-4a63-a027-ef6ecf8f8254
keywords:
- Mensaje de MCIWNDM_SETINACTIVETIMER de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4504d84b254dfb67616568f5f97bba8e3bc2e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534636"
---
# <a name="mciwndm_setinactivetimer-message"></a>MCIWNDM \_ SETINACTIVETIMER

El mensaje **MCIWNDM \_ SETINACTIVETIMER** establece el período de actualización que usa MCIWnd para actualizar la barra de control en la ventana MCIWnd, actualizar la información de la posición que se muestra en la barra de título de la ventana y enviar mensajes de notificación a la ventana primaria cuando la ventana de MCIWnd está inactiva. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) .


```C++
MCIWNDM_SETINACTIVETIMER 
wParam = (WPARAM) (UINT) inactive; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*inactiva*
</dt> <dd>

Período de actualización, en milisegundos. El valor predeterminado es 2000 milisegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
</dt> </dl>

 

 





