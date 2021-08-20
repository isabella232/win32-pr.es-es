---
description: El método NotifyOwnerMessage pasa mensajes específicos a la ventana de vídeo.
ms.assetid: 8b27281a-5b8a-46c3-aa66-390d4496f30e
title: Método CBaseControlWindow.NotifyOwnerMessage (Ctlutil.h)
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
ms.openlocfilehash: 35d71057027bd8fbd572dffd714f761ff101ba0de95dd42dcf058009b0cb1b04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526855"
---
# <a name="cbasecontrolwindownotifyownermessage-method"></a>Método CBaseControlWindow.NotifyOwnerMessage

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

*Hwnd* 
</dt> <dd>

Controle la ventana de vídeo.

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

Segundo parámetro de mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve NO \_ ERROR.

## <a name="remarks"></a>Comentarios

Cuando la ventana de vídeo es un elemento secundario de otra ventana, no recibe determinados mensajes de ventana de nivel superior. Estos mensajes pueden ser valiosos para un representador, ya que podrían afectar a su comportamiento. `NotifyOwnerMessage` pasa cualquiera de los mensajes siguientes a la ventana de vídeo.

-   WM \_ ACTIVATEAPP
-   WM \_ DEVMODECHANGE
-   WM \_ DISPLAYCHANGE
-   PALETA \_ WMCHANGED
-   PALETA \_ WMISCHANGING
-   WM \_ QUERYNEWPALETTE
-   WM \_ SYSCOLORCHANGE

Puede solicitar que el distribuidor del complemento [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (PID) haga que una ventana se convierta en un elemento secundario de otra ventana. Cuando esto sucede, el PID buscará determinados mensajes que podrían enviarse a la ventana propietaria. A continuación, el PID reenviará esos mensajes a la ventana de propiedad. El procesamiento predeterminado de los mensajes consiste en enviarlos al procedimiento de ventana propiedad de forma sincrónica mediante una llamada a la función **SendMessage de** Win32.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




