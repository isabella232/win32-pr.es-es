---
description: Evento que se señala cuando el pin se bloquea correctamente o el usuario cancela un bloque pendiente.
ms.assetid: 699bb7f7-e4f7-47c3-bbb1-0bc6556651ae
title: CDynamicOutputPin::m_hNotifyCallerPinBlockedEvent miembro (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hNotifyCallerPinBlockedEvent
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cfea481a3f24aee808fffba9be91b1fecf63fce8a875dc056420a8f075b677d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656410"
---
# <a name="cdynamicoutputpinm_hnotifycallerpinblockedevent-member"></a>Miembro CDynamicOutputPin::m \_ hNotifyCallerPinBlockedEvent

Evento que se señala cuando el pin se bloquea correctamente o el usuario cancela un bloque pendiente.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE m_hNotifyCallerPinBlockedEvent;
```



## <a name="remarks"></a>Observaciones

Antes de acceder a esta variable, mantenga presionada la sección [**crítica CDynamicOutputPin::m \_ BlockStateLock.**](cdynamicoutputpin-m-blockstatelock.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




