---
description: El método IncremementPinVersion incrementa el número de versión en el conjunto de pines.
ms.assetid: e1b3ec33-104d-4a12-9b11-f8bea09690a7
title: Método CBaseFilter.IncrementPinVersion (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IncrementPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01c82a5f506673b6145b468004bbc900d3acdb051f525df20930344137618e72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824126"
---
# <a name="cbasefilterincrementpinversion-method"></a>Método CBaseFilter.IncrementPinVersion

El `IncremementPinVersion` método incrementa el número de versión en el conjunto de pines.

## <a name="syntax"></a>Sintaxis


```C++
void IncrementPinVersion();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método incrementa la variable [**miembro CBaseFilter::m \_ PinVersion.**](cbasefilter-m-pinversion.md) Si el filtro crea o destruye de forma dinámica los pines, llame a este método cada vez que cambien.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> <dt>

[**CBaseFilter::GetPinVersion**](cbasefilter-getpinversion.md)
</dt> </dl>

 

 




