---
description: Identificador de subproceso del subproceso propietario.
ms.assetid: 495598db-a0c9-473b-8184-121a1939b55a
title: CCritSec::m_currentOwner miembro (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_currentOwner
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6dcb8d968f1f437087a94c5b08db12d31952d92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072279"
---
# <a name="ccritsecm_currentowner-member"></a>Miembro CCritSec::m \_ currentOwner

Identificador de subproceso del subproceso propietario.

## <a name="syntax"></a>Sintaxis


```C++
DWORD m_currentOwner;
```



## <a name="remarks"></a>Observaciones

Esta variable miembro solo se define en la versión de depuración de la clase base. Las [funciones de depuración de sección crítica](critical-section-debugging-functions.md) usan este miembro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CCritSec (clase)**](ccritsec.md)
</dt> </dl>

 

 




