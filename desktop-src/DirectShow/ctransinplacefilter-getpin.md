---
description: 'Método CTransInPlaceFilter.GetPin: el método GetPin recupera un pin.'
ms.assetid: d8e4973b-2af4-4141-ab2e-ea2159cd51be
title: Método CTransInPlaceFilter.GetPin (Transip.h)
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
ms.openlocfilehash: 1075f2a14c58b085b73f2e4283458286c118a7ae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084773"
---
# <a name="ctransinplacefiltergetpin-method"></a>Método CTransInPlaceFilter.GetPin

El `GetPin` método recupera un pin.

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

Número del pin especificado, indexado a partir de cero. En este filtro, el pin 0 es el pin de entrada y el pin 1 es el pin de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero al objeto [**CBasePin**](cbasepin.md) que implementa el pin o **NULL** si se produce un error en el método.

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CTransformFilter::GetPin.**](ctransformfilter-getpin.md) La primera vez que se llama al método, crea ambos pines.

Este método no incrementa el recuento de referencias en el pin devuelto, por lo que el pin devuelto no tiene un recuento de referencias pendiente. Si el autor de la llamada necesita mantener una referencia en el pin, debe llamar al método **IUnknown::AddRef** en el pin.

Si el filtro usa los pines [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) y [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) predeterminados, probablemente no necesite invalidar este método. Sin embargo, si el filtro usa pines que extienden esas clases, debe invalidar este método para crear pins de ese tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransInPlaceFilter (clase)**](ctransinplacefilter.md)
</dt> </dl>

 

 




