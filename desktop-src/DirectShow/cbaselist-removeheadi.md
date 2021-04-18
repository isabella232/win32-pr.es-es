---
description: El método RemoveHeadI quita el primer elemento de la lista.
ms.assetid: 7e448e32-ea31-4015-9219-1f990bf8763d
title: Método CBaseList. RemoveHeadI (Wxlist. h)
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
ms.openlocfilehash: 2d9b99dbac1d99587145aa2eba293ffa7ace959c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671227"
---
# <a name="cbaselistremoveheadi-method"></a>CBaseList. RemoveHeadI, método

El `RemoveHeadI` método quita el primer elemento de la lista.

## <a name="syntax"></a>Sintaxis


```C++
void* RemoveHeadI();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero al elemento, o **null** si la lista está vacía.

## <a name="remarks"></a>Observaciones

Este método elimina el nodo de lista, pero no el elemento que contiene el nodo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseList**](cbaselist.md)
</dt> </dl>

 

 




