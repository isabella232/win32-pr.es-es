---
description: El método EndOfStream notifica al filtro que el PIN de entrada ha recibido una notificación de final de secuencia.
ms.assetid: bdfd03f9-81e0-4d52-959e-82fd1a67e1c3
title: Método CBaseRenderer. EndOfStream (Renbase. h)
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
ms.openlocfilehash: 6e12da02ffbce99b29d324c1166b3d4cdf2265c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660754"
---
# <a name="cbaserendererendofstream-method"></a>CBaseRenderer. EndOfStream, método

El `EndOfStream` método notifica al filtro que el PIN de entrada ha recibido una notificación de final de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

El PIN de entrada del filtro llama a este método cuando recibe una notificación de final de secuencia.

Este método establece la [**marca CBaseRenderer:: m \_ BeOS**](cbaserenderer-m-beos.md) en **true** y llama al método [**CBaseRenderer:: SendEndOfStream**](cbaserenderer-sendendofstream.md) para programar un evento de [**\_ finalización de EC**](ec-complete.md) . Si el filtro está en pausa y en espera de un ejemplo, este método completa la transición de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




