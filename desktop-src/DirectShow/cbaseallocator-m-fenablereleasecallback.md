---
description: 'Marca que indica si la devolución de llamada de versión está habilitada. Esta marca se establece en el método de constructor. Si el valor es FALSE, al llamar al método CBaseAllocator:: SetNotify, se desencadena una aserción (en las compilaciones de depuración).'
ms.assetid: cc9adc7c-ec44-41e7-875a-b3e553120804
title: 'Miembro CBaseAllocator:: m_fEnableReleaseCallback (Amfilter. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671749"
---
# <a name="cbaseallocatorm_fenablereleasecallback-member"></a>Miembro fEnableReleaseCallback CBaseAllocator:: m \_

Marca que indica si la devolución de llamada de versión está habilitada. Esta marca se establece en el método de constructor. Si el valor es **false**, al llamar al método [**CBaseAllocator:: SetNotify**](cbaseallocator-setnotify.md) , se desencadena una aserción (en las compilaciones de depuración).

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_fEnableReleaseCallback;
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

 

 




