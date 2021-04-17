---
description: El método NotifyOwnerMessage pasa mensajes específicos a la ventana de vídeo.
ms.assetid: 8b27281a-5b8a-46c3-aa66-390d4496f30e
title: Método CBaseControlWindow. NotifyOwnerMessage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.NotifyOwnerMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9073d37987404849ba8aa3acbda9919df840b410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661386"
---
# <a name="cbasecontrolwindownotifyownermessage-method"></a>CBaseControlWindow. NotifyOwnerMessage, método

El `NotifyOwnerMessage` método pasa mensajes específicos a la ventana de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NotifyOwnerMessage(
   long     hwnd,
   long     uMsg,
   LONG_PTR wParam,
   LONG_PTR lParam
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador* 
</dt> <dd>

Identificador de la ventana de vídeo.

</dd> <dt>

*uMsg* 
</dt> <dd>

Detalles del mensaje.

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

NO devuelve ningún \_ error.

## <a name="remarks"></a>Observaciones

Cuando la ventana de vídeo es un elemento secundario de otra ventana, no recibe ciertos mensajes de ventana de nivel superior. Estos mensajes pueden ser valiosos para un representador, porque podrían afectar a su comportamiento. `NotifyOwnerMessage` pasa cualquiera de los mensajes siguientes a la ventana de vídeo.

-   ACTIVATEAPP de WM \_
-   DEVMODECHANGE de WM \_
-   DISPLAYCHANGE de WM \_
-   PALETTECHANGED de WM \_
-   PALETTEISCHANGING de WM \_
-   QUERYNEWPALETTE de WM \_
-   SYSCOLORCHANGE de WM \_

Puede solicitar que el distribuidor de complementos de [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (PID) haga que una ventana se convierta en un elemento secundario de otra ventana. Cuando esto ocurre, el PID buscará determinados mensajes que puedan enviarse a la ventana propietaria. A continuación, el PID reenviará esos mensajes a la ventana de propiedad. El procesamiento predeterminado de los mensajes es enviarlos al procedimiento de ventana propiedad de forma sincrónica mediante una llamada a la función **SendMessage** de Win32.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




