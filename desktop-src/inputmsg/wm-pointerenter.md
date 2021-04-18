---
title: Mensaje WM_POINTERENTER
description: Se envía a una ventana cuando un nuevo puntero entra en el intervalo de detección sobre la ventana (se mantiene el mouse) o cuando un puntero existente se mueve dentro de los límites de la ventana.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8a0222
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_POINTERENTER
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
ms.openlocfilehash: 4d0f6304408514390bb40f2d0e78a766f9e2d118
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105720232"
---
# <a name="wm_pointerenter-message"></a>Mensaje WM_POINTERENTER

Se envía a una ventana cuando un nuevo puntero entra en el intervalo de detección sobre la ventana (se mantiene el mouse) o cuando un puntero existente se mueve dentro de los límites de la ventana.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> \[! Aún\]  
> Las aplicaciones de escritorio deben tener en cuenta los ppp. Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERENTER                 0x0249
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene el identificador de puntero y la información adicional. Use las siguientes macros para recuperar información específica en el parámetro wParam.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): el identificador de puntero.
-   [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica si este mensaje es el primer mensaje generado por un nuevo puntero que entra en el intervalo de detección (mantener el mouse).
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica si este mensaje fue generado por un puntero que no ha dejado el intervalo de detección. Esta marca siempre se establece para los mensajes de **WM_POINTERENTER** .
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si este mensaje fue generado por un puntero que está en contacto con. Esta marca no se establece para un puntero en el intervalo de detección (se mantiene el mouse).

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

Si una aplicación procesa este mensaje, debe devolver cero.

Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Observaciones

La notificación de **WM_POINTERENTER** se puede usar en una ventana para proporcionar comentarios al usuario mientras el puntero se encuentra sobre su superficie o, de lo contrario, reaccionar a la presencia de un puntero sobre su superficie.

Esta notificación solo se envía a la ventana que recibe la entrada para el puntero. En la tabla siguiente se enumeran algunas de las situaciones en las que se envía esta notificación.



| Acción                                                   | Marcas establecidas                                                                                                                                         | Notificaciones enviadas a                                 |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Un nuevo puntero entra en el intervalo de detección (se mantiene el mouse).            | [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)<br/> [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)<br/> | Ventana en la que el puntero entra en el intervalo de detección. |
| Un puntero de desplazamiento cruza dentro de los límites de la ventana. | [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)<br/>                                                                      | Ventana en la que se ha cruzado el puntero.          |



 

> \[! Aún\]  
> Cuando una ventana pierde la captura de un puntero y recibe la notificación [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , normalmente no recibirá ninguna notificación adicional. Por esta razón, es importante que no realice suposiciones basadas en WM_POINTERUP de WM_POINTERDOWN emparejadas uniformemente [](wm-pointerdown.md) / [](wm-pointerup.md) o **WM_POINTERENTER** / notificaciones [**WM_POINTERLEAVE**](wm-pointerleave.md) .

 

Cuando las entradas proceden del mouse, como resultado de la integración del mouse y del mensaje de puntero, no se envía **WM_POINTERENTER** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



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

 

