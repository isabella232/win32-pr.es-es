---
description: El método CheckInputType comprueba si un tipo de medio especificado es aceptable para la entrada.
ms.assetid: 11f156f7-add2-45be-a0d3-05d21f596b89
title: Método CTransformFilter. CheckInputType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckInputType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63c48a0502ee074b0940f85386dca0619a3ad12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660301"
---
# <a name="ctransformfiltercheckinputtype-method"></a>CTransformFilter. CheckInputType, método

El `CheckInputType` método comprueba si un tipo de medio especificado es aceptable para la entrada.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CheckInputType(
   const CMediaType *mtIn
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mtIn* 
</dt> <dd>

Puntero a un objeto [**CMediaType**](cmediatype.md) que especifica el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                                | Descripción                              |
|------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                       | El tipo de medio es aceptable.<br/>     |
| <dl> <dt>**\_tipo VFW \_ E \_ no \_ aceptado**</dt> </dl> | El tipo de medio no es aceptable.<br/> |



 

## <a name="remarks"></a>Observaciones

La clase derivada debe implementar este método. Devuelve S \_ OK si el formato de entrada propuesto es aceptable o un código de error en caso contrario.

Este método no necesita comprobar si el formato de entrada es compatible con el formato de salida (si existe). El PIN de entrada comprueba que se llama al método [**CheckTransform**](ctransformfilter-checktransform.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




