---
description: Prefijo de cada búfer, en bytes.
ms.assetid: 471b73bf-f959-41aa-84ba-324a2738dd0e
title: CBaseAllocator::m_lPrefix miembro (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lPrefix
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc52db44dcdfa050cf8bc7faf57cb7094d8cac91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070150"
---
# <a name="cbaseallocatorm_lprefix-member"></a>Miembro CBaseAllocator::m \_ lPrefix

Prefijo de cada búfer, en bytes. Si el valor es distinto de cero, cada puntero de búfer devuelto por el método [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) va precedido de un bloque de bytes de tamaño *m \_ lPrefix*. Este bloque de memoria se denomina *prefijo*. La variable [**miembro CBaseAllocator::m \_ lSize**](cbaseallocator-m-lsize.md) no incluye el valor de prefijo.

## <a name="syntax"></a>Sintaxis


```C++
long m_lPrefix;
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

 

 




