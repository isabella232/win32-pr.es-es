---
title: MCIWNDM_SETINACTIVETIMER mensaje (Vfw.h)
description: El mensaje MCIWNDM SETFRACCIÓNTIMER establece el período de actualización utilizado por MCIWnd para actualizar la barra de seguimiento en la ventana MCIWnd, actualizar la información de posición mostrada en la barra de título de la ventana y enviar mensajes de notificación a la ventana primaria cuando la ventana \_ MCIWnd está inactiva. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSet NoTimer.
ms.assetid: 8900c372-0493-4a63-a027-ef6ecf8f8254
keywords:
- MCIWNDM_SETINACTIVETIMER mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370747"
---
# <a name="mciwndm_setinactivetimer-message"></a>Mensaje DE MCIWNDM \_ SETCIÓNTIMER

El **mensaje MCIWNDM \_ SETFRACCIÓNTIMER** establece el período de actualización utilizado por MCIWnd para actualizar la barra de seguimiento en la ventana MCIWnd, actualizar la información de posición mostrada en la barra de título de la ventana y enviar mensajes de notificación a la ventana primaria cuando la ventana MCIWnd está inactiva. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSet NoTimer.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)


```C++
MCIWNDM_SETINACTIVETIMER 
wParam = (WPARAM) (UINT) inactive; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*Inactivo*
</dt> <dd>

Período de actualización, en milisegundos. El valor predeterminado es 2000 milisegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndSetCiónTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
</dt> </dl>

 

 





