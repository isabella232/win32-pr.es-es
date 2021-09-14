---
description: El método CheckInputType comprueba si un tipo de medio especificado es aceptable para la entrada.
ms.assetid: 11f156f7-add2-45be-a0d3-05d21f596b89
title: Método CTransformFilter.CheckInputType (Transfrm.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266516"
---
# <a name="ctransformfiltercheckinputtype-method"></a>Método CTransformFilter.CheckInputType

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

Puntero a un [**objeto CMediaType**](cmediatype.md) que especifica el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                                | Descripción                              |
|------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | El tipo de medio es aceptable.<br/>     |
| <dl> <dt>**TIPO VFW \_ E \_ NO \_ \_ ACEPTADO**</dt> </dl> | El tipo de medio no es aceptable.<br/> |



 

## <a name="remarks"></a>Observaciones

La clase derivada debe implementar este método. Devuelve S \_ OK si el formato de entrada propuesto es aceptable o, en caso contrario, un código de error.

Este método no necesita comprobar que el formato de entrada es compatible con el formato de salida (si existe). El pin de entrada lo comprueba mediante una llamada al [**método CheckTransform.**](ctransformfilter-checktransform.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




