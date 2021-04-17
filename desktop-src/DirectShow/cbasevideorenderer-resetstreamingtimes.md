---
description: El método ResetStreamingTimes restablece todas las horas que controlan el streaming.
ms.assetid: 8a596760-a45a-4486-bb91-aab10bbf927f
title: Método CBaseVideoRenderer. ResetStreamingTimes (Renbase. h)
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
ms.openlocfilehash: d887ca9e246d5e3fb746c119b1ed6784201ec702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660242"
---
# <a name="cbasevideorendererresetstreamingtimes-method"></a>CBaseVideoRenderer. ResetStreamingTimes, método

El `ResetStreamingTimes` método restablece todo el tiempo que controla la transmisión por secuencias.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT ResetStreamingTimes();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Las horas se establecen para que los marcos no se quiten inicialmente y para que se dibuje el primer fotograma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




