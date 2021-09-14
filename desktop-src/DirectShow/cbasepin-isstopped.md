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
ms.openlocfilehash: 4185c02b396f7d0d570081ba1401e0ec9e301d46
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973980"
---
# <a name="cbasepinisstopped-method"></a>Método CBasePin.IsStopped

El `IsStopped` método determina si se detiene el filtro que contiene este pin.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsStopped();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si se detiene el filtro. De lo contrario, **devuelve FALSE**.

## <a name="remarks"></a>Observaciones

No llame a este método desde dentro del método constructor **CBasePin,** ya que es posible que el filtro no se inicialice todavía.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




