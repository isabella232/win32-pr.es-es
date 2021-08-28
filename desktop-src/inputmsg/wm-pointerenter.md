---
title: WM_POINTERENTER mensaje
description: Se envía a una ventana cuando un nuevo puntero entra en el intervalo de detección sobre la ventana (mantener el puntero) o cuando un puntero existente se mueve dentro de los límites de la ventana.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8a0222
keywords:
- WM_POINTERENTER mensajes de entrada y notificaciones
topic_type:
- apiref
api_name:
- WM_POINTERENTER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: dfb871f232ea04b417b0aa038da1aaf7831a6a8e4d86b3c2888ca7c6e3708553
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602285"
---
# <a name="wm_pointerenter-message"></a>WM_POINTERENTER mensaje

Se envía a una ventana cuando un nuevo puntero entra en el intervalo de detección sobre la ventana (mantener el puntero) o cuando un puntero existente se mueve dentro de los límites de la ventana.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> \[! Importante\]  
> Las aplicaciones de escritorio deben tener en cuenta los valores de PPP. Si la aplicación no tiene reconocimiento de PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas pueden parecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a aplicaciones que no tienen reconocimiento de PPP y que están activas de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, consulte [Escritura de aplicaciones Win32 con valores altos de PPP.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_POINTERENTER                 0x0249
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene el identificador del puntero y la información adicional. Use las macros siguientes para recuperar información específica en el parámetro wParam.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador del puntero.
-   [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica si este mensaje es el primer mensaje generado por un nuevo puntero que entra en el intervalo de detección (mantener el puntero).
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica si este mensaje lo generó un puntero que no ha dejado el intervalo de detección. Esta marca siempre se establece para **WM_POINTERENTER** mensajes.
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

## <a name="remarks"></a>Comentarios

El **WM_POINTERENTER** notificación puede ser utilizado por una ventana para proporcionar comentarios al usuario mientras el puntero está sobre su superficie o para reaccionar de otro modo a la presencia de un puntero sobre su superficie.

Esta notificación solo se envía a la ventana que recibe la entrada para el puntero. En la tabla siguiente se enumeran algunas de las situaciones en las que se envía esta notificación.



| Acción                                                   | Conjunto de marcas                                                                                                                                         | Notificaciones enviadas a                                 |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Un nuevo puntero entra en el intervalo de detección (mantener el puntero).            | [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)<br/> [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)<br/> | Ventana sobre la que el puntero entra en el intervalo de detección. |
| Un puntero que mantiene el puntero se cruza dentro de los límites de la ventana. | [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)<br/>                                                                      | Ventana en la que se ha cruzado el puntero.          |



 

> \[! Importante\]  
> Cuando una ventana pierde la captura de [](wm-pointercapturechanged.md) un puntero y recibe la notificación WM_POINTERCAPTURECHANGED, normalmente no recibirá ninguna notificación adicional. Por esta razón, es importante que no realice ninguna [](wm-pointerdown.md)suposición basada en notificaciones de WM_POINTERDOWN WM_POINTERUP o WM_POINTERENTER / [](wm-pointerup.md)  / [**WM_POINTERLEAVE**](wm-pointerleave.md) emparejadas uniformemente.

 

Cuando las entradas proceden del mouse, como resultado de la integración de mensajes de puntero y **mouse,** WM_POINTERENTER no se envía.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                               |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mensajes](messages.md)
</dt> <dt>

**Referencia**
</dt> <dt>

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

