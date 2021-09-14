---
description: El método ScheduleSample programa un ejemplo para su representación.
ms.assetid: 08c218d1-6d0a-4c66-bbde-a39e5d31561c
title: Método CBaseRenderer.ScheduleSample (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c340e54f35b353820b128681cfbc0c5798d38849
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254462"
---
# <a name="cbaserendererschedulesample-method"></a>Método CBaseRenderer.ScheduleSample

El `ScheduleSample` método programa un ejemplo para su representación.

## <a name="syntax"></a>Sintaxis


```C++
virtual BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample del**](/windows/desktop/api/Strmif/nn-strmif-imediasample) ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si la muestra se programó o **FALSE** si se ha eliminado.

## <a name="remarks"></a>Observaciones

Este método determina primero si el ejemplo debe representarse inmediatamente, representarse en el futuro o eliminarse. (Para ello, llama al método [**CBaseRenderer::GetSampleTimes).**](cbaserenderer-getsampletimes.md) Si el ejemplo se debe representar inmediatamente, el método señala el evento [**CBaseRenderer::m \_ RenderEvent.**](cbaserenderer-m-renderevent.md) Si el ejemplo se debe representar en el futuro, el método llama al método [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) para la programación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




