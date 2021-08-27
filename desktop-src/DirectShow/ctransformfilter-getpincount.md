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
ms.openlocfilehash: ac9269149d7f2bbc95e811515f70aa279a4aafd8cf34b2d5077ed69019b86c2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953604"
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

## <a name="remarks"></a>Comentarios

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

 

 




