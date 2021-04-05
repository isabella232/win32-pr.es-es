---
title: Mensaje de TBM_GETLINESIZE (commctrl. h)
description: Recupera el número de posiciones lógicas que el control deslizante de la barra de desplazamiento se mueve en respuesta a la entrada del teclado de las teclas de dirección, como las teclas o. Las posiciones lógicas son los incrementos enteros en el intervalo de la barra de desplazamiento mínimo al máximo.
ms.assetid: b596060a-5bac-4b31-82f3-ee4744a9779c
keywords:
- TBM_GETLINESIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86eb103f34461e545f5a9f56148c48364d880dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997168"
---
# <a name="tbm_getlinesize-message"></a>TBM \_ GETLINESIZE

Recupera el número de posiciones lógicas que el control deslizante de la barra de desplazamiento se mueve en respuesta a la entrada del teclado de las teclas de dirección, como las teclas o. Las posiciones lógicas son los incrementos enteros en el intervalo de la barra de desplazamiento mínimo al máximo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 32 bits que especifica el tamaño de línea para el TrackBar.

## <a name="remarks"></a>Observaciones

La configuración predeterminada para el tamaño de línea es 1.

La barra de control también envía un mensaje de [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con los \_ códigos de notificación de línea TB y TB \_ LINEDOWN a su ventana primaria cuando el usuario presiona las teclas de dirección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





