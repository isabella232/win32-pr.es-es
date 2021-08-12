---
description: El método OnReceiveMessage controla los mensajes de ventana.
ms.assetid: 0f074f9b-00e5-42ff-a491-020d441acad1
title: Método CBaseWindow.OnReceiveMessage (Winutil.h)
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
ms.openlocfilehash: 1a5dbfb84edef1f5257cfda8cae08d27b219909f47a7d88fd29580ae12e48b3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657968"
---
# <a name="cbasewindowonreceivemessage-method"></a>Método CBaseWindow.OnReceiveMessage

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

*Hwnd* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificador del mensaje.

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

Devuelve 0 si se procesó el mensaje o 1 si no se procesó el mensaje.

## <a name="remarks"></a>Observaciones

La clase base controla los mensajes siguientes:

-   WM \_ CLOSE
-   WM \_ MOVE
-   PALETA \_ WMCHANGED
-   WM \_ QUERYNEWPALETTE
-   TAMAÑO \_ WM
-   WM \_ SYSCOLORCHANGE

Una clase derivada puede invalidar este método para controlar otros mensajes. La clase derivada debe llamar al método de clase base para controlar los mensajes que la clase derivada omite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




