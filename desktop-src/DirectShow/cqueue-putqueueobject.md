---
description: Coloca un elemento en la cola.
ms.assetid: 8ac41d80-e7d5-4b3f-9f09-c3d39c94c490
title: Método CQueue. PutQueueObject (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.PutQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5371c843bb348f50539535a3df9a0f6aed00893e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671419"
---
# <a name="cqueueputqueueobject-method"></a>CQueue. PutQueueObject, método

Coloca un elemento en la cola.

## <a name="syntax"></a>Sintaxis


```C++
void PutQueueObject(
   T object
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*object* 
</dt> <dd>

Objeto de tipo **T** (el tipo de plantilla).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método se bloquea hasta que haya espacio en la cola del elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CQueue**](cqueue.md)
</dt> </dl>

 

 




