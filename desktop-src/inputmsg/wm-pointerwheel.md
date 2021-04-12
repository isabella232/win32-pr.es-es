---
title: Mensaje WM_POINTERWHEEL
description: Se envía a la ventana con el foco de teclado en primer plano cuando se gira una rueda de desplazamiento.
ms.assetid: 6eec37da-2200-4be1-bf0b-44704caa1320
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_POINTERWHEEL
topic_type:
- apiref
api_name:
- WM_POINTERWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: ad1177b2e92e47ca40c745e6cd5f1ea2cf259215
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490030"
---
# <a name="wm_pointerwheel-message"></a>Mensaje WM_POINTERWHEEL

Se envía a la ventana con el foco de teclado en primer plano cuando se gira una rueda de desplazamiento.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> \[! Aún\]  
> Las aplicaciones de escritorio deben tener en cuenta los ppp. Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERWHEEL            0x024E
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene el identificador del puntero y el delta de la rueda. Use las siguientes macros para recuperar esta información.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador de puntero.

[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)(wParam): diferencia de la rueda como un valor corto con signo.

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene la ubicación del punto del puntero.

> [!Note]  
> Dado que el puntero puede establecer contacto con el dispositivo a través de un área no trivial, esta ubicación de punto puede ser una simplificación de un área de puntero más compleja. Siempre que sea posible, una aplicación debe usar la información de área de puntero completa en lugar de la ubicación del punto.

 

Utilice las siguientes macros para recuperar las coordenadas físicas de la pantalla del punto.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): la coordenada X (punto horizontal).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): la coordenada Y (punto vertical).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la aplicación procesa este mensaje, debe devolver cero.

Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Observaciones

Para recuperar las unidades de desplazamiento de la rueda, use el **inputData** de la estructura de [**POINTER_INFO**](/previous-versions/windows/desktop/api) devuelta por una llamada a la función [**GetPointerInfo**](/previous-versions/windows/desktop/api) . Este campo contiene un valor con signo y se expresa en un múltiplo de **WHEEL_DELTA**. Un valor positivo indica un giro hacia delante y un valor negativo indica un giro hacia atrás.

Tenga en cuenta que las entradas de la rueda se pueden entregar incluso si el cursor del mouse se encuentra fuera de la ventana de la aplicación. Los mensajes de la rueda se entregan de forma muy similar a las entradas del teclado. La ventana de enfoque de la cola de mensajes foregournd recibe los mensajes de la rueda.

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

 

