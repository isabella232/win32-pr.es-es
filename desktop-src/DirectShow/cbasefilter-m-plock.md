---
description: Puntero a una sección crítica que se usa para serializar los cambios de estado.
ms.assetid: 4fecd9a6-54df-49d7-bf2f-5dcaef919ad7
title: CBaseFilter::m_pLock miembro (Amfilter.h)
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
ms.openlocfilehash: 3bc8d3b627e6cd8c3ae4821864f6980db5acd251c721bb8841be40e04377ad55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659798"
---
# <a name="cbasefilterm_plock-member"></a>CBaseFilter::m \_ miembro pLock

Puntero a una sección crítica que se usa para serializar los cambios de estado.

## <a name="syntax"></a>Sintaxis


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Observaciones

Esta variable se inicializa en el constructor de clase; vea [**CBaseFilter::CBaseFilter**](cbasefilter-cbasefilter.md).

Mantenga esta sección crítica durante las transiciones de estado o cuando un método acceda al estado durante varias operaciones. La clase base contiene la sección crítica en los métodos siguientes:

-   [**CBaseFilter::FindPin**](cbasefilter-findpin.md)
-   [**CBaseFilter::GetSyncSource**](cbasefilter-getsyncsource.md)
-   [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md)
-   [**CBaseFilter::IsActive**](cbasefilter-isactive.md)
-   [**CBaseFilter::SetSyncSource**](cbasefilter-setsyncsource.md)
-   [**CBaseFilter::P ause**](cbasefilter-pause.md)
-   [**CBaseFilter::Run**](cbasefilter-run.md)
-   [**CBaseFilter::Stop**](cbasefilter-stop.md)

No mantenga esta sección crítica durante las operaciones de streaming (es decir, al entregar muestras a un filtro de nivel inferior). Serializar las operaciones de streaming mediante una sección crítica diferente. De lo contrario, puede provocar un interbloqueo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> <dt>

[Subprocesos y secciones críticas](threads-and-critical-sections.md)
</dt> </dl>

 

 




