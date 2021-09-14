---
description: Número de búferes que se proporcionarán.
ms.assetid: 73f87b14-4346-4909-bd1e-c4981cde403d
title: CBaseAllocator::m_lCount miembro (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16ab469db1d50007bd3aa55ab692c51aa7600452
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070152"
---
# <a name="cbaseallocatorm_lcount-member"></a>Miembro CBaseAllocator::m \_ lCount

Número de búferes que se proporcionarán. El [**método CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) establece este valor. Los búferes no se asignan hasta que se llama al método [**CBaseAllocator::Commit.**](cbaseallocator-commit.md) La variable miembro [**CBaseAllocator::m \_ lAllocated**](cbaseallocator-m-lallocated.md) especifica el número actual de búferes asignados.

## <a name="syntax"></a>Sintaxis


```C++
long m_lCount;
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

 

 




