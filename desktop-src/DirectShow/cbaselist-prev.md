---
description: El método Prev recupera la posición anterior en la lista.
ms.assetid: 537c3019-373a-4974-a42e-72150da72767
title: Método CBaseList. PREV (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Prev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03c35a89754b27aa67a5bba33ee694433d74c0fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660664"
---
# <a name="cbaselistprev-method"></a>CBaseList. PREV (método)

El `Prev` método recupera la posición anterior en la lista.

## <a name="syntax"></a>Sintaxis


```C++
POSITION Prev(
   POSITION pos
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* 
</dt> <dd>

Valor de posición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el indicador de posición anterior a la posición especificada en *pos*.

## <a name="remarks"></a>Observaciones

Si *pos* es la primera posición de la lista, el método devuelve **null**. Si *pos* es **null**, el método devuelve la última posición de la lista.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseList**](cbaselist.md)
</dt> </dl>

 

 




