---
description: Hora de detención. De forma predeterminada, el valor se establece en un número muy grande. La clase derivada puede restablecer el valor en su constructor o cuando se inicializa el filtro.
ms.assetid: 1fddcf84-fd9a-4dad-892c-1b0abbb0ca55
title: 'Miembro CSourceSeeking:: m_rtStop (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtStop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28031f245ef877eca38129df2a86210f90093db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660931"
---
# <a name="csourceseekingm_rtstop-member"></a>Miembro rtStop CSourceSeeking:: m \_

Hora de detención. De forma predeterminada, el valor se establece en un número muy grande. La clase derivada puede restablecer el valor en su constructor o cuando se inicializa el filtro.

## <a name="syntax"></a>Sintaxis


```C++
CRefTime m_rtStop;
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

 

 




