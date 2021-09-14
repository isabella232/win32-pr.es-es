---
description: El método Unlock desbloquea el objeto de sección crítica.
ms.assetid: 61811e0e-df77-48e9-96d5-b7dff8c8db9b
title: Método CCritSec.Unlock (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Unlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca84ce452d71d0d3111039d7a95d8f5dd3155058
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061324"
---
# <a name="ccritsecunlock-method"></a>Método CCritSec.Unlock

El **método Unlock** desbloquea el objeto de sección crítica.

## <a name="syntax"></a>Sintaxis


```C++
void Unlock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método llama a [**la función LeaveCriticalSection.**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection) Llame a este método una vez por cada llamada al [**método CCritSec::Lock.**](ccritsec-lock.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CCritSec (clase)**](ccritsec.md)
</dt> </dl>

 

