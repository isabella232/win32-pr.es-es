---
description: Marca que indica si los requisitos del búfer han cambiado.
ms.assetid: 34d946f9-125c-40fb-b09e-82457add07d6
title: CBaseAllocator::m_bChanged miembro (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7edb5ed770628d7dfd982017e720ef0136bace74dd7e311121925f6c8657d2fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131505"
---
# <a name="cbaseallocatorm_bchanged-member"></a>Miembro CBaseAllocator::m \_ bChanged

Marca que indica si los requisitos del búfer han cambiado. El [**método CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) establece el valor en **TRUE.** En una clase derivada, el método virtual puro [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) debe volver a establecer el valor en **FALSE.** Una vez asignados los búferes, no es necesario volver a asignarlos mientras *m \_ bChanged* sea **FALSE.**

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_bChanged;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseAllocator (clase)**](cbaseallocator.md)
</dt> </dl>

 

 




