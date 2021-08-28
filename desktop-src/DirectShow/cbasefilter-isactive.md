---
description: El método IsActive determina si el filtro está activo actualmente (en ejecución o en pausa).
ms.assetid: 3bbb50d5-6a07-4932-940c-4466b95e6412
title: Método CBaseFilter.IsActive (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fbbd9fedf94816d518ef9f8826542399d1d1e97f97137b2d86581d36c4a33e53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076645"
---
# <a name="cbasefilterisactive-method"></a>Método CBaseFilter.IsActive

El `IsActive` método determina si el filtro está activo actualmente (en ejecución o en pausa).

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsActive();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si el filtro está en pausa o en ejecución, o **FALSE** si se detiene.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




