---
description: El método ScheduleSample programa un ejemplo para la representación.
ms.assetid: 08c218d1-6d0a-4c66-bbde-a39e5d31561c
title: Método CBaseRenderer. ScheduleSample (Renbase. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661137"
---
# <a name="cbaserendererschedulesample-method"></a>CBaseRenderer. ScheduleSample, método

El `ScheduleSample` método programa un ejemplo para la representación.

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

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si se ha programado el ejemplo, o **false** si se ha quitado el ejemplo.

## <a name="remarks"></a>Observaciones

En primer lugar, este método determina si el ejemplo se debe representar inmediatamente, se representa en el futuro o se quita. (Para ello, llama al método [**CBaseRenderer:: GetSampleTimes**](cbaserenderer-getsampletimes.md) ). Si el ejemplo se debe representar inmediatamente, el método señala al evento [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) . Si el ejemplo se debe representar en el futuro, el método llama al método [**IReferenceClock:: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) para la programación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




