---
description: 'Método CTransformFilter.GetMediaType: el método GetMediaType recupera un tipo de medio preferido para el pin de salida.'
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: Método CTransformFilter.GetMediaType (Transfrm.h)
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
ms.openlocfilehash: 6415b8e3d8ae4e292b7e2592b123120927081ea8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095123"
---
# <a name="ctransformfiltergetmediatype-method"></a>Método CTransformFilter.GetMediaType

El `GetMediaType` método recupera un tipo de medio preferido para el pin de salida.

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

Puntero a un [**objeto CMediaType**](cmediatype.md) que recibe el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                            | Descripción                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Correcto.<br/>              |
| <dl> <dt>**VFW \_ S \_ NO \_ MORE \_ ITEMS**</dt> </dl> | Índice fuera del intervalo.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Índice menor que cero.<br/> |



 

## <a name="remarks"></a>Comentarios

El método [**CTransformOutputPin::GetMediaType**](ctransformoutputpin-getmediatype.md) del pin de salida llama a este método. La clase derivada debe implementar este método. Para obtener más información, [**vea CBasePin::GetMediaType**](cbasepin-getmediatype.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




