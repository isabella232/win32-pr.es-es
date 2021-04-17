---
description: Recupera el siguiente elemento de la cola.
ms.assetid: 406ae640-5903-427d-91f9-8b01beb1aaa7
title: Método CQueue. GetQueueObject (Wxutil. h)
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
ms.openlocfilehash: c3ae68c0564c7f76f38e91b7d27c8c3deb5ef2b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680866"
---
# <a name="cqueuegetqueueobject-method"></a>CQueue. GetQueueObject, método

Recupera el siguiente elemento de la cola.

## <a name="syntax"></a>Sintaxis


```C++
T GetQueueObject();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un objeto de tipo **T** (el tipo de plantilla).

## <a name="remarks"></a>Observaciones

Este método se bloquea hasta que un elemento esté disponible en la cola.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CQueue**](cqueue.md)
</dt> </dl>

 

 




