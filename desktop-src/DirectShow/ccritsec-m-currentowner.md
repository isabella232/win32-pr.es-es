---
description: Identificador de subproceso del subproceso propietario.
ms.assetid: 495598db-a0c9-473b-8184-121a1939b55a
title: 'Miembro CCritSec:: m_currentOwner (Wxutil. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661231"
---
# <a name="ccritsecm_currentowner-member"></a>Miembro currentOwner CCritSec:: m \_

Identificador de subproceso del subproceso propietario.

## <a name="syntax"></a>Sintaxis


```C++
DWORD m_currentOwner;
```



## <a name="remarks"></a>Observaciones

Esta variable miembro solo se define en la versión de depuración de la clase base. Las [funciones de depuración de sección crítica](critical-section-debugging-functions.md) utilizan este miembro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CCritSec**](ccritsec.md)
</dt> </dl>

 

 




