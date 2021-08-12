---
description: El método GetNextAdviseTime recupera la hora de la siguiente solicitud de aviso.
ms.assetid: 2a376250-fb39-46d7-a5a8-e3a3143cd209
title: Método CAMSchedule.GetNextAdviseTime (Dsschedule.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetNextAdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c7fd04622a5cdab8bade32f41b090d8f480db292209d284804b5180134954f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662352"
---
# <a name="camschedulegetnextadvisetime-method"></a>Método CAMSchedule.GetNextAdviseTime

El `GetNextAdviseTime` método recupera la hora de la siguiente solicitud de aviso.

## <a name="syntax"></a>Sintaxis


```C++
REFERENCE_TIME GetNextAdviseTime();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la hora de referencia de la siguiente solicitud de aviso o MAX \_ TIME no se programa ninguna solicitud.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dsschedule.h (incluir Secuencias.h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLASE CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




