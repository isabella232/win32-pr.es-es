---
title: Mensaje de TBM_GETPAGESIZE (commctrl. h)
description: Recupera el número de posiciones lógicas que el control deslizante de la barra de desplazamiento se mueve en respuesta a la entrada del teclado, como las teclas o, o la entrada del mouse, como los clics en el canal de la barra de desplazamiento.
ms.assetid: f0c5feac-2723-440e-96c0-dac37b0531ed
keywords:
- TBM_GETPAGESIZE controles de mensajes de Windows
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
ms.openlocfilehash: ac58c0b935b468cf8af565fba2db67c88418ee4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150311"
---
# <a name="tbm_getpagesize-message"></a>TBM \_ GETPAGESIZE

Recupera el número de posiciones lógicas que el control deslizante de la barra de desplazamiento se mueve en respuesta a la entrada del teclado, como las teclas o, o la entrada del mouse, como los clics en el canal de la barra de desplazamiento. Las posiciones lógicas son los incrementos enteros en el intervalo de la barra de desplazamiento mínimo al máximo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 32 bits que especifica el tamaño de página para el TrackBar.

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

[**TBM \_ SETPAGESIZE**](tbm-setpagesize.md)
</dt> </dl>

 

 





