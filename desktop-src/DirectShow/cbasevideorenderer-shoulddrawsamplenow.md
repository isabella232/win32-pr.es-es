---
description: El método ShouldDrawSampleNow determina si el vídeo se debe dibujar sin establecer un vínculo de aviso de temporizador con el reloj.
ms.assetid: 2cbefc66-0d99-4559-b210-3163cd413dbf
title: Método CBaseVideoRenderer. ShouldDrawSampleNow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c96b7453eb6009121fd6782030f7988663f5e8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679093"
---
# <a name="cbasevideorenderershoulddrawsamplenow-method"></a>CBaseVideoRenderer. ShouldDrawSampleNow, método

El `ShouldDrawSampleNow` método determina si el vídeo se debe dibujar sin establecer un vínculo de aviso de temporizador con el reloj.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *ptrStart,
   REFERENCE_TIME *ptrEnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) para el ejemplo.

</dd> <dt>

*ptrStart* 
</dt> <dd>

Puntero a la hora de inicio de la representación.

</dd> <dt>

*ptrEnd* 
</dt> <dd>

Puntero a la hora de detener la representación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Devuelve S \_ OK para indicar que el dibujo se realiza a la vez sin esperar, es \_ false para indicar que se dibuje en el tiempo *ptrStart*, o bien un error para indicar que no se dibuja el ejemplo; es decir, se omite para ahorrar tiempo.

## <a name="remarks"></a>Observaciones

Esta función miembro invalida [**CBaseRenderer:: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




