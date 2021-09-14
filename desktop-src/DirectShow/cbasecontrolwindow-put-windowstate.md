---
description: El método put \_ WindowState establece el estado de la ventana.
ms.assetid: 0d22fa84-17bc-4228-b86e-d31857156802
title: CBaseControlWindow.put_WindowState método (Ctlutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173857"
---
# <a name="cbasecontrolwindowput_windowstate-method"></a>CBaseControlWindow.put \_ (método WindowState)

El `put_WindowState` método establece el estado de la ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_WindowState(
   long WindowState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Windowstate* 
</dt> <dd>

Nuevo estado de la ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

Esta función miembro toma los mismos parámetros que la función **ShowWindow** de Microsoft Win32 (por ejemplo, WS \_ SHOWNORMAL, WS \_ SHOWMINNOACTIVATE y WS \_ SHOWMAXIMIZED).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




