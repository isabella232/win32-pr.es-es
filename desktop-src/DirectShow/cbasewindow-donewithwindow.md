---
description: El método DoneWithWindow destruye la ventana.
ms.assetid: 03c97884-7d91-4b59-b867-dda231d2a184
title: Método CBaseWindow. DoneWithWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoneWithWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc31e893a4015aa8b4356d265ca4065ee336c3ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660230"
---
# <a name="cbasewindowdonewithwindow-method"></a>CBaseWindow. DoneWithWindow, método

El `DoneWithWindow` método destruye la ventana.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT DoneWithWindow();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Llame a este método desde el método de destructor del objeto derivado.

Si se llama a este método desde el mismo subproceso que creó la ventana, el método realiza las acciones siguientes:

-   Llama al método [**CBaseWindow:: InactivateWindow**](cbasewindow-inactivatewindow.md) , que desactiva la ventana.
-   Llama al método [**CBaseWindow:: UninitialiseWindow**](cbasewindow-uninitialisewindow.md) , que libera los recursos utilizados por la ventana.
-   Destruye la ventana.

Si el subproceso que realiza la llamada `DoneWithWindow` no es el subproceso que creó la ventana, el método envía un mensaje privado "Destroy" a la ventana. Cuando la ventana recibe este mensaje, llama a `DoneWithWindow` sí mismo. (Si [**CBaseWindow:: m \_ BDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) es **true**, la ventana envía el mensaje).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




