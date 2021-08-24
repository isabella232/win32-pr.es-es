---
description: Recupera el identificador del subproceso en el objeto CMsgThread.
ms.assetid: dacbdc68-91a0-46d4-805f-fe51cb047e19
title: Método CMsgThread.GetThreadHandle (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ecb968156302c4fd1a8c48d1c6f3175977059298d2f6af5207abc376a6e107a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585695"
---
# <a name="cmsgthreadgetthreadhandle-method"></a>Método CMsgThread.GetThreadHandle

Recupera el identificador del subproceso en el [**objeto CMsgThread.**](cmsgthread.md)

## <a name="syntax"></a>Sintaxis


```C++
HANDLE GetThreadHandle();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del subproceso.

## <a name="remarks"></a>Comentarios

El identificador del subproceso se puede pasar a funciones de espera, como [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects). El identificador del subproceso se señala cuando se cierra el subproceso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMsgThread (clase)**](cmsgthread.md)
</dt> </dl>

 

