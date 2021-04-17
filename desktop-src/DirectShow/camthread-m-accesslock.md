---
description: Sección crítica que bloquea el subproceso para que no tenga acceso a otros subprocesos.
ms.assetid: 9bc360be-52d6-4db1-b384-8bc9e25c0914
title: 'Miembro CAMThread:: m_AccessLock (Wxutil. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690682"
---
# <a name="camthreadm_accesslock-member"></a>Miembro AccessLock CAMThread:: m \_

Sección crítica que bloquea el subproceso para que no tenga acceso a otros subprocesos.

## <a name="syntax"></a>Sintaxis


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a>Observaciones

Los métodos [**CAMThread:: Create**](camthread-create.md) y [**CAMThread:: CallWorker**](camthread-callworker.md) incluyen este bloqueo para serializar las operaciones en el subproceso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAMThread**](camthread.md)
</dt> </dl>

 

 




