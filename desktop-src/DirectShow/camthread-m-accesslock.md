---
description: Sección crítica que bloquea el acceso al subproceso por parte de otros subprocesos.
ms.assetid: 9bc360be-52d6-4db1-b384-8bc9e25c0914
title: MIEMBRO DE SUBPROCESO::m_AccessLock (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_AccessLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6edb4b58b630cfdcfd6eefc43b908cf6aeb0f084
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160249"
---
# <a name="camthreadm_accesslock-member"></a>Miembro CAMThread::m \_ AccessLock

Sección crítica que bloquea el acceso al subproceso por parte de otros subprocesos.

## <a name="syntax"></a>Sintaxis


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a>Observaciones

Los [**métodos CAMThread::Create**](camthread-create.md) y [**CAMThread::CallWorker**](camthread-callworker.md) mantienen este bloqueo para serializar las operaciones en el subproceso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




