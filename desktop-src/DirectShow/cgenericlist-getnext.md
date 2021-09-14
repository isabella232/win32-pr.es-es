---
description: El método GetNext recupera el elemento en la posición especificada y avanza la posición.
ms.assetid: d24d3388-1af9-4a62-bdb6-d3d3f5b0b97a
title: Método CGenericList.GetNext (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.GetNext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9491e58d817ce2c9dc4fb59fafa9bf96812a013a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070098"
---
# <a name="cgenericlistgetnext-method"></a>Método CGenericList.GetNext

El `GetNext` método recupera el elemento en la posición especificada y avanza la posición.

## <a name="syntax"></a>Sintaxis


```C++
OBJECT* GetNext(
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

Devuelve un puntero a un objeto de tipo **OBJECT** (el tipo de plantilla).

## <a name="remarks"></a>Observaciones

Este método avanza el indicador de posición a la siguiente posición. Si el indicador de posición se mueve más allá del final de la lista, el método lo establece en **NULL.**

Si *rp* es **NULL,** el método devuelve **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CGenericList (Clase)**](cgenericlist.md)
</dt> </dl>

 

 




