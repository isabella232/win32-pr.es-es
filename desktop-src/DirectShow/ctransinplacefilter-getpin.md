---
description: El método GetPin recupera un PIN.
ms.assetid: d8e4973b-2af4-4141-ab2e-ea2159cd51be
title: Método CTransInPlaceFilter. GetPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae93b663af5427bc61367ae03a3abd6790b8634a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680813"
---
# <a name="ctransinplacefiltergetpin-method"></a>CTransInPlaceFilter. GetPin, método

El `GetPin` método recupera un PIN.

## <a name="syntax"></a>Sintaxis


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*n* 
</dt> <dd>

Número del PIN especificado, indizado desde cero. En este filtro, el pin 0 es el PIN de entrada y el pin 1 es el PIN de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero al objeto [**CBasePin**](cbasepin.md) que implementa el PIN, o **null** si se produce un error en el método.

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CTransformFilter:: GetPin**](ctransformfilter-getpin.md) . La primera vez que se llama al método, se crean ambos PIN.

Este método no incrementa el recuento de referencias en el PIN devuelto, por lo que el PIN devuelto no tiene un recuento de referencias pendiente. Si el autor de la llamada necesita mantener una referencia en el código PIN, debe llamar al método **IUnknown:: AddRef** en el código PIN.

Si el filtro usa los pin predeterminados [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) y [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) , probablemente no sea necesario invalidar este método. Sin embargo, si el filtro usa PIN que amplían esas clases, debe invalidar este método para crear los pin de ese tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>TRANSip. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




