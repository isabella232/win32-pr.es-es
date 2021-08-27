---
title: TBM_SETPAGESIZE mensaje (Commctrl.h)
description: Establece el número de posiciones lógicas que el control deslizante de la barra de seguimiento se mueve en respuesta a la entrada del teclado, como las teclas o o la entrada del mouse, como los clics en el canal de la barra de seguimiento.
ms.assetid: 34edb868-4b6b-4b3f-b315-3ce39346b134
keywords:
- TBM_SETPAGESIZE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_SETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87cf41547a996e9726002101998ea859b7dbc6cc3e7ed3f87927fdae8bdadd2f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046105"
---
# <a name="tbm_setpagesize-message"></a>Mensaje \_ SETPAGESIZE de TBM

Establece el número de posiciones lógicas que el control deslizante de la barra de seguimiento se mueve en respuesta a la entrada del teclado, como las teclas o o la entrada del mouse, como los clics en el canal de la barra de seguimiento. Las posiciones lógicas son los incrementos enteros en el intervalo de posiciones del control deslizante mínimo a máximo de la barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Nuevo tamaño de página.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 32 bits que especifica el tamaño de página anterior.

## <a name="remarks"></a>Comentarios

La barra de seguimiento también envía un mensaje [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con los códigos de notificación PAGEUP y TB PAGEDOWN de TB a su ventana primaria cuando recibe la entrada del teclado o del mouse que desplaza la \_ \_ página.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TBM \_ GETPAGESIZE**](tbm-getpagesize.md)
</dt> </dl>

 

 





