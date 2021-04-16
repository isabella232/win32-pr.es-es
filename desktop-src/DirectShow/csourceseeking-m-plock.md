---
description: Puntero a un objeto de sección crítica.
ms.assetid: dc791bc4-857c-4a79-9aa8-3c5974c23483
title: 'Miembro CSourceSeeking:: m_pLock (Ctlutil. h)'
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
ms.openlocfilehash: 2f8de9159e917d24701635a428e0f5e6a1b9cb55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690549"
---
# <a name="csourceseekingm_plock-member"></a>Miembro Plock CSourceSeeking:: m \_

Puntero a un objeto de sección crítica. La `CSourceSeeking` clase utiliza esta sección crítica para sincronizar el acceso a las horas de inicio y detención, la duración y las variables de velocidad. Esta variable se inicializa en el método de constructor; vea [**CSourceSeeking:: CSourceSeeking**](csourceseeking-csourceseeking.md).

## <a name="syntax"></a>Sintaxis


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




