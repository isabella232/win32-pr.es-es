---
title: Mensaje de TBM_SETLINESIZE (commctrl. h)
description: Establece el número de posiciones lógicas que se mueve el control deslizante de la barra de desplazamiento en respuesta a la entrada del teclado de las teclas de dirección, como las teclas o. Las posiciones lógicas son los incrementos enteros en el intervalo de la barra de desplazamiento mínimo al máximo.
ms.assetid: 7fe3f9b8-2ddf-4460-882f-6be439f83daa
keywords:
- TBM_SETLINESIZE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996059"
---
# <a name="tbm_setlinesize-message"></a>TBM \_ SETLINESIZE

Establece el número de posiciones lógicas que se mueve el control deslizante de la barra de desplazamiento en respuesta a la entrada del teclado de las teclas de dirección, como las teclas o. Las posiciones lógicas son los incrementos enteros en el intervalo de la barra de desplazamiento mínimo al máximo.

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

La configuración predeterminada para el tamaño de línea es 1.

La barra de control también envía un mensaje de [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con los \_ códigos de notificación de línea TB y TB \_ LINEDOWN a su ventana primaria cuando el usuario presiona las teclas de dirección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TBM \_ GETLINESIZE**](tbm-getlinesize.md)
</dt> </dl>

 

 





