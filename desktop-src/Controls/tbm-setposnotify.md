---
title: TBM_SETPOSNOTIFY mensaje (Commctrl.h)
description: 'TBM_SETPOSNOTIFY mensaje: establece la posición lógica actual del control deslizante en una barra de seguimiento.'
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- TBM_SETPOSNOTIFY de mensajes controles de Windows
topic_type:
- apiref
api_name:
- TBM_SETPOSNOTIFY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7201f3056ed05e6321ab9d9bd726edc3b4470f0b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104083"
---
# <a name="tbm_setposnotify-message"></a>Mensaje \_ TBM SETPOSNOTIFY

Establece la posición lógica actual del control deslizante en una barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

wParam no se usa.

</dd> <dt>

*lParam* 
</dt> <dd>

Nueva posición lógica del control deslizante. Las posiciones lógicas válidas son los valores enteros del intervalo de posiciones del control deslizante mínimo al máximo de la barra de seguimiento. Si este valor está fuera del intervalo máximo y mínimo del control, la posición se establece en el valor máximo o mínimo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Al llamar a **TBM \_ SETPOSNOTIFY,** se establecerá la ubicación del control deslizante de la barra de seguimiento como lo haría [**TBM \_ SETPOS,**](tbm-setpos.md) pero también hará que la barra de seguimiento notifique a su elemento primario de un movimiento a través de un mensaje WM [**\_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL.**](wm-vscroll.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[ R2\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





