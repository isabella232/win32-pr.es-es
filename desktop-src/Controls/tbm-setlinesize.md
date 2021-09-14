---
title: TBM_SETLINESIZE mensaje (Commctrl.h)
description: Establece el número de posiciones lógicas que el control deslizante de la barra de seguimiento mueve en respuesta a la entrada del teclado desde las teclas de dirección, como las teclas o . Las posiciones lógicas son los incrementos enteros en el intervalo de posiciones del control deslizante mínimo a máximo de la barra de seguimiento.
ms.assetid: 7fe3f9b8-2ddf-4460-882f-6be439f83daa
keywords:
- TBM_SETLINESIZE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_SETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec898ed09b20f15023ef04a399f5644df746e495
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166462"
---
# <a name="tbm_setlinesize-message"></a>Mensaje \_ SETLINESIZE de TBM

Establece el número de posiciones lógicas que el control deslizante de la barra de seguimiento mueve en respuesta a la entrada del teclado desde las teclas de dirección, como las teclas o . Las posiciones lógicas son los incrementos enteros en el intervalo de posiciones del control deslizante mínimo a máximo de la barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Nuevo tamaño de línea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 32 bits que especifica el tamaño de línea anterior.

## <a name="remarks"></a>Observaciones

El valor predeterminado para el tamaño de línea es 1.

La barra de seguimiento también envía un mensaje [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con los códigos de notificación LINEUP y TB LINEDOWN de TB a su ventana primaria cuando el usuario presiona las teclas de \_ \_ dirección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TBM \_ GETLINESIZE**](tbm-getlinesize.md)
</dt> </dl>

 

 





