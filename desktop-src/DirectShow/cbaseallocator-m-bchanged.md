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
ms.openlocfilehash: 86c700f3c0ee820206613bcf3147652b1826b57a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070168"
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

 

 




