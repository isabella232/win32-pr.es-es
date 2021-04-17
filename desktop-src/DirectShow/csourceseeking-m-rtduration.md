---
description: 'Duración de la secuencia. De forma predeterminada, el valor se establece en el valor de la variable miembro CSourceSeeking:: m \_ rtStop.'
ms.assetid: a87b321e-3179-4485-969b-bf12cb634b43
title: 'Miembro CSourceSeeking:: m_rtDuration (Ctlutil. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660773"
---
# <a name="csourceseekingm_rtduration-member"></a>Miembro rtDuration CSourceSeeking:: m \_

Duración de la secuencia. De forma predeterminada, el valor se establece en el valor de la variable miembro [**CSourceSeeking:: m \_ rtStop**](csourceseeking-m-rtstop.md) .

## <a name="syntax"></a>Sintaxis


```C++
CRefTime m_rtDuration;
```



## <a name="remarks"></a>Observaciones

Mantenga presionada la sección **m \_ Plock** Critical antes de tener acceso a esta variable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




