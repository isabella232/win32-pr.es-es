---
title: TBM_GETPAGESIZE mensaje (Commctrl.h)
description: Recupera el número de posiciones lógicas que el control deslizante de la barra de seguimiento mueve en respuesta a la entrada del teclado, como las teclas o o la entrada del mouse, como los clics en el canal de la barra de seguimiento.
ms.assetid: f0c5feac-2723-440e-96c0-dac37b0531ed
keywords:
- TBM_GETPAGESIZE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_GETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1aa3ef3412fd00c18972b62d4d868ff1dbc97cb4787693b3746281b4884706e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046505"
---
# <a name="tbm_getpagesize-message"></a>Mensaje \_ GETPAGESIZE de TBM

Recupera el número de posiciones lógicas que el control deslizante de la barra de seguimiento mueve en respuesta a la entrada del teclado, como las teclas o o la entrada del mouse, como los clics en el canal de la barra de seguimiento. Las posiciones lógicas son los incrementos enteros en el intervalo de posiciones del control deslizante mínimo al máximo de la barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 32 bits que especifica el tamaño de página de la barra de seguimiento.

## <a name="remarks"></a>Comentarios

La barra de seguimiento también envía un mensaje [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con los códigos de notificación PAGEUP y TB PAGEDOWN de TB a su ventana primaria cuando recibe la entrada del teclado o del mouse que se desplaza por la \_ \_ página.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TBM \_ SETPAGESIZE**](tbm-setpagesize.md)
</dt> </dl>

 

 





