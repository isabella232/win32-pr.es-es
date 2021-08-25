---
description: El método IsStopped determina si se detiene el filtro que contiene este pin.
ms.assetid: ffeac352-2f9b-44be-a8e8-7e9238d0b18e
title: Método CBasePin.IsStopped (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IsStopped
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64e833ef495ace41a9dcd1614b69e4a081befce0e429fa7aad800a73ce490439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916395"
---
# <a name="cbasepinisstopped-method"></a>CBasePin.IsStopped (método)

El `IsStopped` método determina si se detiene el filtro que contiene este pin.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsStopped();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si se detiene el filtro. De lo contrario, **devuelve FALSE.**

## <a name="remarks"></a>Comentarios

No llame a este método desde dentro del método de constructor **CBasePin,** ya que es posible que el filtro no se haya inicializado todavía.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




