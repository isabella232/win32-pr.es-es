---
description: Se envía cuando un usuario realiza un gesto de lápiz. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 9433aadf-3440-4249-8f2c-3e22ebc949fb
title: WM_TABLET_FLICK mensaje (Tpcshrd.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb01fce646d2e7c6cb4e1b25c2f49f0c4dde5258ba2167e117a23eff22a5d1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842793"
---
# <a name="wm_tablet_flick-message"></a>Mensaje \_ DE WM TABLET \_ FLICK

Se envía cuando un usuario realiza un gesto de lápiz. Una ventana recibe este mensaje a través de su [*función WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_FLICK    (WM_TABLET_DEFBASE + 11)     
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Estructura [**DE DATOS \_ DE FLICK**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) que contiene información sobre el gesto de lápiz que se produjo.

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura [**FLICK \_ POINT que**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) especifica dónde se produjo el gesto de lápiz.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Un gesto de lápiz es un gesto de lápiz unidireccional que requiere que el usuario se pondrá en contacto con el digitalizador en un movimiento rápido y sencillo. Un gesto se caracteriza por una alta velocidad y un alto grado de recta. Un gesto se identifica por su dirección. Los gestos se pueden realizar en ocho direcciones correspondientes a las direcciones cardinal y secundaria de la brújula.

Cuando se produce un gesto de lápiz, Windows notifica primero a una aplicación mediante el envío de un mensaje **WM \_ TABLET \_ FLICK,** que una ventana recibe a través de su [*función WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Devuelve la **constante FLICK \_ WM \_ HANDLED \_ MASK,** descrita en [Flicks Constants](flicks-constants.md), para indicar que la aplicación respondió al mensaje **DE WM TABLET \_ \_ FLICK.** Si la aplicación no devuelve **FLICK \_ WM \_ HANDLED \_ MASK,** Windows realiza la acción predeterminada especificada en el panel de control de gestos mediante el envío de una notificación de seguimiento, como [**WM \_ APPCOMMAND,**](../inputdev/wm-appcommand.md) [**WM \_ VSCROLL**](../controls/wm-vscroll.md)o [**WM \_ KEYDOWN,**](../inputdev/wm-keydown.md)en función de la acción asociada al gesto de lápiz.

Tenga cuidado al controlar el **mensaje \_ WM TABLET \_ FLICK.** **WM \_ TABLET \_ FLICK** se pasa a través de [**la función SendMessageTimeout.**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) Si llama a métodos en una interfaz COM, ese objeto debe estar dentro del mismo proceso. Si no es así, COM produce una excepción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Tpcshrd.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**estructura de \_ datos de movimiento**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data)
</dt> <dt>

[**wm \_ tablet \_ flick message**](wm-tablet-flick-message.md)
</dt> <dt>

[gestos de gestos de gestos](flicks-gestures.md)
</dt> <dt>

[responder a los gestos de lápiz](/previous-versions/windows/desktop/ms703447(v=vs.85))
</dt> </dl>

 

 
