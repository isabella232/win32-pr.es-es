---
description: Puntero a un objeto de sección crítica.
ms.assetid: dc791bc4-857c-4a79-9aa8-3c5974c23483
title: CSourceSeeking::m_pLock miembro (Ctlutil.h)
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
ms.openlocfilehash: 3f230fcaee4ebb59520319d5dfd7cf8295ce8721716cd1ffb02b534e242bd99b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054025"
---
# <a name="csourceseekingm_plock-member"></a>Miembro CSourceSeeking::m \_ pLock

Puntero a un objeto de sección crítica. La clase usa esta sección crítica para sincronizar el acceso a las variables `CSourceSeeking` start y stop times, duration y rate. Esta variable se inicializa en el método constructor; vea [**CSourceSeeking::CSourceSeeking**](csourceseeking-csourceseeking.md).

## <a name="syntax"></a>Sintaxis


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 




