---
description: Puntero a una sección crítica que se usa para serializar los cambios de estado.
ms.assetid: 4fecd9a6-54df-49d7-bf2f-5dcaef919ad7
title: 'Miembro CBaseFilter:: m_pLock (Amfilter. h)'
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
ms.openlocfilehash: 40b2f6ece048fc6463fda0a22792d57839d59e55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660461"
---
# <a name="cbasefilterm_plock-member"></a>Miembro Plock CBaseFilter:: m \_

Puntero a una sección crítica que se usa para serializar los cambios de estado.

## <a name="syntax"></a>Sintaxis


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Observaciones

Esta variable se inicializa en el constructor de clase; vea [**CBaseFilter:: CBaseFilter**](cbasefilter-cbasefilter.md).

Mantenga esta sección crítica durante las transiciones de estado o cuando un método tiene acceso al estado en varias operaciones. La clase base contiene la sección crítica en los métodos siguientes:

-   [**CBaseFilter::FindPin**](cbasefilter-findpin.md)
-   [**CBaseFilter::GetSyncSource**](cbasefilter-getsyncsource.md)
-   [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md)
-   [**CBaseFilter:: IsActive**](cbasefilter-isactive.md)
-   [**CBaseFilter::SetSyncSource**](cbasefilter-setsyncsource.md)
-   [**CBaseFilter::P ause**](cbasefilter-pause.md)
-   [**CBaseFilter:: Run**](cbasefilter-run.md)
-   [**CBaseFilter:: Stop**](cbasefilter-stop.md)

No conserve esta sección crítica durante las operaciones de streaming (es decir, al entregar muestras a un filtro de nivel inferior). Serialice las operaciones de streaming con una sección crítica diferente. De lo contrario, puede producir un interbloqueo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseFilter**](cbasefilter.md)
</dt> <dt>

[Subprocesos y secciones críticas](threads-and-critical-sections.md)
</dt> </dl>

 

 




