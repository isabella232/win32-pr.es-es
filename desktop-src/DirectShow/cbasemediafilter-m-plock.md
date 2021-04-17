---
description: Puntero a una sección crítica.
ms.assetid: 7d949b7f-a6a7-4ab5-b651-f85b70d55065
title: 'Miembro CBaseMediaFilter:: m_pLock (Amfilter. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660937"
---
# <a name="cbasemediafilterm_plock-member"></a>Miembro Plock CBaseMediaFilter:: m \_

Puntero a una sección crítica.

## <a name="syntax"></a>Sintaxis


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Observaciones

La sección crítica se mantiene durante las transiciones de estado ([**CBaseMediaFilter:: Run**](cbasemediafilter-run.md), [**CBaseMediaFilter::P ause**](cbasemediafilter-pause.md), [**CBaseMediaFilter:: Stop**](cbasemediafilter-stop.md)), al tener acceso al reloj de referencia ([**CBaseMediaFilter:: SetSyncSource**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter:: GetSyncSource**](cbasemediafilter-getsyncsource.md)) y en el método [**CBaseMediaFilter:: IsActive**](cbasemediafilter-isactive.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




