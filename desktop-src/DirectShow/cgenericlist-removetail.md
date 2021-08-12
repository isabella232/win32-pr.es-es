---
description: El método RemoveTail quita el último elemento de la lista.
ms.assetid: 377af676-8042-430e-87a6-b41c00482a90
title: Método CGenericList.RemoveTail (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed0b39d72eac68310dacdf2bfdc1d3c28bb35695b3d77230ba37f6fe81c417ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656161"
---
# <a name="cgenericlistremovetail-method"></a>CGenericList.RemoveTail (método)

El `RemoveTail` método quita el último elemento de la lista.

## <a name="syntax"></a>Sintaxis


```C++
OBJECT* RemoveTail();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a un objeto de tipo **OBJECT** (el tipo de plantilla) o **NULL** si la lista está vacía.

## <a name="remarks"></a>Observaciones

Este método elimina el nodo de lista, pero no el elemento contenido en el nodo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CGenericList (Clase)**](cgenericlist.md)
</dt> </dl>

 

 




