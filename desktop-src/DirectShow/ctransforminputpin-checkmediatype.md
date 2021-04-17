---
description: El método CheckMediaType determina si el PIN acepta un tipo de medio específico.
ms.assetid: e09a4a3e-ac39-4d0e-9e8c-3e8f18057d0d
title: Método CTransformInputPin. CheckMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6841370795a3131cdbcc95a3bab160be2011c600
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680343"
---
# <a name="ctransforminputpincheckmediatype-method"></a>CTransformInputPin. CheckMediaType, método

El `CheckMediaType` método determina si el PIN acepta un tipo de medio específico.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mtIn* 
</dt> <dd>

Puntero a un objeto [**CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK u otro valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método implementa el método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) virtual puro. Llama al método [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) del filtro, que también es virtual puro. La clase derivada del filtro debe implementar **CheckInputType** para determinar si un tipo de entrada determinado es aceptable.

Si el PIN de salida del filtro está conectado, este método también llama al método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) del filtro para determinar si el tipo de entrada es compatible con el tipo de salida. El método **CheckTransform** es también virtual puro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




