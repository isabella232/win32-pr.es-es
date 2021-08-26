---
title: WM_POINTERHWHEEL mensaje
description: Se publica en la ventana con el foco de teclado en primer plano cuando se gira una rueda de desplazamiento horizontal.
ms.assetid: 6eec37da-2200-4be1-bf0b-44504caa1320
keywords:
- WM_POINTERHWHEEL mensajes de entrada y notificaciones
topic_type:
- apiref
api_name:
- WM_NCPOINTERCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9de03b198603f06b4c1c1401714bd2fd5edfe28784890c4b9ab00a025dbaab7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015242"
---
# <a name="wm_pointerhwheel-message"></a>WM_POINTERHWHEEL mensaje

Se publica en la ventana con el foco de teclado en primer plano cuando se gira una rueda de desplazamiento horizontal.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> \[! Importante\]  
> Las aplicaciones de escritorio deben tener en cuenta los valores de PPP. Si la aplicación no tiene reconocimiento de PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas pueden parecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a aplicaciones que no tienen reconocimiento de PPP y que están activas de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, consulte [Escritura de aplicaciones Win32 con valores altos de PPP.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_POINTERHWHEEL            0x024F
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene el identificador de puntero y la diferencia de rueda. Use las macros siguientes para recuperar esta información.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador de puntero.

[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)(wParam): delta de rueda como valor corto con firma.

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene la ubicación de punto del puntero.

> [!Note]  
> Dado que el puntero puede hacer contacto con el dispositivo a través de un área no trivial, esta ubicación de punto puede ser una simplificación de un área de puntero más compleja. Siempre que sea posible, una aplicación debe usar la información completa del área de puntero en lugar de la ubicación del punto.

 

Use las macros siguientes para recuperar las coordenadas de pantalla física del punto.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): la coordenada x (punto horizontal).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): coordenada y (punto vertical).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la aplicación procesa este mensaje, debe devolver cero.

Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Comentarios

Para recuperar las unidades de desplazamiento de rueda, use **el archivo inputData** de la [**POINTER_INFO**](/previous-versions/windows/desktop/api) estructura devuelta mediante una llamada a la [**función GetPointerInfo.**](/previous-versions/windows/desktop/api) Este campo contiene un valor con firma y se expresa en un múltiplo de **WHEEL_DELTA**. Un valor positivo indica una rotación hacia delante y un valor negativo indica una rotación hacia atrás.

Tenga en cuenta que las entradas de rueda se pueden entregar incluso si el cursor del mouse se encuentra fuera de la ventana de la aplicación. Los mensajes de rueda se entregan de forma muy similar a las entradas del teclado. La ventana de foco de la cola de mensajes de advertencia recibe los mensajes de rueda.

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

 

