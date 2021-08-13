---
description: Sección crítica que protege el estado de bloqueo.
ms.assetid: 6d20cf4c-2c27-41e6-8d01-6cb5e3876a38
title: CDynamicOutputPin::m_BlockStateLock miembro (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa5382a30dcd434965c53e893d6818ab0f08a84c19ea0ddec53846c0c01c80f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656685"
---
# <a name="cdynamicoutputpinm_blockstatelock-member"></a>Miembro CDynamicOutputPin::m \_ BlockStateLock

Sección crítica que protege el estado de bloqueo.

## <a name="syntax"></a>Sintaxis


```C++
CCritSec m_BlockStateLock;
```



## <a name="remarks"></a>Observaciones

Mantenga esta sección crítica antes de usar cualquiera de las siguientes variables miembro:

-   [**CDynamicOutputPin::m \_ BlockState**](cdynamicoutputpin-m-blockstate.md)
-   [**CDynamicOutputPin::m \_ dwBlockCallerThreadID**](cdynamicoutputpin-m-dwblockcallerthreadid.md)
-   [**CDynamicOutputPin::m \_ dwNumOutstandingOutputPinUsers**](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md)
-   [**CDynamicOutputPin::m \_ hNotifyCallerPinBlockedEvent**](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




