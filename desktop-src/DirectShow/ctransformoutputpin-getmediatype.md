---
description: El método GetMediaType recupera un tipo de medio preferido, por valor de índice.
ms.assetid: d106e6d1-66ff-4460-9ea2-c93f16116cf4
title: Método CTransformOutputPin. GetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e52a5bc3b6a2b931a8592372e2ef636863c50ef6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680744"
---
# <a name="ctransformoutputpingetmediatype-method"></a>CTransformOutputPin. GetMediaType, método

El `GetMediaType` método recupera un tipo de medio preferido, por valor de índice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMediaType(
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

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                            | Descripción                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                   | Correcto<br/>            |
| <dl> <dt>**VFW \_ S \_ no hay \_ más \_ elementos**</dt> </dl> | Índice fuera del intervalo<br/> |



 

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) . Si el PIN de entrada del filtro no está conectado, el método devuelve VFW \_ s \_ no hay \_ más \_ elementos. De lo contrario, llama al método [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) del filtro para recuperar el tipo de medio. El método **CTransformFilter:: GetMediaType** es virtual puro; la clase derivada del filtro debe reemplazarla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




