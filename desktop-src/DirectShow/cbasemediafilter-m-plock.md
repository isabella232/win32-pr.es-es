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
ms.openlocfilehash: 126aa213004dd032eea43b28198b6f8b49fe7f3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273276"
---
# <a name="cbasemediafilterm_plock-member"></a>Miembro PLock de CBaseMediaFilter::m \_

Puntero a una sección crítica.

## <a name="syntax"></a>Sintaxis


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Observaciones

La sección crítica se mantiene durante las transiciones de estado [**(CBaseMediaFilter::Run**](cbasemediafilter-run.md), [**CBaseMediaFilter::P ause**](cbasemediafilter-pause.md), [**CBaseMediaFilter::Stop**](cbasemediafilter-stop.md)), al acceder al reloj de referencia ([**CBaseMediaFilter::SetSyncSource**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter::GetSyncSource**](cbasemediafilter-getsyncsource.md)) y en el método [**CBaseMediaFilter::IsActive.**](cbasemediafilter-isactive.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseMediaFilter (clase)**](cbasemediafilter.md)
</dt> </dl>

 

 




