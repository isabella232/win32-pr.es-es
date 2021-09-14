---
title: MCIWNDM_SETTIMERS mensaje (Vfw.h)
description: El mensaje MCIWNDM SETTIMERS establece los períodos de actualización usados por MCIWnd para actualizar la barra de seguimiento en la ventana MCIWnd, actualizar la información de posición mostrada en la barra de título de la ventana y enviar mensajes de notificación a la ventana \_ primaria.
ms.assetid: 06407c67-b620-4f80-9fe9-456cdf3d0666
keywords:
- MCIWNDM_SETTIMERS mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMERS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bba3fa2e474a15dc23deb9cdc6d00d148b8cd3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250730"
---
# <a name="mciwndm_settimers-message"></a>Mensaje DE MCIWNDM \_ SETTIMERS

El mensaje **MCIWNDM \_ SETTIMERS** establece los períodos de actualización usados por MCIWnd para actualizar la barra de seguimiento en la ventana MCIWnd, actualizar la información de posición mostrada en la barra de título de la ventana y enviar mensajes de notificación a la ventana primaria. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetTimers.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)


```C++
MCIWNDM_SETTIMERS 
wParam = (WPARAM) (UINT) active; 
lParam = (LPARAM) (UINT) inactive; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="active"></span><span id="ACTIVE"></span>*Activo*
</dt> <dd>

Período de actualización usado por MCIWnd cuando es la ventana activa. El valor predeterminado es 500 milisegundos. Storage para este valor se limita a 16 bits.

</dd> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*Inactivo*
</dt> <dd>

Período de actualización utilizado por MCIWnd cuando es la ventana inactiva. El valor predeterminado es 2000 milisegundos. Storage para este valor se limita a 16 bits.

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

[**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)
</dt> </dl>

 

 





