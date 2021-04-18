---
description: El método ActivateWindow ajusta el tamaño de la ventana según los requisitos de la clase derivada.
ms.assetid: 39e23080-e4ae-46d5-bb3f-306c92bbfe14
title: Método CBaseWindow. ActivateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.ActivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f747f108bb6c7e42e90a0ff8503ec59a83c59699
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680653"
---
# <a name="cbasewindowactivatewindow-method"></a>CBaseWindow. ActivateWindow, método

El `ActivateWindow` método ajusta el tamaño de la ventana según los requisitos de la clase derivada.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT ActivateWindow();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                              |
|-----------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | La ventana ya estaba activada.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Correcto.<br/>                      |



 

## <a name="remarks"></a>Observaciones

Estos métodos llaman al método [**CBaseWindow:: GetDefaultRect**](cbasewindow-getdefaultrect.md) para determinar el tamaño de la ventana. La clase derivada debe invalidar **GetDefaultRect** para devolver el tamaño de las imágenes que se van a mostrar.

Si la ventana ya está activa, al llamar a `ActivateWindow` se mueve la ventana a la parte superior del orden Z, pero no se cambia el tamaño de la ventana. Lo mismo sucede si la ventana tiene un elemento primario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




