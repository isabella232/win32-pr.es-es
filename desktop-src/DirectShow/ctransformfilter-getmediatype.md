---
description: El método GetMediaType recupera un tipo de medio preferido para el PIN de salida.
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: Método CTransformFilter. GetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba751e291a1ffa8e030be7e77cfd456956718baa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661051"
---
# <a name="ctransformfiltergetmediatype-method"></a>CTransformFilter. GetMediaType, método

El `GetMediaType` método recupera un tipo de medio preferido para el PIN de salida.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
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



| Código devuelto                                                                                            | Descripción                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                   | Correcto.<br/>              |
| <dl> <dt>**VFW \_ S \_ no hay \_ más \_ elementos**</dt> </dl> | Índice fuera del intervalo.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Índice inferior a cero.<br/> |



 

## <a name="remarks"></a>Observaciones

El método [**CTransformOutputPin:: GetMediaType**](ctransformoutputpin-getmediatype.md) del PIN de salida llama a este método. La clase derivada debe implementar este método. Para obtener más información, vea [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




