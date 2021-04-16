---
description: El método ResetEndOfStream restablece las marcas de fin de secuencia.
ms.assetid: 80f6d49b-a825-4c3c-b693-7b1d9298f541
title: Método CBaseRenderer. ResetEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0269ee2dfafea9265b5eeb82caa4c39f8d91320c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671730"
---
# <a name="cbaserendererresetendofstream-method"></a>CBaseRenderer. ResetEndOfStream, método

El `ResetEndOfStream` método restablece las marcas de fin de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT ResetEndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Este método borra la condición de final de secuencia anterior. En ese momento, el filtro puede recibir datos nuevos. Los métodos [**CBaseRenderer:: Stop**](cbaserenderer-stop.md) y [**CBaseRenderer:: BeginFlush**](cbaserenderer-beginflush.md) llaman a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




