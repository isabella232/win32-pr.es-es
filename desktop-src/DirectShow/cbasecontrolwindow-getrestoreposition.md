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
ms.openlocfilehash: 215b71d731227641df02716dd2b760f7e023bbec0c50bc66ac6d390ed87d002e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757615"
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

## <a name="remarks"></a>Comentarios

Esto es igual que los valores devueltos por la función [**CBaseControlWindow::GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) cuando la ventana no está maximizada ni minimizada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




