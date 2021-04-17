---
description: El método AddAfter inserta una lista después de la posición especificada.
ms.assetid: c2a2e599-0a83-4eb0-aceb-c483f153ba7e
title: Método CBaseList. AddAfter (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fdab54a124986b462e0ef592bba888e27c09b53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660680"
---
# <a name="cbaselistaddafter-method"></a>CBaseList. AddAfter, método

El `AddAfter` método inserta una lista después de la posición especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddAfter(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* 
</dt> <dd>

Posición después de la cual se va a insertar la lista.

</dd> <dt>

*pList* 
</dt> <dd>

Puntero a la lista que se va a insertar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Los indicadores de posición existentes, incluido el especificado en el parámetro *pos* , siguen siendo válidos. Si se produce un error en el método, es posible que se hayan agregado algunos elementos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseList**](cbaselist.md)
</dt> </dl>

 

 




