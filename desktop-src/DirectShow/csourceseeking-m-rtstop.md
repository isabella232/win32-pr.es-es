---
description: Hora de detenerse. De forma predeterminada, el valor se establece en un número muy grande. La clase derivada puede restablecer el valor en su constructor o cuando se inicializa el filtro.
ms.assetid: 1fddcf84-fd9a-4dad-892c-1b0abbb0ca55
title: CSourceSeeking::m_rtStop miembro (Ctlutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072258"
---
# <a name="csourceseekingm_rtstop-member"></a>Miembro CSourceSeeking::m \_ rtStop

Hora de detenerse. De forma predeterminada, el valor se establece en un número muy grande. La clase derivada puede restablecer el valor en su constructor o cuando se inicializa el filtro.

## <a name="syntax"></a>Sintaxis


```C++
CRefTime m_rtStop;
```



## <a name="remarks"></a>Observaciones

Mantenga **presionada \_ la sección m pLock** critical antes de acceder a esta variable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 




