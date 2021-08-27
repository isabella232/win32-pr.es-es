---
description: Marca que indica si la devolución de llamada de versión está habilitada. Esta marca se establece en el método constructor. Si el valor es FALSE, al llamar al método CBaseAllocator::SetNotify se produce una aserción (en compilaciones de depuración).
ms.assetid: cc9adc7c-ec44-41e7-875a-b3e553120804
title: CBaseAllocator::m_fEnableReleaseCallback miembro (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fEnableReleaseCallback
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2fc1dfebb051ddffffce341547562901153b47bd5da002ebd847965593a73d93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131465"
---
# <a name="cbaseallocatorm_fenablereleasecallback-member"></a>Miembro CBaseAllocator::m \_ fEnableReleaseCallback

Marca que indica si la devolución de llamada de versión está habilitada. Esta marca se establece en el método constructor. Si el valor es **FALSE**, la llamada al método [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) hace que se desasozca una aserción (en compilaciones de depuración).

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_fEnableReleaseCallback;
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

 

 




