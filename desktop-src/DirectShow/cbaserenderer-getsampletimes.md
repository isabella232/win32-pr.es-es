---
description: El método GetSampleTimes recupera las marcas de tiempo de un ejemplo.
ms.assetid: a8fead22-a12c-489d-9c42-d5b61f480c25
title: Método CBaseRenderer.GetSampleTimes (Renbase.h)
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
ms.openlocfilehash: 2d759cbcf2a9638b54e6194bcac7e7b24254c0d37987995d511fb4ffce85f1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954964"
---
# <a name="cbaserenderergetsampletimes-method"></a>Método CBaseRenderer.GetSampleTimes

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

Puntero a la interfaz [**IMediaSample del**](/windows/desktop/api/Strmif/nn-strmif-imediasample) ejemplo.

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

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                                    | Descripción                                                                        |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                           | El ejemplo debe representarse inmediatamente.<br/>                              |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                        | El ejemplo debe programarse para su representación, en función de las marcas de tiempo.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                         | No represente este ejemplo.<br/>                                              |
| <dl> <dt>**HORA DE INICIO DE VFW \_ E \_ DESPUÉS DEL \_ \_ \_ FINAL**</dt> </dl> | Marca de tiempo no activa: la hora de finalización es anterior a la hora de inicio.<br/>            |



 

## <a name="remarks"></a>Comentarios

El filtro llama a este método para determinar cómo debe controlar un ejemplo. Si el valor devuelto es S \_ OK, el filtro representa el ejemplo inmediatamente. Si el valor devuelto es S FALSE, el filtro programa el ejemplo para su \_ representación, en función de las marcas de tiempo. Si el valor devuelto es un código de error, el filtro rechaza el ejemplo.

Este método devuelve S OK si el ejemplo no tiene marcas de tiempo o si \_ el filtro no tiene un reloj de referencia. De lo contrario, devuelve el valor del [**método CBaseRenderer::ShouldDrawSampleNow.**](cbaserenderer-shoulddrawsamplenow.md) En la clase base, **ShouldDrawSampleNow** siempre devuelve S \_ FALSE. La clase derivada puede invalidar este comportamiento. Por ejemplo, si la clase derivada implementa la administración del control de calidad, podría devolver E \_ FAIL para quitar un ejemplo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




