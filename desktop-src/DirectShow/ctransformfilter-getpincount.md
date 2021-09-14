---
description: El método GetPinCount recupera el número de pines del filtro.
ms.assetid: 29039ada-fccd-4890-b36b-3dd5c0bbdc3e
title: Método CTransformFilter.GetPinCount (Transfrm.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246675"
---
# <a name="ctransformfiltergetpincount-method"></a>Método CTransformFilter.GetPinCount

El `GetPinCount` método recupera el número de pines del filtro.

## <a name="syntax"></a>Sintaxis


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve 2.

## <a name="remarks"></a>Observaciones

Este método invalida el [**método CBaseFilter::GetPinCount.**](cbasefilter-getpincount.md) La **clase CTransformFilter** admite exactamente un pin de entrada y un pin de salida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




