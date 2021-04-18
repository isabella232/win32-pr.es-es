---
description: El método GetSampleTimes recupera las marcas de tiempo de un ejemplo.
ms.assetid: a8fead22-a12c-489d-9c42-d5b61f480c25
title: Método CBaseRenderer. GetSampleTimes (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetSampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c389c2ea55ddb15c59fe30e03f392d68aa3b5ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660335"
---
# <a name="cbaserenderergetsampletimes-method"></a>CBaseRenderer. GetSampleTimes, método

El `GetSampleTimes` método recupera las marcas de tiempo de un ejemplo.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetSampleTimes(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> <dt>

*pStartTime* 
</dt> <dd>

Puntero a una variable que recibe la hora de inicio.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Puntero a una variable que recibe la hora de finalización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                                    | Descripción                                                                        |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                           | El ejemplo se debe representar inmediatamente.<br/>                              |
| <dl> <dt>**S \_ false**</dt> </dl>                        | El ejemplo debe programarse para la representación, en función de las marcas de tiempo.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                         | No represente este ejemplo.<br/>                                              |
| <dl> <dt>**hora de inicio de VFW \_ E \_ después del \_ \_ \_ final**</dt> </dl> | Marca de tiempo incorrecta: la hora de finalización es anterior a la hora de inicio.<br/>            |



 

## <a name="remarks"></a>Observaciones

El filtro llama a este método para determinar cómo debe controlar un ejemplo. Si el valor devuelto es S \_ OK, el filtro representa el ejemplo inmediatamente. Si el valor devuelto es S \_ false, el filtro programa el ejemplo para su representación, en función de las marcas de tiempo. Si el valor devuelto es un código de error, el filtro rechaza el ejemplo.

Este método devuelve S \_ OK si el ejemplo no tiene marcas de tiempo, o si el filtro no tiene un reloj de referencia. De lo contrario, devuelve el valor del método [**CBaseRenderer:: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) . En la clase base, **ShouldDrawSampleNow** siempre devuelve S \_ false. La clase derivada puede invalidar este comportamiento. Por ejemplo, si la clase derivada implementa la administración de control de calidad, podría devolver E \_ no quitar un ejemplo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




