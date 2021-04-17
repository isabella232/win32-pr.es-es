---
description: El método IsEndOfStreamDelivered consulta si el evento de finalización de EC se ha \_ entregado al administrador de gráficos de filtro.
ms.assetid: 13138626-35b0-4da1-9c7e-5d22d86ad2e3
title: Método CBaseRenderer. IsEndOfStreamDelivered (Renbase. h)
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
ms.openlocfilehash: f60216afc6481411010fb2f2b0618c36a7d7acf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671196"
---
# <a name="cbaserendererisendofstreamdelivered-method"></a>CBaseRenderer. IsEndOfStreamDelivered, método

El `IsEndOfStreamDelivered` método consulta si el evento de finalización de EC se ha \_ entregado al administrador de gráficos de filtro.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsEndOfStreamDelivered();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la marca [**CBaseRenderer:: m \_ bEOSDelivered**](cbaserenderer-m-beosdelivered.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




