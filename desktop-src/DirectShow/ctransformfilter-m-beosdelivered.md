---
description: Marca que indica si el filtro ha enviado una notificación de fin de flujo.
ms.assetid: 93f897de-04bb-4de4-a612-39b27c7d6f6c
title: Miembro CTransformFilter::m_bEOSDelivered (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bEOSDelivered
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38d27fabb9dd3ed2a37ed5d836bfdfb1036f4255e6af48580ab6e0678abad74b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655109"
---
# <a name="ctransformfilterm_beosdelivered-member"></a>Miembro CTransformFilter::m \_ bEOSDelivered

Marca que indica si el filtro ha enviado una notificación de fin de flujo.

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_bEOSDelivered;
```



## <a name="remarks"></a>Observaciones

Si el filtro se detiene cuando no tiene una conexión de entrada, envía una notificación de fin de flujo de bajada y establece esta marca en **TRUE.** La notificación de fin de flujo garantiza que el filtro de nivel inferior no espera muestras. Tenga en cuenta que el [**método EndOfStream del**](ctransformfilter-endofstream.md) filtro no establece esta marca.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




