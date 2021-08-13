---
description: El método ActivateWindow puede cambiar el tamaño de la ventana según los requisitos de la clase derivada.
ms.assetid: 39e23080-e4ae-46d5-bb3f-306c92bbfe14
title: Método CBaseWindow.ActivateWindow (Winutil.h)
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
ms.openlocfilehash: e00c3ccc43e2583ce8664e62967a22f753148cfa271dd1995e2374c2bfa53c71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658249"
---
# <a name="cbasewindowactivatewindow-method"></a>Método CBaseWindow.ActivateWindow

El `ActivateWindow` método puede cambiar el tamaño de la ventana según los requisitos de la clase derivada.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT ActivateWindow();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                              |
|-----------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | La ventana ya estaba activada.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>                      |



 

## <a name="remarks"></a>Observaciones

Estos métodos llaman [**al método CBaseWindow::GetDefaultRect**](cbasewindow-getdefaultrect.md) para determinar el tamaño de la ventana. La clase derivada debe invalidar **GetDefaultRect para** devolver el tamaño de las imágenes que se mostrarán.

Si la ventana ya está activa, la llamada a mueve la ventana a la parte superior del orden Z, pero no cambia `ActivateWindow` el tamaño de la ventana. Lo mismo sucede si la ventana tiene un elemento primario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




