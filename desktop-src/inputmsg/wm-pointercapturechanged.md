---
title: WM_POINTERCAPTURECHANGED mensaje
description: Se envía a una ventana que pierde la captura de un puntero de entrada.
ms.assetid: 6eec37da-227c-4be1-bf0b-98704caa1322
keywords:
- WM_POINTERCAPTURECHANGED mensajes de entrada y notificaciones
topic_type:
- apiref
api_name:
- WM_POINTERCAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 768dc81be57bb61a23acab7ebea450dba577d60a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569524"
---
# <a name="wm_pointercapturechanged-message"></a>WM_POINTERCAPTURECHANGED mensaje

Se envía a una ventana que pierde la captura de un puntero de entrada.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_POINTERCAPTURECHANGED           0x024C
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene información sobre el puntero de entrada que se pierde. Use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) para obtener el identificador de puntero.

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene un identificador para la ventana que captura el puntero de entrada. Este valor puede ser NULL si la ventana ya no captura el puntero.

Si este mensaje se genera a partir del procesamiento interno, el valor puede ser el identificador de la ventana que recibe el mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Observaciones

Una ventana debe usar esta notificación para detener el procesamiento de mensajes posteriores e iniciar cualquier limpieza necesaria para que se pierda el puntero. El procesamiento de los gestos asociados al puntero también debe finalizar (por ejemplo, llamando a [**StopInteractionContext)**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)y los contactos restantes se deben volver a asociar a la ventana.

Normalmente, si una ventana recibe la **notificación WM_POINTERCAPTURECHANGED,** no se reciben notificaciones posteriores relacionadas con el puntero de entrada. Por este problema, no dependa de las notificaciones emparejadas, como [**WM_POINTERENTER**](wm-pointerenter.md) y [**WM_POINTERLEAVE**](wm-pointerleave.md).

**WM_POINTERCAPTURECHANGED** no [**incluye**](/previous-versions/windows/desktop/api) POINTER_INFO datos. Aparte de la [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) que se establece, los datos devueltos por [**GetPointerInfo**](/previous-versions/windows/desktop/api) (o cualquier variante) son idénticos a los devueltos antes de la notificación.

Si la aplicación no procesa esta notificación, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) puede generar uno o varios mensajes WM_GESTURE o, si no se reconoce un gesto, **DefWindowProc** puede generar entradas del mouse. [](../wintouch/wm-gesture.md)

Si una aplicación consume selectivamente alguna entrada de puntero y pasa el resto a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), el comportamiento resultante es indefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                               |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Mensajes](messages.md)
</dt> </dl>

 

