---
description: El método ThrottleWait inserta un período de espera después de cada fotograma.
ms.assetid: 69306093-f5db-4170-b30f-e33cfa448e9f
title: Método CBaseVideoRenderer.ThrottleWait (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ThrottleWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7408cfb011fa0fbbb223b6757ddb10ff9cbd357b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973943"
---
# <a name="cbasevideorendererthrottlewait-method"></a>Método CBaseVideoRenderer.ThrottleWait

El `ThrottleWait` método inserta un período de espera después de cada fotograma.

## <a name="syntax"></a>Sintaxis


```C++
void ThrottleWait();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función miembro espera un período de tiempo obtenido del miembro de datos **m \_ trThrottle.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




