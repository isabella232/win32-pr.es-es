---
title: WM_NCPOINTERUPDATE mensaje
description: Se publica para proporcionar una actualización en un puntero que hizo contacto sobre el área no cliente de una ventana o cuando un contacto no capturado se mueve sobre el área no cliente de una ventana.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704caa1322
keywords:
- WM_NCPOINTERUPDATE mensajes de entrada y notificaciones
topic_type:
- apiref
api_name:
- WM_NCPOINTERUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 6f1cf786af00175f75b5faee11b384aa31618d89427826f9c1454006df461f0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062425"
---
# <a name="wm_ncpointerupdate-message"></a>WM_NCPOINTERUPDATE mensaje

Se publica para proporcionar una actualización en un puntero que hizo contacto sobre el área no cliente de una ventana o cuando un contacto no capturado se mueve sobre el área no cliente de una ventana. Mientras el puntero mantiene el puntero, el mensaje tiene como destino la ventana sobre la que se encuentra el puntero. Mientras el puntero está en contacto con la superficie, el puntero se captura implícitamente en la ventana en la que el puntero hizo contacto y esa ventana continúa recibiendo la entrada del puntero hasta que se interrumpe el contacto.

Si una ventana ha capturado este puntero, este mensaje no se publica. En su [**lugar, WM_POINTERUPDATE**](wm-pointerupdate.md) se publica en la ventana que ha capturado este puntero.

> \[! Importante\]  
> Las aplicaciones de escritorio deben tener en cuenta los valores de PPP. Si la aplicación no es compatible con PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas pueden parecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a aplicaciones que no son compatibles con PPP y que están activas de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, consulte [Escritura de aplicaciones Win32 con valores altos de PPP.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_NCPOINTERUPDATE                 0x0241
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene el identificador de puntero y la información adicional. Use las macros siguientes para recuperar esta información.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador de puntero

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): valor de prueba de impacto devuelto al procesar [**el WM_NCHITTEST**](../inputdev/wm-nchittest.md) mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene la ubicación de punto del puntero.

> [!Note]  
> Dado que el puntero puede hacer contacto con el dispositivo a través de un área no trivial, esta ubicación de punto puede ser una simplificación de un área de puntero más compleja. Siempre que sea posible, una aplicación debe usar la información completa del área de puntero en lugar de la ubicación de punto.

 

Use las macros siguientes para recuperar las coordenadas de pantalla física del punto.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): la coordenada x (punto horizontal).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): coordenada y (punto vertical).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Comentarios

Si la aplicación no procesa este mensaje, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) puede realizar una o varias acciones del sistema en función del resultado de la prueba de acceso incluida en el mensaje. Normalmente, las aplicaciones no deben tener que controlar este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                               |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mensajes](messages.md)
</dt> </dl>

 

