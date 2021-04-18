---
description: El método CurrentMediaType recupera el tipo de medio para la conexión del PIN actual.
ms.assetid: 1c42664d-160a-4f76-9d7a-40414c5c1704
title: Método CTransformOutputPin. CurrentMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee9ee15c3cda2baf8ab8d6e9cb0ec3c797e91a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680747"
---
# <a name="ctransformoutputpincurrentmediatype-method"></a>CTransformOutputPin. CurrentMediaType, método

El `CurrentMediaType` método recupera el tipo de medio para la conexión del PIN actual.

## <a name="syntax"></a>Sintaxis


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve una referencia a la variable miembro [**CBasePin:: m \_ MT**](cbasepin-m-mt.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




