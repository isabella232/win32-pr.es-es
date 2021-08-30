---
description: El método InputPin recupera un puntero al pin de entrada del filtro.
ms.assetid: 533a962e-225d-4f10-a9c3-1464bea512ba
title: Método CTransInPlaceFilter.InputPin (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.InputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e70e91780ba1c0d1e1a3d204a6d99826e80a2fe23cbac4125d0b6300e4fdf005
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083895"
---
# <a name="ctransinplacefilterinputpin-method"></a>Método CTransInPlaceFilter.InputPin

El `InputPin` método recupera un puntero a la patilla de entrada del filtro.

## <a name="syntax"></a>Sintaxis


```C++
CTransInPlaceInputPin* InputPin();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la variable [**miembro CTransformFilter::m \_ pInput.**](ctransformfilter-m-pinput.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransInPlaceFilter (clase)**](ctransinplacefilter.md)
</dt> </dl>

 

 




