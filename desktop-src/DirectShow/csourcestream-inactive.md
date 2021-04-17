---
description: 'El método Inactive notifica al pin que el filtro ya no está activo. Este método invalida el método CBasePin:: INACTIVE. Si el subproceso de streaming está activo, este método lo detiene y espera a que se cierre el subproceso.'
ms.assetid: 82cf0f13-e563-4a0b-b2e1-25ab19f7ed78
title: Método CSourceStream. Inactive (Source. h)
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
ms.openlocfilehash: 6c4fab336f5f06d932189ee991fd190d1ae42b27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690418"
---
# <a name="csourcestreaminactive-method"></a>CSourceStream. Inactive (método)

El `Inactive` método notifica al pin que el filtro ya no está activo. Este método invalida el método [**CBasePin:: Inactive**](cbasepin-inactive.md) . Si el subproceso de streaming está activo, este método lo detiene y espera a que se cierre el subproceso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK u otro valor **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




