---
description: El método Addtail (anexa otra lista al final de esta lista.
ms.assetid: 996523cd-d9ba-406a-afdf-494d328dc9dd
title: Método CBaseList. Addtail ((Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36d42f0b80703457032e5dde37f6d1549da089c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670940"
---
# <a name="cbaselistaddtail-method"></a>CBaseList. Addtail (, método

El `AddTail` método anexa otra lista al final de esta lista.

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddTail(
   CBaseList *pList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pList* 
</dt> <dd>

Puntero a la lista que se va a anexar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Si se produce un error en el método, es posible que algunos elementos se hayan agregado a la lista.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseList**](cbaselist.md)
</dt> </dl>

 

 




