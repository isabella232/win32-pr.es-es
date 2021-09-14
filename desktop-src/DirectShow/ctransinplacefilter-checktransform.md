---
description: El método CheckTransform comprueba si un tipo de medio de entrada es compatible con un tipo de medio de salida. Este método invalida el método CTransformFilter::CheckTransform.
ms.assetid: d0953014-4a49-4738-a449-c247396a6794
title: Método CTransInPlaceFilter.CheckTransform (Transip.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255309"
---
# <a name="ctransinplacefilterchecktransform-method"></a>Método CTransInPlaceFilter.CheckTransform

El `CheckTransform` método comprueba si un tipo de medio de entrada es compatible con un tipo de medio de salida. Este método invalida el [**método CTransformFilter::CheckTransform.**](ctransformfilter-checktransform.md)

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

Puntero a un [**objeto CMediaType**](cmediatype.md) que especifica el tipo de entrada.

</dd> <dt>

*mtOut* 
</dt> <dd>

Puntero a un **objeto CMediaType** que especifica el tipo de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

El **filtro CTransInPlace** nunca llama a `CheckTransform` . En su lugar, todas las conexiones de pin usan [**CTransformFilter::CheckInputType para**](ctransformfilter-checkinputtype.md) comprobar el tipo de medio, con la suposición de que los tipos de entrada y salida siempre coinciden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransInPlaceFilter (clase)**](ctransinplacefilter.md)
</dt> </dl>

 

 




