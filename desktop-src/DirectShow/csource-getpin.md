---
description: 'El método GetPin recupera un PIN. Este método implementa el método CBaseFilter:: GetPin virtual puro.'
ms.assetid: 7f30a1ba-8e7b-4bde-9f4d-a85b3a2122e9
title: CSource. GetPin (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f11ff79c9d2d535a3370183b7f36bae25c5e1383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670705"
---
# <a name="csourcegetpin-method"></a>CSource. GetPin, método

El `GetPin` método recupera un PIN. Este método implementa el método [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) virtual puro.

## <a name="syntax"></a>Sintaxis


```C++
CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*n* 
</dt> <dd>

Número del PIN especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el puntero al objeto [**CBasePin**](cbasepin.md) que implementa el PIN, o **null** si el índice está fuera del intervalo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSource**](csource.md)
</dt> </dl>

 

 




