---
description: Capacidades de búsqueda.
ms.assetid: c849db20-7567-41e0-9a57-85070a6e6a3a
title: CSourceSeeking::m_dwSeekingCaps miembro (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwSeekingCaps
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4addb06b120801b0d5e697c7df93ab8ba620bbd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361355"
---
# <a name="csourceseekingm_dwseekingcaps-member"></a>Miembro CSourceSeeking::m \_ dwSeekingCaps

Capacidades de búsqueda.

## <a name="syntax"></a>Sintaxis


```C++
DWORD m_dwSeekingCaps;
```



## <a name="remarks"></a>Observaciones

De forma predeterminada, el valor se establece en la combinación bit a bit de las marcas siguientes:

-   AM \_ SEEKING \_ CanSeekForwards
-   AM \_ SEEKING \_ CanSeekBackwards
-   AM \_ SEEKING \_ CanSeekAbsolute
-   AM \_ SEEKING \_ CanGetStopPos
-   AM \_ SEEKING \_ CanGetDuration

Si el filtro admite un conjunto diferente de funcionalidades, invalide este valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 




