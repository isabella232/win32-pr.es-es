---
description: Marca que indica si el filtro ha enviado una notificación de final de secuencia.
ms.assetid: 93f897de-04bb-4de4-a612-39b27c7d6f6c
title: 'Miembro CTransformFilter:: m_bEOSDelivered (Transfrm. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661032"
---
# <a name="ctransformfilterm_beosdelivered-member"></a>Miembro bEOSDelivered CTransformFilter:: m \_

Marca que indica si el filtro ha enviado una notificación de final de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_bEOSDelivered;
```



## <a name="remarks"></a>Observaciones

Si el filtro se detiene cuando no tiene una conexión de entrada, envía una notificación de final de secuencia de nivel inferior y establece esta marca en **true**. La notificación de final de secuencia garantiza que el filtro de nivel inferior no espera los ejemplos. Tenga en cuenta que el método [**EndOfStream**](ctransformfilter-endofstream.md) del filtro no establece esta marca.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




