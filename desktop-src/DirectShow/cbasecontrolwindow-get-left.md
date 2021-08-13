---
description: El método get \_ Left recupera la coordenada de la ventana izquierda actual.
ms.assetid: 9ee71bd3-1ff5-4574-8dcd-5ba6490d9785
title: CBaseControlWindow.get_Left método (Ctlutil.h)
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
ms.openlocfilehash: 9317c1c061fe8528903bdd2e7129d0cfdc9e6dd67b9722841360d131e15cfb10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660528"
---
# <a name="cbasecontrolwindowget_left-method"></a>CBaseControlWindow.get \_ Left (método)

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

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

La ventana tiene una posición en el escritorio. Esta posición se expresa en píxeles mediante cuatro coordenadas (izquierda, superior, derecha e inferior). Las interfaces automatizadas por OLE suelen expresar esta posición a través de la izquierda, la parte superior, el ancho y el alto; esta es la convención usada en DirectShow. Todas las coordenadas se expresan en píxeles y al cambiar cualquier coordenada se actualizará la ventana inmediatamente.

Al establecer las coordenadas izquierda o superior, la ventana se mueve hacia la izquierda y hacia arriba, respectivamente; estas coordenadas no tienen ningún efecto en el ancho y el alto de la ventana. Del mismo modo, establecer el ancho y el alto no tiene ningún efecto en las coordenadas izquierda y superior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




