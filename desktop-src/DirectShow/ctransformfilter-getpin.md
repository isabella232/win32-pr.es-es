---
description: 'Método CTransformFilter.GetPin: el método GetPin recupera un pin.'
ms.assetid: 5d278ef0-e5ce-439e-93b1-fec988c55854
title: Método CTransformFilter.GetPin (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e76cafce2ca5a9881b87d9248c144dc584971c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085083"
---
# <a name="ctransformfiltergetpin-method"></a>Método CTransformFilter.GetPin

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

Este método implementa el método [**CBaseFilter::GetPin**](cbasefilter-getpin.md) virtual puro. La primera vez que se llama al método, crea ambos pines.

Este método no incrementa el recuento de referencias en el pin devuelto, por lo que el pin devuelto no tiene un recuento de referencias pendiente. Si el autor de la llamada necesita mantener una referencia en el pin, debe llamar al método **IUnknown::AddRef** en el pin.

Si el filtro usa los pines [**CTransformInputPin**](ctransforminputpin.md) y [**CTransformOutputPin**](ctransformoutputpin.md) predeterminados, probablemente no necesite invalidar este método. Sin embargo, si el filtro usa pines que extienden esas clases, debe invalidar este método para crear pins de ese tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




