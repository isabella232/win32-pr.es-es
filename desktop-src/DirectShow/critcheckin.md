---
description: Devuelve TRUE si el subproceso actual es el propietario de la sección crítica especificada.
ms.assetid: 96158f08-07a0-42a9-b173-0a05456a5f3a
title: Función CritCheckIn (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckIn
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff31707dc409db1e72c36866150c5a0b24c53f9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660449"
---
# <a name="critcheckin-function"></a>CritCheckIn función)

Devuelve **true** si el subproceso actual es el propietario de la sección crítica especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CritCheckIn(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcCrit* 
</dt> <dd>

Puntero a una sección crítica de [**CCritSec**](ccritsec.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

En las compilaciones de depuración, devuelve **true** si el subproceso actual es el propietario de esta sección crítica o **false** en caso contrario. En las compilaciones comerciales, siempre devuelve **true**.

## <a name="remarks"></a>Observaciones

Esta función es especialmente útil dentro de la macro [**Assert**](assert.md) para comprobar si un subproceso es propietario de un bloqueo determinado.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo usar esta función:


```
{
    CCritSec MyLock;  // Critical section is not locked yet.
    
    ASSERT(CritCheckIn(&MyLock)); // This assert will fire.

    // Lock the critical section.    
    CAutoLock cObjectLock(&MyLock);
     
    ASSERT(CritCheckIn(&MyLock)); // This assert will not fire.

} // Lock goes out of scope here.
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de depuración de sección crítica](critical-section-debugging-functions.md)
</dt> </dl>

 

 




