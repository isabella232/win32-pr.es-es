---
description: 'El método QueryDirection recupera la dirección del PIN (entrada o salida). Este método implementa el método IPin:: QueryDirection.'
ms.assetid: c28332dc-5ac4-4c89-98b4-281424f36ba9
title: Método CBasePin. QueryDirection (Amfilter. h)
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
ms.openlocfilehash: 7e2ebfaa3d12b5f582b4b67014280fa0a0d5299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670875"
---
# <a name="cbasepinquerydirection-method"></a>CBasePin. QueryDirection, método

El `QueryDirection` método recupera la dirección del PIN (entrada o salida). Este método implementa el método [**IPin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) .

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

Puntero a una variable que recibe un miembro del tipo enumerado de la [**\_ dirección del PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el \_ puntero S o E \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




