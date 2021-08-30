---
description: El método GetNextI recupera el elemento en la posición especificada y avanza la posición.
ms.assetid: 3ec217ec-b0f9-4ff4-bdb7-ac204df99010
title: Método CBaseList.GetNextI (Wxlist.h)
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
ms.openlocfilehash: b45556c1657961bdebf378f7e3908501f0bf5b971cf0c6533a55477b05a40ad9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983514"
---
# <a name="cbaselistgetnexti-method"></a>Método CBaseList.GetNextI

El `GetNextI` método recupera el elemento en la posición especificada y avanza la posición.

## <a name="syntax"></a>Sintaxis


```C++
void* GetNextI(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rp* \[ Ref\]
</dt> <dd>

Referencia a un valor POSITION.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero al elemento. Si *rp* es **NULL,** el método devuelve **NULL.**

## <a name="remarks"></a>Comentarios

Este método avanza el indicador de posición a la siguiente posición. Si el indicador de posición se mueve más allá del final de la lista, el método lo establece en **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseList (clase)**](cbaselist.md)
</dt> </dl>

 

 




