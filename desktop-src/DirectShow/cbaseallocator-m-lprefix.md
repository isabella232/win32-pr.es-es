---
description: Prefijo de cada búfer, en bytes.
ms.assetid: 471b73bf-f959-41aa-84ba-324a2738dd0e
title: 'Miembro CBaseAllocator:: m_lPrefix (Amfilter. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660325"
---
# <a name="cbaseallocatorm_lprefix-member"></a>Miembro lPrefix CBaseAllocator:: m \_

Prefijo de cada búfer, en bytes. Si el valor es distinto de cero, cada puntero de búfer devuelto por el método [**CBaseAllocator:: getBuffer**](cbaseallocator-getbuffer.md) va precedido de un bloque de bytes de tamaño *m \_ lPrefix*. Este bloque de memoria se denomina *prefijo*. La variable miembro [**CBaseAllocator:: m \_ Lsize**](cbaseallocator-m-lsize.md) no incluye el valor de prefijo.

## <a name="syntax"></a>Sintaxis


```C++
long m_lPrefix;
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

 

 




