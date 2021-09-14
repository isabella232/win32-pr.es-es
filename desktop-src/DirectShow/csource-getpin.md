---
description: El método GetPin recupera un pin. Este método implementa el método CBaseFilter::GetPin virtual puro.
ms.assetid: 7f30a1ba-8e7b-4bde-9f4d-a85b3a2122e9
title: Método CSource.GetPin (Source.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070035"
---
# <a name="csourcegetpin-method"></a>Método CSource.GetPin

El `GetPin` método recupera un pin. Este método implementa el método [**CBaseFilter::GetPin**](cbasefilter-getpin.md) virtual puro.

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

Número del pin especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el puntero al [**objeto CBasePin**](cbasepin.md) que implementa el pin o **NULL** si el índice está fuera del intervalo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSource (clase)**](csource.md)
</dt> </dl>

 

 




