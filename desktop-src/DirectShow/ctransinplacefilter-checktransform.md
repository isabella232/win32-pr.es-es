---
description: 'El método CheckTransform comprueba si un tipo de medio de entrada es compatible con un tipo de medio de salida. Este método invalida el método CTransformFilter:: CheckTransform.'
ms.assetid: d0953014-4a49-4738-a449-c247396a6794
title: Método CTransInPlaceFilter. CheckTransform (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a80132723be0b70f2c4afe93306d7f581b7734c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681105"
---
# <a name="ctransinplacefilterchecktransform-method"></a>CTransInPlaceFilter. CheckTransform, método

El `CheckTransform` método comprueba si un tipo de medio de entrada es compatible con un tipo de medio de salida. Este método invalida el método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mtIn* 
</dt> <dd>

Puntero a un objeto [**CMediaType**](cmediatype.md) que especifica el tipo de entrada.

</dd> <dt>

*mtOut* 
</dt> <dd>

Puntero a un objeto **CMediaType** que especifica el tipo de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

El filtro **CTransInPlace** nunca llama a `CheckTransform` . En su lugar, todas las conexiones de PIN usan [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) para comprobar el tipo de medio, con la suposición de que los tipos de entrada y salida siempre coinciden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>TRANSip. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




