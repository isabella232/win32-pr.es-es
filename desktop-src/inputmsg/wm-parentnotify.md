---
title: Mensaje WM_PARENTNOTIFY
description: Se envía a una ventana cuando se produce una acción significativa en una ventana descendiente.
ms.assetid: 4bdc37da-227c-4be1-bf0b-99704caa1444
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_PARENTNOTIFY
topic_type:
- apiref
api_name:
- WM_PARENTNOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 2e19edf25933a035514f9c42b0da6014eccfdb0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534707"
---
# <a name="wm_parentnotify-message"></a>Mensaje WM_PARENTNOTIFY

Se envía a una ventana cuando se produce una acción significativa en una ventana descendiente. Este mensaje se ha ampliado para incluir el evento [**WM_POINTERDOWN**](wm-pointerdown.md) . Cuando se crea la ventana secundaria, el sistema envía [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) justo antes de que la función [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) que crea la ventana devuelva. Cuando se destruye la ventana secundaria, el sistema envía el mensaje antes de que se produzca cualquier procesamiento para destruir la ventana.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> \[! Aún\]  
> Las aplicaciones de escritorio deben tener en cuenta los ppp. Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_PARENTNOTIFY             0x0210
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La palabra de orden inferior de *wParam* especifica el evento para el que se notifica al elemento primario. El valor de la palabra de orden superior depende del valor de la palabra de orden inferior. Este parámetro puede ser uno de los valores siguientes.



| LOWORD (*wParam*)                                                                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WM_CREATE"></span><span id="wm_create"></span><dl> <dt>**WM_CREATE**</dt> <dt>0x0001</dt> </dl>                | Se está creando la ventana secundaria.<br/> HIWORD (*wParam*) es el identificador de la ventana secundaria.<br/> *lParam* es un identificador de la ventana secundaria.<br/>                                                                                                                                                                                                                          |
| <span id="WM_DESTROY"></span><span id="wm_destroy"></span><dl> <dt>**WM_DESTROY**</dt> <dt>0x0002</dt> </dl>             | Se está destruyendo la ventana secundaria.<br/> HIWORD (*wParam*) es el identificador de la ventana secundaria.<br/> *lParam* es un identificador de la ventana secundaria.<br/>                                                                                                                                                                                                                        |
| <span id="WM_LBUTTONDOWN"></span><span id="wm_lbuttondown"></span><dl> <dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt> </dl> | El usuario ha colocado el cursor sobre la ventana secundaria y ha hecho clic en el botón primario del mouse.<br/> HIWORD (*wParam*) no está definido.<br/> *lParam* es la coordenada x del cursor es la palabra de orden inferior y la coordenada y del cursor es la palabra de orden superior.<br/>                                                                                                       |
| <span id="WM_MBUTTONDOWN"></span><span id="wm_mbuttondown"></span><dl> <dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt> </dl> | El usuario ha colocado el cursor sobre la ventana secundaria y ha hecho clic en el botón central del mouse.<br/> HIWORD (*wParam*) no está definido.<br/> *lParam* es la coordenada x del cursor es la palabra de orden inferior y la coordenada y del cursor es la palabra de orden superior.<br/>                                                                                                     |
| <span id="WM_RBUTTONDOWN"></span><span id="wm_rbuttondown"></span><dl> <dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt> </dl> | El usuario ha colocado el cursor sobre la ventana secundaria y ha hecho clic con el botón secundario del mouse.<br/> HIWORD (*wParam*) no está definido.<br/> *lParam* es la coordenada x del cursor es la palabra de orden inferior y la coordenada y del cursor es la palabra de orden superior.<br/>                                                                                                      |
| <span id="WM_XBUTTONDOWN"></span><span id="wm_xbuttondown"></span><dl> <dt>**WM_XBUTTONDOWN**</dt> <dt>0x020B</dt> </dl> | El usuario ha colocado el cursor sobre la ventana secundaria y ha hecho clic en el primer o el segundo botón X.<br/> HIWORD (*wParam*) indica el botón que se presionó. Este parámetro puede ser uno de los siguientes valores: XBUTTON1 o XBUTTON2.<br/> *lParam* es la coordenada x del cursor es la palabra de orden inferior y la coordenada y del cursor es la palabra de orden superior.<br/> |
| <span id="WM_POINTERDOWN"></span><span id="wm_pointerdown"></span><dl> <dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt> </dl> | Un puntero ha hecho contacto con la ventana secundaria.<br/> HIWORD (*wParam*) contiene el identificador del puntero que generó el evento [**WM_POINTERDOWN**](wm-pointerdown.md) .<br/>                                                                                                                                                                                            |



 

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

Si la aplicación procesa este mensaje, devuelve cero.

Si la aplicación no procesa este mensaje, llama a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Observaciones

Este mensaje también se envía a todas las ventanas antecesoras de la ventana secundaria, incluida la ventana de nivel superior.

Todas las ventanas secundarias, excepto las que tienen el estilo de ventana extendido **WS_EX_NOPARENTNOTIFY** , envían este mensaje a sus ventanas principales. De forma predeterminada, las ventanas secundarias de un cuadro de diálogo tienen el estilo de **WS_EX_NOPARENTNOTIFY** , a menos que se llame a la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) para crear la ventana secundaria sin este estilo.

Esta notificación proporciona a las ventanas antecesoras de la ventana secundaria una oportunidad para examinar la información del puntero y, si es necesario, capturar el puntero mediante las funciones de captura de puntero.

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

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM_CREATE**](../winmsg/wm-create.md)
</dt> <dt>

[**WM_DESTROY**](../winmsg/wm-destroy.md)
</dt> <dt>

[**WM_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md)
</dt> <dt>

[**WM_MBUTTONDOWN**](../inputdev/wm-mbuttondown.md)
</dt> <dt>

[**WM_RBUTTONDOWN**](../inputdev/wm-rbuttondown.md)
</dt> <dt>

[**WM_XBUTTONDOWN**](../inputdev/wm-xbuttondown.md)
</dt> </dl>

 

