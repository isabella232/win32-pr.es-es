---
description: El método GetMediaType recupera un tipo de medio preferido, por valor de índice.
ms.assetid: 96f102b0-e2d1-49a1-84af-aa4622cae2a9
title: Método CBasePin. GetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c54c5cd769a8efa0c720c7050cca45b00b8209e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671803"
---
# <a name="cbasepingetmediatype-method"></a>CBasePin. GetMediaType, método

El `GetMediaType` método recupera un tipo de medio preferido, por valor de índice.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iPosition* 
</dt> <dd>

Valor de índice de base cero.

</dd> <dt>

*pMediaType* 
</dt> <dd>

Puntero a un objeto [**CMediaType**](cmediatype.md) que recibe el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los de la tabla siguiente.



| Código devuelto                                                                                            | Descripción                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                   | Correcto.<br/>              |
| <dl> <dt>**VFW \_ S \_ no hay \_ más \_ elementos**</dt> </dl> | Índice fuera del intervalo.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Índice inferior a cero.<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl>           | error inesperado.<br/>     |



 

## <a name="remarks"></a>Observaciones

En la lista de tipos de medios preferidos del PIN, este método devuelve el tipo con un valor de índice de *iPosition*. La clase [**CEnumMediaTypes**](cenummediatypes.md) llama a este método para enumerar los tipos de medios preferidos.

La clase base devuelve E \_ inesperada. Invalide este método en la clase derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




