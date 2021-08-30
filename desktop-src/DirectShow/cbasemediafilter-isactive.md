---
description: El método IsActive determina si el objeto está activo (en ejecución o en pausa).
ms.assetid: 6531cf1f-e057-4094-9354-d5a32371c83c
title: Método CBaseMediaFilter.IsActive (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.IsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c2e59e15994f9a00f15538b95bf303195083bb364b5a34378ee32cd99bd88a50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084505"
---
# <a name="cbasemediafilterisactive-method"></a>Método CBaseMediaFilter.IsActive

El `IsActive` método determina si el objeto está activo (en ejecución o en pausa).

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsActive();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si el objeto está en pausa o en ejecución, o **FALSE** si se detiene.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseMediaFilter (clase)**](cbasemediafilter.md)
</dt> </dl>

 

 




