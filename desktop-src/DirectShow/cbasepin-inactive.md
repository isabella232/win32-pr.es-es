---
description: El método Inactive notifica al pin que el filtro ya no está activo.
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: Método CBasePin. Inactive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 431b243107c365b5d9fda729fff2de80d9193c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671101"
---
# <a name="cbasepininactive-method"></a>CBasePin. Inactive (método)

El `Inactive` método notifica al pin que el filtro ya no está activo.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Cuando el filtro se detiene, la clase [**CBaseFilter**](cbasefilter.md) llama a este método en todas las clavijas conectadas del filtro.

Este método no hace nada en la clase base. Las clases derivadas deben invalidar este método para liberar los recursos obtenidos por el método [**CBasePin:: Active**](cbasepin-active.md) ; por ejemplo, para anular la confirmación de los asignadores del PIN.

El estado interno del administrador de gráficos de filtro no se actualiza hasta que se devuelve este método, por lo que no se prueba el estado desde este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




