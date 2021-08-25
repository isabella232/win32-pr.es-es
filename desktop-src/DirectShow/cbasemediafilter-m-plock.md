---
description: Puntero a una sección crítica.
ms.assetid: 7d949b7f-a6a7-4ab5-b651-f85b70d55065
title: CBaseMediaFilter::m_pLock miembro (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad92cf07cc096c50ffa50f862c26f6133fc8dbb9b9b059419bb516e07cbd5daa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910795"
---
# <a name="cbasemediafilterm_plock-member"></a>CBaseMediaFilter::m \_ miembro pLock

Puntero a una sección crítica.

## <a name="syntax"></a>Sintaxis


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Comentarios

La sección crítica se mantiene durante las transiciones de estado ([**CBaseMediaFilter::Run**](cbasemediafilter-run.md), [**CBaseMediaFilter::P ause**](cbasemediafilter-pause.md), [**CBaseMediaFilter::Stop**](cbasemediafilter-stop.md)), al acceder al reloj de referencia ([**CBaseMediaFilter::SetSyncSource**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter::GetSyncSource**](cbasemediafilter-getsyncsource.md)) y en el método [**CBaseMediaFilter::IsActive.**](cbasemediafilter-isactive.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseMediaFilter (clase)**](cbasemediafilter.md)
</dt> </dl>

 

 




