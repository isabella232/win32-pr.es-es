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
ms.openlocfilehash: 3e28aa890e15602376b9500243a89e8f0e3d3bb6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062517"
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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




