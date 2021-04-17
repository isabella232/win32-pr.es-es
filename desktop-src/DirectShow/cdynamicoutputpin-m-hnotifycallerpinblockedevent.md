---
description: Evento que se señala cuando el PIN se bloquea correctamente o el usuario cancela un bloque pendiente.
ms.assetid: 699bb7f7-e4f7-47c3-bbb1-0bc6556651ae
title: 'Miembro CDynamicOutputPin:: m_hNotifyCallerPinBlockedEvent (Amfilter. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670507"
---
# <a name="cdynamicoutputpinm_hnotifycallerpinblockedevent-member"></a>Miembro hNotifyCallerPinBlockedEvent CDynamicOutputPin:: m \_

Evento que se señala cuando el PIN se bloquea correctamente o el usuario cancela un bloque pendiente.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE m_hNotifyCallerPinBlockedEvent;
```



## <a name="remarks"></a>Observaciones

Antes de tener acceso a esta variable, conserve la sección crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




