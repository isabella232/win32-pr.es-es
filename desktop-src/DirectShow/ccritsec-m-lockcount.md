---
description: Número de bloqueos pendientes en este objeto.
ms.assetid: 27506c1d-6a9a-4410-80fb-6d4f2fd2f824
title: 'Miembro CCritSec:: m_lockCount (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lockCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88098a8ded025a899e2092a96308bd6c54750758
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671165"
---
# <a name="ccritsecm_lockcount-member"></a>Miembro lockCount CCritSec:: m \_

Número de bloqueos pendientes en este objeto.

## <a name="syntax"></a>Sintaxis


```C++
DWORD m_lockCount;
```



## <a name="remarks"></a>Observaciones

Esta variable miembro solo se define en la versión de depuración de la clase base. En la sección crítica, las funciones de [depuración](critical-section-debugging-functions.md) de funciones utilizan este miembro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CCritSec**](ccritsec.md)
</dt> </dl>

 

 




