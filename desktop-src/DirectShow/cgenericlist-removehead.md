---
description: El método RemoveHead quita el primer elemento de la lista.
ms.assetid: 95902028-d2c2-4c16-9ca6-ef57174a9292
title: Método CGenericList.RemoveHead (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da9267d6b3e0c3196b3a9d1e873f222649b66684
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070097"
---
# <a name="cgenericlistremovehead-method"></a>CGenericList.RemoveHead (método)

El `RemoveHead` método quita el primer elemento de la lista.

## <a name="syntax"></a>Sintaxis


```C++
OBJECT* RemoveHead();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a un objeto de tipo **OBJECT** (tipo de plantilla) o **NULL** si la lista está vacía.

## <a name="remarks"></a>Observaciones

Este método elimina el nodo de lista, pero no el elemento que contiene el nodo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CGenericList (clase)**](cgenericlist.md)
</dt> </dl>

 

 




