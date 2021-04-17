---
description: El método lock bloquea el objeto de sección crítica.
ms.assetid: b08be5ec-3f02-4ed8-8791-20e4d2a0c55f
title: Método CCritSec. Lock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Lock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 19599e9cd3c3b8fa913bd07d22fe743aaaa1382f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681267"
---
# <a name="ccritseclock-method"></a>CCritSec. Lock (método)

El método **Lock** bloquea el objeto de sección crítica.

## <a name="syntax"></a>Sintaxis


```C++
void Lock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método llama a la función [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) .

Llame a la función miembro [**CCritSec:: Unlock**](ccritsec-unlock.md) para desbloquear la sección crítica. Puede realizar varias llamadas al método **Lock** en el mismo subproceso. Asegúrese de llamar a **Unlock** un número de veces correspondiente.

Si el objeto ya está bloqueado por otro subproceso, el método **CCritSec:: Lock** se bloquea hasta que se libera el objeto o hasta que se produce una excepción de interbloqueo posible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CCritSec**](ccritsec.md)
</dt> </dl>

 

