---
title: Mensaje de MCIWNDM_SETTIMERS (VFW. h)
description: El \_ mensaje MCIWNDM SETTIMERS establece los períodos de actualización usados por MCIWnd para actualizar la barra de control en la ventana MCIWnd, actualizar la información de posición que se muestra en la barra de título de la ventana y enviar mensajes de notificación a la ventana primaria.
ms.assetid: 06407c67-b620-4f80-9fe9-456cdf3d0666
keywords:
- Mensaje de MCIWNDM_SETTIMERS de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801327"
---
# <a name="mciwndm_settimers-message"></a>MCIWNDM \_ SETTIMERS

El mensaje **MCIWNDM \_ SETTIMERS** establece los períodos de actualización usados por MCIWnd para actualizar la barra de control en la ventana MCIWnd, actualizar la información de posición que se muestra en la barra de título de la ventana y enviar mensajes de notificación a la ventana primaria. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) .


```C++
MCIWNDM_SETTIMERS 
wParam = (WPARAM) (UINT) active; 
lParam = (LPARAM) (UINT) inactive; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="active"></span><span id="ACTIVE"></span>*Active*
</dt> <dd>

Período de actualización usado por MCIWnd cuando se trata de la ventana activa. El valor predeterminado es 500 milisegundos. El almacenamiento de este valor está limitado a 16 bits.

</dd> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*inactiva*
</dt> <dd>

Período de actualización usado por MCIWnd cuando se trata de la ventana inactiva. El valor predeterminado es 2000 milisegundos. El almacenamiento de este valor está limitado a 16 bits.

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

[**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)
</dt> </dl>

 

 





