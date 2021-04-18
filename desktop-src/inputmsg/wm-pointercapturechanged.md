---
title: Mensaje WM_POINTERCAPTURECHANGED
description: Se envía a una ventana que está perdiendo la captura de un puntero de entrada.
ms.assetid: 6eec37da-227c-4be1-bf0b-98704caa1322
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_POINTERCAPTURECHANGED
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105720233"
---
# <a name="wm_pointercapturechanged-message"></a>Mensaje WM_POINTERCAPTURECHANGED

Se envía a una ventana que está perdiendo la captura de un puntero de entrada.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_POINTERCAPTURECHANGED           0x024C
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene información sobre el puntero de entrada que se está perdida. Use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) para obtener el identificador de puntero.

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene un identificador de la ventana que está capturando el puntero de entrada. Este valor puede ser NULL si la ventana ya no captura el puntero.

Si este mensaje se genera a partir del procesamiento interno, el valor puede ser el identificador de la ventana que recibe el mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Observaciones

Una ventana debe usar esta notificación para detener el procesamiento de mensajes posteriores e iniciar cualquier limpieza necesaria para que el puntero se pierda. El procesamiento de gestos asociados al puntero también debe finalizar (por ejemplo, llamando a [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)) y los contactos restantes se vuelven a asociar a la ventana.

Normalmente, si una ventana recibe la notificación **WM_POINTERCAPTURECHANGED** , no se reciben notificaciones posteriores relacionadas con el puntero de entrada. Por este motivo, no dependa de las notificaciones emparejadas como [**WM_POINTERENTER**](wm-pointerenter.md) y [**WM_POINTERLEAVE**](wm-pointerleave.md).

**WM_POINTERCAPTURECHANGED** no incluye datos de [**POINTER_INFO**](/previous-versions/windows/desktop/api) . Aparte de la marca [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) que se va a establecer, los datos devueltos por [**GetPointerInfo**](/previous-versions/windows/desktop/api) (o cualquier variante) son idénticos a los que se devolvieron antes de la notificación.

Si la aplicación no procesa esta notificación, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) puede generar uno o más mensajes [**WM_GESTURE**](../wintouch/wm-gesture.md) o, si no se reconoce un gesto, **DefWindowProc** puede generar la entrada del mouse.

Si una aplicación usa selectivamente alguna entrada de puntero y pasa el resto a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), el comportamiento resultante es indefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mensajes](messages.md)
</dt> </dl>

 

