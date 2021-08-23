---
description: El método RemoveHeadI quita el primer elemento de la lista.
ms.assetid: 7e448e32-ea31-4015-9219-1f990bf8763d
title: Método CBaseList.RemoveHeadI (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc4d9e039735888d6694422a1802b73b3781316210fd42e13eec9bac5094d322
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814315"
---
# <a name="cbaselistremoveheadi-method"></a>Método CBaseList.RemoveHeadI

El `RemoveHeadI` método quita el primer elemento de la lista.

## <a name="syntax"></a>Sintaxis


```C++
void* RemoveHeadI();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero al elemento o **NULL** si la lista está vacía.

## <a name="remarks"></a>Comentarios

Este método elimina el nodo de lista, pero no el elemento que contiene el nodo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseList (clase)**](cbaselist.md)
</dt> </dl>

 

 




