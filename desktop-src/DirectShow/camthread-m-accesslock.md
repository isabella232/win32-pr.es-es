---
description: Sección crítica que bloquea el acceso al subproceso por parte de otros subprocesos.
ms.assetid: 9bc360be-52d6-4db1-b384-8bc9e25c0914
title: Miembro M_ACCESSLOCK (Wxutil.h)
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
ms.openlocfilehash: 72e5823b7acadd3c1c0f3752606825d1b2981aac4a64903c5944e3df82252aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017603"
---
# <a name="camthreadm_accesslock-member"></a>Miembro DE ACCESSLock DE CAMThread::m \_

Sección crítica que bloquea el acceso al subproceso por parte de otros subprocesos.

## <a name="syntax"></a>Sintaxis


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a>Comentarios

Los [**métodos CAMThread::Create**](camthread-create.md) y [**CAMThread::CallWorker**](camthread-callworker.md) mantienen este bloqueo para serializar las operaciones en el subproceso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




