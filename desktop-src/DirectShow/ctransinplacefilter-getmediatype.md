---
description: 'Método CTransInPlaceFilter.GetMediaType: el método GetMediaType recupera un tipo de medio preferido para el pin de salida.'
ms.assetid: 1bc6c06d-f399-4b8a-81f2-7fffe4630236
title: Método CTransInPlaceFilter.GetMediaType (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a714d3dba30b3038d6c04ecedd51db4196a3c4d899d7c607dd12f9a068f8a803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079305"
---
# <a name="ctransinplacefiltergetmediatype-method"></a>Método CTransInPlaceFilter.GetMediaType

El `GetMediaType` método recupera un tipo de medio preferido para el pin de salida.

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

Puntero a un [**objeto CMediaType**](cmediatype.md) que recibe el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ UNEXPECTED.

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CTransformFilter::GetMediaType.**](ctransformfilter-getmediatype.md) En la **clase CTransInPlaceFilter,** cada pin llama al pin conectado opuesto para enumerar los tipos de medios preferidos. El pin de entrada llama al pin de entrada del filtro de bajada y el pin de salida llama al pin de salida del filtro ascendente. Por lo tanto, nunca se llama `GetMediaType` al método del filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransInPlaceFilter (clase)**](ctransinplacefilter.md)
</dt> </dl>

 

 




