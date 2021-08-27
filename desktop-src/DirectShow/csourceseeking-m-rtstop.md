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
ms.openlocfilehash: a4408fddf42070012aa6e1eb3a0268e8e449b571828c0904524f3cc8d27df3bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103005"
---
# <a name="csourceseekingm_rtstop-member"></a>Miembro CSourceSeeking::m \_ rtStop

Hora de detenerse. De forma predeterminada, el valor se establece en un número muy grande. La clase derivada puede restablecer el valor en su constructor o cuando se inicializa el filtro.

## <a name="syntax"></a>Sintaxis


```C++
CRefTime m_rtStop;
```



## <a name="remarks"></a>Comentarios

Mantenga **presionada \_ la sección m pLock** critical antes de acceder a esta variable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 




