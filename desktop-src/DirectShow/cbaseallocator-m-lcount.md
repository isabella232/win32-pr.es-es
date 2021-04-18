---
description: Número de búferes que se van a proporcionar.
ms.assetid: 73f87b14-4346-4909-bd1e-c4981cde403d
title: 'Miembro CBaseAllocator:: m_lCount (Amfilter. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660878"
---
# <a name="cbaseallocatorm_lcount-member"></a>Miembro lCount CBaseAllocator:: m \_

Número de búferes que se van a proporcionar. El método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) establece este valor. Los búferes no se asignan hasta que se llama al método [**CBaseAllocator:: commit**](cbaseallocator-commit.md) . La variable miembro [**CBaseAllocator:: m \_ lAllocated**](cbaseallocator-m-lallocated.md) especifica el número actual de búferes asignados.

## <a name="syntax"></a>Sintaxis


```C++
long m_lCount;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




