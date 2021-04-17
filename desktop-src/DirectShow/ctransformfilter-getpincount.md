---
description: El método GetPinCount recupera el número de clavijas en el filtro.
ms.assetid: 29039ada-fccd-4890-b36b-3dd5c0bbdc3e
title: Método CTransformFilter. GetPinCount (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba1d2046bf7be31a9c0d3f3d43b13aeeffd1f76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661036"
---
# <a name="ctransformfiltergetpincount-method"></a>CTransformFilter. GetPinCount, método

El `GetPinCount` método recupera el número de clavijas en el filtro.

## <a name="syntax"></a>Sintaxis


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve 2.

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CBaseFilter:: GetPinCount**](cbasefilter-getpincount.md) . La clase **CTransformFilter** admite exactamente un PIN de entrada y un PIN de salida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




