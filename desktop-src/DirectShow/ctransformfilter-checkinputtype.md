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
ms.openlocfilehash: 6ef410ac8d96160b39ca9b7103e5125be8619169ba6b287a32b8769e57a0cbf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053625"
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



 

## <a name="remarks"></a>Comentarios

La clase derivada debe implementar este método. Devuelve S OK si el formato de entrada propuesto es aceptable o un código de error en caso \_ contrario.

Este método no necesita comprobar que el formato de entrada es compatible con el formato de salida (si existe). El pin de entrada lo comprueba mediante una llamada al [**método CheckTransform.**](ctransformfilter-checktransform.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




