---
title: Mensaje de MCIWNDM_SETACTIVETIMER (VFW. h)
description: El \_ mensaje MCIWNDM SETACTIVETIMER establece el período de actualización que usa MCIWnd para actualizar la barra de control en la ventana MCIWnd, actualizar la información de la posición que se muestra en la barra de título de la ventana y enviar mensajes de notificación a la ventana primaria cuando la ventana de MCIWnd está activa. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSetActiveTimer.
ms.assetid: a30c0091-d9bb-44a3-a7b0-d1be30adcd9c
keywords:
- Mensaje de MCIWNDM_SETACTIVETIMER de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150630"
---
# <a name="mciwndm_setactivetimer-message"></a>MCIWNDM \_ SETACTIVETIMER

El mensaje **MCIWNDM \_ SETACTIVETIMER** establece el período de actualización que usa MCIWnd para actualizar la barra de control en la ventana MCIWnd, actualizar la información de la posición que se muestra en la barra de título de la ventana y enviar mensajes de notificación a la ventana primaria cuando la ventana de MCIWnd está activa. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) .


```C++
MCIWNDM_SETACTIVETIMER 
wParam = (WPARAM) (UINT) active; 
lParam = 0L; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="active"></span><span id="ACTIVE"></span>*Active*
</dt> <dd>

Período de actualización, en milisegundos. El valor predeterminado es 500 milisegundos.

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

[**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)
</dt> </dl>

 

 





