---
description: El método GetNextI recupera el elemento en la posición especificada y hace avanzar la posición.
ms.assetid: 3ec217ec-b0f9-4ff4-bdb7-ac204df99010
title: Método CBaseList. GetNextI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetNextI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f96be8d8cdf286a4017e56af7050970d45e8a56e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670933"
---
# <a name="cbaselistgetnexti-method"></a>CBaseList. GetNextI, método

El `GetNextI` método recupera el elemento en la posición especificada y hace avanzar la posición.

## <a name="syntax"></a>Sintaxis


```C++
void* GetNextI(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RP* \[ CLI\]
</dt> <dd>

Referencia a un valor de posición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero al elemento. Si *RP* es **null**, el método devuelve **null**.

## <a name="remarks"></a>Observaciones

Este método avanza el indicador de posición hasta la posición siguiente. Si el indicador de posición se desplaza más allá del final de la lista, el método lo establece en **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseList**](cbaselist.md)
</dt> </dl>

 

 




