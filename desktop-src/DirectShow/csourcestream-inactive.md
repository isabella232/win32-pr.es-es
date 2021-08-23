---
description: El método Inactivo notifica al pin que el filtro ya no está activo. Este método invalida el método CBasePin::Inactive. Si el subproceso de streaming está activo, este método lo detiene y espera a que se cierre el subproceso.
ms.assetid: 82cf0f13-e563-4a0b-b2e1-25ab19f7ed78
title: Método CSourceStream.Inactive (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9d9424f4299d7a07ad98010846fa917307bd38eead028b4b8c38c40e2284c1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687375"
---
# <a name="csourcestreaminactive-method"></a>Método CSourceStream.Inactive

El `Inactive` método notifica al pin que el filtro ya no está activo. Este método invalida el [**método CBasePin::Inactive.**](cbasepin-inactive.md) Si el subproceso de streaming está activo, este método lo detiene y espera a que se cierre el subproceso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK u otro valor **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




