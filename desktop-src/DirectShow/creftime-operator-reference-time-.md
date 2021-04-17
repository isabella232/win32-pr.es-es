---
description: El operador de tiempo de referencia \_ () convierte el objeto en un \_ tipo de datos de hora de referencia.
ms.assetid: 36f51e03-a458-46e6-9657-977b263c127f
title: Método CRefTime. Operator REFERENCE_TIME (Reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ceeeb00ba1de4f305f87ef3fe15e70a8d91457
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680398"
---
# <a name="creftimeoperator-reference_time-method"></a>Método CRefTime. Operator REFERENCE \_ Time

El `REFERENCE_TIME()` operador convierte el objeto en un tipo de datos de [**\_ hora de referencia**](reference-time.md) .

## <a name="syntax"></a>Sintaxis


```C++
REFERENCE_TIME operator REFERENCE_TIME() const;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de [**CRefTime:: m \_ hora**](creftime-m-time.md).

## <a name="remarks"></a>Observaciones

En el ejemplo siguiente se muestra cómo usar este operador de conversión:


```C++
CRefTime cRT(1000);
REFERENCE_TIME rt = (REFERENCE_TIME)cRT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Reftime. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




