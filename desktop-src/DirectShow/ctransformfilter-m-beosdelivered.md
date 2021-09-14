---
description: Marca que indica si el filtro ha enviado una notificación de fin de flujo.
ms.assetid: 93f897de-04bb-4de4-a612-39b27c7d6f6c
title: CTransformFilter::m_bEOSDelivered miembro (Transfrm.h)
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
ms.openlocfilehash: f24b87f9808c53b5f64f66031a8ee2a4e9449089
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246674"
---
# <a name="ctransformfilterm_beosdelivered-member"></a>Miembro CTransformFilter::m \_ bEOSDelivered

Marca que indica si el filtro ha enviado una notificación de fin de flujo.

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_bEOSDelivered;
```



## <a name="remarks"></a>Observaciones

Si el filtro se detiene cuando no tiene una conexión de entrada, envía una notificación de fin de flujo de bajada y establece esta marca en **TRUE.** La notificación de fin de flujo garantiza que el filtro de nivel inferior no espera muestras. Tenga en cuenta que el [**método EndOfStream**](ctransformfilter-endofstream.md) del filtro no establece esta marca.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




