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
ms.openlocfilehash: d61c0e934208ad72e678595ce668c6c7ff72eda3371c792b294df9f2d5915612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954754"
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

## <a name="remarks"></a>Comentarios

Esta función miembro espera un período de tiempo obtenido del miembro de datos **m \_ trThrottle.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




