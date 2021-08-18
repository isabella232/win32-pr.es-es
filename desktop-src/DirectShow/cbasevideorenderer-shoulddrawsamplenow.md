---
description: El método ShouldDrawSampleNow determina si el vídeo se debe dibujar sin establecer un vínculo de aviso de temporizador con el reloj.
ms.assetid: 2cbefc66-0d99-4559-b210-3163cd413dbf
title: Método CBaseVideoRenderer.ShouldDrawSampleNow (Renbase.h)
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
ms.openlocfilehash: e3c0297ccf670de12380c5f02af2c67d6050bac29dd1fa7e7e89a6e6c7c20592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074691"
---
# <a name="cbasevideorenderershoulddrawsamplenow-method"></a>Método CBaseVideoRenderer.ShouldDrawSampleNow

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

Puntero a la [**interfaz IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> <dt>

*ptrStart* 
</dt> <dd>

Puntero a la hora de comenzar la representación.

</dd> <dt>

*ptrEnd* 
</dt> <dd>

Puntero al momento en que se detiene la representación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Devuelve S OK para significar draw a la vez sin esperar, S FALSE para significar \_ \_ draw at time *ptrStart* o un error para significar no dibujar el ejemplo; es decir, omitirlo para ahorrar tiempo.

## <a name="remarks"></a>Comentarios

Esta función miembro invalida [**CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




