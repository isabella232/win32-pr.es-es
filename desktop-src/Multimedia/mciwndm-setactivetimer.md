---
title: MCIWNDM_SETACTIVETIMER mensaje (Vfw.h)
description: El mensaje MCIWNDM SETACTIVETIMER establece el período de actualización utilizado por MCIWnd para actualizar la barra de seguimiento en la ventana MCIWnd, actualizar la información de posición mostrada en la barra de título de la ventana y enviar mensajes de notificación a la ventana primaria cuando la ventana \_ MCIWnd está activa. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSetActiveTimer.
ms.assetid: a30c0091-d9bb-44a3-a7b0-d1be30adcd9c
keywords:
- MCIWNDM_SETACTIVETIMER mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1924a991f0627009a8e622c8f8be086b2e045635
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250767"
---
# <a name="mciwndm_setactivetimer-message"></a>Mensaje DE MCIWNDM \_ SETACTIVETIMER

El mensaje **MCIWNDM \_ SETACTIVETIMER** establece el período de actualización utilizado por MCIWnd para actualizar la barra de seguimiento en la ventana MCIWnd, actualizar la información de posición mostrada en la barra de título de la ventana y enviar mensajes de notificación a la ventana primaria cuando la ventana MCIWnd está activa. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetActiveTimer.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)


```C++
MCIWNDM_SETACTIVETIMER 
wParam = (WPARAM) (UINT) active; 
lParam = 0L; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="active"></span><span id="ACTIVE"></span>*Activo*
</dt> <dd>

Período de actualización, en milisegundos. El valor predeterminado es 500 milisegundos.

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

[**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)
</dt> </dl>

 

 





