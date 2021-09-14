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
ms.openlocfilehash: 85ff046b7e1f7a0ccfcc41f630785a3e8404e256
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070030"
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

 

 




