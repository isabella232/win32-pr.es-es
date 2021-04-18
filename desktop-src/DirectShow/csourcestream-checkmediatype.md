---
description: 'El método CheckMediaType determina si el PIN acepta un tipo de medio específico. Este método implementa el método CBasePin:: CheckMediaType virtual puro.'
ms.assetid: 3db7c74c-a6aa-4b49-b2a5-9bf8db35fd7e
title: CSourceStream. CheckMediaType (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f8b6c18613f5c187fc637febd08b74260a1e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660723"
---
# <a name="csourcestreamcheckmediatype-method"></a>CSourceStream. CheckMediaType, método

El `CheckMediaType` método determina si el PIN acepta un tipo de medio específico. Este método implementa el método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) virtual puro.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaType* 
</dt> <dd>

Puntero a un objeto [**CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                            | Descripción                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Este pin es compatible con este tipo de medio.<br/>        |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | El PIN no admite este tipo de medio.<br/> |



 

## <a name="remarks"></a>Observaciones

De forma predeterminada, el PIN admite un solo tipo de medio. Este método recupera el tipo admitido mediante una llamada a la versión de un solo parámetro del método [**CSourceStream:: GetMediaType**](csourcestream-getmediatype.md) y lo compara con el tipo propuesto. Si el PIN admite más de un tipo de medio, Invalide este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




