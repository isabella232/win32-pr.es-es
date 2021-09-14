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
ms.openlocfilehash: 626f1e8f4101eb48e79bc1cf679d1b91be9b2b31
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070155"
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

 

 




