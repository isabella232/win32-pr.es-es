---
description: El método OutputPin recupera un puntero al pin de salida del filtro.
ms.assetid: 8c8c125e-553d-43c5-bc63-a0c7d5b01260
title: Método CTransInPlaceFilter. OutputPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.OutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4e74708062d66c8678af9541df762103ae36537
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680201"
---
# <a name="ctransinplacefilteroutputpin-method"></a>CTransInPlaceFilter. OutputPin, método

El `OutputPin` método recupera un puntero a la clavija de salida del filtro.

## <a name="syntax"></a>Sintaxis


```C++
CTransInPlaceOutputPin* OutputPin();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la variable miembro [**CTransformFilter:: m \_ pOutput**](ctransformfilter-m-poutput.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>TRANSip. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




