---
description: El método GetDueHandle recupera el identificador de evento que se va a señalar.
ms.assetid: 495ea76d-8b94-48a9-8025-06ab18b66693
title: Método CCmdQueue.GetDueHandle (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62fbe0e38e24891add93e63e0c03d521289ed345078e8e567a376e9bd639d997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016423"
---
# <a name="ccmdqueuegetduehandle-method"></a>Método CCmdQueue.GetDueHandle

El `GetDueHandle` método recupera el identificador de evento que se va a señalar.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE GetDueHandle();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de eventos.

## <a name="remarks"></a>Comentarios

Devuelve el identificador de eventos cada vez que haya comandos diferidos que deben ejecutarse (cuando [**CCmdQueue::GetDueCommand**](ccmdqueue-getduecommand.md) no se bloqueará).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CCmdQueue (clase)**](ccmdqueue.md)
</dt> </dl>

 

 




