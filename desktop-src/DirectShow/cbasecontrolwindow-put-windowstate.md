---
description: El \_ método de WindowState Put establece el estado de la ventana.
ms.assetid: 0d22fa84-17bc-4228-b86e-d31857156802
title: Método CBaseControlWindow.put_WindowState (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1944e9bd39816cd1f022296b69fdac60d0779f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661341"
---
# <a name="cbasecontrolwindowput_windowstate-method"></a>CBaseControlWindow. put ( \_ método de WindowState)

El `put_WindowState` método establece el estado de la ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_WindowState(
   long WindowState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*WindowState* 
</dt> <dd>

Nuevo estado de ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro toma los mismos parámetros que la función **ShowWindow** de Microsoft Win32 (por ejemplo, WS \_ SHOWNORMAL, WS \_ SHOWMINNOACTIVATE y WS \_ SHOWMAXIMIZED).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




