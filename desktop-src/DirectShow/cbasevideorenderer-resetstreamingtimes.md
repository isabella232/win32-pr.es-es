---
description: El método ResetStreamingTimes restablece todas las veces que controlan el streaming.
ms.assetid: 8a596760-a45a-4486-bb91-aab10bbf927f
title: Método CBaseVideoRenderer.ResetStreamingTimes (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ResetStreamingTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bebf6f827cac883660b383b76f3a6ead7987e9fb468d0fd6f14205f59ad4d530
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074779"
---
# <a name="cbasevideorendererresetstreamingtimes-method"></a>Método CBaseVideoRenderer.ResetStreamingTimes

El `ResetStreamingTimes` método restablece todas las veces que controlan el streaming.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT ResetStreamingTimes();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Las horas se establecen para que los fotogramas no se descartarán inicialmente y para que se dibujará el primer fotograma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




