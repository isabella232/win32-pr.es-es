---
title: TBM_GETLINESIZE mensaje (Commctrl.h)
description: Recupera el número de posiciones lógicas que el control deslizante de la barra de seguimiento mueve en respuesta a la entrada del teclado de las teclas de dirección, como las teclas o . Las posiciones lógicas son los incrementos enteros en el intervalo de posiciones del control deslizante mínimo a máximo de la barra de seguimiento.
ms.assetid: b596060a-5bac-4b31-82f3-ee4744a9779c
keywords:
- TBM_GETLINESIZE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166526"
---
# <a name="tbm_getlinesize-message"></a>Mensaje \_ GETLINESIZE de TBM

Recupera el número de posiciones lógicas que el control deslizante de la barra de seguimiento mueve en respuesta a la entrada del teclado de las teclas de dirección, como las teclas o . Las posiciones lógicas son los incrementos enteros en el intervalo de posiciones del control deslizante mínimo a máximo de la barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 32 bits que especifica el tamaño de línea de la barra de seguimiento.

## <a name="remarks"></a>Observaciones

El valor predeterminado para el tamaño de línea es 1.

La barra de seguimiento también envía un mensaje [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con los códigos de notificación LINEUP y TB LINEDOWN de TB a su ventana primaria cuando el usuario presiona las teclas de \_ \_ dirección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





