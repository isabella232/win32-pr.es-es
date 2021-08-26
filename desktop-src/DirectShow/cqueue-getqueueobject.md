---
description: Recupera el siguiente elemento de la cola.
ms.assetid: 406ae640-5903-427d-91f9-8b01beb1aaa7
title: Método CQueue.GetQueueObject (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.GetQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c32039a82e3a0b5c086cbe18e895bdec1aaac09d4947b90d9ba18e8c6636d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108285"
---
# <a name="cqueuegetqueueobject-method"></a>Método CQueue.GetQueueObject

Recupera el siguiente elemento de la cola.

## <a name="syntax"></a>Sintaxis


```C++
T GetQueueObject();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un objeto de tipo **T** (el tipo de plantilla).

## <a name="remarks"></a>Comentarios

Este método se bloquea hasta que un elemento está disponible en la cola.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CQueue (clase)**](cqueue.md)
</dt> </dl>

 

 




