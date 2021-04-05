---
title: Mensaje de TBM_SETPAGESIZE (commctrl. h)
description: Establece el número de posiciones lógicas que se mueve el control deslizante de la barra de desplazamiento en respuesta a la entrada del teclado, como las teclas o, o la entrada del mouse, como los clics en el canal de la barra de desplazamiento.
ms.assetid: 34edb868-4b6b-4b3f-b315-3ce39346b134
keywords:
- TBM_SETPAGESIZE controles de mensajes de Windows
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
ms.openlocfilehash: ec5d8a396bb605b4276346e84e7b46bfbefe0657
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079602"
---
# <a name="tbm_setpagesize-message"></a>TBM \_ SETPAGESIZE

Establece el número de posiciones lógicas que se mueve el control deslizante de la barra de desplazamiento en respuesta a la entrada del teclado, como las teclas o, o la entrada del mouse, como los clics en el canal de la barra de desplazamiento. Las posiciones lógicas son los incrementos enteros en el intervalo de la barra de desplazamiento mínimo al máximo.

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

## <a name="remarks"></a>Observaciones

La barra de desplazamiento también envía un mensaje de [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con los \_ códigos de notificación TB RePág y TB \_ Av Pág a su ventana primaria cuando recibe la entrada del teclado o del mouse que se desplaza por la página.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TBM \_ GETPAGESIZE**](tbm-getpagesize.md)
</dt> </dl>

 

 





