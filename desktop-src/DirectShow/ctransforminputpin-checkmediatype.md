---
description: 'Método CTransformInputPin.CheckMediaType: el método CheckMediaType determina si el pin acepta un tipo de medio específico.'
ms.assetid: e09a4a3e-ac39-4d0e-9e8c-3e8f18057d0d
title: Método CTransformInputPin.CheckMediaType (Transfrm.h)
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
ms.openlocfilehash: c775618c9fe30de6171919d5b8bc8a80ea81d3a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085003"
---
# <a name="ctransforminputpincheckmediatype-method"></a>Método CTransformInputPin.CheckMediaType

El `CheckMediaType` método determina si el pin acepta un tipo de medio específico.

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

Puntero a un [**objeto CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK u otro valor **HRESULT.**

## <a name="remarks"></a>Comentarios

Este método implementa el método [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) virtual puro. Llama al método [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) del filtro, que también es virtual puro. La clase derivada del filtro debe implementar **CheckInputType para** determinar si un tipo de entrada determinado es aceptable.

Si el pin de salida del filtro está conectado, este método también llama al método [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) del filtro para determinar si el tipo de entrada es compatible con el tipo de salida. El **método CheckTransform** también es virtual puro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




