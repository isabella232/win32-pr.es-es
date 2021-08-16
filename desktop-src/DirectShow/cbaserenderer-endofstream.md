---
description: El método EndOfStream notifica al filtro que el pin de entrada recibió una notificación de fin de flujo.
ms.assetid: bdfd03f9-81e0-4d52-959e-82fd1a67e1c3
title: Método CBaseRenderer.EndOfStream (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ff047865aa4f52dee6c03411cddb0c957327851f0f6ca1b7a03f0b6adaacfe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822736"
---
# <a name="cbaserendererendofstream-method"></a>Método CBaseRenderer.EndOfStream

El `EndOfStream` método notifica al filtro que el pin de entrada recibió una notificación de fin de flujo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

El pin de entrada del filtro llama a este método cuando recibe una notificación de fin de flujo.

Este método establece la marca [**CBaseRenderer::m \_ bEOS**](cbaserenderer-m-beos.md) en **TRUE** y llama al método [**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md) para programar un [**evento EC \_ COMPLETE.**](ec-complete.md) Si el filtro está en pausa y esperando un ejemplo, este método completa la transición de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




