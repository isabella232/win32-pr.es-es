---
description: Duración de la secuencia. De forma predeterminada, el valor se establece en el valor de la variable miembro CSourceSeeking::m \_ rtStop.
ms.assetid: a87b321e-3179-4485-969b-bf12cb634b43
title: CSourceSeeking::m_rtDuration miembro (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtDuration
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6aa62a3cdf906a4e9666b7786c08e49fca250ef042d187902132410cc2f0abaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053975"
---
# <a name="csourceseekingm_rtduration-member"></a>Miembro CSourceSeeking::m \_ rtDuration

Duración de la secuencia. De forma predeterminada, el valor se establece en el valor de la variable miembro [**CSourceSeeking::m \_ rtStop.**](csourceseeking-m-rtstop.md)

## <a name="syntax"></a>Sintaxis


```C++
CRefTime m_rtDuration;
```



## <a name="remarks"></a>Comentarios

Mantenga **presionada la \_ sección m pLock** critical antes de acceder a esta variable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 




