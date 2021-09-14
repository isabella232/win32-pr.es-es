---
description: El método GetRestorePosition recupera la posición en la que se restaurará la ventana cuando no esté maximizada ni minimizada.
ms.assetid: 5f129be3-c4d8-4583-bbc8-870e0bcafd80
title: Método CBaseControlWindow.GetRestorePosition (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetRestorePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f922a97f69f4dae03d4e61a54bd99c52d69a984a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974001"
---
# <a name="cbasecontrolwindowgetrestoreposition-method"></a>Método CBaseControlWindow.GetRestorePosition

El método recupera la posición en la que se restaurará la ventana cuando `GetRestorePosition` no esté maximizada ni minimizada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRestorePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pLeft* 
</dt> <dd>

Puntero al valor de la coordenada situada más a la izquierda.

</dd> <dt>

*pTop* 
</dt> <dd>

Puntero al valor de la parte superior de la ventana.

</dd> <dt>

*pWidth* 
</dt> <dd>

Puntero al valor para el ancho de la ventana.

</dd> <dt>

*pHeight* 
</dt> <dd>

Puntero al valor para el alto de la ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

Esto es igual que los valores devueltos por la función [**CBaseControlWindow::GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) cuando la ventana no se maximiza ni minimiza.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




