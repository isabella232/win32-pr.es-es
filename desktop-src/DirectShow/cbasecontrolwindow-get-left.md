---
description: El \_ método get Left recupera la coordenada de la ventana izquierda actual.
ms.assetid: 9ee71bd3-1ff5-4574-8dcd-5ba6490d9785
title: Método CBaseControlWindow.get_Left (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04f586cede24f8ff2017ae4004fc45c584a57f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671422"
---
# <a name="cbasecontrolwindowget_left-method"></a>CBaseControlWindow. Get \_ left (método)

El `get_Left` método recupera la coordenada de la ventana izquierda actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Left(
   long *pLeft
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pLeft* 
</dt> <dd>

Puntero a la coordenada izquierda, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

La ventana tiene una posición en el escritorio. Esta posición se expresa en píxeles por cuatro coordenadas (izquierda, superior, derecha e inferior). Las interfaces automatizadas por OLE suelen expresar esta posición a la izquierda, la parte superior, el ancho y el alto. Esta es la Convención usada en DirectShow. Todas las coordenadas se expresan en píxeles y, al cambiar cualquier coordenada, la ventana se actualizará inmediatamente.

Al establecer las coordenadas izquierda o superior, la ventana se mueve a la izquierda y hacia arriba, respectivamente; estas coordenadas no tienen ningún efecto en el ancho y el alto de la ventana. Del mismo modo, establecer el ancho y el alto no tiene ningún efecto en las coordenadas izquierda y superior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




