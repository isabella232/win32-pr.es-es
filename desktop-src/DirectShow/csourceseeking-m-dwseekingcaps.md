---
description: Búsqueda de funcionalidades.
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
ms.openlocfilehash: 98044f8a05c22022f66e6014be591d99ec57451e33e8f2d7d464e6793bec19e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054035"
---
# <a name="csourceseekingm_dwseekingcaps-member"></a>Miembro CSourceSeeking::m \_ dwSeekingCaps

Búsqueda de funcionalidades.

## <a name="syntax"></a>Sintaxis


```C++
DWORD m_dwSeekingCaps;
```



## <a name="remarks"></a>Comentarios

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 




