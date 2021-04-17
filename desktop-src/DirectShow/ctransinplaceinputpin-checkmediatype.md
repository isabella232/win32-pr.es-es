---
description: El método CheckMediaType determina si el PIN acepta un tipo de medio específico.
ms.assetid: 2d5f784a-8970-487d-94ef-d96d04f8eb2e
title: Método CTransInPlaceInputPin. CheckMediaType (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22f271759bc0ade6b820aed2039bbc16a2cf4a31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660365"
---
# <a name="ctransinplaceinputpincheckmediatype-method"></a>CTransInPlaceInputPin. CheckMediaType, método

El `CheckMediaType` método determina si el PIN acepta un tipo de medio específico.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*p.p.* 
</dt> <dd>

Puntero a un objeto [**CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si el tipo de medio propuesto es aceptable. De lo contrario, devuelve S \_ false o un código de error.

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CTransformInputPin:: CheckMediaType**](ctransforminputpin-checkmediatype.md) . Llama al método [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) del filtro para comprobar el tipo de entrada. Si el PIN de salida está conectado, este método también llama al método [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el PIN de entrada de nivel inferior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>TRANSip. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




