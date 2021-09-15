---
title: WM_POINTERLEAVE mensaje
description: Se envía a una ventana cuando un puntero sale del intervalo de detección sobre la ventana (mantener el mouse) o cuando un puntero se mueve fuera de los límites de la ventana.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8c1322
keywords:
- WM_POINTERLEAVE mensajes de entrada y notificaciones
topic_type:
- apiref
api_name:
- WM_POINTERDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 2ee58fd74f266d067f6211e156d984a3b3d1c477
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569496"
---
# <a name="wm_pointerleave-message"></a>WM_POINTERLEAVE mensaje

Se envía a una ventana cuando un puntero sale del intervalo de detección sobre la ventana (mantener el mouse) o cuando un puntero se mueve fuera de los límites de la ventana.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> \[! Importante\]  
> Las aplicaciones de escritorio deben tener en cuenta los valores de PPP. Si la aplicación no tiene reconocimiento de PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas pueden parecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a aplicaciones que no tienen reconocimiento de PPP y que están activas de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, consulte [Escritura de aplicaciones Win32 con valores altos de PPP.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_POINTERLEAVE                 0x024A
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene el identificador de puntero y la información adicional. Use las macros siguientes para recuperar esta información.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador del puntero.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica si este mensaje lo generó un puntero que no tiene el intervalo de detección izquierdo. Esta marca no se establece cuando el puntero sale del intervalo de detección de la ventana.
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si este mensaje lo generó un puntero que está en contacto. Esta marca no se establece para un puntero en el intervalo de detección (mantener el puntero).

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

Si una aplicación procesa este mensaje, debe devolver cero.

Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Observaciones

El **WM_POINTERLEAVE** notificación puede ser utilizado por una ventana para cambiar el modo o detener cualquier comentario al usuario mientras el puntero está sobre la superficie de la ventana.

Esta notificación solo se envía a la ventana que recibe la entrada para el puntero. En la tabla siguiente se enumeran algunas de las situaciones en las que se envía esta notificación.



| Acción                                        | Conjunto de marcas                                                         | Notificaciones enviadas a                                |
|-----------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------|
| Un puntero que mantiene el puntero cruza los límites de la ventana. | [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api) | Ventana fuera de cuyo límite se movió el puntero.  |
| Un puntero sale del intervalo de detección.        | N/D                                                               | Ventana para la que el puntero deja el intervalo de detección. |



 

> \[! Importante\]  
> Cuando una ventana pierde la captura de [](wm-pointercapturechanged.md) un puntero y recibe la notificación WM_POINTERCAPTURECHANGED, normalmente no recibirá ninguna notificación adicional. Por esta razón, es importante que no realice ninguna [](wm-pointerdown.md)suposición basada en notificaciones de WM_POINTERDOWN WM_POINTERUP o WM_POINTERENTER / [](wm-pointerup.md) [](wm-pointerenter.md) / **WM_POINTERLEAVE** emparejadas uniformemente.

 

Si el contacto se mantiene con el digitalizador de entrada y el puntero se mueve fuera de la **ventana,** WM_POINTERLEAVE no se genera. **WM_POINTERLEAVE** se genera solo cuando un puntero que mantiene el puntero cruza los límites de la ventana o se termina el contacto.

**WM_POINTERLEAVE** se publica en la cola de mensajes publicados si la entrada se origina desde un dispositivo del mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                               |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Mensajes](messages.md)
</dt> <dt>

**Referencia**
</dt> <dt>

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

