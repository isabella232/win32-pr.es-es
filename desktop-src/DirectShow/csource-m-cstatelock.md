---
description: Objeto de sección crítica que protege el estado del filtro. El método auxiliar CSource::p StateLock devuelve un puntero a esta variable miembro.
ms.assetid: faaf5fea-54bc-4856-9bca-3ed420c491e4
title: CSource::m_cStateLock miembro (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_cStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5de77935fd71f0b82f3cfe1f70dae3879c97bd86b4ca6b802efd46dd42730288
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915315"
---
# <a name="csourcem_cstatelock-member"></a>Miembro CSource::m \_ cStateLock

Objeto de sección crítica que protege el estado del filtro. El [**método auxiliar CSource::p StateLock**](csource--pstatelock.md) devuelve un puntero a esta variable miembro.

## <a name="syntax"></a>Sintaxis


```C++
CCritSec m_cStateLock;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSource (clase)**](csource.md)
</dt> </dl>

 

 




