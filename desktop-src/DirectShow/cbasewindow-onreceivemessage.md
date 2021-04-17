---
description: El método OnReceiveMessage controla los mensajes de ventana.
ms.assetid: 0f074f9b-00e5-42ff-a491-020d441acad1
title: Método CBaseWindow. OnReceiveMessage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: defef9a7ca24d6875eda508989615f308a2385b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660315"
---
# <a name="cbasewindowonreceivemessage-method"></a>CBaseWindow. OnReceiveMessage, método

El `OnReceiveMessage` método controla los mensajes de ventana.

## <a name="syntax"></a>Sintaxis


```C++
virtual LRESULT OnReceiveMessage(
   HWND   hwnd,
   INT    uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificador de mensaje.

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

Devuelve 0 si se procesó el mensaje o 1 si no se procesó el mensaje.

## <a name="remarks"></a>Observaciones

La clase base controla los siguientes mensajes:

-   cierre de WM \_
-   movimiento de WM \_
-   PALETTECHANGED de WM \_
-   QUERYNEWPALETTE de WM \_
-   tamaño de WM \_
-   SYSCOLORCHANGE de WM \_

Una clase derivada puede invalidar este método para controlar otros mensajes. La clase derivada debe llamar al método de clase base para controlar los mensajes que la clase derivada omite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




