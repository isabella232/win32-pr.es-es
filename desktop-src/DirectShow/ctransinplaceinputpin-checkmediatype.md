---
description: 'Método CTransInPlaceInputPin.CheckMediaType: el método CheckMediaType determina si el pin acepta un tipo de medio específico.'
ms.assetid: 2d5f784a-8970-487d-94ef-d96d04f8eb2e
title: Método CTransInPlaceInputPin.CheckMediaType (Transip.h)
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
ms.openlocfilehash: 91a1889e9c8a4060b734449df9f73474c16d1aec09d6534de048359ced156958
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654854"
---
# <a name="ctransinplaceinputpincheckmediatype-method"></a>Método CTransInPlaceInputPin.CheckMediaType

El `CheckMediaType` método determina si el pin acepta un tipo de medio específico.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntero a un [**objeto CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si el tipo de medio propuesto es aceptable. De lo contrario, devuelve S \_ FALSE o un código de error.

## <a name="remarks"></a>Observaciones

Este método invalida el [**método CTransformInputPin::CheckMediaType.**](ctransforminputpin-checkmediatype.md) Llama al método [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) del filtro para comprobar el tipo de entrada. Si el pin de salida está conectado, este método también llama al método [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el pin de entrada de nivel inferior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransInPlaceInputPin (clase)**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




