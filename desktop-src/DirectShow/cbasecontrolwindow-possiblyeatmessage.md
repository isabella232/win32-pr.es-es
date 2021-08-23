---
description: El método PossiblyEatMessage reenvía los mensajes del teclado y del mouse a la ventana de purga de mensajes.
ms.assetid: 8e344c5d-2f94-454f-89b7-45c539b6e833
title: Método CBaseControlWindow.PossiblyEatMessage (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 403fb4d170f9c3cf0b7d68d3ac6ce1fdcc9c81a14b1c76d74e67bb64d4d9cc8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017343"
---
# <a name="cbasecontrolwindowpossiblyeatmessage-method"></a>Método CBaseControlWindow.PossiblyEatMessage

El `PossiblyEatMessage` método reenvía los mensajes del teclado y del mouse a la ventana de purga de mensajes.

## <a name="syntax"></a>Sintaxis


```C++
BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uMsg* 
</dt> <dd>

Mensaje de ventana.

</dd> <dt>

*wParam* 
</dt> <dd>

Primer parámetro de mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

Segundo parámetro de mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si el mensaje se reenvía a la ventana o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

La ventana de purga de mensajes es una ventana designada para recibir determinados mensajes del mouse y del teclado. Inicialmente, la ventana es **NULL**; se puede establecer llamando a [**CBaseControlWindow::p ut \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md).

Si la ventana de purga de mensajes no es **NULL,** `PossiblyEatMessage` envía los mensajes siguientes a esa ventana:

-   WM \_ CHAR
-   WM \_ DEADCHAR
-   WM \_ KEYDOWN
-   WM \_ KEYUP
-   WM \_ LBUTTONDBLCLK
-   WM \_ LBUTTONDOWN
-   WM \_ LBUTTONUP
-   WM \_ MBUTTONDBLCLK
-   WM \_ MBUTTONDOWN
-   WM \_ MBUTTONUP
-   WM \_ MOUSEACTIVATE
-   WM \_ MOUSEMOVE
-   WM \_ NCLBUTTONDBLCLK
-   WM \_ NCLBUTTONDOWN
-   WM \_ NCLBUTTONUP
-   WM \_ NCMBUTTONDBLCLK
-   WM \_ NCMBUTTONDOWN
-   WM \_ NCMBUTTONUP
-   WM \_ NCMOUSEMOVE
-   WM \_ NCRBUTTONDBLCLK
-   WM \_ NCRBUTTONDOWN
-   WM \_ NCRBUTTONUP
-   WM \_ RBUTTONDBLCLK
-   WM \_ RBUTTONDOWN
-   WM \_ RBUTTONUP
-   WM \_ SYSCHAR
-   WM \_ SYSDEADCHAR
-   WM \_ SYSKEYDOWN
-   WM \_ SYSKEYUP

Omite otros mensajes. Si la ventana de purga de mensajes **es NULL,** el método omite todos los mensajes de la ventana. El método devuelve **TRUE si** publica el mensaje o **FALSE** en caso contrario. La **clase CBaseWindow** llama a este método cuando recibe un mensaje de ventana.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




