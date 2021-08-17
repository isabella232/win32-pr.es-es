---
description: Coloca un elemento en la cola.
ms.assetid: 8ac41d80-e7d5-4b3f-9f09-c3d39c94c490
title: Método CQueue.PutQueueObject (Wxutil.h)
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
ms.openlocfilehash: 8e6e3539b12f81421e90de1f8311210aa2acb77173be2991bd6f15a1c84d39ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539016"
---
# <a name="cqueueputqueueobject-method"></a>Método CQueue.PutQueueObject

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

Objeto de tipo **T** (tipo de plantilla).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método se bloquea hasta que hay espacio en la cola para el elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CQueue (clase)**](cqueue.md)
</dt> </dl>

 

 




