---
description: El método GetOwnerWindow recupera el identificador de la ventana propietaria, m \_ hwndOwner.
ms.assetid: fa576b42-b4a7-4374-8ba4-7d21e86d9d61
title: Método CBaseControlWindow. GetOwnerWindow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetOwnerWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e4d3811f85abd68bcd7d625dce0e9e8963be39a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660597"
---
# <a name="cbasecontrolwindowgetownerwindow-method"></a>CBaseControlWindow. GetOwnerWindow, método

El `GetOwnerWindow` método recupera el identificador de la ventana propietaria, **m \_ hwndOwner**.

## <a name="syntax"></a>Sintaxis


```C++
HWND GetOwnerWindow();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la ventana propietaria.

## <a name="remarks"></a>Observaciones

Recupera la ventana propietaria sin llamar al método de interfaz. Use esta función miembro en lugar de [**CBaseControlWindow:: get \_ Owner**](cbasecontrolwindow-get-owner.md), a menos que llame a esto externamente a través del método [**IVideoWindow:: get \_ Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




