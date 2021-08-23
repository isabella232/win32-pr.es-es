---
description: Número de subprocesos de streaming con este pin.
ms.assetid: f8650a17-edab-4d69-91da-78107c3c60b9
title: CDynamicOutputPin::m_dwNumOutstandingOutputPinUsers miembro (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwNumOutstandingOutputPinUsers
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 29fc593065af4252f58ce4bb08dd41fac82926dc11490377f6a8af614794b22a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688715"
---
# <a name="cdynamicoutputpinm_dwnumoutstandingoutputpinusers-member"></a>Miembro CDynamicOutputPin::m \_ dwNumOutstandingOutputPinUsers

Número de subprocesos de streaming con este pin.

## <a name="syntax"></a>Sintaxis


```C++
DWORD m_dwNumOutstandingOutputPinUsers;
```



## <a name="remarks"></a>Comentarios

El [**método CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) incrementa esta variable y el método [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) la disminuye. Cuando el valor es mayor que cero, algún subproceso usa esta marca para transmitir datos o para cambiar el tipo de conexión. El pin no se puede bloquear mientras este es el caso.

Antes de acceder a esta variable, mantenga presionada la sección [**crítica CDynamicOutputPin::m \_ BlockStateLock.**](cdynamicoutputpin-m-blockstatelock.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> <dt>

[**CDynamicOutputPin::StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md)
</dt> </dl>

 

 




