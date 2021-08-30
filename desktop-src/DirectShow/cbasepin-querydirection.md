---
description: El método QueryDirection recupera la dirección del pin (entrada o salida). Este método implementa el método IPin::QueryDirection.
ms.assetid: c28332dc-5ac4-4c89-98b4-281424f36ba9
title: Método CBasePin.QueryDirection (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryDirection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3769b7cd510b21d91a0b855fa0551cf698b91812e5aab3fc53bda32bb4ce82cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056235"
---
# <a name="cbasepinquerydirection-method"></a>Método CBasePin.QueryDirection

El `QueryDirection` método recupera la dirección del pin (entrada o salida). Este método implementa el [**método IPin::QueryDirection.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QueryDirection(
   PIN_DIRECTION *pPinDir
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPinDir* 
</dt> <dd>

Puntero a una variable que recibe un miembro del tipo [**enumerado \_ PIN DIRECTION.**](/windows/win32/api/strmif/ne-strmif-pin_direction)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o E \_ POINTER.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




