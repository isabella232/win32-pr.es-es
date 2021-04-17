---
description: El método PossiblyEatMessage reenvía los mensajes de teclado y del mouse a la ventana de purga de mensajes.
ms.assetid: 8e344c5d-2f94-454f-89b7-45c539b6e833
title: Método CBaseControlWindow. PossiblyEatMessage (Ctlutil. h)
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
ms.openlocfilehash: 9bfadcfbbd6833d8f3e9b65bd39d0cdbef4a006e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660468"
---
# <a name="cbasecontrolwindowpossiblyeatmessage-method"></a>CBaseControlWindow. PossiblyEatMessage, método

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

Segundo parámetro del mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el mensaje se reenvió a la ventana o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

La ventana de purga de mensajes es una ventana designada para recibir determinados mensajes del mouse y del teclado. Inicialmente, la ventana es **null**; se puede establecer llamando a [**CBaseControlWindow::p UT \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md).

Si la ventana de purga de mensajes no es **null**, `PossiblyEatMessage` envía los mensajes siguientes a esa ventana:

-   carácter de WM \_
-   DEADCHAR de WM \_
-   KEYDOWN de WM \_
-   KEYUP de WM \_
-   LBUTTONDBLCLK de WM \_
-   LBUTTONDOWN de WM \_
-   LBUTTONUP de WM \_
-   MBUTTONDBLCLK de WM \_
-   MBUTTONDOWN de WM \_
-   MBUTTONUP de WM \_
-   MOUSEACTIVATE de WM \_
-   MOUSEMOVE de WM \_
-   NCLBUTTONDBLCLK de WM \_
-   NCLBUTTONDOWN de WM \_
-   NCLBUTTONUP de WM \_
-   NCMBUTTONDBLCLK de WM \_
-   NCMBUTTONDOWN de WM \_
-   NCMBUTTONUP de WM \_
-   NCMOUSEMOVE de WM \_
-   NCRBUTTONDBLCLK de WM \_
-   NCRBUTTONDOWN de WM \_
-   NCRBUTTONUP de WM \_
-   RBUTTONDBLCLK de WM \_
-   RBUTTONDOWN de WM \_
-   RBUTTONUP de WM \_
-   SYSCHAR de WM \_
-   SYSDEADCHAR de WM \_
-   SYSKEYDOWN de WM \_
-   SYSKEYUP de WM \_

Omite otros mensajes. Si la ventana de purga de mensajes es **null**, el método omite todos los mensajes de ventana. El método devuelve **true** si envía el mensaje o **false** en caso contrario. La clase **CBaseWindow** llama a este método cuando recibe un mensaje de ventana.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




