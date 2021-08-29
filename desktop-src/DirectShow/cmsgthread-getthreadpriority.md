---
description: Usa la función GetThreadPriority de Microsoft Win32 para recuperar la prioridad del subproceso de trabajo actual.
ms.assetid: a9db15cf-2c22-4c61-a817-20af5ade434b
title: Método CMsgThread.GetThreadPriority (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24f102a315ebb20bc9c17ed6a7bab6bae2e503e13aa62bd11883c7a8290702ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915915"
---
# <a name="cmsgthreadgetthreadpriority-method"></a>Método CMsgThread.GetThreadPriority

Usa la función **GetThreadPriority** de Microsoft Win32 para recuperar la prioridad del subproceso de trabajo actual.

## <a name="syntax"></a>Sintaxis


```C++
int GetThreadPriority();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la prioridad del subproceso como un entero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMsgThread (clase)**](cmsgthread.md)
</dt> </dl>

 

 




