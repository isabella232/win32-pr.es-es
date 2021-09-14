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
ms.openlocfilehash: e188a29689a6dd1a54ef401f8bd2677e30989972
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072261"
---
# <a name="csourceseekingm_rtduration-member"></a>Miembro CSourceSeeking::m \_ rtDuration

Duración de la secuencia. De forma predeterminada, el valor se establece en el valor de la variable miembro [**CSourceSeeking::m \_ rtStop.**](csourceseeking-m-rtstop.md)

## <a name="syntax"></a>Sintaxis


```C++
CRefTime m_rtDuration;
```



## <a name="remarks"></a>Observaciones

Mantenga **presionada la \_ sección m pLock** critical antes de acceder a esta variable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 




