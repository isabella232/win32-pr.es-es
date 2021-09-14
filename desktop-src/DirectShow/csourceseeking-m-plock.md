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
ms.openlocfilehash: 2f8de9159e917d24701635a428e0f5e6a1b9cb55
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361352"
---
# <a name="csourceseekingm_plock-member"></a>Miembro CSourceSeeking::m \_ pLock

Puntero a un objeto de sección crítica. La clase usa esta sección crítica para sincronizar el acceso a las variables `CSourceSeeking` start y stop times, duration y rate. Esta variable se inicializa en el método constructor; vea [**CSourceSeeking::CSourceSeeking.**](csourceseeking-csourceseeking.md)

## <a name="syntax"></a>Sintaxis


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 




