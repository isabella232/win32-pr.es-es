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
ms.openlocfilehash: c3ae68c0564c7f76f38e91b7d27c8c3deb5ef2b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473992"
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

## <a name="remarks"></a>Observaciones

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

 

 




