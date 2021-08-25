---
description: Número de bloqueos pendientes en este objeto.
ms.assetid: 27506c1d-6a9a-4410-80fb-6d4f2fd2f824
title: Miembro CCritSec::m_lockCount (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lockCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9885f3270c021432342605ad84c1b521672022f4a13cecac5ac49c9248c65d17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872215"
---
# <a name="ccritsecm_lockcount-member"></a>Miembro CCritSec::m \_ lockCount

Número de bloqueos pendientes en este objeto.

## <a name="syntax"></a>Sintaxis


```C++
DWORD m_lockCount;
```



## <a name="remarks"></a>Comentarios

Esta variable miembro solo se define en la versión de depuración de la clase base. Las [funciones de funciones de depuración de sección](critical-section-debugging-functions.md) crítica usan este miembro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CCritSec (clase)**](ccritsec.md)
</dt> </dl>

 

 




