---
description: El método IsEndOfStreamDelivered consulta si el evento EC COMPLETE se ha entregado al administrador de \_ gráficos de filtros.
ms.assetid: 13138626-35b0-4da1-9c7e-5d22d86ad2e3
title: Método CBaseRenderer.IsEndOfStreamDelivered (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.IsEndOfStreamDelivered
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f15c2bca14e6c0f55f46441bbb4de362e6375d0b67f3012a4ad234a9366b188
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954884"
---
# <a name="cbaserendererisendofstreamdelivered-method"></a>Método CBaseRenderer.IsEndOfStreamDelivered

El `IsEndOfStreamDelivered` método consulta si el evento EC COMPLETE se ha entregado al administrador de \_ gráficos de filtro.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsEndOfStreamDelivered();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la [**marca CBaseRenderer::m \_ bEOSDelivered.**](cbaserenderer-m-beosdelivered.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




